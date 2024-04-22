### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1

# 석영 채굴!

## 단계 1
남은 열을 만드는 데 필요한 **블록**의 수를 **계산**하는 코드를 작성하세요. 다음은 몇 가지 사실입니다: 총 **6개의 열**이 있고 각 열은 **6 블록 높이**입니다. ``||loops: on start||``에서 ``||variable:height||``와 ``||variable:quantity||`` 변수를 올바른 숫자로 생성하고 설정한 다음, ``||variable:total blocks||`` 변수를 생성하세요.

## 단계 2
조건을 설정하세요, ``||logic: if||`` ``||variable:total blocks||`` = ``||variable:height||`` * ``||variable:quantity||``이면, ``||player: say||`` "충분한 블록을 모았습니다!".

## 단계 3
이제 ``||variable:change total blocks||``에 1을 추가하는 명령과 ``||player: say||`` ``||variable:total blocks||``를 추가하여, 얼마나 많은 블록을 모았는지 알 수 있게 하세요. 반드시 ``||blocks: pillar of quartz block broken||``를 추가하여 블록을 부술 때마다 카운트가 보이도록 해야 합니다. 모두 완료하면 "충분한 블록을 모았습니다!"라는 메시지가 표시됩니다.

```ghost
blocks.onBlockBroken(PILLAR_QUARTZ_BLOCK, function () {
    total_blocks += 1
    if (total_blocks == height * quantity) {
        player.say("Collected enough blocks!")
    }
})
let total_blocks = 0
let quantity = 0
let height = 0
height = 6
quantity = 6
```
