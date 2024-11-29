### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 채팅창에 학번과 이름 말하기!

## Step 1
- 채팅창에 말하기 명령을 이용하여 본인의 학번과 이름을 말하는 코드를 작성하세요.
- 출력 예시 : 저는 10300 고규현 입니다!

## Step 2
2번 (1번방)
에이전트가 오른쪽으로 방향으로 360도 회전 후 왼쪽 방향으로 360도 회전 하는 코드를 작성하세요.
![image](https://github.com/user-attachments/assets/cf8d0c87-1d70-45ea-8467-e5c7d0e03151)

```ghost
player.say(":)")
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
```
