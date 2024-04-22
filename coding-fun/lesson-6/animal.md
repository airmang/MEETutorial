### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# 협동 활동

## 단계 1
동물들에게 적합한 집을 지을 수 있는 블록을 선택하세요. 우리가 수업에서 사용한 모든 블록들을 사용할 수 있습니다!


```ghost
player.onChat("run", function () {
    agent.teleportToPlayer()
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
    	
    }
    agent.place(FORWARD)
    agent.destroy(FORWARD)
    agent.setItem(GRASS, 1, 1)
    for (let index = 0; index < 4; index++) {
    	
    }
})

```
