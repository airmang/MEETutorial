### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 길따라가기

## 2번
- 에이전트를 벽돌 블록을 따라서 황금 블록까지 도착하게 하는 코드를 작성하세요.

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
```
