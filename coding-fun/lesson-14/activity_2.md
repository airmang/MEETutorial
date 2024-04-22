### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 모래성!

## 단계 1
제시된 도전 과제를 극복하기 위해 코딩 초능력을 사용하세요. 해결 방법은 여러 가지일 수 있음을 기억하세요.

```ghost
player.onTravelled(SNEAK, function () {
    mobs.applyEffect(INVISIBILITY, mobs.target(NEAREST_PLAYER), 3, 1)
    mobs.spawn(CHICKEN, pos(0, 0, 0))
    mobs.give(
    mobs.target(NEAREST_PLAYER),
    GRASS,
    1
    )
})
player.onChat("jump", function () {
	
})

```