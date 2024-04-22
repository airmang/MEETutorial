### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 비트 심기!

## 단계 1

두 개의 함수 **plantSeed**와 **plantSection**이 제공됩니다. 새로운 ``||player: on chat||`` 명령을 만들고 그 안에 ``||functions: call plantSection||``을 추가하세요. ``||agent: agent inspects block down||``을 확인하는 ``||logic: if||`` 문을 추가하세요.  
만약 아래의 블록이 ``||blocks: lapis lazuli||``라면, 에이전트는 ``||agent: turn right||``, ``||agent: move forward||``, 그리고 ``||agent: turn right||``를 해야 합니다.  
``||logic: Else||`` 에이전트가 ``||agent: inspects the block down||``을 하고 그것이 ``||blocks: a block of quartz||``라면, 에이전트는 ``||agent: turn left||``, ``||agent: move forward||``, 그리고 ``||agent: turn left||``를 해야 합니다.  
마지막으로 ``||functions: call plantSection||``를 호출하세요.

#### ~ tutorialhint
``` blocks
player.onChat("run", function () {
    plantSection()
})
```

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

/**
* You need to check if the Agent is stepping on a lapis block turn right, if quartz turn left.
*/
```
## Step 2
Add an ``||logic:if||`` statement to the ``||player:on chat||`` command. Within the **true** of the ``||logic:if|`` block add a ``||logic:" " = " "||`` block. If when ``||agent:agent inspects block down||`` is **equal (=)** to ``||blocks:lapis lazuli||`` the agent needs to ``||agent: turn right||``, ``||agent:move forward||`` and ``||agent:turn right||``. 

#### ~ tutorialhint
``` blocks
player.onChat("run", function () {
    plantSection()
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    }

})
```

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

/**
* You need to check if the Agent is stepping on a lapis block turn right, if quartz turn left.
*/
```

## Step 3
Click two times on the **+** symbols of the ``||logic:if||`` block. Click on the ** - ** to delete the **else** block. Add a ``||logic:" " = " "||`` block to the **blank** space of the ``||logic:else if||`` block. If ``||agent:agent inspects block down||`` is **equal (=)** to ``||blocks:a block of quartz||``. The agent needs to ``||agent:turn left||``, ``||agent:move forward||`` and ``||agent:turn left||``.  

#### ~ tutorialhint
``` blocks
player.onChat("run", function () {
    plantSection()
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    } else if (agent.inspect(AgentInspection.Block, DOWN) == BLOCK_OF_QUARTZ) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }

})
```

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

/**
* You need to check if the Agent is stepping on a lapis block turn right, if quartz turn left.
*/
```

## Step 4
 Finally add another ``||functions: call plantSection||`` within the ``||player:on chat||`` command outside of the ``||logic:if||`` statement.  

#### ~ tutorialhint
``` blocks
player.onChat("run", function () {
    plantSection()
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    } else if (agent.inspect(AgentInspection.Block, DOWN) == BLOCK_OF_QUARTZ) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
    plantSection()
})
```

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

/**
* You need to check what block your Agent is on. If on a lapis block turn right, else if quartz turn left.
*/

/**
* You can click on the + button of an If block to add an Else
*/

```

```ghost
player.onChat("turn", function () {
    plantSection()
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    } else if (agent.inspect(AgentInspection.Block, DOWN) == BLOCK_OF_QUARTZ) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    }
    plantSection()
})
```

