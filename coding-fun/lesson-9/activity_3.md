### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 로버를 찾아서

## 단계 1
이 코딩 스니펫을 수정하세요. 여기에 목표가 있습니다: **앞쪽**을 **검사**하여 **석영** 블록을 찾지 **못하면**, 에이전트는 **앞으로 이동**해야 합니다. 만약 **아래쪽**에 **금** 블록을 **감지**하면, 에이전트는 **오른쪽으로 회전**해야 합니다. 만약 **아래쪽**에 **철** 블록을 감지하면, 에이전트는 **왼쪽으로 회전**해야 합니다. 마지막에 에이전트는 "로버를 찾았습니다!"라고 말해야 합니다.


```template
player.onChat("rover", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != BLOCK_OF_QUARTZ) {
            if (agent.inspect(AgentInspection.Block, UP) == GOLD_BLOCK) {
            agent.turn(LEFT_TURN)
        }
            if (agent.inspect(AgentInspection.Block, RIGHT) == IRON_BLOCK) {
            agent.turn(RIGHT_TURN)
        }
        agent.move(FORWARD, 1)
    }
    player.say("Found the rover!")
})
```

