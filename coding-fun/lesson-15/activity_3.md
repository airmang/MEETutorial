### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1

# 예쁜 것들!

## 단계 1
당신의 임무는 목욕탕 바닥 테두리를 따라 **석영 기둥**과 **청금석** 블록의 교대 패턴을 구성하는 것입니다. 먼저 ``||variable:blockA||``와 ``||variable:blockB||`` 변수를 생성하세요. ``||variable:blockA variable||``를 **석영 블록**으로 설정하고 ``||variable:blockB variable||``를 **청금석 블록**으로 설정하세요. 이 명령들을 ``||loops: on start||`` 블록에 추가하세요.

## 단계 2
``||logic: If||`` ``||count||`` = **0**이면, 에이전트는 ``||variable:blockA||``를 설정하고, ``||agent:destroy down||``, ``||agent:place down||``를 수행하고 ``||variable:change the count by 1||``를 해야 합니다. ``||logic: Else||`` 에이전트는 ``||blockB||``를 설정하고 블록을 놓고 ``||change count by -1||``를 해야 합니다.

## 단계 3
에이전트는 한 줄에 블록을 놓아야 하며, 이는 ``||loops: while||`` 에이전트가 **앞쪽**에 블록을 ``||logic:not||`` ``|| detect||``할 때까지 수행됩니다.

## 단계 4
에이전트가 완성해야 할 저수지의 **4**면이 있으므로, ``||loops: repeat||`` 블록을 추가하세요. 에이전트에게 블록을 놓으라고 지시하기 전에 ``||count||``를 **0**으로 설정하세요.

```template
let count = 0
player.onChat("floor", function () {
    count = 0
})
```


```ghost
player.onChat("floor", function () {
    count = 0
    for (let index = 0; index < 4; index++) {
        while (!(agent.detect(AgentDetection.Block, FORWARD))) {
            if (count == 0) {
                agent.setItem(blockA, 1, 1)
                agent.destroy(DOWN)
                agent.place(DOWN)
                count += 1
            } else {
                agent.setItem(blockB, 1, 1)
                agent.destroy(DOWN)
                agent.place(DOWN)
                count += -1
            }
            agent.move(FORWARD, 1)
        }
        agent.turn(RIGHT_TURN)
    }
})
let count = 0
let blockB = 0
let blockA = 0
blockA = BLOCK_OF_QUARTZ
blockB = LAPIS_LAZULI_BLOCK
```
