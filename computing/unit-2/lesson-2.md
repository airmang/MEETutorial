### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 암호해독하기

## 6번
- 에이전트를 이용하여 암호를 해독하고 해독한 암호의 값을 채팅창에 말하세요.
- 블록은 검사하였을 때 고유의 숫자 값을 갖고 있습니다. 에이전트의 블록 검사를 이용하여 값을 알아내고 연산을 진행하세요.
- 왼쪽부터 오른쪽 방향으로 차례대로 읽어야 합니다.
- 황금 블록 : 곱하기
- 다이아 블록 : 빼기
- 에메랄드 블록 : 더하기

- 예) 빨간 콘크리트 , 황금 , 초록 콘크리트, 다이아, 노랑 콘크리트 =
- 예) 빨간 콘크리트 + 초록 콘크리트 - 노랑 콘크리트 =

- 반드시 선택구조를 이용하여 문제를 해결하세요 (사용하지 않으면 0점)

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
player.say(0 - 0 * 0 + 0 / 0)
let cnt = 0
```
