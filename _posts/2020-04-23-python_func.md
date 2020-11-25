---
title: "파이썬 함수_v0.1"
excerpt: "파이썬 함수 정리"

categories:
  - python
tags:
  - python
---

map(): iterable한 데이터의 개별 item을 함수의 인자로 전달하여 결과 반환
iterable: member를 하나씩 차례로 반환 가능한 object
'''
def func(x):
	return x *2
	
map(func, [1,2,3,4])
>> [2, 4, 6, 8]

c= {1:10, 2:20, 3:30}
map(func, x)
>> [2, 4, 6]

map(func, x[i] for i in x])
>> [20, 40, 60]

'''