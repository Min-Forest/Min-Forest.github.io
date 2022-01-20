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

## Q5. 파일에 문자열 저장 후 다시 읽어서 출력하기

```python
f1 = open("test.txt", 'w')
f1.write("Life is too short")
f1.close()

f2 = open("test.txt",'r')
print(f2.read())
f2.close()
```

🤩 **1차 결과** : Life is too short

## Q6. 파일에 문자열 저장 후 다시 읽어서 출력하기

```python
user_input = input("저장할 내용을 입력하세요:")
f = open('test.txt','a')
f.write(user_input)
f.write('\n')
f.close()
```

🤩 **1차 결과** :   
Life is too short1   
2

## Q7. 파일의 특정 문자 바꿔 저장하기

```python
f = open('test.txt', 'r')
body = f.read()
f.close()

body = body.replace('java','python')

f = open('test.txt','w')
f.write(body)
f.close()
```

🤩 **1차 결과** :   
Life is too short   
you need python   
