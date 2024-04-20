### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1


# Hazing Two

## 단계 1
단계 1은 hazing two를 하는 것입니다.

## 단계 2
완료되면 **Play** 버튼을 눌러 코드를 컴파일합니다. Minecraft에서 코드를 실행하는 것을 잊지 마세요.

```blocks
player.onChat("run", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.destroy(UP)
    }
})

```
