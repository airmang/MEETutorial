### @explicitHints true
### @hideIteration true 
# 활동 1 - 건물을 수리해라

```python
player.say()
agent.move()
agent.turn()
agent.place()
agent.set_item()
agent.set_item(agent.inspect(AgentInspection.BLOCK, FORWARD), 1, 1)
if True:
    pass
if True:
    pass
else:
    pass
while False:
    pass
for index in range(4):
    pass
```

## 수행평가
agent에게 명령을 내려 건물을 수리하세요.

### ~ tutorialhint 
`||agent.에이전트가 블록을 검사: 블록kind 방향 direction||`명령어는 조사한 블록의 값을 반환합니다.
