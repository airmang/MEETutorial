### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Hazing 

## 단계 1
Agent는 늑대가 들어오지 않도록 **트립와이어**를 설정해야 합니다. ``||agent:agent set block||``을 **트립와이어**로 설정하고 카운트를 **64**로 설정합니다. ``||loops:while||`` 블록을 사용하고 그 안에 조건을 넣습니다.

#### ~ tutorialhint
조건에서 **not**을 사용하는 것을 기억하세요.

```blocks
player.onChat("hazing", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
    	
    }
})

``` 
```ghost
player.onChat("hazing", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})
```
