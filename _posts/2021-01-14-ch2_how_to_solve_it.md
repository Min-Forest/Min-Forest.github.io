# 2장_연습문제 풀이 : 점프 투 파이썬

## Q1. 평균 점수 구하기
--------
```
scores = [80,75,55]
i=0
while scores:
    sum=scores.pop()
    i+=1
avg=sum/i
print(avg)
```

:skull: 1차 결과 : 26.666666666666668
> sum=scores.pop() 부분에서 += 처리한다는 걸 =를 넣는 실수

:satisfied: 2차 결과 : 70.0
> sum+=scores.pop() 으로 변경하여 성공! 


## Q2. 자연수 13 홀,짝 판단하기
-----

