### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 건축

## 단계 1
``||mobs:Give||`` 명령어를 사용하여 자신에게 최소한 **34개의 에메랄드** 블록을 줍니다. 새로운 ``||variable||``을 생성하고 이를 **count**라고 이름 지어줍니다. ``||blocks:on block placed||`` 블록을 가져와서 이를 **에메랄드**로 설정합니다. ``||change count||`` 블록을 ``||blocks: on block placed||`` 안에 드래그하고 ``||player: say||`` 블록을 추가합니다. ``||player: say||`` 블록 안에 ``||count||``를 추가합니다. 이렇게 하면 블록을 배치할 때마다 게임이 얼마나 많은 블록을 배치했는지 계산합니다.

### ~ tutorialhint 

철, 금, 에메랄드 또는 다이아몬드를 선택할 수 있습니다.

```blocks
let count = 0
blocks.onBlockPlaced(EMERALD_BLOCK, function () {
    count += 1
    player.say(count)
})

```

```ghost
blocks.onBlockBroken(STONE, function () {
    count += 1
    player.say(count)
})
let count = 0
mobs.give(
mobs.target(NEAREST_PLAYER),
STONE,
1
)
})
```


