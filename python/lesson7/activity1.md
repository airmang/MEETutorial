### @explicitHints true

# 활동 1 - 물 장애물.

```python
agent.turn(LEFT_TURN)
agent.place(RIGHT)
agent.move(FORWARD, 5)
agent.detect(AgentDetection.BLOCK, FORWARD) 
while True:
      pass
```

## 단계 1
**부분 1:** 에이전트가 앞에 레드스톤 더스트가 있을 때 전진하도록 코드를 작성하세요.

## 단계 2
**부분 2:** 에이전트가 이동하면서 오른쪽에 두 블록 높이의 벽을 설치하는 시퀀스를 코드에 추가하세요.
### ~ tutorialhint
에이전트에게 블록을 줄 필요가 없습니다. 에이전트의 인벤토리에 이미 필요한 블록이 있습니다.
```template
//아래 줄을 귀하의 코드로 대체하세요 #     
//에이전트 감지 조건이 있는 While 반복문 |부분 1
//에이전트가 오른쪽에 블록을 설치하게 합니다       |부분 2
//에이전트가 위로 이동하게 합니다                  |부분 2
//에이전트가 오른쪽에 블록을 설치하게 합니다       |부분 2
//에이전트가 다시 아래로 이동하게 합니다           |부분 2:
    agent.move(FORWARD, 1)
//While 반복문의 끝                                
```