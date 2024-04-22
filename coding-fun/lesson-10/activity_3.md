### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 주변 환경

## 단계 1
**바닥에 있는 블록**이 **팩트 아이스가 아닌 경우**, 에이전트를 프로그래밍하여 다음 블록을 찾아 **파괴하고 수집**하도록 합니다: **철**, **금**, **에메랄드**, **다이아몬드**.

```ghost
player.onChat("3", function () {
    agent.setItem(STONE, 64, 1)
    while (agent.inspect(AgentInspection.Block, DOWN) != PACKED_ICE) {
        if (agent.inspect(AgentInspection.Block, DOWN) == IRON || agent.inspect(AgentInspection.Block, DOWN) == GOLD) {
            agent.turn(LEFT_TURN)
            agent.destroy(DOWN)
            agent.collectAll()
        }
        if (agent.inspect(AgentInspection.Block, DOWN) == DIAMOND || agent.inspect(AgentInspection.Block, DOWN) == EMERALD) {
            agent.turn(RIGHT_TURN)
            agent.destroy(DOWN)
            agent.collectAll()
        }
        agent.move(FORWARD, 1)
    }
})
```

