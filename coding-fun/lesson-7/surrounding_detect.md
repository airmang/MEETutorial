### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 주변 환경

## 단계 1
에이전트가 **아래쪽 블록을 조사**하고 그 블록이 **돌**인 동안, 에이전트는 **앞으로 이동**해야 합니다. 에이전트가 앞쪽에 블록을 **감지하지 못하면**, 에이전트는 앞으로 이동해야 하며, 그렇지 않으면 **왼쪽으로 회전**해야 합니다.


```template
player.onChat("inspect", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == STONE) {
        
    }
})
```

```ghost
player.onChat("inspect", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == STONE) {
        if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else {
            agent.turn(LEFT_TURN)
        }
    }
})
```
