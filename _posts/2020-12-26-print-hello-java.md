---
title: Print Hello Java
toc: true
tags:
- "#java"
- "#beginner"
- "#notadeveloper"
categories:
- LearnJava
---

# 1. Main Class
드디어 첫 java 코드를 작성해 봅니다. <br>
지난번에 만들었던 project를 열었습니다.

![]({{ 'assets/images/javaj-class-main.png' | relative_url }})

여기서 `public class Main` 이라는 애가 뭔지 알아봅시다. 

`Main` class 는 main() method를 가지고 있는 클래스 입니다. <br>
딱히 다른건 업네요. main() method가 중요한데, 꼭 class이름이 Main이 아니여도 상관 없습니다. 


# 2. Main Method
main method는 기본 프로젝트에 `public static void main(String[] args)`로 정의 되었습니다. 
public static이라는 친구에 대해 좀 찾아봤는데요. Java 참 흥미롭군요. 

우선 `public`이라는 것은 해당 `method`가 공개 되어있다는 뜻이며 다른 유형의 개체에서 호출될 수 있다는 것을 의미합니다. 

[https://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html](https://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html) 이 링크에서 자세한 설명을 확인할 수 있습니다. 

`static`은 class 객체를 새로 만들지 않아도 class.method방식으로 호출할 수 있다고 합니다. 
class안에 포함된 method들은 static이 있으면 class 객체를 생성하지 않고도 호출 할 수 있는 반변, static이 없으면 class 객체를 생성해야지만 접근 가능한 것으로 이해 했습니다. 

사실, 아직 뭔말인지 잘 모르는데 이렇게 정리하고 넘어가겠습니다. <br>
`public class Person` 이 있고 이 안에 method로 `public static void sayMyName()`이 있는 경우 `static`이 붙어 있기 때문에 `Person.sayMyName();`이렇게 호출 가능합니다.<br>

반대로, `static`이 안붙어있는 `public void sayMyName()`인 경우에는 `Person`이라는 클래스 객체를 `Person scott = new Person();` 이렇게 생성한 후에 `scott.sayMyName();`으로 호출 할 수 있습니다.

이러한 이유는 method가 해당 class의 특정 instance(object)가 아니라 class와 연결되어 있다는 것을 의미한다고 하는데요. 저는 이 말이 무슨말인지 모르겠습니다 ㅎㅎ;

keep going!
# 3. Print Hello Java
드디어.. 대망의 첫 코딩 😀<br>
아래와 같이 작성한 후에 `shift` + `f10` 키를 눌러 줍니다.

```java
package com.company;

public class Main {

    public static void main(String[] args) {
        // print hello java
        System.out.println("Hello Java!");
    }
}
```
![]({{ 'assets/images/print-hello-java.png' | relative_url }})

크으! 

이렇게 첫 코딩 완료!    Java 이제 첫 문을 열었네요.
