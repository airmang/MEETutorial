### @explicitHints true

# 활동 2 - 바위 부수기.

```python
agent.destroy(FORWARD)
agent.place(RIGHT)
agent.collect_all()
agent.move(FORWARD, 5)
agent.till(BACK)
for i in range(4):
      pass
if agent.inspect(AgentInspection.BLOCK, FORWARD) == GRASS:
    pass
else: 
    pass
```

## 단계 1
**부분 1:** 에이전트가 전진하면서 길을 막고 있는 **돌** 블록을 부수고 모으도록 코드를 작성하세요.
### ~ tutorialhint
에이전트 감지 조건 명령 구조:  
```python
agent.inspect(AgentInspection.BLOCK, DIRECTION) == BLOCK_TYPE
```

## 단계 2
**부분 2:** 이제 에이전트가 **풀** 블록 위에 갈아엎고 묘목을 심도록 코드에 추가하세요.
### ~ tutorialhint
에이전트 감지 조건 명령 구조:  
```python
agent.inspect(AgentInspection.BLOCK, DIRECTION) == BLOCK_TYPE
```

```template
//아래에 당신의 함수를 배치하세요 #
//아래에 함수에 대한 주석을 대체하세요                  |부분 1   
//함수 1을 선언하세요                                    |부분 1
//에이전트가 앞에 있는 블록을 파괴하게 합니다             |부분 1
    agent.move(FORWARD, 1)
//아래에 함수에 대한 주석을 대체하세요                          |부분 2   
//함수 2를 선언하세요                                          |부분 2
//에이전트가 전진하게 합니다                                    |부분 2
//에이전트가 뒤를 갈아엎게 합니다                               |부분 2
//에이전트가 뒤에 묘목을 심게 합니다                            |부분 2
//아래 줄을 귀하의 코드로 대체하세요 #  
//For 반복문을 12로 설정합니다                          |부분 1
//돌(STONE)에 대한 에이전트 감지 조건을 가진 if else 조건문 |부분 1
//바위를 제거하기 위한 함수를 호출합니다                |부분 1
//풀(GRASS)에 대한 에이전트 감지 조건을 가진 Elif 조건문            |부분 2            
//나무를 심기 위한 함수를 호출합니다                             |부분 2
//if else 조건문의 Else 부분                            |부분 1
//에이전트가 전진하게 합니다                             |부분 1          
```