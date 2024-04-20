### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 소

## 단계 1
시작 코드를 살펴보고 실행해 보세요. 이 코드를 사용하면 블록을 세지 않고 에이전트를 이동시킬 수 있습니다. 에이전트가 이동해야 하는 경로를 살펴보고, 에이전트가 올바른 방향으로 회전하도록 코딩 시퀀스를 완성하세요. 에이전트가 **금 판**에 도달할 수 있는지 확인하세요.

```template
player.onChat("sheep", function () {
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.move(FORWARD, 1)
    }
    agent.turn(LEFT_TURN)
})

```