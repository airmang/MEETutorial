### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# 에이전트가 골드 플레이트로 이동하도록 프로그래밍하세요!

## Step 1
''|player:on chat||`` 명령어를 선택하고 **run**에서 **1**로 이름을 변경합니다. ''|agent: agent move||`` 블록을 선택하고 이 블록을 ''|player:on chat||`` 명령어 내부로 끌어 놓습니다. 에이전트가 골드 플레이트에 도달할 수 있도록 에이전트가 이동하는 **number** 단계를 **3**로 변경합니다. 완료되면 **Play** 버튼을 눌러 코드를 컴파일한 후 마인크래프트로 이동하여 **t**를 누르고 **1**를 입력합니다.

#### ~ tutorialhint 
"||agent: agent move||" 블록 안의 숫자를 변경하여 에이전트가 이동할 단계 수를 변경할 수 있습니다. 또한 "||agent: agent turn||" 블록을 사용하여 에이전트를 왼쪽 또는 오른쪽으로 돌릴 수 있습니다.



```ghost
player.onChat("1", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})

``` 