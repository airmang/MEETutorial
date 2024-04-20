### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 대나무 은신처

## 단계 1
모래 패치의 각 면에 에이전트가 **3**개의 대나무 블록을 심도록 프로그램하세요. 에이전트가 활동을 완료할 수 있도록 ``||agent: agent turn||`` 명령어를 추가하세요.

#### ~ tutorialhint
2개의 **반복** 루프가 있어야 합니다. 하나는 다른 하나 안에 중첩되어 있어야 합니다.
 
```ghost
player.onChat("bamboo", function () {
    for (let index = 0; index < 3; index++) {
        agent.setItem(BAMBOO, 64, 1)
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
})
```
