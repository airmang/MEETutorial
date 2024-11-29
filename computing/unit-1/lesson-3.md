### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 벽 수리하기

## 6번
- 에이전트를 이용하여 미완성된 집의 벽을 건설하도록 하세요.
- 가로길이는 6 세로길이는 5 입니다.
- 반드시 반복문을 사용해서 문제를 해결하세요. (사용안하면 0점)

```ghost
agent.move(FORWARD, 1)
agent.turn(LEFT_TURN)
if (true) {
	
} else {
	
}
if (agent.detect(AgentDetection.Block, FORWARD)) {
	
}
while (agent.inspect(AgentInspection.Block, FORWARD) == GRASS) {
	
}
for (let index = 0; index < 4; index++) {
	
}
agent.place(FORWARD)
agent.destroy(FORWARD)
agent.collectAll()
agent.setItem(GRASS, 1, 1)
let cnt = 0
```
