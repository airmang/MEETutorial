### @explicitHints true
### @hideIteration true 
# Diamond rush. 

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
for i in range(10):
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
각 줄의 시작과 끝에서 따옴표(**'**)를 삭제하세요. 에이전트가 골드 블록을 향해 이동하면서 지나가는 각 다이아몬드 블록을 세는 코드를 완성하세요. 마지막에, 에이전트가 골드 블록에 도달하면, 에이전트는 지나간 다이아몬드 블록의 수를 앞에 하나씩 놓아야 합니다. 이 블록들은 피스톤에 의해 자동으로 쌓입니다.
```template
'diamond = 0'
'for index in range(11):'
'    agent.move(FORWARD, 1)'
'for index2 in range(diamond):'
'    agent.place(FORWARD)'
'    loops.pause(500)'
```
