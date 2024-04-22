### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 자원을 캐세요!

## 단계 1
에이전트는 **금 광석**과 **철 광석** 블록을 캐야 합니다. 에이전트가 다양한 방향으로 움직이도록 프로그래밍할 수 있는 몇 가지 ``||player:on chat||`` 명령을 생성해 보세요. 예를 들어, **앞으로**, **뒤로**, **오른쪽** 등입니다. 에이전트가 얼마나 멀리 움직일지 지정하는 대신 변수를 사용할 수 있습니다. 게임 내 채팅에서 명령을 입력할 때, **앞으로**와 **숫자**를 입력하세요. 예를 들어, 에이전트가 **5단계 앞으로 이동**하길 원한다면 **앞으로 5**를 입력하세요. 이렇게 하면 코드를 변경하지 않고도 에이전트가 움직여야 할 단계 수를 즉시 변경할 수 있습니다.

### ~ tutorialHint
에이전트가 광물을 캐도록 프로그래밍하기 위해 ``||agent: destroy||``와 ``||agent: collect||`` 블록을 추가하는 것을 잊지 마세요.

```template
player.onChat("forward", function (num1) {
    agent.move(FORWARD, num1)
})
```
```ghost
player.onChat("right", function (num1) {
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, num1)
})
player.onChat("back", function (num1) {
    agent.turn(RIGHT_TURN)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, num1)
})
player.onChat("left", function (num1) {
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, num1)
})
player.onChat("collect", function () {
    agent.destroy(DOWN)
    agent.collectAll()
})
```


