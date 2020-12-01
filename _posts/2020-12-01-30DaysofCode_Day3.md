---
title: "[HackerRank_Day3] Intro to Conditional Statements"
excerpt: "hackerRank 30일 코스 따라하기_3일차"

categories:
  - python, 자료구조
tags:
  - python, 자료구조
---

## Boolean   
<small>   
논리문으로 같다, 다르다임   
몇몇 언어에서는 true를 숫자 1로 대체하고, false는 숫자 0으로 대체할 수 있음   
   
## 조건문    
몇 불린 조건에 의존하여 다른 워크플로우를 보여주는 방법임    
if-else문은 프로그래밍 조건문에서 대부분 넓게 사용되고 있음    

<img src = "https://s3.amazonaws.com/hr-challenge-images/13689/1446563087-4ec019a919-332px-If-Then-Else-diagram.svg.png">     

if문을 사용하는 경우 else 없이 사용이 가능함    
또는 if(condition): elif(condition)으로 사용이 가능함

## 논리 연산
<small>
* || 는 OR, 논리합
* && 은 AND, 논리곱
* ! 는 NOT, 부정
* ? :    
v = c ? a : b;   
condition이 true면 a, condition이 false면 b를 value에 할당   
c ? a: b if c가 true면 a 아니면 b   
    
## Swich Statement
<small>
val0, val1, val2가 있을 때 switch해서 사용할 수 있음
if...elif....elif 문이 switch 또는 case문을 대체함

###### https://docs.python.org/3.5/tutorial/controlflow.html

```
#!/bin/python3

import math
import os
import random
import re
import sys



if __name__ == '__main__':
    N = int(input())
    if N%2 != 0:
        print("Weird")
    else: 
        if (2<=N & N<=5):
            print("Not Weird")
        elif (6<=N & N<=20):
            print("Weird")
        elif (20 <= N):
            print("Not Weird")
```
