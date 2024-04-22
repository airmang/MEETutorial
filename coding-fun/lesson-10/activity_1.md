### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 주변 환경

## 단계 1
**바닥에 있는 블록**이 **팩트 아이스**인지 **조사하는 동안**, 에이전트가 **오른쪽 블록을 감지하면** **앞으로 이동**해야 합니다. 그렇지 않으면 **오른쪽으로 이동**해야 합니다.


```ghost
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == PACKED_ICE) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
            agent.move(FORWARD, 1)
        } else {
            agent.move(RIGHT, 1)
        }
    }
})
```

