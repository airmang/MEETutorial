### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 치킨 쿠프

## 단계 1
에이전트는 **철창**을 **9** 블록씩 **2** 층을 배치해야 합니다. **철창**이 필요한 쪽은 총 **4** 쪽입니다. 두 번째 층을 지을 때는 ``||agent:agent move up||``를 사용하는 것을 잊지 마세요.

#### ~ tutorialhint
마지막에는 ``||loops:repeat|`` 명령어가 서로 중첩된 채로 **3**개가 있을 것입니다. 에이전트의 인벤토리에 64개 이상의 블록이 있는지 확인하세요!

```ghost
player.onChat("chicken", function () {
    for (let index = 0; index < 2; index++) {
        agent.setItem(IRON_BARS, 1, 1)
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < 9; index++) {
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
        }
        agent.move(UP, 1)
    }
})

```
