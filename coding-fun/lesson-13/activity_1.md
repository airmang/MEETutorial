### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 라바 수영

## 단계 1
당신의 도전 과제는 라바 호수를 가로질러 ``||player:swim||``하는 것입니다. **가장 가까운 플레이어**에게 ``||mobs:applying fire resistance||``을 시도해보세요.


```ghost
player.onTravelled(SWIM_LAVA, function () {
    mobs.applyEffect(FIRE_RESISTANCE, mobs.target(NEAREST_PLAYER), 10, 1)
    mobs.clearEffect(mobs.target(NEAREST_PLAYER))
})
```
