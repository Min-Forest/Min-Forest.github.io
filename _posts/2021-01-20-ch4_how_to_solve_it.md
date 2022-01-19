---
layout: single
title:  "4장_연습문제 풀이 : 점프 투 파이썬!"
---

## Q1. 자연수 홀,짝 판별하는 함수 만들기

```python
def is_odd(number):
  if number%2 ==1:
    return True
  else:
    return False
    
print(is_odd(3)) #자연수 3으로 테스트
```

🤩 **1차 결과** : True

## Q2. 입력으로 들어오는 모든 수의 평균 값 계산 함수 만들기

```python
def avg_numbers(*args):
    result = 0
    for i in args:
        result += i 
    return result / len(args)

print(avg_numbers(1,2)) 
print(avg_numbers(1,2,3,4,5))
```
🤩 **1차 결과** : 1.5 / 3.0

## Q3. 잘못된 부분 찾아 고치기

```python
input1 = int(input("첫번째 숫자를 입력하세요:"))
input2 = int(input("두번째 숫자를 입력하세요:"))
# int 함수를 사용하여 문자열 입력을 숫자(정수)형으로 변경

total = input1 + input2
print("두 수의 합은 %s입니다" %total)
```
🤩 **1차 결과** :   
첫번째 숫자를 입력하세요:121   
두번째 숫자를 입력하세요:212   
두 수의 합은 333입니다   

## Q4. 출력 결과가 다른 것 고르기

```python
print("you" "need" "python")
print("you"+"need"+"python")
print("you","need","python") #다른 놈
print("".join(["you","need"m"python"]))
```
🤩 **1차 결과** :  
youneedpython   
youneedpython   
you need python   
youneedpython   



