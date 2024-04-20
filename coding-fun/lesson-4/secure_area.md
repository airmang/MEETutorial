### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 영역 확보

## 단계 1
에이전트가 **참나무 울타리**를 건설하도록 프로그램하세요. 에이전트는 오른쪽에 **참나무 울타리** 블록을 배치하고, 장애물을 파괴하고, 앞으로 이동해야 합니다. 울타리는 **17 블록** 길이여야 합니다.

#### ~ tutorialhint
에이전트가 오른쪽에 블록을 배치하고 왼쪽의 블록을 파괴하는 것을 확인하세요.

```blocks
player.onChat("fence", function () {
    agent.setItem(OAK_FENCE, 64, 1)
    for (let index = 0; index < 17; index++) {
            }
})
```
```ghost
player.onChat("fence", function () {
    agent.setItem(OAK_FENCE, 64, 1)
    for (let index = 0; index < 17; index++) {
        agent.place(RIGHT)
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```
