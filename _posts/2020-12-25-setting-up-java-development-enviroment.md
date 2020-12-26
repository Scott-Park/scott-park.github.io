---
title: Setting up Java development enviroment
tags:
- "#java"
- "#beginner"
- "#JDK"
- "#IntelliJ"
- "#atFrist"
- "#notadeveloper"
- "#setting"
categories:
- LearnJava
toc: true
---

# 1. JDK Install
Development evniroment
- **Windwos 10(current and almost use)**
- MacOS

대부분 window환경에서 개발하고 작업하므로 이 글은 windwos 10 기준으로 작성 되었습니다. 

Java개발을 위해 먼저 JDK(Java Development Kit)을 다운로드 합니다. <br>
무료로 사용 가능한 OpenJDK인 Amazon Corretto 11을 설치 하였습니다. <br>

[https://aws.amazon.com/ko/corretto/](https://aws.amazon.com/ko/corretto/)
![]({{ 'assets/images/aws-correto-download.png' | relative_url }})

**설치 파일:** [https://corretto.aws/downloads/latest/amazon-corretto-11-x64-windows-jdk.msi](https://corretto.aws/downloads/latest/amazon-corretto-11-x64-windows-jdk.msi)
![]({{ 'assets/images/aws-correto-download-windows.png' | relative_url }})

설치 후에 `java -version`으로 잘 설치되었는지 확인 합니다.
![]({{ 'assets/images/java-version.png' | relative_url }})

버전 정보가 나오면 JDK는 설치 완료 했습니다.

<br>
<br>
<br>
# 2. IntelliJ IDE install 
Google에서 `java best ide`를 검색해봤더니 intellij가 제일 좋다고 하여 다운 받습니다. <br>
홈페이지도 아주 맘에 듭니다. `탁월하고 인체공학적인 IDE`
![]({{ 'assets/images/about-intellij.png' | relative_url }})

[https://www.jetbrains.com/ko-kr/idea/download/download-thanks.html?platform=windows&code=IIC](https://www.jetbrains.com/ko-kr/idea/download/download-thanks.html?platform=windows&code=IIC)
![]({{ 'assets/images/download-intellij.png' | relative_url }})

프로그램 설치 과정에서 나오는 체크박스에는 바탕화면 바로가기와 `.java`만 선택하고 나머지는 몰라서 선택 안했습니다. 
![]({{ 'assets/images/install-intellij-choose-checkbox.png' | relative_url }})

설치 완료!
<br>
<br>
<br>

# 3. Start first project

IntelliJ를 설치 하였으니 이제 실행해 봅니다. 

처음 실행하면 기존 설정을 불러올 것인가를 물어보는데 기존 설정이 없으니 그냥 넘어 갑니다. 

![]({{ 'assets/images/first-running-intellij.png' | relative_url }})

기본 화면이 멋지네요.<br>
여기서 `New Project`를 선택해 줍니다. <br>
(왼쪽 메뉴에 Learn 도 괜찮을 것 같아요)

![]({{ 'assets/images/intellij-base-window.png' | relative_url }})

여기서부터는 저도 뭔지 잘 몰라서 제 맘대로 했습니다. <br>
아무것도 선택하지 않았습니다.

![]({{ 'assets/images/intellij-new-project.png' | relative_url }})

Create project from template 선택 후 나타나는 Command Line App 선택

![]({{ 'assets/images/intellij-new-project2.png' | relative_url }})

Project 이름 설정, 저는 helloIntelliJ로 했습니다.

![]({{ 'assets/images/intellij-new-project-name-setting.png' | relative_url }})

만들어진 프로젝트에서 메인 코드까지 확장

![]({{ 'assets/images/intellij-new-project-main.png' | relative_url }})

이렇게 Java 개발 환경을 설정 하였습니다. <br>
이제 시작이네요. 😉
