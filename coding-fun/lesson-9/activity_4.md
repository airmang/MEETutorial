### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 로버를 수리하다

## 단계 1
이 코딩 스니펫을 수정하세요. 여기에 목표가 있습니다: **공기** 블록을 **검사**하면서 찾지 **못하면**, 에이전트는 **오른쪽으로 이동**해야 합니다. 만약 에이전트가 **앞쪽**에 **청금석** 블록을 찾으면, 에이전트는 **오른쪽으로 이동**한 다음 **왼쪽으로 회전**하고 다시 **오른쪽으로 이동**해야 합니다. 그 후에 에이전트는 "파손된 부분을 찾았습니다!"라고 말하고 **앞쪽**에 **레드스톤 블록을 놓아야** 합니다.


```template
player.onChat("repair", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) == AIR) {
        agent.move(RIGHT, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) == LAPIS_LAZULI_BLOCK) {
            agent.move(RIGHT, 1)
            agent.turn(RIGHT_TURN)
            agent.move(LEFT, 1)
        }
    }
    player.say("Found the break!")
    agent.setItem(GRASS, 1, 1)
    agent.place(FORWARD)
})
```
