### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 큰 협곡!

## 단계 1
에이전트를 프로그램하여 얼음의 협곡을 가로질러 **다리를 만들도록** 하세요. ``||agent:set block or item||``을 사용하여 에이전트가 인벤토리에 필요한 재료를 가지고 있는지 확인하세요. 건축 재료로 **오크**를 선택하고 **블록의 양**은 **64**로 설정하세요. 에이전트가 아래쪽에 블록을 감지하지 **못하면** ``||loops:while||``, 에이전트가 오크 판자를 **아래쪽**에 놓고 **앞으로** 이동하여 다리를 만들도록 프로그램하세요.

```template
player.onChat("chasm", function () {
    agent.setItem(PLANKS_OAK, 1, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, DOWN))) {
    	
    }
})
```

```ghost
player.onChat("chasm", function () {
    agent.setItem(PLANKS_OAK, 64, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})

```