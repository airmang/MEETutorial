### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 포탈을 가동시키세요!

## 단계 1
**금 판** 위에 서 있을 때 번개가 치도록 해야 합니다. 먼저, ``||gameplay: weather||``를 비로 설정해야 합니다 ``||loops: on start||``. 그런 다음 ``||logic: if||``, ``||blocks: test for||`` 그리고 ``||mobs: spawn a lightning bolt||``를 ``||player: on walk||`` 안에 배치하여 정확한 순간에 번개가 치도록 만듭니다.

### ~ tutorialHint
금 판은 당신 아래 **0, -1, 0** 좌표에 있습니다.

```ghost
player.onTravelled(WALK, function () {
    if (blocks.testForBlock(GOLD_BLOCK, pos(0, -1, 0))) {
        mobs.spawn(LIGHTNING_BOLT, pos(0, 0, 0))
    }
})
gameplay.setWeather(RAIN)
```
