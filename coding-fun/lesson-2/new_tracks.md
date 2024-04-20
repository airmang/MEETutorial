### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1


# 거북이 트랙을 따라 에이전트를 이동시키세요!

## 단계 1
``||agent: agent move forward||`` 블록을 사용하여 거북이 트랙을 따라 에이전트를 이동시키세요.

#### ~ tutorialhint 
코드를 더 효율적으로 만들기 위해 ``||loops:repeat||`` 블록을 사용해 보세요.

## 단계 2
완료되면 **Play** 버튼을 눌러 코드를 컴파일하세요. Minecraft에서 코드를 실행하는 것을 잊지 마세요.

```blocks
player.onChat("run", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
for (let index = 0; index < 4; index++) {
    	
 }
```