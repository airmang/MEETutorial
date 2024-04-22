### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 3D 공간

## 단계 1
이 도전을 해결하려면, 에이전트가 **금** 블록까지 가서 수집하는 프로그램을 작성해야 합니다. 에이전트는 먼저 지상에서 이 작업을 수행한 다음, **3단계 위로 이동**하여 이전 절차를 반복해야 합니다.

```template
player.onChat("3D", function () {
    for (let index = 0; index < 2; index++) {
    }
})
``` 
```ghost
player.onChat("3D", function () {
    for (let index = 0; index < 2; index++) {
        while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
            if (!(agent.detect(AgentDetection.Block, FORWARD))) {
                agent.move(FORWARD, 1)
            } else {
                agent.turn(LEFT_TURN)
            }
        }
        agent.destroy(FORWARD)
        agent.collectAll()
        agent.move(UP, 3)
    }
})
```
