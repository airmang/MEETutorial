### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 초보자용 집을 지어봅시다!

## 단계 1
제공된 샘플 코드를 사용하여 블록의 행 1개를 배치하세요. 그런 다음 에이전트가 동일한 절차를 **4번 반복**하도록 하고, ``||agent: move up||``을 사용하여 **위로 이동**하고 더 **반복**하도록 합니다. ``||variable: height||``를 가져와서 ``||loops: repeat||`` 블록에 추가하세요. 이 코드를 사용하면 **1채**의 집을 지을 수 있습니다.

### ~ tutorialHint
명령을 게임 내 채팅에 입력할 때 숫자를 입력하는 것을 잊지 마세요. 예를 들어 **house 2 5**와 같이 입력합니다.

```template    
 player.onChat("house", function (height, size) {
    for (let index = 0; index < size; index++) {
        agent.setItem(STONE, 1, 1)
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
})
```

```ghost
player.onChat("build-simple", function (size, height) {
    for (let index = 0; index < height; index++) {
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < size; index++) {
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



