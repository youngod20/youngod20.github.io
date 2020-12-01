---
title: "[HackerRank_Day2] Operaters"
excerpt: "hackerRank 30일 코스 따라하기_2일차"

categories:
  - python, 자료구조
tags:
  - python, 자료구조
---

## Operators
<small>
1. 단항연산(Unary): operand를 하나만 갖는 연산자
2. 이항연산(Binary): operand를 두개만 갖는 연산자
3. 삼항연산(Ternary): operand를 세개만 갖는 연산자
       

## 산술 연산자(Arithmetic Operators)
<small>
1. +: 더하기   
2. -: 빼기   
3. *: 곱하기   
4. /: 나누기   
5. %: 나머지

## 더하기 연산(Additional Operators)
<small>
1. '+'  이항연산에서 문자열 병합으로 사용함
2. '++' 단항연산에서 증감연산으로 사용함(후 증가)   
3. '--' 단항연산에서 증감연산으로 사용함(후 감소)
4. '!'  단항연산에서 부정으로 사용됨. true or false   
5. '==' 이항연산에서 2개의 값이 같은지 확인용
6. '!=' 이항연산에서 2개의 값이 다른지 확인용
7. '<, >, <=, =>' 이항연산에서 보다 작다, 보다 크다, 보다 같거나 같다 또는 크거나 같다 등 두 값을 비교할 때 사용함
8. '&&, ||' 이항연산에서 true or false에서 논리형 AND, 논리형 OR로 사용함
9. '?'  간단한 조건문으로 사용됨 (ex if ? then: else)


#### 문제풀이
```
#!/bin/python3

import math
import os
import random
import re
import sys

# Complete the solve function below.
def solve(meal_cost, tip_percent, tax_percent):
    tip = (tip_percent/100) * meal_cost  
    tax = (tax_percent/100) * meal_cost  
    total_cost = meal_cost + tip + tax 
    round_cost = round(total_cost)
    return round_cost
    
if __name__ == '__main__':
    meal_cost = float(input())
    tip_percent = int(input())
    tax_percent = int(input())
    print(solve(meal_cost, tip_percent, tax_percent))

```





