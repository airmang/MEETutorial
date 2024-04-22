### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 주변 환경

## 단계 1
**바닥에 있는 블록**이 **팩트 아이스가 아닌 경우**, 에이전트가 **오른쪽 블록을 감지하면** **앞으로 이동**해야 합니다. 그렇지 않으면 **오른쪽으로 이동**해야 합니다. 같은 루프 내에서, 에이전트가 **바닥 블록을 조사하고** 그것이 **조약돌** **또는** **자갈**인 경우, 그것을 **아래로 파괴하고** **모두 수집**해야 합니다.


```template
player.onChat("ice", function () {
    while (0 == 0) {
        if (true) {
        	
        } else {
        	
        }
        if (agent.inspect(AgentInspection.Block, DOWN) == COBBLESTONE ||agent.inspect(AgentInspection.Block, DOWN) == GRAVEL ) {
        	
        }
    }
})
```
```ghost
player.onChat("2", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != PACKED_ICE) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
            agent.move(FORWARD, 1)
        } else {
            agent.move(RIGHT, 1)
        }
        if (agent.inspect(AgentInspection.Block, DOWN) == COBBLESTONE || agent.inspect(AgentInspection.Block, DOWN) == GRAVEL) {
            agent.destroy(DOWN)
            agent.collectAll()
        }
    }
})
```
