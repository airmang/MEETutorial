### @explicitHints true
### @hideIteration true 
# 활동 2 - 방화선.

```python
agent.turn(LEFT_TURN)
agent.place(RIGHT)
agent.move(FORWARD, 5)
agent.detect(AgentDetection.BLOCK, FORWARD) 
while True:
      pass
```

## 단계 1
에이전트가 앞에 레드스톤 더스트가 있을 때 전진하게 하는 코드를 작성하세요.
전진하는 동안 에이전트는 왼쪽에 한 블록 높이의 벽을 만들어야 합니다.
지형 높이가 바뀔 때 에이전트는 위로 올라가서 벽을 계속 이어가야 합니다.

```template
//아래 줄을 귀하의 코드로 대체하세요 #
//레드스톤 감지 조건이 있는 While 반복문 1 
//블록 감지 조건이 있는 While 반복문 2 
agent.place(LEFT)
//에이전트가 위로 올라가게 합니다                            
//에이전트가 왼쪽에 블록을 설치하게 합니다         
//에이전트가 전진하게 합니다
//While 반복문 2의 끝
//에이전트가 왼쪽에 블록을 설치하게 합니다         
//에이전트가 전진하게 합니다
//While 반복문 1의 끝                         
```