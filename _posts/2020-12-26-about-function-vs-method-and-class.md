---
title: About Function vs Method and Class
toc: true
tags:
- "#java"
- "#beginner"
- "#notadeveloper"
categories:
- LearnJava
---

# 1. Intro
Java를 책으로 공부해보려다 책이 너무 많아 Youtube로 선택 했습니다.<br>
제가 선택한 영상은 [https://www.youtube.com/watch?v=eIrMbAQSU34](https://www.youtube.com/watch?v=eIrMbAQSU34) 입니다. 

gogo!
# 2. Function이란 무엇인가?
> 함수는 단일 관련 작업을 수행하는 데 사용되는 정리되고 재사용 가능한 코드 블록입니다.

예를 들면 sendEmail(), moveLeft(), moveRight()와 같이 `단일 작업`을 수행하기 위해 정의된 코드 블럭인 것입니다. 

Java에서는 함수는 다음과 같이 구성합니다. 
```java
type name_of_function(type paremeters) {
    codes..
    return vale_of_type
}		
```

type은 이 함수가 반환(`return`)할 type을 명시합니다. <br>
다음 표는 사용할 수 있는 type이며, 함수 선언 시에는 Primitive Type를 써줍니다.<br>
자료형이라고도 하는데 찾아보니.. 별도 페이지로 다뤄야할 것 같습니다. 😉


| Primitive Type | Reference Type  |
| -------- | -------- | 
|  boolean | Boolean |
|  byte | Byte  |
|  char | Character  |
|  float | Float |
|  int | Integer   |
|  long | Long  |
|  short | Short  |
|  double | Double  |


Function은 반환할 type을 가지며 paremeter를 전달받아 처리할 수 있으며, type 형태의 값을 함수의 결과로 반환 합니다. <br>
반환한 값은 Fucntion을 호출한 곳으로 전달 됩니다. 

example>
```java
int pluseOne(int inputNumber) {  // int type값을 반환하는 함수이고 인자로 int type값을 받습니다.
    int pluseNumber = inputNumber + 1; // 전달된 값에 1을 더합니다.
		return pluseNumber;  // 1을 더한 값을 반환 합니다.
}

int firstNumber = 1;  // 처음 값을 1로 셋팅 합니다. 
int result = pluseOne(firstNumber); // 함수를 호출하여 결과를 받아보면, reult는 2가 되겠죠?!
```

이제 함수가 뭔지 대충 이해가 됩니다. 
반환할 자료형 type이 필요하고, parameter로 값을 받아서 함수안에서 처리해준 다음 return!
## 2-1. void function
위 표에서 Primitive Type안에 void라는 type은 없습니다. <br>
void형으로 선언한 함수는 반환(`return`) 값이 존재하지 않음을 뜻합니다. 

ex><br>
```java
void printGivenString(String name) {
    System.out.println(name);
}
```

위 예시처럼 void type 함수는 반환값이 없다는 특징을 가집니다. <br>
언제 void type 함수를 사용해야 할까요?<br>
제 개인적인 생각은 어떤 작업이 결과에 영향을 미치지 않을때? 예를 들면 그냥 값을 출력할때? 정도라고 생각합니다. 일단 킵 고잉 해보죠.

# 2. Method란 무엇인가?
> 메소드는 호출될 때만 실행되는 코드 블록입니다.

음.. method도 function과 거의 똑같은 정의 입니다. <br>
그렇다면, function과 method는 어떤 차이가 있길래 이름이 다른걸까요? 

답은, Method는 Class안에 정의된 함수를 `method`라고 합니다. 
즉, 독립 함수로 정의되지 않고 class라는 것 안에 존재 해야 합니다. 

function이라 불릴때는 class로 감싸져 있지 않는 함수들을 `function`이라 부르고,<br>
class로 감싸져서 class안에 함수로 동작하는 애들은 `method`라 부르기로 이해하면 될것 같습니다. 


# 3. Class란 무엇인가? 
좀 난이도가 있네요 class.. 🤔

우선 youtube 영상에선 class를 다음과 같이 정의 했습니다. 

> A container for related functions

그리고 비유를 장바구니로 표현합니다. <br>
장바구니 안에 담긴 물건들을 `attribute`,  `method`라고 비유 했는데요. 

그래서 method와 function의 차이는 class안에 정의되었는지 여부라 이해 했습니다. <br>
같은 기능의 함수라도 class 안에 정의되면 `method`, 그렇지 않으면 `function`. 

class가 좀 불명확해서 찾아보았더니, w3schools에선 다음과 같이 설명 합니다. 

> Everything in Java is associated with classes and objects, along with its attributes and methods. For example: in real life, a car is an object. The car has attributes, such as weight and color, and methods, such as drive and brake.
> 
A Class is like an object constructor, or a "blueprint" for creating objects.

from. [https://www.w3schools.com/java/java_classes.asp](https://www.w3schools.com/java/java_classes.asp)


정리해보면, <br>
`class`는 것은 객체(`object`)를  나타내는 이름이고, `object`(객체)는 class에 정의된 속성값과 메소드들로 구성되어 만들어진 개체 입니다.. 

이해가 좀 안되서 이렇게 이해하려 합니다. <br>
- `class`는 object를 나타내는 이름
- `object`는 class에 정의된 속성과 함수로 만들어진 개체.

이해한 내용을 `사람`을 예로 들어 보겠습니다.<br>

`class`: 사람<br>
`object`:  사람이라는 class 안에 정의된 `머리`, `목`, `팔`, `몸`, `다리`, `머리카락`, `머리카락 색`, `눈`, `눈 색`, `피부`, `피부 색`, `이름`, `나이`, `성별`, `먹는다`, `잔다`, `걷는다` 등 으로 만들어진(또는 구성된) 개체, 여기서 method는 `먹는다`, `걷는다`, `잔다`와 같은 action이 정의된 함수들이고 나머지는 속성 값들. 

사람이라는 클래스는 머리, 몸, 다리, 걷고, 자고, 먹고 등등을 하는 속성과 메소드를 가지고 있고 이를 통해 만들어진 개체를 객체(object)라고 말한다. 

저는 이렇게 이해 했습니다. <br>
이것만 했는데도 머리가 아프네요.. 

keep going!
