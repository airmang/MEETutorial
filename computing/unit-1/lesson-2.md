### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 뛰어넘거나 파괴하거나

## 3번
- 에이전트를 황금 블록까지 도착하게 하는 코드를 작성하세요.
- 참나무 울타리를 만날경우 위로 2칸 뛰어넘어서 이동하고 다이아 블록을 만날경우 파괴하고 전진하세요.

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
