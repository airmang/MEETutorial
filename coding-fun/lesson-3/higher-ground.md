### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# 높은 곳으로!

## 단계 1
에이전트를 프로그램하여 **오크** 블록으로 **10** 블록 높이의 탑을 만드세요. 먼저, 에이전트가 **64** 블록의 **오크 판자**를 가지고 있는지 ``||agent:set block or item||`` 명령을 사용하여 확인하세요. 에이전트가 오크 판자를 **앞쪽**, **왼쪽** 및 **오른쪽**에 놓도록 ``||agent:agent place||`` 블록을 사용하여 프로그램하세요. 에이전트는 블록을 놓은 후에 **위로 이동**해야 합니다.

#### ~ tutorialhint 
``||loops:repeat||`` 블록을 사용해 보세요. 숫자를 **10**으로 변경하세요.

## 단계 2
에이전트를 프로그램하여 탑에서 **아래로 이동**하고 **10** 블록 높이의 **사다리**를 만드세요. 당신이 올라갈 수 있도록 사다리가 필요합니다!

#### ~ tutorialhint 
에이전트의 인벤토리에서 ``||agent: agent set block||``을 사용하여 **64** 블록의 **사다리**를 선택하는 것을 잊지 마세요. 그래야 에이전트가 사다리를 놓을 수 있습니다.

```ghost
player.onChat("tower", function () {
    agent.move(FORWARD, 1)
    agent.setItem(LADDER, 64, 1)
    for (let index = 0; index < 10; index++) {
        agent.place(FORWARD)
        agent.move(UP, 1)
    }
    agent.move(DOWN, 10)
})

```