---
title: Type Casting
tags:
- "#java"
- "#beginner"
- "#notadeveloper"
categories:
- LearnJava
toc: true
toc_sticky: true
---

# Intro
오늘 다룰 내용은 `casting` 입니다.

`casting`은 자료형을 변환하는 것을 말합니다.  
예를들면, `int` -> `double`, `string` -> `int`와 같이 자료형이 달라 연산이 안되는 경우, 또는 어떤 함수의 결과가 double형인데 int로 저장하고 싶을 경우에 사용할 수 있을 것 같습니다. 

# Casting
`casting`을 조금 더 확실히 알기 위해서는 몇가지 알아할 내용이 있습니다.  

## 1. type별 bytes 
byte -> short -> int(float) -> long(double) 순서로 자료형이 처리할 수 있는 데이터 크기가 커집니다.   
이것이 왜 필요하냐면, `casting`시에 데이터가 누락될 수 있기 때문입니다. 

예를들어, double형 데이터는 8bytes를 저장할 수 있는데 이를 int형으로 casting 할 경우 bytes가 8 -> 4로 줄어들기 때문에 데이터 유실이 발생할 수 있다고 합니다. 

| Primitive Type |  Data | Memory Size | Description | 
| -------- | -------- | -------- | -------- | 
|  boolean | 참과 거짓 | 	1 bit | Stores true or false values |
|  byte | 정수 | 	1 byte | Stores whole numbers from -128 to 127 |
|  char | 문자 |	2 bytes | Stores a single character/letter or ASCII values |
|  float | 실수 | 4 bytes | Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits |
|  int | 정수 | 4 bytes | Stores whole numbers from -2,147,483,648 to 2,147,483,647 |
|  long |  정수 | 	8 bytes | 	Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
|  short | 정수 | 	2 bytes | 	Stores whole numbers from -32,768 to 32,767 |
|  double | 실수 | 8 bytes | Stores fractional numbers. Sufficient for storing 15 decimal digits |


## 2. Implicit type casting(Widening)
명시적 형 변환은 `1. type별 bytes`에서 알아본 각 tyep별 bytes와 관계가 있습니다.   

JAVA에서 compiler가 자동으로 자료형을 변환하는 것을 `implicit type casting`이라 하며 이 것이 발생하는 기준은 두 변수의 데이터 사이즈가 같거나 **대상 변수의 데이터 사이즈가 소스 변수의 데이터 사이즈가 클 경우** 자동 유형 변환이 발생할 수 있습니다.


![]({{ 'assets/images/Numbers/implicit type casting.png' | relative_url }})


**example>**

short x 는 int y보다 작기 때문에 자동으로 int 형으로 변환이 일어납니다.  
이는 Java compiler가 자동으로 int형 사이즈(4byte)의 메모리를 할당하고 short x데이터를 int형으로 변환하여 저장한 후에<br>
x + 2; 를 계산하여 y에 저장하게 됩니다. 

![]({{ 'assets/images/Numbers/Casting-short-int.png' | relative_url }})

이렇듯 `implicit type casting`은 작은 자료형을 큰 자료형과 연산하거나 저장할때 발생 합니다. 

<br>

## 3. Explicit type casting(Narrowing)
묵시적 형 변환은 `implicit tyep casting`과 반대로, 변수의 데이터 사이즈가 작을 경우 사용하며 `(type)`을 꼭 지정해줘야 합니다. 

일반적으로 데이터사이즈가 작은 변수에 더 큰 데이터사이즈의 변수 또는 값을 할당할 경우 명시적 캐스팅이 필요합니다.

![]({{ 'assets/images/Numbers/implicit type casting.png' | relative_url }})


example>
double 형 변수를 int형 값과 더해 int형 변수에 저장하려고 하면 에러가 발생합니다.   
하지만 아래와 같이 double형 변수 앞에 `(int)`처럼 변환하고자 하는 type을 지정해주면 컴파일러가 이를 확인하고 변환 해줍니다.

이러한 Explicit type casting에는 데이터가 유실 될 수 있으니 되도록 같은 type을 사용하는 것이 좋다고 합니다. 

![]({{ 'assets/images/Numbers/explicit tyep casting - example.png' | relative_url }})


End. 😉
