### @explicitHints true
# 활동 2 - 세탁기 돌리기.

```python
for i in range(2):
pass
agent.collect_all()
agent.move(FORWARD, 5)
agent.drop_all(FORWARD)
agent.turn(LEFT)

```

## 1단계
**1부:** 에이전트가 더러운 세탁물을 줍고, 기계 안으로 **앞으로** 이동하여 왼쪽으로 **20**번 회전한 다음 기계 밖으로 나와
더러운 세탁물이 있던 반대편에 깨끗한 세탁물을 놓도록 코드를 작성하세요.

## 2단계
**2부:** 같은 코드를 편집하여 에이전트가 **3** 묶음의 세탁물에 대해 동일한 작업을 수행하도록 합니다. 다른 코드 전에 `||loops: for||` 반복문을 사용하여 이를 수행하세요.

### ~ tutorialhint 
이 경우, 두 반복문은 같은 변수 이름을 사용해서는 안 되므로, 두 번째 반복문의 변수 이름을 변경하는 것을 잊지 마세요.
큰 코드 덩어리를 들여쓰기 하려면 들여쓰기하고 싶은 모든 코드를 강조 표시한 다음 **tab** 키를 누르세요.

```template
//아래 줄을 코드로 대체하세요 #    
//반복 2 설정값 3으로                              | 2부
agent.collect_all()
agent.move(FORWARD, 7)
agent.drop_all(FORWARD)
//반복 1                              | 1부
//에이전트가 왼쪽으로 20번 회전하도록 함          | 1부 
//반복 1 끝
//에이전트가 모두 수집하도록 함                 | 1부          
//에이전트가 뒤로 이동하도록 함                   | 1부
//에이전트가 왼쪽에 모든 것을 떨어뜨리도록 함 | 1부
//반복 2 끝
```