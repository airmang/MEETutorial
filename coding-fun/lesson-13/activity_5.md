### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 비를 내려라!

## 단계 1
마인크래프트에서 춤추면서 비를 내리게 해보세요! 이를 위해 여러 이벤트 핸들러를 사용해야 합니다. 1. 변수를 생성합니다. 예를 들어: **walk**, **jump** 그리고/또는 **break**. 2. 이벤트 핸들러를 선택합니다. 예를 들어 ``||player: on player fall||``, ``||player: on player walk||``. 3. 각 해당 이벤트 블록 내에서 새로운 ``||variables||``를 ``||logic: true||``로 설정합니다. 4. ``||loop: forever||`` 블록을 사용하고 그 안에 ``||logic: if statement||``를 드래그합니다. 모든 조건을 ``||logic:true||``로 설정하고, 그 안에 **rain**으로 설정된 ``||gameplay: weather||`` 블록을 추가합니다.

### ~ tutorialHint
```blocks
let walk = false
player.onTravelled(WALK, function () {
    walk = true
})
loops.forever(function () {
    if (walk == true && "" == "") {
    	
    }
})

```

```ghost
let climb = false
let walk = false
let _break = false
player.onTravelled(CLIMB, function () {
    climb = true
})
player.onTravelled(WALK, function () {
    walk = true
})
blocks.onBlockBroken(STONE, function () {
    _break = true
})
loops.forever(function () {
    if (walk == true && climb == (true && _break == true)) {
        gameplay.setWeather(RAIN)
    }
})
```
