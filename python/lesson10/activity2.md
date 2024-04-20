### @explicitHints true
### @hideIteration true 

# 블라인드 라이트.

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
에이전트가 골드 블록으로 가는 통로를 앞으로 걸어가면서 레드스톤 블록 위에 레드스톤 램프를 인벤토리에 배치하도록 합니다.

### ~ tutorialhint
루프를 사용해 보세요.

