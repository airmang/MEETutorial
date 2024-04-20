### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1

# 에이전트를 금판까지 움직이게 프로그래밍하세요!

## 첫 번째 단계
``||player:on chat||`` 명령어와 ``||agent:agent move||`` 명령어를 사용하여 에이전트가 금판 쪽으로 움직이도록 프로그래밍하세요. 에이전트가 **위로** 움직이도록 프로그래밍할 수 있습니다. 완료되면 **실행** 버튼을 눌러 코드를 컴파일하세요. 게임에서 코드를 실행하기 위해 마인크래프트로 이동하세요.

```ghost
player.onChat("up", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```