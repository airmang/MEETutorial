### @explicitHints true
# 에이전트 인베이더

```python
pos(0, 0, 0)
mobs.spawn(FIREWORKS_ROCKET, agent.get_position())
blocks.place()
blocks.test_for_block(GRASS, pos(0, 0, 0))
positions.add(pos(0, 0, 0), pos(0, 0, 0))
pos(0, 0, 0)
loops.pause(100)
agent.move(FORWARD, 5)
agent.get_position()
gameplay.title(mobs.target(NEAREST_PLAYER), "Congratulations!", "You won!")
mobs.target(NEAREST_PLAYER)
player.say("HI")
if True: 
    pass
else: 
    pass
elif:
    pass
while True:
    pass
```
## 1단계
**활동 1 - 게임 컨트롤:**
컨트롤러에는 두 개의 '버튼'이 있습니다. 파란색은 에이전트를 왼쪽으로, 빨간색은 오른쪽으로 이동시킵니다. 에이전트가 올바른 방향으로 이동하도록 코드를 작성하세요. 아래의 블록 테스트 명령어를 사용하여 특정 위치에 블록이 있는지 확인할 수 있습니다:
```python
blocks.test_for_block(BLOCK_NAME, pos(0, 0, 0))
```

### ~ tutorialhint
**True**로 설정된 `||loops:while||` 루프는 계속 반복됩니다. 코딩 창에 사전에 주어진 코드는 삭제하지 마세요.

## 2단계
**활동 2 - 발사 시스템 -**
**1부:** 에이전트가 위에 있는 금 블록을 쏘도록 다른 함수를 작성하세요.
**FIREWORKS_ROCKET**을 사용하여 쏘는 `||mobs: mob spawn||` 명령어를 사용하세요. 쏘아진 금 블록은 사라지도록 **AIR** 블록으로 교체해야 합니다.
에이전트의 위치를 얻기 위해 `||agent: agent position||` 명령어를 사용하세요.
**AIR** 블록의 위치를 얻기 위해 `||agent: agent position||` 명령어가 들어간 위치 추가 명령어를 사용하세요.
두 명령어를 함께 사용하면 다음과 같습니다:
```python 
positions.add(agent.get_position(), pos(0, 0, 0))
```
## 3단계
**2부:** 코드에 추가하여 에이전트가 두 번째 줄의 금 블록을 쏘도록 하세요. 추가적인 `||logic: elif||` 조건문을 사용하세요.

## 4단계
**활동 3 - 점수 시스템:**
변수 `||variables:score||`가 주어졌습니다. 에이전트가 금 블록을 쏠 때마다 변수에 **1**을 추가하세요.
while 루프의 조건을 편집하여 `||variables:score||`가 **15** 이하일 때만 반복되도록 하세요.
`||gameplay:show title||` 명령어를 사용하여 게임 시작과 끝에 스플래시 화면을 추가하세요.
다음 명령어를 사용하여 `||variable:score||` 변수를 전역으로 선언하세요:
```
global score 
```

### ~ tutorialhint
**<=**는 **이하**를 의미합니다.


```template
//아래에 함수를 작성하세요 #
//함수 2 선언하기                                                            |활동 2 1부
//점수 변수를 전역으로 선언하기                                               |활동 3      
//조건문, 블록 조건 테스트, 에이전트 위치 + 2                                 |활동 2 1부
//에이전트 위치에서 불꽃놀이 로켓 생성하기                                    |활동 2 1부
//100ms 동안 일시 정지하기                                                   |활동 2 1부
//에이전트 위치 + 2에 공기 블록 배치하기                                      |활동 2 1부
//변수 점수에 1 추가하기                                                     |활동 3
//조건문 elif, 블록 조건 테스트, 에이전트 위치 + 3                            |활동 2 2부
//에이전트 위치에서 불꽃놀이 로켓 생성하기                                    |활동 2 2부
//100ms 동안 일시 정지하기                                                   |활동 2 2부
//에이전트 위치 + 3에 공기 블록 배치하기                                      |활동 2 2부
//변수 점수에 1 추가하기                                                     |활동 3
//아래에 함수에 대한 주석을 작성하세요                                        |활동 1      
//함수 선언하기                                                              |활동 1
//조건문 if, 블록 조건 테스트 (밝은 파란색 콘크리트)                          |활동 1
//에이전트를 오른쪽으로 이동시키기                                            |활동 1
//조건문 elif, 블록 조건 테스트 (빨간색 콘크리트)                             |활동 1
//에이전트를 왼쪽으로 이동시키기                                              |활동 1
//아래 코드를 교체하세요 #  
점수 = 0
//게임플레이 타이틀 명령어를 사용하여 시작 스플래시 화면 추가하기              |활동 3
//점수가 15 이하일 때만 반복하도록 while 루프 변경하기                        |활동 3
//조건이 True인 while 루프                                                    |활동 1
//함수 호출하기                                                              |활동 1
//함수 2 호출하기                                                            |활동 2 1부
//게임플레이 타이틀 명령어를 사용하여 종료 스플래시 화면 추가하기              |활동 3
//에이전트 위치에 번개 생성하기                                               |활동 3  
if 점수 > 15
player.execute("scoreboard players set @p 점수 15")
```
