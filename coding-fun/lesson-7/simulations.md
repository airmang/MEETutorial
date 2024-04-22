### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 시뮬레이션  

## 단계 1
시뮬레이션에 오신 것을 환영합니다! 에이전트가 금 블록을 수집하고 그 길에 있는 장애물을 파괴하도록 프로그램하세요.


```template
player.onChat("simulations", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
        if (agent.inspect(AgentInspection.Block, LEFT) == GOLD_BLOCK) {
        	
        }
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.turn(LEFT_TURN)
        }
    }
})

```
```ghost
player.onChat("5", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
        if (agent.inspect(AgentInspection.Block, LEFT) == GOLD_BLOCK) {
            agent.destroy(LEFT)
            agent.collectAll()
        }
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.turn(LEFT_TURN)
        }
        agent.move(FORWARD, 1)
    }
    agent.destroy(FORWARD)
    agent.collectAll()
})
```
