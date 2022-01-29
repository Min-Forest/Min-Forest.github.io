---
layout: single
title:  "5장_연습문제 풀이 : 점프 투 파이썬!"
---

## Q1. Calculator 클래스를 상속하는 UpgradeCalculator를 만들고 값을 뺄 수 있는 minus 메서드를 추가

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


