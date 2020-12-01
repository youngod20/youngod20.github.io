---
title: "[HackerRank_Day0] Hello, World"
excerpt: "hackerRank 30일 코스 따라하기_0일차"

categories:
  - python, 자료구조
tags:
  - python, 자료구조
---

## Class
#### Class는 methods라 불리는 function과 variables를 모아둠     
#### Class를 작성할 때는 변수의 시작글자를 대문자로 작성함       
#### 또한 변수 작성 시, 띄워쓰기를 해서 작성해야 하는 경우 낙타의 혹과 같은 형태로 작성한다고 하여 CamelCase라고 부름            
>  ex. MyClass           
#### 변수는 숫자나 띄워쓰기 형태로 시작하지 않음             
                             
## Variable             
#### 변수명은 메모리에 저장됨              
#### 변수를 지정할 때 시작글자를 소문자로 지정하며 CamelCase로 작성 가능함            
#### 언더바를 제외한 다른 특수문자를 사용할 수 없으며, 띄워쓰기도 허용되지 않음              
#### 또한 시작하는 문자가 아닌 경우 숫자를 포함할 수 있음               
#### 변수는 filed라고 불리는 변수 중 하나임                 
                          
#### 각 변수는 데이터타입이 있으며, 데이터 타입을 선언하지 않는 경우 동작하지 않을 수 있음              
#### 데이터타입 String은 문자타입을 말하며, myString이라는 변수에 'Hi'라는 문자를 선언하기 위해서는 아래와 같이 작성해야 함               
                             
'''          
String myString = "Hi!";              
'''               
                    
#### 두 따옴표 사이의 글자는 String을 표시하는 방법임                 
                    
#### CamelCase 대신 camel_case 라고 작성하는 방법을 lower snake case라고 부르며 자바에서는 사용되지 않고, C++, C, Python 등에서 사용됨                    
#### 특별한 변수(private calss variables or constants)인 경우 자바에서 사용되기도 함                    
                    
## Function                    
#### task 수행을 설명하기 위한 패키지의 일부                    
                    
## Method                    
#### 객체지향 프로그래밍에서 method는 Class의 필드에서 작동하는 함수 유형임                    
                    
'''                    
int myMethod(){                    
        // ...does cool stuff.                    
}                    
void myMethod(int myInt){                    
        // ...does cool sutff.                    
}                    
'''                    
                    
## Object
#### class의 instance 또는 variable                    
                    
## Stream
#### input-output을 핸들링하며, 언어마다 자체 메커니즘을 가지고 있음                    
#### Scanner 사용시 stdin으로 부터 읽는 방법은 다음과 같음                    
                    
'''                    
Scanner scan = new Scanner(System.in);                    
'''                    
                    
#### System.in으로부터 읽어들일 때 new Scanner object를 생성했고, scan이라는 이름으로 접근이 가능함                    
#### stdin으로 부터 정보를 읽기위해 너의 scanner objectdp Scanner의 methods를 적용하는 것이 필요함                    
                    
                    
'''                    
scan.next(); // returns the next token of input                    
scan.hasNext(); // returns true if there is another token of input (false otherwise)                    
scan.nextLine() // returns the next LINE of input                    
scan.hasNextLine(); // returns true if there is another line of input                    
'''                    
                    
#### input stream으로부터 읽어들이는 것이 끝났을 때 resource leak를 막기위해 닫아야 함
                    
'''                    
scan.close();                    
'''                    
                    
## 전체 흐름 코드
                    
'''                    
Scanner scan = new Scanner(System.in); // open scanner                    
String s = scan.next(); // read the next token and save it to 's'                    
scan.close(); // close scanner                    
System.out.println(s); // print 's' to System.out, followed by a new line                    
'''                    
                                    
#### 또한 System.out.printin을 이용해서 프린트 또는 quoted text를 컴바인하는 것이 가능함(e.g.: System.out.println("Input received: " + s);).                    