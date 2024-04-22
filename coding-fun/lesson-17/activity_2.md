### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 시청을 건설해봅시다!

## 단계 1
우리는 당신을 위해 **plantSeed**라는 함수를 만들었습니다. 이것은 단순히 이전 활동에서 사용한 코드입니다. 이제 작업 공간에 ``||player: on chat||`` 명령을 드래그하고 이를 **run**이라고 이름 지어주세요. ``||loops: repeat||`` 루프를 추가하고 **Advanced** 섹션을 클릭한 다음 **Functions**를 클릭하고 ``||function:call plantSeed||`` 함수를 루프에 드래그하세요. 에이전트가 **plantSeed** 함수를 몇 번 반복해야 하는지 세어보세요.

### ~ tutorialHint
함수는 **Advanced** 섹션에 있습니다. 코드에 대한 메모를 남기는 것도 좋은 습관입니다. 우리가 함수에 대해 남겨둔 것처럼 말이죠.

```template
/**
 * A function allows you to easily reuse code.
 */
function plantSeed () {
    agent.till(FORWARD)
    agent.move(FORWARD, 1)
    agent.place(DOWN)
}
```

```ghost
player.onChat("plantSection", function () {
    for (let index = 0; index < 11; index++) {
        plantSeed()
    }
    agent.move(FORWARD, 1)
})
```
