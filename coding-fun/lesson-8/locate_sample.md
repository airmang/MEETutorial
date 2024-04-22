### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 샘플을 찾아라!

## 단계 1
에이전트가 **아래쪽 블록을 조사**하고 **블루 아이스를 찾지 못하는 동안**, 에이전트를 프로그램하여 **파괴하고 아래로 이동**하도록 하세요. 에이전트가 **블루 아이스를 찾으면**, 그것을 **아래로 파괴하고 샘플을 수집**하도록 해야 합니다.

```ghost 
player.onChat("ice", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != ICE) {
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
    }
    agent.destroy(DOWN)
    agent.collectAll()
    
})
```

