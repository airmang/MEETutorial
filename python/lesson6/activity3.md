### @explicitHints true
### @hideIteration true 
# 활동 3 - 통과하기.

```python
agent.detect(AgentDetection.BLOCK, FORWARD) 
agent.turn(LEFT_TURN)
agent.move(FORWARD, 5)
for i in range(2):
      pass
if True:
      pass
```

## 단계 1
에이전트가 코스를 지나가면서 무작위로 배치된 블록을 감지하고 피할 수 있는 코드를 작성하세요. 이를 위해 `||logic:if else||` 조건문을 사용하고, 그 사이에 **elif** 조건문을 추가하세요. **if** 조건에는 **and not** 연산자 사이에 두 개의 `||agent:agent detect||` 명령을 사용하세요. **elif** 조건에는 **and** 연산자 사이에 두 개의 `||agent:agent detect||` 명령을 사용하세요. **and not** 연산자가 있는 두 조건의 예시:
```python
agent.detect(AgentDetection.BLOCK, DIRECTION) and not agent.detect(AgentDetection.BLOCK, DIRECTION)
```

### ~ tutorialhint 
여러 조건을 함께 사용할 때 **and** 또는 **and not**을 사용하여 여러 상태를 확인할 수 있습니다.

```template
//아래 줄을 귀하의 코드로 대체하세요 #    
//for 반복문은 23으로 설정                                            
//and not 연산자로 분리된 두 Agent detect 명령을 사용하는 if else 조건문
agent.move(LEFT, 1)                              
//and 연산자로 분리된 두 Agent detect 명령을 사용하는 elif 조건문
agent.move(RIGHT, 2)
//else if 조건문의 else 부분             
agent.move(FORWARD, 1)                                   
//반복문의 끝                                       
```