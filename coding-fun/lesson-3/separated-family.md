### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 가족을 찾아서!

## 단계 1
에이전트가 얼음의 깊은 틈을 가로질러 다리를 만들도록 프로그램하세요. 에이전트의 인벤토리에 **오크 판자** **64**개가 있는지 확인하세요.

#### ~ tutorialhint 
**while** 루프에서 **not**을 사용하는 것을 잊지 마세요. 에이전트가 어디에 블록을 놓기를 원하는지 생각해보세요.


```ghost
player.onChat("family", function () {
    agent.setItem(PLANKS_OAK, 64, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
})

```
