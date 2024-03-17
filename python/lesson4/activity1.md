### @explicitHints true
### @hideIteration true 
# 활동 1 - 동물 분류하기.

```python
blocks.place()
mobs.spawn()
world(0, 0, 0)
```

## 1단계
Minecraft 세계에서 **왼쪽**에서 **오른쪽**으로 가는 동물의 목록을 포함한 **My_list**라는 리스트를 사용한 코드를 작성하세요.
이미 주어진 `||mobs:spawn mob at position||` 명령어 다음에 **4개** 더 추가하세요. 우리에 있는 표지판의 정보를 사용하여 이 명령어들을 완성하세요.

### ~ tutorialhint 
리스트 위치는 0부터 시작한다는 것을 기억하세요.

```template 
location1 = world(-2, 40, -11)
location2 = world(-2, 40, -5)
location3 = world(-8, 40, -0)
location4 = world(-13, 40, -5)
location5 = world(-13, 40, -11)
//아래 줄을 귀하의 코드로 대체하세요 #   

//동물의 목록 

mobs.spawn(My_list[0], location1)
//리스트의 세 번째 동물을 location2에 스폰
//리스트의 다섯 번째 동물을 location3에 스폰
//리스트의 두 번째 동물을 location4에 스폰
//리스트의 네 번째 동물을 location5에 스폰
```