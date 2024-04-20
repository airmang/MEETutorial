### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1


# Hazing One

## 단계 1
``||agent:agent set block||``을 **tripwire**로 설정하고, 개수를 **64**로 설정합니다.

## 단계 2
``||loops:while||`` 블록을 사용하고, ``||loops:while||`` 블록 안에 조건을 넣습니다.

#### ~ tutorialhint

```blocks
player.onChat("hazing", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
    	
    }
})

``` 
## 단계 3
``||loops:while||`` 블록 안에 ``||agent: agent place||``와 ``||agent: agent move||`` 블록을 추가합니다.

```blocks
player.onChat("run", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})
```
