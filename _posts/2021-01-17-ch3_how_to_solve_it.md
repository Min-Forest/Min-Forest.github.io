---
layout: single
title:  "3장_연습문제 풀이 : 점프 투 파이썬!"
---

## Q1. 다음 코드의 결과값은? 

```python
a = "Life is too short, you need python"

if "wife" in a: print("wife")
elif "python" in a and "you" not in a: print("python")
elif "shirt" not in a: print("shirt")
elif "need" in a: print("need")
else: print("none")
```

🤩 **1차 결과** : shirt

## Q2. while문을 사용해 1부터 1000까지의 자연수 중 3의 배수의 합 구하기 

```python
result = 0
i = 1
while i <= 1000:
    if i % 3 == 0:
        result += i
    i += 1
    
print(result)
```
🤩 **1차 결과** : 166833

## Q3. while문을 사용하여 별을 표시하는 프로그램 작성하기 

```python
i = 0 
while True:
    i += 1
    if i == 6 : break
    print('*'*i)
```
🤩 **1차 결과** : 
 *
 **
 ***
 ****
 *****

## Q4. for문을 사용해 1부터 100까지의 숫자 출력하기 

```python
for i in range(1,101):  #숫자 리스트를 만들어주는 range 함수를 함께 써주는 경우가 많다 ^_^ 
    print(i)
```
🤩 **1차 결과** : 1 2 3 4 ... 99 100

## Q5. for문을 사용하여 A 학급의 평균 점수를 구해보자. 

```python
A = [70,60,55,75,95,90,80,80,85,100]
total = 0
for score in A:
    total += score
average = total/len(A) 
#len(A)은 요소의 개수를 구할 때
#A.count()는 '특정' 요소의 개수를 구할 때
print(average)
```
🤩 **1차 결과** : 79.0

## Q6. 리스트 내포를 사용하여 표현해보기

```python
'''원문
numbers = [1,2,3,4,5]
result = []
for n in numbers:
if n % 2 == 1:
result.append(n*2)'''

#리스트 내포 변환후
numbers = [1,2,3,4,5]
result = [n*2 for n in numbers if n%2 == 1] #리스트[] 안에 for문이 들어가 있는 형태
print(result)
```
🤩 **1차 결과** : [2, 6, 10]
