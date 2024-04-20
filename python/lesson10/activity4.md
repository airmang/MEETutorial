### @explicitHints true
### @hideIteration true 

# 봄도착

```python
agent.move(FORWARD, 5)
pos(0, 0, 0)
player.say("Finished")
agent.place(LEFT)
agent.inspect(AgentInspection.BLOCK, DOWN) 
agent.turn(RIGHT_TURN)
agent.destroy(BACK)
agent.drop_all(FORWARD)
agent.collect_all()
loops.pause(500)
for index in range(10):
    pass
if True: 
    pass
else: 
    pass
elif:
    pass
while True:
    pass
```

## Step 1
코드 창에서 작동하지 않는 코드가 주어졌습니다. 각 행의 처음과 끝에서 따옴표(**'**)를 삭제합니다. 
이 코드는 에이전트가 한 줄로 구역을 이동하도록 함으로써 각 풀 블록에 꽃을 심도록 되어 있습니다.
조건부를 추가하고 메인 루프를 디버깅하면 코드를 끝낼 수 있습니까?
```template
'for index in range(4):'
'   for index2 in range(8):'
'        if agent.inspect(AgentInspection.BLOCK, DOWN) == GRASS:'
'            agent.place(DOWN)'
'        agent.move(FORWARD, 1)'
'   agent.turn(RIGHT_TURN)'
'   agent.move(FORWARD, 1)'
'   agent.turn(RIGHT_TURN)'
'   for index3 in range(8):'
'       if True:'
'           agent.place(DOWN)'
'       agent.move(FORWARD, 1)'
'   agent.turn(LEFT_TURN)'
'   agent.move(FORWARD, 1)'
'   agent.turn(LEFT_TURN)'
```

