### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 새끼 곰을 찾아라!

## 단계 1
``||loops:while||`` 및 ``||agent:agent detect||`` 명령을 사용하여 에이전트가 얼마나 멀리 가는지 모르는 경로를 파도록 프로그램하세요. 에이전트는 모든 눈을 통해 걸어갈 수 있도록 ``||agent:destroy forward & up||``이 필요합니다! 완료되면 **Play** 버튼을 눌러 코드를 컴파일하세요. 마인크래프트에서 코드를 실행하는 것을 잊지 마세요.

#### ~ tutorialhint 
코드 스니펫의 모양을 보고 어떻게 함께 맞추는지 살펴보세요. ``||agent:agent move forward||``를 사용하세요.

```template
player.onChat("cub", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
    	
    }
})
```

```ghost
player.onChat("cub", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.destroy(UP)
    }
})

```
