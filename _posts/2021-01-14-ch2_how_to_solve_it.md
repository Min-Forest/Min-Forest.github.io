---
layout: single
title:  "2장_연습문제 풀이 : 점프 투 파이썬!"
---

## Q1. 평균 점수 구하기

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

```python
pin = "881120-1068234" #문제에서 주어진 부분
where = pin.find('-')
yyyymmdd = pin[:where]
num = pin[where+1:]
print(yyyymmdd)
print(num)
```

🤩 **1차 결과** : 881120     
1068234 

## Q4. 주민등록번호에서 성별을 나타내는 숫자 출력하기

```python
pin = "881120-1068234" 
print(pin[7])
```

🤩 **1차 결과** : 1

## Q5. replace 함수 사용해보기

```python
a = "a:b:c:d"
b = a.replace(':','#')
print(b)
```

🤩 **1차 결과** : a#b#c#d

## Q6. 리스트 정렬 변경하기

```python
a = [1,3,5,4,2]
a.sort()
a.reverse()
print(a)
```

🤩 **1차 결과** : [5, 4, 3, 2, 1]

## Q7. 리스트를 문자열로 변경하기 (join 함수 활용)

```python
a = ['Life', 'is', 'too', 'short']
result = ' '.join(a)
print(result)
```

🤩 **1차 결과** : Life is too short

## Q8. 튜플에 값 추가하여 출력하기

```python
a = (1, 2, 3)
a = a + (4,)
print(a)
```

😨 **1차 결과** : TypeError
> can only concatenate tuple (not "int") to tuple   
> 값 한 개를 괄호로 묶으면 튜플이 아니라 그냥 값이 되므로 주의할 것

🤩 **2차 결과** : (1, 2, 3, 4)
> (4)를 (4,)로 변경하여 성공!



