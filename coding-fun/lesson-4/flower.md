### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# 지역을 예쁘게 만들어봅시다!

## 단계 1
은신처의 **4**면에 **14개의 민들레**를 심어야 합니다. 에이전트는 한 면에 **14**개의 민들레를 심을 수 있습니다.

#### ~ tutorialhint 
``||agent:agent set block||`` 명령어에 대한 카운트를 선택하는 것을 잊지 마세요.


```ghost
player.onChat("flower", function () {
    for (let index = 0; index < 4; index++) {
        for (let index = 0; index < 14; index++) {
            agent.setItem(YELLOW_FLOWER, 64, 1)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.turn(RIGHT_TURN)
    }
})

```
