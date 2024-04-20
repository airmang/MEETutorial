### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# 에이전트를 프로그래밍하여 모든 쓰레기를 수집하세요!

## 단계 1
``||agent: agent destroy||``와 ``||agent:agent collect all||`` 블록을 사용하여 거북이 트랙을 청소하세요. 코드를 더 효율적으로 만들기 위해 ``||loops:repeat||`` 블록을 사용해 보세요. 완료되면 **Play** 버튼을 눌러 코드를 컴파일하세요. Minecraft에서 코드를 실행하는 것을 잊지 마세요.


```ghost
player.onChat("garbage", function () {
    for (let index = 0; index < 4; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.collectAll()
    }
})
```
