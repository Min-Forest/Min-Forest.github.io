---
layout: single
title:  "5장_연습문제 풀이 : 점프 투 파이썬!"
---

## Q1. 주어진 클래스를 상속하는 UpgradeCalculator를 만들고 값을 빼는 minus 메서드 추가

```python
# 메서드 이름을 __init__으로 하여(생성자) 객체가 생성되는 시점에 자동으로 호출 (초기값 설정)
class Calculator:
    def __init__(self): 
        self.value = 0
         
    def add(self, val):
        self.value += val

# Calculator class 상속
class UpgradeCalculator(Calculator):
    def minus(self, val):
        self.value -= val
        
# 동작 확인
cal = UpgradeCalculator()
cal.add(10)
cal.minus(7)
print(cal.value) # 3 출력
```

🤩 **1차 결과** : 3   

## Q2. 객체변수 value가 100 이상의 값은 가질 수 없도록 제한하는 MaxLimitCalculator 클래스 만들기

```python
class Calculator:
    def __init__(self): 
        self.value = 0
         
    def add(self, val):
        self.value += val

# 상속 및 메서드 오버라이딩 
class MaxLimitCalculator(Calculator):
    def add(self, val):
        self.value += val
        if self.value >= 100:
            self.value = 100
        

#동작 테스트
cal = MaxLimitCalculator()
cal.add(50)
cal.add(60)
print(cal.value) 
```

🤩 **1차 결과** : 100   

## Q3. 결과 예측 하기

```python
all([1,2,abs(-3)-3]) # all(1, 2, 0)이 되어 False 출력
                     # all 은 반복 가능한 자료형을 입력 인수로 받고, 모두 참이면 True

chr(ord('a')) == 'a' # chr(97) == 'a'가 되어 True 출력 
```

🤩 **1차 결과** : (상단 주석 참고)

## Q4. filter와 lambda 사용하여 음수 제거하기

```python
print(list(filter(lambda x : x >= 0, [1,-2,3,-5,8,-3])))

#list로 감싸주어야 리스트 형태의 값으로 출력할 수 있음

```

🤩 **1차 결과** : [1, 3, 8]   

## Q5. 10진수, 16진수 변환

```python
print(int('0xea',16))
#'0xea' , 'ea' 어느 형태로 입력해도 출력은 234로 동일하다.

```

🤩 **1차 결과** : 234   

## Q6. map과 lambda 사용해보기

```python
# map(f, iterable)은 함수와 반복 가능한 자료형을 입력으로 받아,
# 각 요소를 함수 f 수행한 결과를 묶어서 돌려주는 함수.

input = [1,2,3,4]
print(list(map(lambda x: x*3, input)))

```

🤩 **1차 결과** : [3, 6, 9, 12]   



