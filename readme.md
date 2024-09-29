# DevOps

# 1. 통합 개발 환경 구축

## 개발 환경이란?

**IDE(통합 개발 환경, Integrated Development Environment)는 소프트웨어 개발을 지원하는 다양한 도구를 통합한 프로그램입니다. 개발자는 IDE를 사용해 코드 작성, 컴파일, 디버깅, 배포까지 한 곳에서 관리할 수 있습니다. IDE는 개발을 보다 효율적이고 편리하게 만들어주며, 다음과 같은 주요 기능을 제공합니다.**

① 코드 편집기: 코드를 작성할 수 있는 텍스트 편집기입니다. 보통 구문 강조(Syntax Highlighting), 코드 자동 완성(Autocomplete) 기능이 있어 코드 작성 속도와 정확성을 높여줍니다.

② 컴파일러/인터프리터: 개발자가 작성한 소스 코드를 기계어로 번역하여 실행할 수 있는 프로그램입니다. 대부분의 IDE는 이를 통합하여 한 번의 클릭으로 코드를 컴파일하고 실행할 수 있게 합니다.

③ 디버거: 코드 실행 중 발생하는 오류를 찾아내고 수정할 수 있도록 돕는 도구입니다. 중단점(Breakpoint)을 설정하여 코드의 특정 지점에서 프로그램을 멈추고 상태를 분석할 수 있습니다.

④ 프로젝트 관리 도구: 여러 파일과 폴더로 구성된 프로젝트를 관리할 수 있는 기능을 제공합니다. 이를 통해 파일 탐색 및 구조 관리를 용이하게 할 수 있습니다.

⑤ 버전 관리 통합: Git 같은 버전 관리 시스템과 연동되어 코드의 변경 이력을 추적하고 협업할 수 있도록 돕습니다.

⑥ 빌드 자동화 도구: 프로젝트를 빌드하고 필요한 라이브러리를 자동으로 설정하는 도구가 포함될 수 있습니다.

⑦ 플러그인 및 확장 기능: IDE는 다양한 언어 지원과 기능 추가를 위해 플러그인 시스템을 갖추고 있어 개발자가 필요한 도구나 기능을 쉽게 확장할 수 있습니다.

<br>

## 대표적인 IDE

① Visual Studio: Microsoft에서 제공하는 IDE로, 주로 .NET 기반의 개발에 사용됩니다.
② IntelliJ IDEA: JetBrains에서 제공하는 IDE로, 주로 Java 개발에 많이 사용되며 다양한 언어를 지원합니다.
③ Eclipse: 오픈소스 IDE로 Java를 비롯한 다양한 언어의 개발에 널리 사용됩니다.
④ PyCharm: Python 개발에 특화된 JetBrains의 IDE입니다.

**IDE는 단순한 텍스트 에디터와 달리 소프트웨어 개발의 모든 과정을 통합하여 관리할 수 있어 개발자들에게 매우 유용한 도구입니다.**

<br><br>

## 1.1 Java 설치

### 1.1.1 Java 17 다운로드

Oracle에서 제공하는 JDK(Java Development Kit) 17을 다운로드할 수 있습니다. 아래 절차를 따라 Java 17을 설치하세요.

① 다운로드 절차: Oracle JDK 다운로드 사이트로 이동합니다.
- URL: https://www.oracle.com/java/technologies/javase-jdk17-downloads.html

② 운영체제 선택
1) 본인의 운영체제에 맞는 파일을 선택합니다. Windows, macOS, 또는 Linux 용 다운로드 파일이 제공됩니다.
   - Windows: .exe 또는 .msi 설치 파일
   - macOS: .dmg 설치 파일
   - Linux: .tar.gz 또는 패키지 관리 시스템을 통한 설치
2) 설치 파일 다운로드
운영체제에 맞는 설치 파일을 다운로드합니다.

<br>

### 1.1.2 Java 17 설치

① Windows 설치 절차
1) 다운로드한 .exe 또는 .msi 파일을 실행합니다.
2) 설치 마법사에 따라 Next를 클릭하여 진행합니다.
3) 설치 경로를 지정할 수 있으며, 기본 경로는 C:\Program Files\Java\jdk-17\입니다. 원하는 위치에 설치하거나 기본 경로를 사용하면 됩니다.
4) Install을 클릭하여 설치를 완료합니다.

② macOS 설치 절차:
1) 다운로드한 .dmg 파일을 실행한 후 패키지 설치를 진행합니다.
2) 화면의 안내에 따라 Java 17을 설치합니다.

③ Linux 설치 절차:
1) .tar.gz 파일을 다운로드한 후, 압축을 풀어 설치합니다.

```bash
tar -xvzf jdk-17_linux-x64_bin.tar.gz
sudo mv jdk-17 /usr/local/
```

또한, 패키지 관리 시스템으로 설치할 수도 있습니다.

<br>

### 1.1.3 환경 변수 설정 (Windows 기준)

Java 설치가 완료되면 환경 변수를 설정해야 합니다. 환경 변수를 설정해야 터미널에서 java와 javac 명령어를 사용할 수 있습니다.

① 시스템 속성 열기
1) 바탕화면에서 내 PC 아이콘을 우클릭한 후 속성을 선택합니다.
2) 왼쪽 메뉴에서 고급 시스템 설정을 클릭합니다.

② 환경 변수 버튼 클릭
- 고급 탭에서 환경 변수 버튼을 클릭합니다.

③ JAVA_HOME 변수 추가
- 시스템 변수에서 새로 만들기를 클릭합니다.
1) 변수 이름: JAVA_HOME
2) 변수 값: C:\Program Files\Java\jdk-17 (설치 경로에 따라 변경 가능)

④ Path 변수에 추가
1) 시스템 변수 목록에서 Path를 선택한 후 편집을 클릭합니다.
2) 새로 만들기를 클릭하고, JAVA_HOME\bin 경로를 추가합니다.
3) %JAVA_HOME%\bin

확인을 눌러 모든 창을 닫습니다.

<br>

### 1.1.4 설치 확인

환경 변수 설정 후, Java가 올바르게 설치되었는지 확인하려면 명령 프롬프트 또는 터미널을 열고 다음 명령어를 입력하세요.

<br>

```bash
java -version

java version "17.0.0" 2021-09-14 LTS
Java(TM) SE Runtime Environment (build 17.0.0+35-LTS-2724)
Java HotSpot(TM) 64-Bit Server VM (build 17.0.0+35-LTS-2724, mixed mode)
```

<br>

### 1.1.5 자바 컴파일러 확인

Java 컴파일러(javac)도 함께 확인하려면 다음 명령어를 실행하세요.

```bash
javac -version
```

정상적으로 설치되었다면 javac 17.0.0 같은 버전 정보가 출력됩니다.


<br><br>

## 1.2 Visual Studio Code 설치

### 1.2.1 Visual Studio Code 다운로드

① VS Code 다운로드 페이지로 이동:
- URL: https://code.visualstudio.com/

② 운영체제 선택:
- 본인의 운영체제에 맞는 설치 파일을 선택합니다. Windows, macOS, 또는 Linux를 선택할 수 있습니다.
1) Windows: .exe 설치 파일
2) macOS: .zip 또는 .dmg 설치 파일
3) Linux: .deb 또는 .rpm 파일

③ 설치 파일 다운로드
- 운영체제에 맞는 파일을 다운로드한 후 실행하여 설치를 진행합니다.

<br>

### 1.2.2 Visual Studio Code 설치

① Windows의 경우 .exe 파일을 실행하고 설치 마법사에 따라 설치를 완료합니다.

② macOS는 .zip 파일을 풀고 Applications 폴더로 이동합니다.

③ Linux는 다운로드한 패키지를 설치합니다.

