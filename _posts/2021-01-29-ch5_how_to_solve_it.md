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




