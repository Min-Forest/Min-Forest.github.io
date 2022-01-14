# 2장_연습문제 풀이 : 점프 투 파이썬

## Q1. 평균 점수 구하기
--------
```
scores = [80,75,55]
i=0
while scores:
    ~~sum=scores.pop()~~
    i+=1
avg=sum/i


print(avg)
```

:disappointed: 1차 결과 : 26.666666666666668
> sum=scores.pop() 부분에서 실수가 있었다.   
> += 으로 변경하면 해결될 것 같다.




## Q2. 자연수 13 홀,짝 판단하기
-----