<br>

### 1.2.3 한국어 확장팩 설치

① VS Code 실행
설치가 완료되면 VS Code를 실행합니다.

② 확장팩 설치
- 좌측 하단의 **Extensions 아이콘(확장기능 마켓)**을 클릭하거나, Ctrl + Shift + X(Windows) 또는 Cmd + Shift + X(macOS)를 눌러 확장 마켓을 엽니다.

③ Korean Language Pack 검색
검색창에 korean 또는 Korean Language Pack을 입력하고, **"Korean Language Pack for Visual Studio Code"**를 선택합니다.

④ 설치

Install 버튼을 클릭하여 한국어 언어팩을 설치합니다.

⑤ 언어 변경
설치 후 VS Code를 다시 시작하거나, VS Code 하단에 표시된 "언어를 변경할까요?" 메시지를 따라 한국어로 변경할 수 있습니다.

<br>

### 1.2.4 컬러 테마 변경

① 컬러 테마 설정 열기
상단 메뉴에서 파일 > 기본 설정 > 테마 색 설정을 클릭하거나, Ctrl + K를 누르고 곧바로 Ctrl + T를 눌러 테마 선택 창을 엽니다.

② 테마 선택
컬러 테마 선택창이 나타나면 다양한 테마 중에서 마음에 드는 테마를 선택합니다.
기본 제공 테마 외에도, 추가적인 컬러 테마를 다운로드하려면 확장 기능 마켓에서 테마를 검색해 설치할 수 있습니다. 예: One Dark Pro, Dracula Official 등.

<br>

### 1.2.5 Extension Pack for Java 설치

① 확장 기능 마켓 열기
- 확장 기능(Extensions) 아이콘을 클릭하거나, Ctrl + Shift + X(Windows) 또는 Cmd + Shift + X(macOS)를 눌러 확장 기능 마켓을 엽니다.

② Extension Pack for Java 검색:
- 검색창에 Extension Pack for Java를 입력하고, **Microsoft에서 제공하는 "Extension Pack for Java"**를 선택합니다.

③ 설치
Install 버튼을 클릭하여 설치합니다.

**이 확장팩은 Java 개발에 필요한 여러 플러그인(JDK, Maven, Debugger 등)을 포함하고 있습니다.**

<br>

### 1.2.6 Spring Boot Extension Pack 설치

① 확장 기능 마켓 열기
- 마찬가지로 확장 기능(Extensions) 아이콘을 클릭하여 확장 마켓을 엽니다.

② Spring Boot Extension Pack 검색
검색창에 Spring Boot Extension Pack을 입력하고, **"Spring Boot Extension Pack"**을 선택합니다.

③ 설치
Install 버튼을 클릭하여 설치합니다.

**이 확장팩은 Spring Boot 개발에 필요한 다양한 도구(Spring Initializr, Spring Boot Dashboard, Spring Tools 등)를 포함하고 있습니다.**

<br>

### 1.2.7 Git Extension Pack 설치

① 확장 기능 마켓 열기
확장 기능(Extensions) 아이콘을 클릭하여 확장 마켓을 엽니다.

② Git Extension Pack 검색
검색창에 Git Extension Pack을 입력하고, **"Git Extension Pack"**을 선택합니다.

③ 설치
Install 버튼을 클릭하여 설치합니다.

**이 확장팩은 Git을 통합 관리할 수 있는 여러 도구(GitLens, Git History 등)를 포함하고 있습니다.**

<br><br>

## 1.3 Git bash 설치

Git Bash를 다운로드하고 설치하는 방법과 GitHub 가입 및 레포지토리 생성 방법은 아래 단계에 따라 진행됩니다.

### 1.3.1 Git Bash 다운로드 및 설치
Git Bash는 Git을 명령줄에서 사용하기 위한 프로그램으로, 특히 Windows 환경에서 많이 사용됩니다.

① Git 공식 웹사이트로 이동
- URL: https://git-scm.com/

② 운영체제 선택 및 다운로드
- 메인 페이지에서 본인의 운영체제에 맞는 Git 설치 파일을 다운로드합니다. Windows의 경우 "Download for Windows" 버튼을 클릭하여 설치 파일을 다운로드합니다.

③ 설치 파일 실행
다운로드한 파일을 실행하여 설치 마법사를 시작합니다.

④ 설치 옵션 선택
설치 과정 중 몇 가지 선택 사항이 있습니다. 기본 설정을 사용해도 무방하지만, 각 옵션을 설명하면 다음과 같습니다.

1) 컴포넌트 선택: 기본 설정을 사용합니다.
2) 편집기 선택: Git 커밋 메시지 편집기 선택입니다. 기본값으로 Vim이 설정되어 있지만, Visual Studio Code 같은 다른 에디터를 선택할 수 있습니다.
3) 환경 변수 설정: "Git from the command line and also from 3rd-party software"를 선택하면 Git Bash뿐만 아니라 모든 명령줄에서 Git 명령어를 사용할 수 있습니다.
4) HTTPS 전송 백엔드: OpenSSL을 기본값으로 유지합니다.
5) 라인 엔딩 변환: "Checkout Windows-style, commit Unix-style line endings"를 선택하여 다양한 운영체제에서 코드 충돌을 방지합니다.

⑤ 설치 완료
나머지 옵션을 기본값으로 진행하여 설치를 완료합니다.

⑥ 설치 확인
설치가 완료된 후 Git Bash를 실행합니다.
Git이 정상적으로 설치되었는지 확인하려면 Git Bash에서 다음 명령어를 입력하세요

```bash
git --version
```

git version 2.x.x 와 같은 출력이 나오면 정상적으로 설치된 것입니다.

<br>

### 1.3.2 GitHub 가입
GitHub는 Git을 기반으로 한 코드 호스팅 플랫폼으로, 개발자들이 협업하고 프로젝트를 관리할 수 있는 곳입니다.

① GitHub 공식 웹사이트로 이동
URL: https://github.com/

② 회원가입 페이지로 이동
오른쪽 상단의 Sign up 버튼을 클릭하여 회원가입 페이지로 이동합니다.

③ 회원가입 정보 입력
이메일 주소를 입력하고, 비밀번호와 사용자 이름을 설정합니다.
reCAPTCHA를 완료한 후, Create account 버튼을 클릭합니다.

④ 계정 설정 및 확인
입력한 이메일로 인증 메일이 전송됩니다. 이메일을 확인하고 GitHub 계정을 인증합니다.

이후 GitHub 계정이 활성화됩니다.

<br>

3. GitHub에서 새로운 레포지토리 생성
GitHub에서 레포지토리(Repository)를 생성하는 과정은 매우 간단합니다. 레포지토리는 소스 코드와 버전을 관리하는 공간입니다.

① GitHub 로그인
GitHub 홈페이지에서 방금 생성한 계정으로 로그인합니다.

② 새로운 레포지토리 생성
로그인 후 오른쪽 상단의 + 아이콘을 클릭하고, New repository를 선택합니다.

③ 레포지토리 정보 입력
1) Repository name: 레포지토리의 이름을 입력합니다. 예를 들어, my-first-repo와 같이 작성할 수 있습니다.
2) Description (Optional): 프로젝트에 대한 설명을 적습니다. (선택 사항)
3) Public 또는 Private: 레포지토리를 **공개(Public)**로 할지 **비공개(Private)**로 할지 선택합니다. 공개로 설정하면 누구나 레포지토리를 볼 수 있고, 비공개로 설정하면 초대된 사람만 볼 수 있습니다.
4) Initialize this repository with a README: 체크박스를 선택하면 기본적으로 README.md 파일이 추가됩니다. 이 파일은 프로젝트에 대한 설명을 담고 있으며, 프로젝트 시작에 유용합니다.

