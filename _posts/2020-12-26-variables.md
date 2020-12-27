---
title: Variables
toc: true
tags:
- "#java"
- "#beginner"
- "#notadeveloper"
categories:
- LearnJava
---

# 1. What is Variable
모르는건 무조건 정의부터 확인합니다 😉

> In computer programming, a variable or scalar is a storage location (identified by a memory address) paired with an associated symbolic name, which contains some known or unknown quantity of information referred to as a value. <br>
> by. wikipedia([https://en.wikipedia.org/wiki/Variable_(computer_science)](https://en.wikipedia.org/wiki/Variable_(computer_science)))

`variable`는 데이터의 저장과 참조를 위해 할당된 메모리 공간을 변수라고 합니다. <br>
또한 변수를 컴파일러에게 알려주는 것을 선언 (Declaration) 이라고 합니다. 

변수가 가지는 type은 다음과 같습니다. 

* Primitive Type: for storing simple values
* Reference Type: for storing complex objects (Date, String, etc)

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

<br>
<br>
<br>
<br>

# 2. Practice
전에 생성한 프로젝트를 그대로 사용 했습니다. 

## 2-1. Declaring and initializing variable
```java
public class Main {

    public static void main(String[] args) {
        // set variable and print variable data
        int age = 33;  // int 형 변수 age를 선언하고 33 데이터 저장(메모리에 저장됨)
        System.out.println(age);  // age라는 변수를 참조하여 메모리에 저장한 값을 출력
    }
}
```

![]({{ 'assets/images/variable-practice.png' | relative_url }})

훌륭합니다. <br>
선언한 변수 age의 값을 변경 해봅니다.

```java
public class Main {

    public static void main(String[] args) {
        // set variable and print variable data
        int age = 33;  // int 형 변수 age를 선언하고 33 데이터 저장(메모리에 저장됨)
				age = 34;  // age 변수에 34라는 값 저장(메모리에 저장되며, 기존 33은 34로 덮어써집니다)
        System.out.println(age);  // age라는 변수를 참조하여 메모리에 저장한 값을 출력
    }
}
```

출력은 34가 잘 나오네요! 😀


## 2-2. Reference variable in a variable
`Primitive type` 변수를 2개 할당해서 하나는 숫자로 초기화하고 다른 하나는 앞서 숫자로 초기화한 변수 이름으로 초기화 해보겠습니다. 

**시나리오**

1. int형 변수 선언과 int 값으로 초기화
2. 새로운 int형 변수 선언과 1번에서 초기화한 변수로 2번 변수 초기화
3. 1번 변수 값 변경
4. 2번 변수 값 출력

```java
public class Main {

    public static void main(String[] args) {
        // set variable and print variable data
        int age = 33;  // age 변수를 33 으로 초기화
        System.out.println(age);  // age 출력 - 33
        int myAge = age;  // myAge 변수를 age 변수 이름으로 초기화
        System.out.println(myAge); // myAge 변수에 저장된 값 출력 - 33
        age = 35;  // age 변수 값 변경 35로 덮어쓰기
        System.out.println(age); // age 변수에 저장된 값 출력 - 35
        System.out.println(myAge); // myAge 변수에 저장된 값 출력 - 33
    }
}
```
![]({{ 'assets/images/variable-practice2.png' | relative_url }})

미리 선언되고 초기화된 변수가 있다면, 새로 선언하는 변수의 값으로 초기화 할 수 있습니다.(단, type이 꼭 같아야 겠죠?!)

myAge는 age의 값(33이 저장된 메모리 공간)을 같이 사용하고 참조만 할 줄 알았는데 실제로 별도의 메모리가 생기고(myAge 선언시 메모리가 생성되고) 여기에 age의 33값을 복사하여 가지고 있는것을 확인할 수 있었습니다. 

그래서 age를 변경해도 myAge는 처음 age를 초기화한 값인 33이 그대로 저장되어 있습니다.

* **Primitive type**은 이렇게 메모리에 저장된 값을 **공유(참조) 하지 않고 복사** 합니다.


## 2-3. Reference Types 
Reference type 에서 `Date`(날짜)를 실습해 봤습니다. 
int, float, char등과 같이 약속된(?고정된?) type이 아니라 별도의 class로 사전에 정의된 type을 참조하여 사용하기 때문에 reference type이라 불리는 것 같습니다. 

그래서 `Reference type`의 변수를 사용할 때는 `new`로 객체를 생성해줘야 한다고 합니다. 

예시에서는 Date를 테스트 해봤습니다. 

```java
import java.util.Date;

public class Main {

    public static void main(String[] args) {
        // Reference types practice - Date
        Date now = new Date();  // now라는 이름의 변수에 Data 클래스 객체(object == instance)를 생성
        System.out.println(now);
    }
}

output: Sun Dec 27 02:02:33 KST 2020
```

Date라는 클래스가 있고 이 클래스 type의 변수를 `now로 선언` 하면서 `new Date();`로 class 객체(object or instance)를 생성 하였습니다. 

이렇게 생성된 객체는 Date 클래스에 정의된 모든 메소드와 속성들을 가지고 있으므로 우리는 now라는 `Reference type 변수`로 모두 사용할 수 있습니다.

IntelliJ에서 `now.`을 입력하시면 아래 이미지와 같이 method들을 사용할 수 있습니다. 👍

![]({{ 'assets/images/variable-practice-reference-type.png' | relative_url }})


## 2-4. Reference Types 2
이번 연습은 `Reference type 변수`를 조금 더 이해할 수 있을 것 같습니다. 

**시나리오**

1. Point 라는 클래스 변수 선언과 Point 클래스 객체 생성
2. 또 다른 Point 클래스 변수 선언과 1에서 생성한 Point 클래스 변수로 초기화
3. 1 에서 생성한 Point 클래스 변수로 값 변경
4. 2에서 초기화한 Point 클래스 값 출력

`2-2. Reference variable in a variable` 에서는 `Primitive type`변수는 값을 복사하여 저장하기 때문에 위 시나리오 대로 했을때 서로 다른값이 출력되었습니다. 

`Reference type 변수`는 복사가 아닌 참조이기 때문에 2-2의 결과와 다름을 알 수 있습니다. 

```java
import java.awt.*;

public class Main {

    public static void main(String[] args) {
        // Reference types practice - Point
        // Point 클래스는 2차원(x, y) 좌표 공간의 위치를 나타냅니다.
        Point point1 = new Point(1, 1); // Point형 변수 point1을 선언하고 (x:1, y:1)로 초기화 합니다.
        System.out.println(point1.x); // point1의 x 값을 출력합니다. - 1
        Point point2 = point1; // Point형 변수 point2를 앞서(x:1, y:1)로 초기화한 point1로 초기화 합니다.
        point1.x = 2; // Point형 변수 point1의 x값을 1에서 2로 변경 합니다.
        System.out.println(point1.x); // point1의 x 값을 출력합니다. - 2
        System.out.println(point2.x); // point2의 x 값을 출력합니다. - 2
    }
}
```

![]({{ 'assets/images/variable-practice-reference-type2.png' | relative_url }})

이렇게 new로 선언한 `Reference type 변수`는 값을 `복사`하지 않고 `참조`하기 때문에 먼저 선언한 point1 값을 변경하면 이를 참조하는 point2도 영향을 받는 다는 것을 알 수 있습니다.

그림으로 조금 설명을 해보면,

1. Point형 변수 point1을 선언하고 (x:1, y:1)로 초기화 합니다.
2. Point형 변수 point2를 앞서(x:1, y:1)로 초기화한 point1로 초기화 합니다.

![]({{ 'assets/images/variable-practice-reference-type-point1.png' | relative_url }})

3. Point형 변수 point1의 x값을 1에서 2로 변경 합니다.

![]({{ 'assets/images/variable-practice-reference-type-point2.png' | relative_url }})

이렇게 `Reference type 변수`는 선언된 변수가 위치한 메모리값을 **복사**가 아닌 **참조** 하기 때문에 위와 같은 현상이 발생합니다. 

위 코드에서 point1이 참조하는 x 값을 바꿨는데 point2도 **동일한 곳을 참조**하기 때문에 point2도 바뀐 x를 출력하게 됩니다.

이해가 잘 되지 않더라도 `Primitive type변수`와 `Reference type 변수`는 무엇이고 대략적으로 어떻다 정도만이라도 알아 보았습니다. 

계속 하다보면, 아! 하겠죠?

keep going!
