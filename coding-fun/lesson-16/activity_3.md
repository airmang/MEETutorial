### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 시청을 지어봅시다!

## 단계 1
건물 재료로 **돌**을 사용하고, **3개**의 ``||variable: 변수||``를 생성하여 **width**, **length**, **height**라고 이름을 붙입니다. 그런 다음 ``||variable: 변수||``를 올바른 매개변수로 설정합니다. ``||player: on chat||`` 명령에 변수를 추가하는 것을 잊지 마세요.

```ghost
player.onChat("town_hall", function (length, width, height) {
    for (let index = 0; index < height; index++) {
        for (let index = 0; index < 2; index++) {
            for (let index = 0; index < length; index++) {
                agent.setItem(STONE, 1, 1)
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
            for (let index = 0; index < width; index++) {
                agent.setItem(STONE, 1, 1)
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
        }
        agent.move(UP, 1)
    }
})
```