④ 레포지토리 생성
모든 정보를 입력한 후 Create repository 버튼을 클릭하여 레포지토리를 생성합니다.

<br>

### 1.3.3 Git Bash에서 GitHub 레포지토리 연결 및 코드 푸시

GitHub에서 생성한 레포지토리를 로컬에서 관리하고, Git Bash를 사용해 코드 변경 사항을 푸시할 수 있습니다.

① 로컬 디렉토리 생성
먼저 Git Bash를 열고 프로젝트를 저장할 디렉토리를 생성합니다.

```bash
mkdir my-first-repo
cd my-first-repo
```

② GitHub 레포지토리 클론
1) GitHub에서 생성한 레포지토리를 로컬에 복제하려면 GitHub 레포지토리 페이지에서 Clone 버튼을 클릭하고, HTTPS 주소를 복사합니다.
2) Git Bash에서 복사한 주소로 레포지토리를 클론합니다.

```bash
git clone https://github.com/사용자이름/my-first-repo.git
```

③ 새 파일 추가 및 커밋
로컬 레포지토리에 파일을 추가하고 Git으로 커밋할 수 있습니다.

```bash
echo "# My First Repository" >> README.md
git add README.md
git commit -m "Add README file"
```

④ GitHub로 푸시
로컬에서 커밋한 변경 사항을 GitHub 레포지토리로 푸시합니다.

```bash
git push origin main
```

**이제 GitHub의 해당 Repository에서 방금 푸시한 내용을 확인할 수 있습니다.**

<br><br>

## 1.4 애플리케이션 제작 및 테스트

### 1.4.1 Spring Boot 프로젝트 생성 (Gradle 기반)

① Spring Initializr 사용
**Spring Initializr**에 접속합니다.

프로젝트 설정을 다음과 같이 선택합니다:

Project: Gradle
Language: Java
Spring Boot: 3.0.x (최신 버전)
Group: com.example
Artifact: demo
Name: demo
Package Name: com.example.demo
Java Version: 17
Dependencies: Spring Web, Spring Boot DevTools, Lombok

"Generate" 버튼을 눌러 프로젝트를 다운로드하고, IDE에서 프로젝트를 엽니다.

② Gradle 설정 확인
build.gradle 파일이 자동으로 생성됩니다. 이 파일에는 Spring Boot 3.0 이상 및 Java 17과 관련된 의존성이 설정됩니다.

```gradle
plugins {
    id 'org.springframework.boot' version '3.0.0'
    id 'io.spring.dependency-management' version '1.0.14.RELEASE'
    id 'java'
}

group = 'com.example'
version = '0.0.1-SNAPSHOT'
sourceCompatibility = '17'

repositories {
    mavenCentral()
}

dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-web'
    testImplementation 'org.springframework.boot:spring-boot-starter-test'
}

test {
    useJUnitPlatform()
}
```

<br>

### 1.4.2 애플리케이션 코드 작성
Spring Boot 애플리케이션의 기본적인 REST API를 구현합니다.

① HelloController 작성
`src/main/java/com/example/demo/HelloController.java` 파일을 생성하여 간단한 컨트롤러를 작성합니다.

```java
package com.example.demo;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

    @GetMapping("/hello")
    public String hello() {
        return "Hello, Spring Boot 3 and Java 17!";
    }
}
```

@RestController: RESTful 웹 서비스를 제공하는 컨트롤러임을 표시합니다.
@GetMapping("/hello"): /hello 경로로 들어오는 GET 요청을 처리하고, 문자열을 반환하는 메서드를 정의합니다.


② DemoApplication 클래스 작성
src/main/java/com/example/demo/DemoApplication.java에 애플리케이션 진입점을 작성합니다.

```java
package com.example.demo;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class DemoApplication {

    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}
```

<br>

### 1.4.3 애플리케이션 실행
① Gradle을 이용해 애플리케이션 실행
Spring Boot 애플리케이션을 Gradle 명령어로 실행합니다.

```bash
./gradlew bootRun
```

./gradlew bootRun 명령어는 프로젝트를 빌드하고, Spring Boot 애플리케이션을 실행합니다.
애플리케이션이 성공적으로 실행되면 기본적으로 **http://localhost:8080**에서 접근할 수 있습니다.

② 브라우저 또는 Postman으로 테스트
브라우저 또는 API 테스트 도구(Postman)를 사용하여 애플리케이션을 테스트합니다.

브라우저에서 **http://localhost:8080/hello**로 이동하거나, Postman을 이용해 GET 요청을 보냅니다.
응답으로 Hello, Spring Boot 3 and Java 17! 메시지를 확인합니다.

<br>

### 1.4.4 JUnit을 사용한 테스트
Spring Boot에서 JUnit을 사용하여 단위 테스트를 작성하고 애플리케이션의 기능을 검증할 수 있습니다.

① HelloControllerTest 작성
`src/test/java/com/example/demo/HelloControllerTest.java` 파일을 생성하여, REST API 테스트를 작성합니다.

```java
package com.example.demo;

import org.junit.jupiter.api.Test;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.autoconfigure.web.servlet.WebMvcTest;
import org.springframework.test.web.servlet.MockMvc;

import static org.springframework.test.web.servlet.request.MockMvcRequestBuilders.get;
import static org.springframework.test.web.servlet.result.MockMvcResultMatchers.content;
import static org.springframework.test.web.servlet.result.MockMvcResultMatchers.status;

@WebMvcTest(HelloController.class)
public class HelloControllerTest {

    @Autowired
    private MockMvc mockMvc;

    @Test
    public void helloTest() throws Exception {
        mockMvc.perform(get("/hello"))
                .andExpect(status().isOk())
                .andExpect(content().string("Hello, Spring Boot 3 and Java 17!"));
    }
}
```

@WebMvcTest(HelloController.class): 이 애너테이션은 컨트롤러의 WebMvc 테스트에만 필요한 부분만 로드합니다.
mockMvc: 가상의 HTTP 요청을 만들고 응답을 검증할 수 있습니다.

테스트는 /hello 경로로 GET 요청을 보내고, 응답이 **Hello, Spring Boot 3 and Java 17!**인지 확인합니다.

② 테스트 실행
IDE(예: IntelliJ IDEA, Eclipse)에서 JUnit 테스트를 실행합니다.
테스트가 성공하면 애플리케이션의 기능이 의도한 대로 동작하는 것을 확인할 수 있습니다.

<br>

### 1.4.5 빌드 및 패키징

① Gradle 빌드 및 JAR 파일 생성

```bash
./gradlew clean build
```

성공적으로 빌드가 완료되면 build/libs 디렉토리에 demo-0.0.1-SNAPSHOT.jar 파일이 생성됩니다.

② JAR 파일 실행

```bash
java -jar build/libs/demo-0.0.1-SNAPSHOT.jar
```

이 명령을 통해 프로젝트가 실행되며, http://localhost:8080/hello 경로로 접근할 수 있습니다.

<br>

### 1.4.6 프로덕션 환경에서 Docker로 배포
Spring Boot 프로젝트를 Docker로 컨테이너화하여 배포할 수 있습니다.

① Dockerfile 작성
프로젝트 루트에 Dockerfile을 작성합니다.

```dockerfile
# Java 17 JDK를 기반으로 Docker 이미지 생성
FROM openjdk:17-jdk-alpine
VOLUME /tmp
ARG JAR_FILE=build/libs/demo-0.0.1-SNAPSHOT.jar
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
```

② Docker 이미지 빌드

```bash
docker build -t springboot-demo .
```

이 명령을 통해 Docker 이미지가 생성됩니다.

③ Docker 컨테이너 실행

```bash
docker run -p 8080:8080 springboot-demo
```

