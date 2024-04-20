### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# 거북이 트랙을 따라 에이전트를 움직이도록 프로그램하세요!

## 단계 1
``||agent: agent move forward||`` 블록을 사용하여 거북이 트랙을 따라 에이전트를 움직이세요. 완료되면 **Play** 버튼을 눌러 코드를 컴파일하세요. 마인크래프트에서 코드를 실행하는 것을 잊지 마세요.

```ghost
player.onChat("tracks", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
for (let index = 0; index < 4; index++) {
    	
 }
```