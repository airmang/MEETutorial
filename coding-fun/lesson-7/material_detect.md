### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 첫 번째 재료 감지하기

## 단계 1
에이전트는 **금** 블록을 **파괴**한 다음 **수집**해야 합니다.

```template
player.onChat("material", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(LEFT, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) == GOLD_BLOCK) {
            
        }
    }
})
```

```ghost
player.onChat("1", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(LEFT, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) == GOLD_BLOCK) {
            agent.destroy(FORWARD)
            agent.collectAll()
        }
    }
})
```