Docker 컨테이너를 실행하면 **http://localhost:8080/hello**에서 애플리케이션을 확인할 수 있습니다.


<br><br><br>

# 2. Git/GitHub

`.gitignore` 는 버전관리가 필요하지 않은 부분의 설정 내용이 들어갑니다.

<br><br>

## 2.1 Git/GitHub 사용법

- Git이란?
    Git은 **분산 버전 관리 시스템(DVCS, Distributed Version Control System)**입니다. 소프트웨어 프로젝트에서 소스 코드를 관리하고, 여러 명이 동시에 작업할 수 있게 도와주는 도구입니다.

- Git의 주요 기능
    버전 관리: 소스 코드의 변경 사항을 기록하고, 특정 시점의 상태로 되돌아가거나 이전 버전과 비교할 수 있습니다.
    분산형 구조: 모든 개발자는 로컬 저장소를 가지고 작업하며, 이 로컬 저장소는 전체 프로젝트의 버전을 관리할 수 있습니다.
    브랜치 관리: 여러 개발자가 서로 다른 기능을 개발하거나 버그 수정을 병렬로 작업할 수 있게 해줍니다. 개발이 끝난 후에는 브랜치를 병합(merge)하여 메인 코드에 포함시킵니다.
    협업 도구: 여러 개발자가 동시에 작업할 수 있도록 도움을 주며, 코드 충돌을 해결하고 통합할 수 있는 기능을 제공합니다.

- Git의 주요 명령어
    git init: 새로운 Git 저장소를 초기화하는 명령어.
    git clone: 원격 저장소를 로컬에 복제하는 명령어.
    git add: 변경된 파일을 스테이징 영역에 추가하는 명령어.
    git commit: 스테이징 영역에 있는 변경 사항을 로컬 저장소에 저장하는 명령어.
    git push: 로컬에서 저장된 변경 사항을 원격 저장소에 업로드하는 명령어.
    git pull: 원격 저장소에서 변경 사항을 로컬로 가져오는 명령어.

- GitHub란?
    GitHub는 Git을 기반으로 한 원격 저장소 호스팅 서비스입니다. 소스 코드를 온라인에서 관리할 수 있게 해주며, 특히 개발자들이 협업을 할 때 사용됩니다. Git을 사용하여 로컬에서 작업한 코드를 GitHub와 같은 원격 저장소에 업로드하고, 팀원들과 공유할 수 있습니다.

- GitHub의 주요 기능
    원격 저장소: 프로젝트의 소스 코드를 클라우드에 저장하고, 팀원들과 공유할 수 있습니다.
    협업 도구: 여러 개발자가 함께 프로젝트를 진행할 수 있는 도구(예: Pull Request, 코드 리뷰 등)를 제공합니다.
    이슈 관리: 프로젝트에서 발생하는 버그나 기능 요청을 추적하고 관리할 수 있습니다.
    프로젝트 관리: 프로젝트의 진행 상황을 관리할 수 있는 보드와 같은 도구를 제공합니다.
    오픈 소스: 누구나 오픈 소스 프로젝트를 시작하거나 참여할 수 있습니다. GitHub는 전 세계의 오픈 소스 프로젝트가 가장 많이 호스팅되는 플랫폼입니다.

- GitHub의 주요 기능과 워크플로우
    Fork: 다른 사용자의 저장소를 복제하여 내 저장소로 가져와 수정할 수 있습니다.
    Pull Request (PR): 수정된 코드를 원래 프로젝트에 제안하는 기능으로, 팀원이나 오픈 소스 커뮤니티에 변경사항을 기여할 수 있습니다.
    GitHub Actions: CI/CD 파이프라인을 자동화할 수 있는 기능으로, 코드를 푸시할 때 자동으로 빌드, 테스트, 배포를 실행할 수 있습니다.

<br><br>

## 2.2 Git 협업 패턴

Git 협업 패턴은 개발자들이 같은 프로젝트에서 효율적으로 작업하고 충돌을 최소화하며 코드 품질을 유지할 수 있도록 돕는 방법들입니다. 팀의 규모나 프로젝트 특성에 따라 다양한 협업 패턴이 존재하며, 여기서는 가장 일반적이고 널리 사용되는 협업 패턴들을 소개하겠습니다.

<br>

### 2.2.1 Git Flow
Git Flow는 Git을 사용한 협업에서 가장 널리 사용되는 워크플로우 중 하나로, 기능 개발, 출시 준비, 버그 수정 등 각 작업의 목적에 따라 브랜치를 분리하여 작업합니다.

① Git Flow 브랜치 구조
  - main: 최종 배포된 코드를 유지하는 브랜치. 항상 안정적인 상태를 유지해야 합니다.
  - develop: 개발 중인 코드가 모이는 브랜치. 모든 기능(feature) 브랜치가 이곳으로 병합됩니다.
  - feature 브랜치: 새로운 기능을 개발할 때 사용하는 브랜치. develop에서 분기하고, 개발 완료 후 다시 develop에 병합합니다.
  - release 브랜치: 릴리스를 준비할 때 사용하는 브랜치로, develop 브랜치에서 분기하여 최종 테스트 및 버그 수정이 이루어집니다. 완료되면 main과 develop에 병합됩니다.
  - hotfix 브랜치: 프로덕션(main)에서 발생한 버그를 긴급히 수정할 때 사용하는 브랜치입니다. main에서 분기하고, 수정이 완료되면 main과 develop에 병합됩니다.

② Git Flow 기본 사용 예시
1) 새로운 기능 개발 (feature 브랜치)

```bash
git checkout develop  # develop 브랜치에서 작업 시작
git checkout -b feature/새로운-기능  # feature 브랜치 생성

# 코딩 작업 수행
git add .  # 변경사항 스테이징
git commit -m "새로운 기능 추가"  # 커밋
git push origin feature/새로운-기능  # 원격 저장소에 푸시
```

2) 개발 완료 후 병합

```bash
git checkout develop  # develop 브랜치로 이동
git pull origin develop  # 최신 상태로 업데이트
git merge feature/새로운-기능  # 기능 병합
git push origin develop  # 원격 저장소에 병합된 상태로 푸시
```

3) 릴리스 준비 (release 브랜치)

```bash
git checkout develop
git checkout -b release/1.0.0  # release 브랜치 생성
# 테스트 및 버그 수정
git commit -m "버그 수정 및 테스트 완료"
git checkout main  # main 브랜치로 이동
git merge release/1.0.0  # release 브랜치 병합
git push origin main  # main 브랜치 푸시
```

4) 핫픽스 수정 (hotfix 브랜치)

```bash
git checkout main
git checkout -b hotfix/긴급-버그-수정
# 버그 수정
git commit -m "긴급 버그 수정"
git checkout main
git merge hotfix/긴급-버그-수정
git push origin main  # main 브랜치 푸시
git checkout develop
git merge hotfix/긴급-버그-수정  # develop에도 수정 반영
```

<br>

### 2.2.2 GitHub Flow
GitHub Flow는 Git Flow보다 간단한 방식으로, 배포 주기가 짧거나 빠른 개발이 요구되는 프로젝트에 적합합니다. main 브랜치는 언제나 배포 가능한 상태를 유지하며, 개발자는 항상 별도의 브랜치에서 작업 후 Pull Request(PR)를 통해 병합합니다.

① GitHub Flow의 흐름
   - main 브랜치는 배포 가능한 상태를 유지: main 브랜치는 항상 안정적이고, 배포 가능한 상태를 유지해야 합니다.
   - 새로운 브랜치 생성: 작업을 시작하기 전, main 브랜치에서 새로운 브랜치를 생성합니다.
   - 작업 완료 후 PR 생성: 작업이 완료되면 Pull Request(PR)를 생성하여 코드 리뷰를 요청합니다.
   - 코드 리뷰 후 병합: 코드 리뷰가 완료되면, main 브랜치에 병합하고 배포를 준비합니다.

