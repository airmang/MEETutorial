### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 씨앗을 심어봅시다!

## 단계 1
먼저 에이전트와 상호작용하여 그의 인벤토리를 열고 씨앗을 주세요. 그런 다음 ``||player: on chat||`` 명령을 생성하고 ``||agent: till forward||``와 ``||agent: place forward||``를 추가하세요.

```ghost
player.onChat("plantSeed", function () {
    agent.till(FORWARD)
    agent.place(FORWARD)
})
```
