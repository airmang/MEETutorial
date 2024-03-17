### @explicitHints true

# 활동 2 - 식단 요구 사항.

```python
blocks.place()
```

## 1단계
미리 정의된 리스트에 있는 모든 항목을 **첫 번째** 개에게 주세요. 첫 **4개**의 `||blocks:place block at position||` 명령의 값을 변경하여 각각 리스트에 있는 항목 중 하나씩 순서대로 배치합니다. 그런 다음 상자에서 음식을 가져와 첫 번째 개에게 주세요.

### ~ tutorialhint 
핫바에서 아이템을 드롭하려면 키보드에서 [**Q**] 키를 누르세요.

## 2단계
추가 비타민이 추가된 리스트에 이미 있는 모든 항목을 **두 번째** 개에게 주세요.
이를 수행하기 위해 **append** 메소드를 사용하여 변수 **Vitamins**을 리스트 끝에 추가합니다.
그런 다음 마지막 `||blocks: place block at position||` 명령의 값을 변경하여 기계에 비타민을 배치하고,
두 번째 개에게 음식을 주세요.

## 3단계
**소고기** 없이 리스트에 이미 있는 모든 항목을 **세 번째** 개에게 주세요.
이를 수행하기 위해 **pop** 메소드를 사용하여 변수 **Beef**을 리스트에서 제거합니다.
그런 다음 세 번째 개에게 음식을 주세요.

### ~ tutorialhint 
**pop** 메소드를 사용할 때는 이름이 아닌 리스트 위치 값을 사용해야 합니다.

```template
Bone = world(-21, 45, -31)
Beef = world(-21, 45, -29)
Chicken = world(-21, 45, -27)
Biscuit = world(-21, 45, -25)
Vitamins = world(-21, 45, -23)
// 아래 줄을 귀하의 코드로 대체하세요 #   
Dog_Food=[Bone, Beef, Chicken, Biscuit]
//append 메소드를 사용하여 리스트에 변수 Vitamins 추가 | 2단계
//pop 메소드를 사용하여 변수 Beef 제거                          | 3단계

blocks.place(REDSTONE_BLOCK, Dog_Food[0]) 
//아래의 리스트 숫자 값을 변경하세요         | 1단계
blocks.place(REDSTONE_BLOCK, Dog_Food[0])
//아래의 리스트 숫자 값을 변경하세요         | 1단계
blocks.place(REDSTONE_BLOCK, Dog_Food[0]) 
//아래의 리스트 숫자 값을 변경하세요         | 1단계
blocks.place(REDSTONE_BLOCK, Dog_Food[0])   
//아래의 리스트 숫자 값을 변경하세요                  | 2단계
blocks.place(REDSTONE_BLOCK, Dog_Food[0]) 
```