② GitHub Flow 예시
1) 새로운 브랜치에서 기능 개발

```bash
git checkout main  # main 브랜치에서 작업 시작
git pull origin main  # 최신 상태로 업데이트
git checkout -b feature/새로운-기능  # 새로운 브랜치 생성
# 코딩 작업 수행
git add .
git commit -m "새로운 기능 추가"
git push origin feature/새로운-기능  # 원격 저장소로 푸시
``

2) PR 생성 및 코드 리뷰
GitHub에서 Pull Request(PR)를 열어 코드 리뷰를 요청합니다.
팀원들이 PR을 검토한 후 승인하면 병합할 수 있습니다.

3) 병합 및 배포

```bash
git checkout main
git merge feature/새로운-기능
git push origin main  # main 브랜치 푸시
```

<br>

### 2.2.3 Forking Workflow

Forking Workflow는 주로 오픈 소스 프로젝트에서 사용하는 패턴으로, 협업자가 프로젝트의 원본 저장소를 복제(fork)하여 작업을 진행한 후, 자신의 변경사항을 원본 저장소에 기여하는 방식입니다. 이 방식은 기여자와 프로젝트 소유자 간의 작업 분리를 명확하게 하며, 프로젝트 소유자는 Pull Request(PR)를 통해 기여자의 코드를 검토하고 병합 여부를 결정합니다.

① Forking Workflow의 흐름
   - 저장소 Fork: 프로젝트의 원본 저장소를 자신의 GitHub 계정으로 복제합니다.
   - 개인 저장소에서 브랜치 생성 및 작업: 포크된 저장소에서 브랜치를 생성하여 작업을 진행합니다.
   - 원본 저장소로 Pull Request: 작업이 완료되면 Pull Request를 보내 원본 저장소에 병합을 요청합니다.
   - 리뷰 및 병합: 프로젝트 소유자가 PR을 리뷰한 후, 원본 저장소에 병합합니다.

② Forking Workflow 예시

1) 저장소 Fork 및 클론
GitHub에서 프로젝트를 Fork하여 개인 계정으로 복제합니다.

```bash
git clone https://github.com/사용자명/프로젝트명.git
cd 프로젝트명
```

2) 브랜치 생성 후 작업

```bash
git checkout -b feature/새로운-기능
# 작업 수행 후 커밋
git add .
git commit -m "새로운 기능 추가"
```

3) Fork된 저장소로 푸시 후 PR 생성

```bash
git push origin feature/새로운-기능
```

4) 원본 저장소로 Pull Request 보내기
GitHub에서 Pull Request를 보내 원본 저장소로 기여합니다.

<br>

### 2.2.4 Trunk-based Development
Trunk-based Development는 작은 단위의 작업을 자주 main 브랜치에 병합하는 패턴입니다. 장기적으로 유지되는 브랜치가 없으며, 모든 개발자들이 작은 단위의 브랜치를 생성하고 작업을 마치자마자 main에 병합합니다.

이 방식은 빠르게 변하는 소프트웨어 개발 환경에 적합하며, CI/CD(지속적 통합/지속적 배포) 파이프라인과 결합하여 자주 배포가 가능합니다.

① Trunk-based Development의 흐름
   - main 브랜치에서 새 브랜치 생성
   - 작업 완료 후 빠르게 병합
   - CI/CD 파이프라인과 연동하여 자동으로 배포

② Trunk-based Development 예시
1) 작업 시작

```bash
git checkout main
git pull origin main
git checkout -b feature/작은-작업
# 작업 수행
git add .
git commit -m "작은 작업 완료"
git push origin feature/작은-작업
```

2) PR을 통해 빠르게 병합

GitHub에서 PR을 열고 코드 리뷰를 거친 후 바로 병합합니다.

<br><br>

## 2.3 Git/GitHub 실습

### 2.3.1 기본 실습

① GitHub에서 저장소 생성
    - GitHub에 가입한 후, 새로운 저장소를 생성합니다.
    - 저장소를 생성하면 원격 저장소의 URL을 제공합니다.
    - 로컬에서 Git 프로젝트 초기화 및 코드 작성

```bash
git init  # 새 Git 저장소 생성
echo "# My Project" >> README.md
git add README.md  # 변경 사항 추가
git commit -m "Initial commit"  # 변경 사항 저장
```

② GitHub 원격 저장소와 연결

```bash
git remote add origin <GitHub 저장소 URL>
git push -u origin main  # 코드를 원격 저장소에 푸시
```

③ 다른 팀원이 pull로 최신 소스 코드 가져오기

```bash
git pull origin main  # 원격 저장소에서 변경 사항 가져오기
```

④ Pull Request로 코드 제안

새로운 브랜치를 생성해 작업한 후, Pull Request(PR)를 열어 코드 리뷰를 요청합니다.

<br><br><br>

# 3. Spring Boot 배포
Spring Boot 애플리케이션을 배포하는 것은 개발 환경에서 애플리케이션을 실행하는 것과는 달리, 운영 환경에 적합한 설정을 통해 안전하고 효율적으로 실행되도록 해야 합니다. 배포 시에는 빌드된 애플리케이션을 서버에서 실행하고, 서버가 다시 시작될 때에도 자동으로 애플리케이션이 구동되도록 설정하는 과정이 필요합니다.

<br>

## 3.1 Spring Boot 배포 도구 소개
Spring Boot 애플리케이션을 배포하는 방법에는 여러 가지 도구와 방법이 존재합니다. 그 중 몇 가지 대표적인 배포 방법들을 소개합니다.

<br>

### 3.1.1 Jar 파일을 통한 배포
Spring Boot는 기본적으로 Java Archive (JAR) 파일로 빌드할 수 있습니다. 이 방식으로 배포할 경우, JAR 파일을 실행 가능한 상태로 만들고 서버에서 실행할 수 있습니다.
장점: 설정이 간단하고 별도의 웹 서버 설정이 필요하지 않음.
단점: 확장성 및 복잡한 환경에서 관리가 어려울 수 있음.

<br>

### 3.1.2 War 파일을 통한 배포
기존의 서블릿 컨테이너(Tomcat, JBoss 등)에 배포하는 방식으로, Web Archive (WAR) 파일을 빌드하여 배포합니다.
장점: 기존의 서블릿 컨테이너를 사용하여 다른 Java 애플리케이션들과 함께 실행 가능.
단점: Spring Boot의 내장 서버를 사용할 수 없으므로 설정이 다소 복잡할 수 있음.

<br>

### 3.1.3 Docker를 사용한 배포
Spring Boot 애플리케이션을 Docker 컨테이너에 배포하여 사용합니다. Docker는 애플리케이션과 그 환경을 패키징하여 이식성을 높이는 도구입니다.
장점: 다른 환경에서도 동일하게 작동하며, 배포와 관리를 쉽게 할 수 있음.
단점: Docker 설정이 필요하고 서버 리소스를 많이 사용할 수 있음.

<br>

### 3.1.4 CI/CD 도구 (Jenkins, GitHub Actions 등)
지속적 통합 및 지속적 배포(Continuous Integration/Continuous Deployment, CI/CD) 도구를 사용하여 배포를 자동화할 수 있습니다. 코드 변경 시 자동으로 빌드하고 테스트 후 서버에 배포하는 파이프라인을 구성합니다.
장점: 자동화된 배포로 효율적이고 빠르게 배포 가능.
단점: 설정 과정이 복잡할 수 있고, 유지 관리가 필요함.

<br>

### 3.1.5 Cloud 서비스 (AWS, Heroku, GCP 등)
AWS, Google Cloud Platform(GCP), Heroku 등 클라우드 서비스를 이용하여 배포하는 방법도 많이 사용됩니다. 특히 Spring Boot 애플리케이션은 클라우드와 잘 호환됩니다.
장점: 클라우드의 다양한 기능을 이용할 수 있고 확장성이 뛰어남.
단점: 클라우드 서비스 사용에 대한 비용이 발생.

<br><br>

## 3.2 Spring Boot 배포 스크립트 작성 및 실행 실습
다음은 Spring Boot 애플리케이션을 JAR 파일로 빌드하고, 서버에서 배포 및 실행하는 스크립트를 작성하는 방법입니다. 여기서는 Linux 환경에서 Spring Boot 애플리케이션을 배포하는 예제를 사용합니다.

<br>

### 3.2.1 애플리케이션 빌드
먼저, Spring Boot 프로젝트를 Gradle 또는 Maven을 사용하여 빌드합니다. Spring Boot는 기본적으로 실행 가능한 JAR 파일을 생성합니다.

<br>

① Maven으로 빌드하는 경우

```bash
./mvnw clean package
```

② Gradle로 빌드하는 경우

```bash
./gradlew clean build
```

이 명령어를 실행하면 target(Maven) 또는 build/libs(Gradle) 디렉토리에 실행 가능한 JAR 파일이 생성됩니다.

<br>

### 3.2.2 배포 스크립트 작성
다음은 Spring Boot 애플리케이션을 서버에서 실행하는 배포 스크립트 예시입니다. 이 스크립트는 애플리케이션을 백그라운드에서 실행하고, 서버 재부팅 시에도 자동으로 시작되도록 설정합니다.

```bash
#!/bin/bash

