### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 등반

## 단계 1
당신의 도전 과제는 접근할 수 없는 지역까지 올라가기 위해 정말 높이 ``||mobs:jump||``하는 것입니다.

```ghost
loops.forever(function () {
    mobs.applyEffect(JUMP_BOOST, mobs.target(NEAREST_PLAYER), 10, 1)
    mobs.clearEffect(mobs.target(NEAREST_PLAYER))
})
```
