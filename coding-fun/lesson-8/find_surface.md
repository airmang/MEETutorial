### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 마그마 도달

## 단계 1
에이전트를 프로그래밍하여 **앞으로 이동**하게 합니다. 에이전트가 **아래쪽 블록을 조사**하고 그것이 **마그마가 아닌** 동안, 에이전트는 **아래로 이동**해야 합니다.


```ghost
player.onChat("magma", function () {
    agent.move(FORWARD, 1)
    while (agent.inspect(AgentInspection.Block, DOWN) != MAGMA_BLOCK) {
        agent.move(DOWN, 1)
    }
})
```