# 스크립트 실행 시 중단될 수 있는 기존 프로세스를 확인하고 종료
APP_NAME="my-springboot-app"
JAR_PATH="/path/to/your-app.jar"
PID=$(pgrep -f $APP_NAME)

if [ -n "$PID" ]; then
    echo "Stopping existing Spring Boot application (PID: $PID)"
    kill -15 $PID
    sleep 5
fi

# 새로운 애플리케이션 시작
echo "Starting Spring Boot application..."
nohup java -jar $JAR_PATH > /dev/null 2>&1 &

echo "Spring Boot application started!"
```

이 스크립트를 /usr/local/bin/deploy_app.sh 같은 경로에 저장한 후, 실행 권한을 부여합니다.

```bash
chmod +x /usr/local/bin/deploy_app.sh
```

<br>

### 3.2.3 배포 스크립트 실행
위에서 작성한 스크립트를 실행하여 Spring Boot 애플리케이션을 배포할 수 있습니다.

```bash
./deploy_app.sh
```

이 스크립트는 애플리케이션을 백그라운드에서 실행하며, 로그는 nohup 명령을 통해 표준 출력과 오류 출력을 무시하게 됩니다. 만약 로그를 확인하고 싶다면 nohup.out 파일을 생성하여 저장하거나 별도의 로그 파일을 지정할 수 있습니다.

<br>

### 3.2.4 시스템 서비스로 등록하기 (선택 사항)
Spring Boot 애플리케이션을 시스템 서비스로 등록하면 서버가 재부팅될 때 자동으로 애플리케이션이 시작되도록 설정할 수 있습니다. systemd를 사용하여 서비스 파일을 생성하는 예시입니다.

```bash
sudo nano /etc/systemd/system/myapp.service
```

파일 내용은 다음과 같습니다.

```ini
[Unit]
Description=My Spring Boot Application
After=network.target

[Service]
User=ec2-user  # 애플리케이션을 실행할 사용자
ExecStart=/usr/bin/java -jar /path/to/your-app.jar
SuccessExitStatus=143
Restart=always

[Install]
WantedBy=multi-user.target
```

이후, 다음 명령어를 통해 서비스 활성화 및 시작이 가능합니다.

```bash
sudo systemctl daemon-reload
sudo systemctl enable myapp.service
sudo systemctl start myapp.service
```

<br>

### 3.2.5 Docker로 배포 스크립트 작성
Spring Boot 애플리케이션을 Docker를 사용하여 배포하는 방법도 널리 사용됩니다. Docker로 Spring Boot 애플리케이션을 배포하려면 Dockerfile을 작성해야 합니다.

```Dockerfile
# Dockerfile

# 베이스 이미지 설정
FROM openjdk:17-jdk-alpine

