### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 주변 환경

## 단계 1
에이전트가 **아래쪽 블록을 감지**하는 동안, 앞으로 이동해야 합니다. 에이전트가 **아래쪽 블록을 조사**하고 **공기**를 발견하면, ``||player:say||`` 명령어를 사용하여 **Crater found!**를 말해야 합니다.


```template
player.onChat("crater", function () {
            player.say("Crater found!")
})
```
```ghost
player.onChat("1", function () {
    while (agent.detect(AgentDetection.Block, DOWN)) {
        agent.move(FORWARD, 1)
    }
    if (agent.inspect(AgentInspection.Block, DOWN) == AIR) {
        player.say("Crater found!")
    }
})
```
