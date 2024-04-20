### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 대나무 경계

## 단계 1
우리가 준비한 시작 코드가 있습니다. 먼저 실행해보세요. 최종 목표는 판다의 플롯을 따라 **4**면에 대나무를 심는 것입니다.

```template
player.onChat("bamboo", function () {
    agent.setItem(BAMBOO, 64, 1)
    for (let index = 0; index < 16; index++) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(LEFT_TURN)
})
```
