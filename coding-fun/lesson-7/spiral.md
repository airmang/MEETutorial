### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 스파이럴

## 단계 1
에이전트가 **앞쪽 블록을 조사**하고 그 블록이 **금 블록이 아닌 동안**, 에이전트는 **앞으로 이동**해야 합니다. 에이전트가 앞쪽에 블록을 **감지하지 못하면**, 에이전트는 앞으로 이동해야 하며, 그렇지 않으면 **왼쪽으로 회전**해야 합니다. 에이전트가 **금 블록에 도달하면**, 그것을 **파괴하고 수집**해야 합니다.


```ghost
player.onChat("3", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
        if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else {
            agent.turn(LEFT_TURN)
        }
    }
    agent.destroy(FORWARD)
    agent.collectAll()
})
```
