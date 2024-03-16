### @explicitHints true
### @hideIteration true 
# 활동 3 - 한 걸음씩.

```python
blocks.place(GRASS_BLOCK, pos(0, 0, 0))
blocks.block_with_data(GRASS_BLOCK, 0)
```

## 1단계
**벽돌 블록**으로 전체 계단을 구축하는 코드를 작성하세요. 세 개의 `||blocks: place block at position||` 명령 모두에서 **두 번째** 매개변수의 **두 번째** 및 **세 번째** 좌표를 변경해야 합니다. 또한, `||blocks: block with data||` 명령에서 데이터 값도 업데이트해야 합니다. 기억하세요, 각 데이터 값은 계단의 방향을 의미합니다.

### ~ tutorialhint 
동쪽, 서쪽, 북쪽, 남쪽 방향을 보려면 벽을 살펴보세요.
데이터 값에 대해: 
0 = W  
1 = E   
2 = N  
3 = S