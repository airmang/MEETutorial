### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1

# 열!

## 단계 1
수로를 만들 차례입니다! 먼저 ``||variable: length||``와 ``||variable: segments||`` 변수를 생성하세요. 그런 다음 ``||variable: set length||``를 **5**로 설정하고 ``||variable: set segments||``를 **6**으로 설정하세요 ``||loops: on start||``.

## 단계 2
이제 ``||player: on chat command||`` 내에서 에이전트가 **1** 부분을 만드는 데 필요한 모든 작업을 추가해야 합니다: ``||agent: set block pillar of quartz||``를 **64**개로 설정하고, ``||agent: place||``와 ``||agent: move forward||``를 추가하세요. Minecraft에서 물은 경사가 있으면 흐르므로, 에이전트는 **왼쪽, 오른쪽, 아래쪽에 블록을 놓아야** 합니다. 이 모든 작업을 ``||variable: length||``번 **반복**하는 ``||loops: repeat||`` 루프 안에 넣으세요.

## 단계 3
이제 첫 번째 ``||loops: repeat||`` 루프를 ``||variables:segments||``번 반복하는 또 다른 ``||loops: repeat||`` 루프 안에 중첩하세요. Minecraft에서 시도해보세요!

### ~ tutorialHint
내부 루프 앞에 ``||agent: agent move down||`` 블록을 추가하여 코드가 작동하게 하세요!

```ghost
player.onChat("build", function () {
    agent.move(DOWN, 1)
    for (let index = 0; index < Segments; index++) {
        for (let index = 0; index < length; index++) {
            agent.setItem(WHITE_CONCRETE, 64, 1)
            agent.place(LEFT)
            agent.place(RIGHT)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.move(DOWN, 1)
    }
})
let Segments = 0
let length = 0
length = 5
Segments = 6
```
