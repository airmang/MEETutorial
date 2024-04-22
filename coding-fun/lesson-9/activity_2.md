### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 깊은 돌

## 단계 1
이 코딩 스니펫을 수정하세요. 에이전트의 목표는 표면을 파서 **왼쪽**에 **금** 블록을 만날 때까지 내려가는 것입니다. 내려가는 도중에 에이전트는 앞에 **돌**이 있는지 감지하고 수집할 것입니다.

```template
player.onChat("dig", function () {
    while (agent.inspect(AgentInspection.Block, LEFT) == AIR) {
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
            if (agent.inspect(AgentInspection.Block, FORWARD) != GRASS) {
                player.say("Found the stone!")
                agent.destroy(FORWARD)
                agent.collectAll()
        }
    }
})
```


