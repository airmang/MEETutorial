@explicitHints true
에이전트 침입자
python
Copy code
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
단계 1
활동 1 - 게임 컨트롤:
컨트롤러에는 파란색 버튼은 에이전트를 왼쪽으로 이동시키고, 빨간색 버튼은 에이전트를 오른쪽으로 이동시킵니다. 빨간색 또는 파란색 블록 위에 서 있으면 올바른 방향으로 에이전트가 이동하도록 코드를 작성하세요. 아래의 블록 테스트 명령을 사용하여 특정 위치에 블록이 있는지 확인하십시오:

python
Copy code
blocks.test_for_block(BLOCK_NAME, pos(0, 0, 0))
~ tutorialhint
True로 설정된 ||loops:while|| 반복문은 계속해서 반복됩니다. 코딩 창에 주어진 코드를 삭제하지 마세요.

단계 2
활동 2 - 발사 시스템:
부분 1: 에이전트가 아래의 금 블록을 발사하도록 다른 함수를 작성하십시오.
FIREWORKS_ROCKET을 사용하여 ||mobs:몹 생성|| 명령을 사용하여 발사하십시오. 각 금 블록이 발사될 때마다 블록이 AIR 블록으로 대체되어 사라져야 합니다.
||agent:에이전트 위치|| 명령을 사용하여 에이전트의 위치를 가져오세요.
||agent:에이전트 위치|| 명령을 사용하여 AIR 블록의 위치를 가져오는 add positions 명령을 사용하세요. 두 명령을 함께 사용하면 다음과 같습니다:

python
Copy code
positions.add(agent.get_position(), pos(0, 0, 0))
단계 3
부분 2: 코드에 추가하여 에이전트가 두 번째 줄의 금 블록을 발사하도록 만듭니다. 추가적인 ||logic:elif|| 조건문을 사용하세요.

단계 4
활동 3 - 점수 계산 시스템:
주어진 코드에서 ||variables:점수||라는 변수가 있습니다. 에이전트가 금 블록을 발사할 때마다 변수에 1을 추가하십시오.
while 루프의 조건을 수정하여 ||variables:점수||가 15보다 작거나 같을 때만 루프가 반복되도록 하십시오.
||gameplay:타이틀 보이기|| 명령을 사용하여 게임 시작과 종료에 각각 두 개의 플래시 화면을 추가하세요. ||variable:점수|| 변수를 전역으로 선언하려면 다음 명령을 사용하세요.

csharp
Copy code
global score 
~ tutorialhint
**<=**는 보다 작거나 같음을 의미합니다.


```template
//아래에 당신의 함수를 대체하세요 #
//함수 2를 선언하세요                                                          |활동 2 부분 1
//전역으로 점수 변수를 선언하세요                                                           |활동 3      
//조건문, 특정 위치에 있는 블록 확인, 에이전트 위치 + 2를 테스트합니다              |활동 2 부분 1
//에이전트 위치에서 폭죽을 생성합니다                                               |활동 2 부분 1
//100ms 동안 일시 중지                                                          |활동 2 부분 1
//에이전트 위치 + 2에 AIR 블록을 배치합니다                                           |활동 2 부분 1
//변수 score에 1을 더합니다                                                         |활동 3
//조건문, 특정 위치에 있는 블록 확인, 에이전트 위치 + 3를 테스트합니다           |활동 2 부분 2
//에이전트 위치에서 폭죽을 생성합니다                                               |활동 2 부분 2
//100ms 동안 일시 중지                                                          |활동 2 부분 2
//에이전트 위치 + 3에 AIR 블록을 배치합니다                                           |활동 2 부분 2
//변수 score에 1을 더합니다                                                         |활동 3
//함수에 대한 주석을 대체합니다                                         |활동 1      
//함수를 선언합니다                                                    |활동 1
//블록 조건(LIGHT_BLUE_CONCRETE)에 대한 If 조건문                      |활동 1
//에이전트를 오른쪽으로 이동시킵니다                                           |활동 1
//블록 조건(RED_CONCRETE)에 대한 Elif 조건문                            |활동 1
//에이전트를 왼쪽으로 이동시킵니다                                             |활동 1
//아래의 코드 라인을 당신의 코드로 대체하세요 #
score = 0
//게임 시작 스플래시 화면을 추가하세요. gameplay title 명령을 사용합니다                      |활동 3
//점수가 15보다 작거나 같을 때만 while 루프가 반복되도록 수정하세요                            |활동 3
//True로 설정된 while 루프                                   |활동 1
//함수를 호출하세요                                            |활동 1
//함수 2를 호출하세요                                                |활동 2 부분 1
//게임 종료 스플래시 화면을 추가하세요. gameplay title 명령을 사용합니다                    |활동 3
//에이전트 위치에 번개를 소환하세요                                                           |활동 3  
if score > 15
player.execute("scoreboard players set @p score 15")
```  