### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1

# 에이전트를 금판까지 움직이게 프로그래밍하세요!

## 첫 번째 단계
에이전트가 금판에 도달하도록 프로그래밍하세요. 당신은 자신의 금판 위에 있어야 하며, 에이전트는 다른 금판 위에 있어야 합니다. 완료되면 **실행** 버튼을 눌러 코드를 컴파일하세요. 게임에서 코드를 실행하기 위해 마인크래프트로 이동하세요.

```ghost
player.onChat("last", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```