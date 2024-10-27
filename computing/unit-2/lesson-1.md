### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 사각형 만들기

## 5번
- 에이전트를 이용하여 입력한 값의 변의 길이를 갖는 사각형을 만드세요.
- square 길이 명령을 이용하여 사각형을 만드세요.
- 다음 채팅명령어를 입력하면: square 매개변수를 사용하세요.
- 반드시 반복문을 사용해서 문제를 해결하세요. (사용안하면 0점)

```ghost
agent.move(FORWARD, 1)
agent.turn(LEFT_TURN)
player.onChat("run", function () {
	
})
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
