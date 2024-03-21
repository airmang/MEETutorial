### @explicitHints true

# 다이아몬드인가, 흙인가?

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
이 코드를 사용하여 다음 네 가지 합계를 계산하십시오. 에이전트를 금 블록으로 이동시켜야 하며, 합계의 답에 따라 다이아몬드 또는 흙 블록을 놓아야 합니다. 답이 1이면 다이아몬드 블록을 놓고, 0이면 흙 블록을 놓으십시오.