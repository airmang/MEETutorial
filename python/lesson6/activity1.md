### @explicitHints true

# 활동 1 - 멈춤과 진행.

```python
loops.pause(2000)
agent.move(FORWARD, 5)
for i in range(2):
      pass
if True:
      pass
agent.detect(AgentDetection.BLOCK, FORWARD)
```

## 1단계
**1부:** 에이전트가 왼쪽에 블록이 **있을 때만** 이동하도록 코드를 작성하세요.
조건에 `||agent: agent detect||` 명령을 사용하세요: 
```python
agent.detect(AgentDetection.BLOCK, LEFT)
```

## 2단계
**2부:** 에이전트가 왼쪽에 블록이 **없을 때** 이동하도록 코드를 수정하세요.
조건 앞에 **not** 연산자를 추가함으로써 이를 수행하세요.

## 3단계
**3부:** 마지막 금 블록에 도달하도록 `||loops:pause||` 명령 후에 에이전트를 다시 이동시키세요.

### ~ tutorialhint
**1000** ms는 **1**초입니다.

```template
//아래 줄을 코드로 대체하세요 #    
//반복 7로 설정                            |1부
//아래 조건에 NOT 연산자 추가          |2부 
//Agent detect 조건이 있는 if 조건문|1부
//에이전트를 앞으로 이동시킴                  |1부
//Agent detect 조건이 있는 if 조건문                |3부
loops.pause(2000)
//에이전트를 앞으로 이동시킴                                  |3부
//반복 끝
```