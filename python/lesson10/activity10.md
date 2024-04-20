### @explicitHints true
### @hideIteration true 

# Do I need to list it out? 

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
## 1단계
목록이 주어졌습니다. 각 행의 처음과 끝에서 따옴표(**'**)를 삭제합니다. 에이전트가 어떤 블록에 서야 하는지 찾으려면 **sort**를 알파벳 순으로 나열합니다
그리고 목록에서 **second** 블록을 가져옵니다. 올바른 블록 유형에 서서 버튼을 누르면 에이전트가 그곳으로 순간이동됩니다. 
플레이어가 **reverse**에 서야 할 블록 유형을 찾으려면 목록의 **reverse**와 목록의 **fourth** 블록을 **pop**에서 찾아야 합니다. 
목록에서 **sixth** 블록을 가져와 해당 블록 위에 섭니다.

```template
'block_list = ["DIAMOND", "ICE", "EMERALD", "STONE", "WOOD", "GOLD", "QUARTZ"]'
```
