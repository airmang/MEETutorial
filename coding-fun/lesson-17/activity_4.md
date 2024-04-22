### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 비트!

## 단계 1
세 가지 함수: ``||functions: plantSeed||``, ``||functions: plantSection||``, 그리고 ``||functions: checkTurn||``이 제공됩니다. 먼저, 새로운 ``||player: on chat||`` 명령을 만들고 조건을 추가하세요: 에이전트가 ``||agent:inspecting the block down||``을 하고 그것이 **금 블록**이 아닌 동안, 필요한 함수를 ``||functions: call||``하세요.


```template
/**
 * We are calling a function inside a function
 */
function plantSection () {
    for (let index = 0; index < 11; index++) {
        plantSeed()
    }
    agent.move(FORWARD, 1)
}
 /**
 * The code was modified to not place seeds if there's no block under the Agent.
 */
function plantSeed () {
    agent.till(FORWARD)
    agent.move(FORWARD, 1)
    if (agent.detect(AgentDetection.Block, DOWN)) {
        agent.place(DOWN)
    }
}
function checkTurn () {
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    } else if (agent.inspect(AgentInspection.Block, DOWN) == BLOCK_OF_QUARTZ) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
}

```


```ghost
player.onChat("plant", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != GOLD_BLOCK) {
        plantSection()
        checkTurn()
    }
})

function checkTurn () {
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    } else if (agent.inspect(AgentInspection.Block, DOWN) == BLOCK_OF_QUARTZ) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
}

```
