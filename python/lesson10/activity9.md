### @explicitHints true
### @hideIteration true 
# The Agent labyrinth.

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
미로를 통해 에이전트를 이동시키세요. 에이전트가 이동할 수 있는 전진, 왼쪽, 오른쪽 제어 방향으로 색상 블록을 사용하는 코드를 작성하세요. 그런 다음 색상 블록 위에 서서 에이전트를 미로의 끝까지 제어하세요.

### ~ tutorialhint
루프 중에 무한 반복을 사용해 보세요.
