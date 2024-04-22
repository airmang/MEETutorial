### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 세상을 바꿔보세요!

## 단계 1
``||player:on player walk||`` 이벤트를 사용하여 특정 ``||positions: world||`` 좌표인 **100, 68, 100**에 블록을 설정합니다. ``||variable||``을 생성하고 이를 **count**라고 이름 지어줍니다. ``||change count by 1||`` 블록과 ``||blocks:place||`` 블록을 드래그하고 ``||count||`` 변수를 추가합니다. 이렇게 하면 1씩 증가하며 해당 블록 ID와 연결된 블록을 배치합니다. 1=돌, 2=잔디, 3=흙 등입니다. 다른 이벤트 블록, 예를 들어 ``||player:on player fall||``을 사용하여 블록을 재설정합니다. 그러기 위해선, ``||set count||``를 **0**으로 드래그하여 카운트를 재시작하고, 동일한 월드 좌표로 설정된 ``||variable:count||`` 변수가 추가된 ``||blocks: place||`` 블록을 추가합니다. 이렇게 하면 세상에서 점프할 때마다 블록이 재설정됩니다.

### ~ tutorialhint 
좌표를 지정할 때는 반드시 ``||positions: world||`` 위치를 사용하는 것을 잊지 마세요.

```blocks
let count = 0
player.onTravelled(WALK, function () {
    count += 1
    blocks.place(count, world(100, 68, 100))
})
```


```ghost
let count = 0
player.onTravelled(WALK, function () {
    count += 1
    blocks.place(count, world(100, 68, 100))
})
player.onTravelled(FALL, function () {
    count = 0
    blocks.place(count, world(100, 68, 100))
})
```

