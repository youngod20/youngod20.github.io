---
title: "[HackerRank_Day1] Data Types"
excerpt: "hackerRank 30일 코스 따라하기_1일차"

categories:
  - python, 자료구조
tags:
  - python, 자료구조
---

# Data Types    
## 기본 데이터 타입(Primitive Data Type)            
    
<small> 
8가지 기본 데이터 타입         
 1. byte         
 2. short          
 3. int (1,2,3, 등)          
 4. long (1.0, 2.5, 3.9 등)            
 5. float             
 6. double           
 7. boolean              
 8. char              
 이 외 중요한 데이터 타입은 String class로, 객체는 변경 불가능한 문자열임
    
             
## Scanner
<small> 
next, nextLine, hasNext, hasNextLine
ex. 
nextInt(): int타입 스캔
nextDouble(): double타입 스캔
nextLine()
      
------    
a b c    
d e    
f    
g    
------     

scan.next() -> a    
scan.next() -> b
scan.nextLine() -> c
(scanner는 공백과 글자를 return함. 마지막 단어부터 다음 라인의 시작까지 읽음)     
scan.nextLine() -> d, e          
scan.next() -> f          
scan.nextLine() -> 공백               
(f 다음부터 다음라인 시작까지 전체를 가져오는데, String이 비어 있게 됨)       
scan.nextLine() -> g         
   

## 가감연산자(Additive Operators)
<small>
더하기 operator은 숫자를 더하고, 문자는 병합함     
ex. a = 1, b =2, System.out.println(a + b) -> 3


    

## 문제 풀이
​​``` 
a = int(input())    
b = float(input())    
c = str(input())    
    
print(i+a)    
print(d+b)    
print(s+c)    
​```
