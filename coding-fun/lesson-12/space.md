### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# 협력 활동

## 단계 1
우주에서 작업하기 위해 필요한 블록을 선택하세요. 우리가 수업에서 사용한 모든 블록을 사용할 수 있습니다!

```ghost
player.onChat("run", function () {
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
    	
    }
    agent.place(FORWARD)
    agent.destroy(FORWARD)
    agent.setItem(GRASS, 1, 1)
    for (let index = 0; index < 4; index++) {
    	
    }
    while (agent.inspect(AgentInspection.Block, DOWN) != PACKED_ICE) {
        if (agent.inspect(AgentInspection.Block, DOWN) == IRON_ORE || agent.inspect(AgentInspection.Block, DOWN) == GOLD_ORE) {
            agent.turn(LEFT_TURN)
            agent.destroy(DOWN)
            agent.collectAll()
        }
        if (agent.inspect(AgentInspection.Block, DOWN) == DIAMOND_ORE || agent.inspect(AgentInspection.Block, DOWN) == EMERALD_ORE) {
            agent.turn(RIGHT_TURN)
            agent.destroy(DOWN)
            agent.collectAll()
        }
        agent.move(FORWARD, 1)
    }
})


``` 