# JAR 파일을 컨테이너에 복사
ARG JAR_FILE=build/libs/*.jar
COPY ${JAR_FILE} app.jar

# 애플리케이션 실행
ENTRYPOINT ["java","-jar","/app.jar"]
```

Docker 이미지 빌드 및 실행

```bash
# Docker 이미지 빌드
docker build -t my-springboot-app .

# Docker 컨테이너 실행
docker run -d -p 8080:8080 my-springboot-app
```

이 스크립트를 사용하여 애플리케이션을 Docker 컨테이너에서 실행할 수 있습니다.

<br><br><br>

# 4. Docker(도커)
Docker는 애플리케이션을 컨테이너라는 경량 환경에서 실행할 수 있도록 하는 플랫폼입니다. 컨테이너는 애플리케이션과 그 의존성을 함께 묶어 일관된 실행 환경을 제공하여, 환경 간의 차이로 인해 발생하는 문제를 최소화할 수 있습니다. Docker는 배포 자동화, 확장성, 빠른 테스트 및 개발 환경 구축에 매우 유용합니다.

<br>

## 4.1 도커 이미지
Docker 이미지(Docker Image)는 컨테이너 실행에 필요한 모든 파일, 라이브러리, 설정 등을 포함한 불변의 템플릿입니다. 이미지를 기반으로 여러 개의 컨테이너를 실행할 수 있습니다. 이미지는 레이어(layer)로 구성되어 있고, 중복된 레이어는 여러 이미지에서 공유되어 저장 공간을 절약합니다.

### 4.1.1 Docker 이미지 주요 개념
베이스 이미지(Base Image): 가장 기본적인 이미지로, 보통 운영 체제 레벨에서의 설정을 포함합니다. 예: ubuntu, alpine
이미지 레이어: 이미지는 여러 레이어로 구성되어 있으며, 명령어를 실행할 때마다 새로운 레이어가 추가됩니다. 변경 사항만 레이어로 기록됩니다.
이미지 저장소: Docker Hub 같은 중앙 저장소에 이미지를 저장하고 가져올 수 있습니다.

주요 명령어
```bash
# 이미지 목록 보기
docker images

# 이미지 다운로드 (pull)
docker pull 이미지이름

# 이미지 삭제
docker rmi 이미지이름

# 이미지 생성 (Dockerfile을 기반으로)
docker build -t 이미지이름 .

# 이미지 실행
docker run 이미지이름
```

<br><br>

## 4.2 도커 엔진 설치
도커 엔진은 도커 컨테이너의 실행, 관리, 모니터링을 담당하는 도구입니다. 다음은 Ubuntu Linux 환경에서 도커 엔진을 설치하는 방법입니다.

<br>

### 4.2.1 패키지 업데이트

```bash
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
```

<br>

### 4.2.2 Docker의 GPG 키 추가

```bash
코sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

<br>

### 4.2.3 Docker 리포지토리 추가

```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

<br>

### 4.2.4 Docker 설치

```bash
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

<br>

### 4.2.5 도커 설치 확인

```bash
sudo docker --version
```

<br>

### 4.2.6 도커 실행 설정
sudo 없이 도커 명령을 실행하려면 현재 사용자를 docker 그룹에 추가합니다.

```bash
sudo usermod -aG docker $USER
```

<br><br>

## 4.3 도커 컨테이너
Docker 컨테이너는 애플리케이션과 그 애플리케이션이 동작하는 환경을 격리하는 독립적인 실행 단위입니다. 컨테이너는 이미지에서 생성되며, 애플리케이션을 포함한 모든 실행 환경이 하나의 컨테이너 안에 들어있습니다.

<br>

### 4.3.1 주요 명령어

```bash
# 컨테이너 실행
docker run -d --name 컨테이너이름 -p 호스트포트:컨테이너포트 이미지이름

# 실행 중인 컨테이너 목록 보기
docker ps

# 종료된 컨테이너까지 포함한 모든 컨테이너 목록
docker ps -a

# 컨테이너 중지
docker stop 컨테이너이름

# 컨테이너 시작
docker start 컨테이너이름

# 컨테이너 삭제
docker rm 컨테이너이름
```

<br>

### 4.3.2 컨테이너 실행 예시

```bash
docker run -d --name my-nginx -p 8080:80 nginx
```

이 명령어는 nginx 이미지를 다운로드하고, 8080 포트로 접근 가능한 NGINX 웹 서버를 실행하는 컨테이너를 생성합니다.

<br><br>

## 4.4 Dockerfile
Dockerfile은 이미지를 생성하기 위한 설정 파일로, 이미지 빌드를 자동화하는 스크립트 역할을 합니다. Dockerfile을 작성하면 애플리케이션을 실행할 환경을 쉽게 정의할 수 있으며, Docker 이미지를 손쉽게 만들 수 있습니다.

<br>

### 4.4.1 Dockerfile 예시

```Dockerfile
# 베이스 이미지 설정
FROM openjdk:17-jdk-alpine

# 작업 디렉토리 설정
WORKDIR /app

# JAR 파일을 컨테이너로 복사
COPY build/libs/myapp.jar myapp.jar

# 애플리케이션 실행
ENTRYPOINT ["java", "-jar", "myapp.jar"]
```

이 예시는 Java 애플리케이션을 컨테이너에서 실행하기 위한 Dockerfile입니다. openjdk 이미지를 기반으로 Java 17 환경을 구성하고, JAR 파일을 컨테이너에 복사한 뒤 실행합니다.

<br>

### 4.4.2 Dockerfile 주요 명령어

FROM: 베이스 이미지를 지정합니다.
WORKDIR: 컨테이너 내부의 작업 디렉토리를 설정합니다.
COPY: 파일을 컨테이너 내부로 복사합니다.
RUN: 컨테이너 내부에서 명령어를 실행합니다.
ENTRYPOINT: 컨테이너 시작 시 실행할 명령을 지정합니다.

<br><br>

## 4.5 도커 컨테이너 및 Dockerfile 실습

### 4.5.1 Spring Boot 애플리케이션을 Docker로 배포하기

① Dockerfile 작성

먼저, Spring Boot 애플리케이션의 루트 디렉토리에 Dockerfile을 작성합니다.

```Dockerfile
# 베이스 이미지로 OpenJDK 17 사용
FROM openjdk:17-jdk-alpine

# 작업 디렉토리 설정
WORKDIR /app

# JAR 파일을 컨테이너로 복사
COPY build/libs/myapp.jar myapp.jar

# 애플리케이션 실행
ENTRYPOINT ["java", "-jar", "myapp.jar"]
```

<br>

② 이미지 빌드

Dockerfile을 작성한 후, 다음 명령어로 Docker 이미지를 빌드합니다.

```bash
docker build -t springboot-app .
```

이 명령어는 Dockerfile을 기반으로 springboot-app이라는 이름의 이미지를 생성합니다.

<br>

③ 컨테이너 실행

생성한 이미지를 실행하여 컨테이너를 시작합니다.

```bash
docker run -d -p 8080:8080 --name springboot-container springboot-app
```

이 명령어는 8080 포트로 애플리케이션을 실행하는 Docker 컨테이너를 생성합니다.

<br>

④ 컨테이너 상태 확인

실행 중인 컨테이너를 확인합니다.

```bash
docker ps
```

⑤ 컨테이너 중지 및 삭제

컨테이너를 중지하고 삭제하려면 다음 명령어를 사용합니다.

```bash
docker stop springboot-container
docker rm springboot-container
```

<br><br><br>

# 5. Jenkins(젠킨스)
Jenkins는 오픈 소스 자동화 서버로, 소프트웨어 개발 파이프라인을 자동화하는 데 널리 사용됩니다. 특히 CI(Continuous Integration, 지속적 통합) 및 CD(Continuous Deployment, 지속적 배포) 프로세스를 구축하는 데 필수적인 도구입니다. Jenkins를 통해 코드를 자동으로 빌드하고 테스트하며 배포할 수 있습니다.

<br>

## 5.1 Jenkins 설치 및 기본 설정

### 5.1.1 Jenkins 설치
Ubuntu를 기준으로 Jenkins 설치 과정을 설명합니다. Jenkins는 공식적으로 패키지 관리자를 통해 설치할 수 있으며, 다음 단계를 따르면 됩니다.

① Java 설치
Jenkins는 Java로 개발되었기 때문에 Java 11 이상이 필요합니다.

```bash
sudo apt update
sudo apt install openjdk-11-jdk
```

<br>

② Jenkins 저장소 추가
Jenkins 패키지를 설치하기 위해 Jenkins 저장소를 시스템에 추가합니다.

```bash
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
```

<br>

③ Jenkins 설치
패키지 목록을 업데이트한 후 Jenkins를 설치합니다.

```bash
sudo apt update
sudo apt install jenkins
```

<br>

④ Jenkins 실행
설치가 완료되면 Jenkins를 실행하고 상태를 확인합니다.

```bash
sudo systemctl start jenkins
sudo systemctl status jenkins
```

Jenkins는 기본적으로 서버의 8080 포트에서 실행됩니다. 웹 브라우저에서 http://<서버IP>:8080으로 접속하여 Jenkins 대시보드에 접근할 수 있습니다.

<br>

⑤ 초기 설정
웹 브라우저에 http://<서버IP>:8080을 입력하여 Jenkins 대시보드에 접근합니다.
초기 화면에서 /var/lib/jenkins/secrets/initialAdminPassword 파일에 있는 초기 관리자 비밀번호를 입력해야 합니다.

```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

<br>

Jenkins 플러그인을 설치합니다. 기본 추천 플러그인을 설치하는 것이 일반적입니다.
관리자 계정을 생성합니다.

이 과정을 마치면 Jenkins 대시보드를 사용할 수 있습니다.

<br><br>

## 5.2 간단한 CI 파이프라인 구축 실습
Jenkins에서 간단한 CI(지속적 통합) 파이프라인을 구성하는 방법을 설명합니다. 이 파이프라인은 코드가 변경될 때마다 자동으로 빌드, 테스트, 배포하는 과정을 자동화합니다.

<br>

### 5.2.1 Jenkins 파이프라인 개요
Jenkins 파이프라인은 Jenkins에서 정의된 스크립트를 통해 빌드, 테스트, 배포 과정을 자동화하는 방식입니다. Jenkins 파이프라인은 선언형(Declarative) 또는 스크립트형(Scripted)으로 작성할 수 있으며, 주로 Jenkinsfile이라는 파일에 정의됩니다.

①  Jenkins 파이프라인 설정 절차
1) 새로운 파이프라인 생성
Jenkins 대시보드에서 **New Item(새 항목)**을 클릭합니다.
**Pipeline(파이프라인)**을 선택하고 프로젝트 이름을 입력한 후 확인 버튼을 누릅니다.
프로젝트 설정 페이지에서 Pipeline 섹션으로 이동합니다.

<br>

② Jenkinsfile 작성
아래는 GitHub에서 소스를 가져와서 빌드하고 테스트하는 간단한 Jenkins 파이프라인 예시입니다.

```groovy
pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/username/repository.git'
            }
        }

        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }

        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        success {
            echo 'Build and tests completed successfully.'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}
```

agent any: Jenkins가 사용할 노드를 정의하며, 이 경우에는 어떤 노드에서든 파이프라인을 실행할 수 있도록 합니다.
stages: 각 단계는 파이프라인의 여러 과정(예: Clone, Build, Test, Deploy)을 나타냅니다.
Clone: GitHub에서 소스 코드를 클론합니다.
Build: Gradle을 사용하여 프로젝트를 빌드합니다.
Test: Gradle을 사용하여 테스트를 실행합니다.
Deploy: 애플리케이션을 배포합니다. 여기서는 간단하게 echo 명령으로 대체하였지만, 실제 배포 스크립트를 넣을 수 있습니다.
post: 빌드 성공 또는 실패 후 실행되는 작업을 정의합니다.

<br>

③ 파이프라인 실행
Jenkins 대시보드에서 생성한 파이프라인 프로젝트를 클릭합니다.
Build Now(지금 빌드) 버튼을 클릭하여 파이프라인을 실행할 수 있습니다.
Jenkins는 GitHub에서 소스 코드를 가져와 빌드하고, 테스트한 후 배포 단계로 넘어갑니다.

<br>

④ 결과 확인
빌드가 성공적으로 완료되면 각 단계의 로그를 확인할 수 있습니다. Jenkins는 각 단계의 상태를 기록하고, 문제가 발생한 경우 어느 단계에서 실패했는지를 쉽게 추적할 수 있습니다.

<br><br><br>

# 6. AWS
AWS(Amazon Web Services)는 클라우드 컴퓨팅 서비스를 제공하는 세계적인 플랫폼입니다. 이 장에서는 AWS의 EC2와 로드밸런서를 중심으로 학습하며, 애플리케이션의 확장성과 가용성을 높이는 방법에 대해 알아봅니다.

<br>

## 6.1 EC2 컨테이너 서비스 학습
EC2(Elastic Compute Cloud)는 AWS에서 제공하는 가상 서버입니다. EC2 인스턴스를 통해 클라우드 환경에서 애플리케이션을 실행할 수 있습니다. 또한, AWS에서는 Docker와 컨테이너 기반 애플리케이션을 EC2에서 실행할 수 있도록 **Amazon ECS(Elastic Container Service)**를 제공합니다. Amazon ECS는 컨테이너화된 애플리케이션을 쉽게 배포, 관리할 수 있는 완전 관리형 컨테이너 오케스트레이션 서비스입니다.

### 6.1.1 EC2 컨테이너 서비스(ECS)의 주요 개념
EC2 인스턴스: AWS 클라우드에서 실행되는 가상 서버.
Docker 컨테이너: 애플리케이션과 그 의존성을 격리된 환경에서 실행할 수 있는 경량화된 환경.
ECS 클러스터: ECS에서 컨테이너가 실행되는 EC2 인스턴스의 그룹. 클러스터 안에서 컨테이너를 실행하고 관리합니다.
태스크 정의(Task Definition): 컨테이너를 어떻게 실행할 것인지 정의한 템플릿. CPU, 메모리, 네트워킹 등을 설정합니다.
서비스(Service): 여러 개의 컨테이너를 실행하거나 배포하는 기능. ECS 서비스는 필요한 만큼의 컨테이너를 유지하도록 관리합니다.

<br>

### 6.1.2 EC2 컨테이너 서비스 설정 절차

① ECS 클러스터 생성
AWS Management Console에 로그인 후 ECS 서비스를 검색하여 선택합니다.
Create Cluster 버튼을 클릭하여 새로운 ECS 클러스터를 생성합니다.
EC2 기반 클러스터를 선택하고 설정합니다.

② 태스크 정의(Task Definition) 생성
ECS 대시보드에서 Task Definitions를 선택합니다.
Create new Task Definition을 클릭하고, 태스크 정의를 만듭니다.
컨테이너의 이미지, CPU, 메모리, 포트 등을 설정합니다.

③ 서비스 생성 및 실행
Services에서 Create Service를 선택합니다.
원하는 태스크 정의를 선택하고, 서비스의 인스턴스 수, 로드 밸런싱 설정 등을 지정합니다.
ECS는 서비스가 항상 실행 상태를 유지하도록 관리합니다.

④ ECS에서 Docker 컨테이너 실행
ECS 클러스터에서 지정된 컨테이너가 EC2 인스턴스에서 실행되며, 관리되는 환경에서 확장성과 가용성을 보장받습니다.

<br><br>

## 6.2 로드밸런서 학습
로드 밸런서는 여러 서버로부터 트래픽을 분산 처리하여 애플리케이션의 성능을 최적화하고 가용성을 높여주는 장치입니다. AWS에서는 **Elastic Load Balancing(ELB)**이라는 관리형 로드 밸런서를 제공합니다. ELB는 들어오는 트래픽을 여러 EC2 인스턴스나 ECS 컨테이너에 자동으로 분산시켜 고가용성을 보장합니다.

### 6.2.1 로드 밸런서의 종류
Application Load Balancer(ALB): HTTP/HTTPS 트래픽에 최적화된 로드 밸런서로, URL 경로와 호스트 이름에 따라 트래픽을 분산할 수 있습니다.
Network Load Balancer(NLB): 네트워크 레벨에서 매우 빠른 성능을 제공하며, TCP 트래픽을 분산 처리합니다.
Classic Load Balancer(CLB): 구형 로드 밸런서로, TCP와 HTTP 트래픽을 처리할 수 있지만 최신 기능은 ALB와 NLB에서 지원됩니다.

<br>

### 6.2.2 로드 밸런서의 주요 기능
자동 스케일링 지원: 로드 밸런서는 EC2 인스턴스의 수에 관계없이 트래픽을 분산 처리합니다.
헬스 체크(Health Check): 연결된 인스턴스나 컨테이너의 상태를 주기적으로 확인하여, 정상 상태의 인스턴스로만 트래픽을 전달합니다.
보안: HTTPS를 통해 안전한 통신을 제공하며, IAM과 통합되어 SSL 인증서를 쉽게 적용할 수 있습니다.

<br>

### 6.2.3 로드 밸런서 설정 절차
① 로드 밸런서 생성
AWS Management Console에서 EC2 서비스로 이동하고 Load Balancers 메뉴를 선택합니다.
Create Load Balancer를 클릭하고 원하는 로드 밸런서 타입을 선택합니다 (예: Application Load Balancer).
로드 밸런서 이름, 네트워크 설정, 보안 그룹 등을 설정합니다.

② 대상 그룹(Target Group) 생성
로드 밸런서가 트래픽을 전달할 대상 인스턴스를 지정하기 위해 Target Group을 생성합니다.

Create Target Group을 클릭하여 대상 그룹을 생성합니다.
대상 그룹에 EC2 인스턴스나 ECS 컨테이너를 추가합니다.
헬스 체크 기준을 설정합니다.

③ 로드 밸런서와 대상 그룹 연결
생성한 로드 밸런서를 대상으로 트래픽이 전달되도록 설정합니다.
Listeners 설정에서 HTTP, HTTPS 등 프로토콜과 포트를 지정하고, 요청이 대상 그룹으로 라우팅되도록 설정합니다.

④ 헬스 체크 설정
대상 그룹의 헬스 체크 설정을 구성하여, 로드 밸런서가 트래픽을 전달하기 전에 인스턴스나 컨테이너의 상태를 확인합니다.
헬스 체크에 실패한 인스턴스는 자동으로 트래픽 대상에서 제외되며, 상태가 회복되면 다시 트래픽을 받을 수 있습니다.

