### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# 거북이 트랙을 따라 이동하고 장애물을 파괴하는 에이전트를 프로그래밍하세요!

## 단계 1
``||agent: agent destroy||``와 ``||agent:agent collect all||`` 블록을 사용하여 길을 막고 있는 **나무 기둥을 파괴**하세요. 코드를 더 효율적으로 만들기 위해 ``||loops:repeat||`` 블록을 사용해 보세요. 완료되면 **Play** 버튼을 눌러 코드를 컴파일하세요. Minecraft에서 코드를 실행하는 것을 잊지 마세요.


```ghost
player.onChat("path", function () {
    for (let index = 0; index < 4; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.collectAll()
    }
})
```

출처: Bing과의 대화, 2024. 4. 20.
(1) github.com. https://github.com/tech8989/EducationContent/tree/6114b0521d805218dc885a356cd16a56b51b0b0e/CodingFUNdamentals1_2_2.md.
(2) github.com. https://github.com/olesolo/EducationContent/tree/2589e14a66689965fb7c87d209215c79000cdcba/coding-fun%2Flesson-2%2Fblocked-path.md.