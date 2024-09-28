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

<br><br><br>

# 2. Git/GitHub

`.gitignore` 는 버전관리가 필요하지 않은 부분의 설정 내용이 들어갑니다.

<br><br>

## 2.1 Git/GitHub 사용법

<br><br>

## 2.2 Git 협업 패턴

<br><br>

## 2.3 Git/GitHub 실습

<br><br><br>

# 3. 배포

<br><br>

## 3.1 배포 도구 소개

<br><br>

## 3.2 배포 스크립트 작성 및 실행 실습

<br><br><br>

# 4. Docker(도커)

<br><br>

## 4.1 도커 이미지

<br><br>

## 4.2 도커 엔진 설치

<br><br>

## 4.3 도커 컨테이너

<br><br>

## 4.4 Dockerfile

<br><br>

## 4.5 도커 컨테이너 및 Dockerfile 실습

<br><br><br>

# 5. Jenkins(젠킨스)

<br><br>

## 5.1 Jenkins 설치 및 기본 설정

<br><br>

## 5.2 간단한 CI 파이프라인 구축 실습

<br><br><br>

# 6. AWS 

<br><br>

## 6.1 EC2 컨테이너 서비스 학습

<br><br>

## 6.2 로드밸런서 학습

