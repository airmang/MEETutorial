### @explicitHints true
### @hideIteration true 
# 눈부신 빛들.

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

## 단계 1
에이전트가 길을 따라 전진하면서 레드스톤 블록 위에 레드스톤 램프를 설치하게 만드세요.

### ~ tutorialhint
에이전트는 이미 필요한 모든 블록을 인벤토리에 가지고 있습니다.