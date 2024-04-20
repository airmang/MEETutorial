### @explicitHints true
### @hideIteration true 

# 다이아몬드냐 흙이냐?

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
이 네 개의 식에 대한 답을 계산하기 위해 코드를 작성하세요. 에이전트를 골드 블록으로 연결해야 합니다. 식의 답에 따라 상자에서 다이아몬드 또는 흙 블록을 배치하여 이 작업을 수행합니다. 왼쪽에서 오른쪽으로 답이 1이면 다이아몬드 블록, 0이면 흙 블록을 배치합니다.
```python
1. 10000 / 10000 + 64.64 + 64.64 - 72 - 57.28
2. 64 / 4 + 64 / 64 - 128 / 8 - 1
3. 19283746 / 19283746 - 1 + 1000 / 100 - 9
4. 8 - 9 + 7 + 32 * 2 - 64 / 2 - 38
```
```template
//식을 계산합니다: 10000 / 10000 + 64.64 + 64.64 - 72 - 57.28 
//
//식을 계산합니다: 64 / 4 + 64 / 64 - 128 / 8 - 1 
//
//식을 계산합니다: 19283746 / 19283746 - 1 + 1000 / 100 - 9
//
//식을 계산합니다: 8 - 9 + 7 + 32 * 2 - 64 / 2 - 38 
```

