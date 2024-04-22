### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 철

## 단계 1
에이전트가 **아래쪽 블록을 조사**하고 이 블록이 **철광석이 아닐 경우**, 에이전트는 **앞으로 이동**해야 합니다. 에이전트가 **앞쪽에 블록을 감지**하면, 그것을 **파괴**해야 합니다. 에이전트가 철을 찾으면, 그것을 **수집**하도록 프로그램하세요. 블록을 수집하기 위해서는 에이전트가 먼저 그것을 파괴해야 한다는 점을 주의하세요.

```ghost
player.onChat("4", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != IRON_ORE) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.move(FORWARD, 1)
    }
    player.say("Found the iron ore!")
    agent.destroy(DOWN)
    agent.collectAll()
})
```
