### @explicitHints true
 
# 활동 2 - 왼쪽인가, 오른쪽인가?

```python
agent.inspect(AgentInspection.BLOCK, FORWARD)
agent.turn(LEFT_TURN)
agent.move(FORWARD, 5)
for i in range(2):
      pass
if True:
      pass
```

## 1단계
**1부:** 에이전트가 표지판에 도달했을 때 왼쪽으로 돌아 금 블록으로 이동하도록 `||logic:if else||` 조건문을 사용하여 코드를 작성하세요. 조건으로 `||agent:agent inspect||` 명령을 사용하고 이를 변수 **left**와 비교하세요.
`||agent:agent inspect||` 명령은 다음과 같습니다:
```python
agent.inspect(AgentInspection.BLOCK, FORWARD)
```
코드에 이미 제공된 변수를 사용하세요: left = BLUE_GLAZED_TERRACOTTA, right = PINK_GLAZED_TERRACOTTA
### ~ tutorialhint 
두 값이 같은지 확인하려면 **==**을 사용하세요.

## 2단계
**2부:** 에이전트가 금 블록에 도달할 때까지 양쪽 방향으로 돌 수 있도록 코드를 편집하세요. 이를 위해 **if**와 **else** 부분 사이에 **elif**
조건문을 추가하세요.
### ~ tutorialhint 
**elif** 조건문을 `||agent:agent inspect||` 명령의
조건으로 사용하고 이를 변수 **right**와 비교하세요.

```template
left = BLUE_GLAZED_TERRACOTTA
right = PINK_GLAZED_TERRACOTTA
//아래 줄을 코드로 대체하세요 #
//아래 반복문의 값을 9에서 21로 변경하세요                     |2부
//반복 9로 설정                                   |1부
//Agent inspect 조건이 있는 if else 조건문 |1부
agent.turn(LEFT_TURN)
//Agent inspect 조건이 있는 elif 조건문            |2부
//에이전트가 오른쪽으로 회전하도록 하세요                                   |2부
//if else 조건문의 else 부분                |1부
//에이전트가 앞으로 이동하도록 하세요                         |1부
//반복 끝                                         |1부
```