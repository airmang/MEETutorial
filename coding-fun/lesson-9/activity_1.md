### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 돌 찾기

## 단계 1
이 코딩 스니펫을 수정하세요. 에이전트가 해야 할 일은 다음과 같습니다: **왼쪽으로 4번 이동**, **아래로 파괴**, **아래로 이동**. 에이전트가 앞쪽에 **돌 블록**을 감지하면, "돌을 찾았다!"라고 말하고, **앞쪽을 파괴**하고 **모두 수집**해야 합니다. 만약 돌이 **감지되지 않으면**, 에이전트는 "여기에는 돌이 없다!"라고 말해야 합니다. 아래로 이동한 후에는 에이전트가 매번 **표면으로 1 블록 올라가야** 합니다. 이 활동은 **4번 반복**되어야 합니다.



```template
player.onChat("stone", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(RIGHT, 4)
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) != STONE) {
            player.say("Found the stone!")
            agent.destroy(FORWARD)
            agent.collectAll()
        } else {
            player.say("No stone here!")
        }
        agent.move(UP, 1)
    }
})
```
