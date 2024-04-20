### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 잎사귀 제거!

## 단계 1
에이전트는 **앞쪽**으로 이동하면서 **8** 블록의 잎사귀를 파괴해야 합니다. 에이전트가 파괴해야 하는 잎사귀 행은 총 **16**개입니다. 에이전트는 ``||agent:destroy forward||``와 ``||agent:move forward||``를 **8**번 실행해야 합니다.
#### ~ tutorialhint 
```blocks
player.onChat("foliage", function () {
    for (let index = 0; index < 8; index++) {
        for (let index = 0; index < 8; index++) {
        	
        }
    }
})

```

```ghost
player.onChat("foliage", function () {
    for (let index = 0; index < 8; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        for (let index = 0; index < 2; index++) {
            agent.move(FORWARD, 1)
            agent.turn(RIGHT_TURN)
        }
    }
})
```
