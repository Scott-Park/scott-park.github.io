---
title: Arithmetic Expressions
toc: true
tags:
- "#java"
- "#beginner"
- "#notadeveloper"
categories:
- LearnJava
---

# Arithmetic Operators
산술 식을 사용하면 Java 내에서 수학적 연산을 수행할 수 있습니다.

이러한 표현은 기초 수학과 훨씬 더 복잡한 알고리즘에 사용될 수 있습니다. 

덧셈, 뺄셈, 곱셉, 나눗셈, 나머지연산은 Java에서 다음 표와 같이 사용합니다.



| Operator | Description | Example |
| -------- | -------- | -------- | 
| + | Addition operator |  1 + 1 = 2 |
| - | Subtraction operator |  2 - 1 = 1 |
| * | Multiplication  operator |  2 * 2 = 4 |
| / | Division  operator |  6 / 3 = 2 |
| % | Modulus  operator |  10 % 3 = 1 |


<br />

## Addition operator test code
두개의 int type 변수를 선언 및 초기화 하고 덧셈 하는 코드 입니다. 

```java
public class Main {

    public static void main(String[] args) {
        // Practice - Arithmetic Operators
        int firstVal = 5;
        int secondVal = 2;

        int firstPlusSecond = firstVal + secondVal;
        // The output will be '7'
        System.out.println(firstPlusSecond);
    }
}
```

```
output: 7
```

<br />

## Subtraction operator test code
두개의 int type 변수를 선언 및 초기화 하고 뺄셈 하는 코드 입니다. 

```java
public class Main {

    public static void main(String[] args) {
        // Practice - Arithmetic Operators
        int firstVal = 4;
        int secondVal = 2;

        int firstMinusSecond = firstVal - secondVal;

        // The output will be '2'
        System.out.println(firstMinusSecond);
    }
}
```

```
output: 2
```
<br />

## Multiplication operator test code
두개의 int type 변수를 선언 및 초기화 하고 곱셈 하는 코드 입니다. 

```java
public class Main {

    public static void main(String[] args) {
        // Practice - Arithmetic Operators
        int firstVal = 4;
        int secondVal = 2;

        int firstMultSecond = firstVal * secondVal;

        // The output will be '8'
        System.out.println(firstMultSecond);
    }
}
```

```
output: 8
```

<br />

## Division operator test code
두개의 int type 변수를 선언 및 초기화 하고 나눗셈 하는 코드 입니다. 

```java
public class Main {

    public static void main(String[] args) {
        // Practice - Arithmetic Operators
        int firstVal = 6;
        int secondVal = 3;

        int firstDivSecond = firstVal / secondVal;

        // The output will be '2'
        System.out.println(firstDivSecond);
    }
}
```

```
output: 2
```
<br />

## Modulus operator test code
두개의 int type 변수를 선언 및 초기화 하고 나머지 연산 하는 코드 입니다. 

나머지 연산은 나눗셈 연산 후 나머지 값을 돌려줍니다.

```java
public class Main {

    public static void main(String[] args) {
        // Practice - Arithmetic Operators
        int firstVal = 17;
        int secondVal = 5;

        int firstModSecond = firstVal % secondVal;

        // The output will be '2'
        System.out.println(firstModSecond);
    }
}
```

```
output: 2
```

<br />
<br />
# Operation Precedence
`+`, `-`, `*`, `/`, `%` 연산은 연산자별 우선순위가 있습니다. 

같은 우선순위 연산자가 여러개 있는 경우 왼쪽에서 오른쪽으로 연산을 수행합니다.


| Operator | Precedence | 
| -------- | -------- |
| `( )` Parenthesis | 	1st     |
|`*`, `/ ` Multiplication and Division | 	2st     |
| `+`,`-` Addition and Subtraction | 	3st     |


<br />
<br />
# Arithmetic Shortcuts
산술 연산을 수행할때 아래 표와 같이 짧은 코드로 `덧셈`, `뺄셈`, `곱셈`, `나눗셈`을 수행할 수 있습니다. 


| Original | Shortcut | Description |
| -------- | -------- | -------- |
| counter = counter + 1;     | **counter++;**     | Increment a variable by 1     |
| counter = counter - 1;    | **counter--;**   | Subtract 1 from a variable |
| x = x + y;    | **x += y;**     | Adding values to a variable     |
| x = x - y;     | **x -= y;**     | Subtracting values from a variable     |
| x = x * y;    | **x \*= y;**    | Multiplying values to a variable     |
| x = x / y;    | **x /= y**    | Dividing values from a variable     |


keep going!  


😉
