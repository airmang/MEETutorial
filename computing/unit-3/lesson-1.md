### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 다이아 캐기

## 8번
- 에이전트를 이용하여 다이아를 캐세요.
- 반드시 다이아만 파괴해야 합니다. (다이아 이외의 블록이 파괴될 경우 0점)
- 다이아를 캐고 난 후에 수집하세요.
- 다이아를 다 캐고 난 후에 몇개의 다이아를 수집했는지 채팅창에 말하세요.(변수를 사용하여 말하지 않으면 0점)

```ghost
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
player.onChat("run", function () {
	
})
player.say(agent.getItemCount(1))
let cnt = 0

```
