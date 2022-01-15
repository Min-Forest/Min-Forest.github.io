---
layout: single
title:  "2장_연습문제 풀이 : 점프 투 파이썬!"
---

## Q1. 평균 점수 구하기
--------
```python
scores = [80,75,55]
i=0
while scores:
    sum=scores.pop()
    i+=1
avg=sum/i
print(avg)
```

😨 **1차 결과** : 26.666666666666668
> sum=scores.pop() 부분에서 += 처리한다는 걸 =를 넣는 실수

🤩 **2차 결과** : 70.0
> sum+=scores.pop() 으로 변경하여 성공! 


## Q2. 자연수 13 홀,짝 판단하기
-----
```python
number = 13
share = number/2
rest = number%2
if (share == 0) & (rest == 0):
    print("홀수, 짝수 모두 아닙니다")
elif rest == 0:
    print("짝수")
else:
    print("홀수")
```

🤩 **1차 결과** : 홀수

## Q3. 홍길동 씨 주민등록번호 나누어 출력하기
-----
```python
pin = "881120-1068234" #문제에서 주어진 부분
where = pin.find('-')
yyyymmdd = pin[:where]
num = pin[where+1:]
print(yyyymmdd)
print(num)
```

🤩 **1차 결과** :  881120
                   1068234 

