### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 공룡을 피해 가세요!

## 단계 1
자신을 ``||mobs:invisible||``로 만들어 공룡을 ``||player:sneak past||``해야 합니다. 이것을 할 수 있을까요?

### ~ tutorialHint
마인크래프트에서 shift와 W를 눌러 몰래 지나가보세요.


```ghost
player.onTravelled(SNEAK, function () {
    mobs.applyEffect(INVISIBILITY, mobs.target(NEAREST_PLAYER), 3, 1)
})
```
