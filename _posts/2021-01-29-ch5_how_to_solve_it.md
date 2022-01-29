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

## Q7. 다음 리스트의 최댓값과 최솟값의 합 구하기

```python
input = [-8,2,7,5,-3,5,0,1]
print(min(input)+max(input)) #min -8 max 7

```

🤩 **1차 결과** : -1   

## Q8. 소숫점 4자리까지 반올림하여 표시하기

```python
print(round(17/3,4))

```

🤩 **1차 결과** : 5.6667   

## Q9. 소숫점 4자리까지 반올림하여 표시하기

```python
import sys
print(sum(map(int, sys.argv[1:])))

#리스트 요소의 자료형이 문자이기 때문에 sum 함수를 쓰기 위해 정수형으로 변환 해줘야 오류가 안난다.

```

🤩 **1차 결과** : 55   

## Q10. os 모듈을 사용하여 다음과 같이 동작하도록 코드를 작성해보기

```python
#1. C:\doit 디렉터리로 이동한다.
#2. dir 명령을 실행하고 그 결과를 변수에 담는다.
#3. dir 명령의 결과를 출력한다.

import os
os.chdir("C://doit") #지정한 디렉터리로 이동
f = os.popen("dir") #명령을 실행 후 변수에 담기
print(f.read()) #명령 결과 읽어서 출력하기
```

🤩 **1차 결과** :  
C 드라이브의 볼륨에는 이름이 없습니다.   
볼륨 일련 번호: E8E1-1983   
   
 C:\doit 디렉터리   
   
2022-01-29  오후 06:19    <DIR>          .   
2022-01-29  오후 06:19    <DIR>          ..   
2022-01-29  오후 06:27                71 test.py   
               1개 파일                  71 바이트   
               2개 디렉터리  415,679,242,240 바이트 남음    


## Q11. glob 모듈을 사용하여 확장자가 .py인 파일만 출력하는 프로그램 만들기

```python
import glob
print(glob.glob("C://doit/*.py"))
```

🤩 **1차 결과** : ['C://doit\\python.py', 'C://doit\\test.py']   

## Q12. time 모듈을 사용하여 현재 날짜와 시간을 다음의 형식으로 표시
  ex. 2018/04/03 17:20:32

```python
import time
print(time.strftime('%Y/%m/%d %X', time.localtime(time.time())))
```

🤩 **1차 결과** : 2022\01\29 21:40:40   
  
## Q13. random 모듈을 사용하여 로또 번호(1~45 사이 숫자 6개)를 생성해보기(단, 중복숫자 없어야함)
  
```python
import random
rotto = []
for i in range(6):
    new = random.randint(1,45) #Return random integer in range [a, b], including both end points.
    while 1:
        if rotto.count(new) == 0:
            rotto.append(new)
            break
        else:
            new = random.randint(1,45)  
print(rotto)
```

🤩 **1차 결과** : [22, 27, 23, 43, 40, 5]   
