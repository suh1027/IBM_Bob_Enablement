# IBM Bob Hands-on Lab 01

# IBM Bob 설치 및 프로젝트 초기 구성

> **실습 목표**
> 
> 
> IBM Bob을 설치하고 기본 화면과 실행 권한을 확인한 뒤, 실습용 `Menu.html` 파일을 로컬 프로젝트로 가져와 Bob IDE에서 열고 `/init` 명령으로 프로젝트 Context를 초기화합니다.
> 
> **예상 시간:** 약 30분
> 

---

## Lab 01 에서 할 일

```
Bob 계정 / Trial 준비
        ↓
IBM Bob IDE 설치
        ↓
Bob IDE 기본 화면 확인
        ↓
Mode / Permission 확인
        ↓
로컬 프로젝트 폴더 구성
        ↓
Menu.html 다운로드
        ↓
Bob IDE에서 프로젝트 열기
        ↓
/init 실행
        ↓
AGENTS.md 확인
```

### 이번 Lab에서 기억할 것

1. **Bob IDE**는 프로젝트를 열고 AI Agent와 함께 개발 작업을 수행하는 개발 환경입니다.
2. **Mode**는 Bob에게 어떤 형태의 작업을 요청할지 구분합니다.
3. **Permission**은 파일 수정이나 명령 실행을 어디까지 자동으로 허용할지 결정합니다.
4. **`/init`**은 현재 프로젝트를 분석해 Bob이 이후 작업에서 참고할 프로젝트 Context를 초기화합니다.

---

# 1. 사전 준비

실습 전에 아래 항목을 확인합니다.

- 인터넷 연결
- IBM Bob에 로그인할 계정

### 권장 환경

- Windows / macOS / Linux
- 최소 4 GB RAM
- 8 GB RAM 이상 권장
- 최소 500 MB 이상의 여유 디스크

---

# 2. IBM Bob 계정 및 Trial 준비

IBM Bob을 처음 사용하는 경우 Bob 웹사이트에서 로그인 또는 Trial 등록을 진행합니다.

- Bob 로그인: [https://bob.ibm.com/login](https://bob.ibm.com/login)
- Bob Trial: [https://bob.ibm.com/ko/trial](https://bob.ibm.com/ko/trial)

교육에서는 Google 또는 GitHub 계정을 이용해 Trial 등록을 진행할 수 있습니다.

---

# 3. IBM Bob IDE 설치

## Step 1. Bob 다운로드 페이지 접속

IBM Bob 다운로드 페이지로 이동합니다.

**다운로드 링크**

[https://bob.ibm.com/ko/download](https://bob.ibm.com/ko/download)

IBM Bob 다운로드 화면

사용 중인 운영체제에 맞는 **Bob IDE**를 다운로드합니다.

- Windows: 설치 파일 다운로드
- macOS: macOS용 설치 파일 다운로드
- Linux: Linux용 설치 방식 사용

> 이번 Hands-on에서는 **Bob IDE**를 사용합니다.
> 
> 
> Bob Shell은 별도 기능이므로 이번 Lab에서는 설치하지 않아도 됩니다.
> 

---

## Step 2. Bob IDE 설치

Windows 기준:

1. 다운로드한 설치 파일 실행
2. 설치 Wizard 진행
3. 특별한 요구사항이 없다면 기본 설치 경로 사용
4. 설치 완료 후 **IBM Bob IDE 실행**

### 완료 확인

Bob IDE가 정상적으로 실행되면 다음 단계로 이동합니다.

---

# 4. Bob IDE 기본 화면 확인

Bob IDE를 처음 실행한 뒤 화면 구성을 간단하게 확인합니다.

| 영역 | 역할 |
| --- | --- |
| **Explorer** | 현재 프로젝트의 파일과 폴더 확인 |
| **Editor** | 소스코드 및 파일 확인 |
| **Bob Chat** | Bob에게 분석, 계획, 수정 작업 요청 |
| **Mode / Permission** | Bob의 작업 방식과 실행 권한 설정 |

---

# 5. Mode와 Permission 확인

아직 실제 코드를 수정하지 않고, 화면에서 기능 위치와 의미만 확인합니다.

## 5-1. Mode

Bob Chat 하단에서 사용할 수 있는 Mode를 확인합니다.

### Ask

프로젝트와 코드에 대해 **질문하거나 분석**할 때 사용합니다.

예:

```
이 프로젝트의 구조를 설명해줘.
```

### Plan

실제 구현 전에 **어떤 파일을 어떻게 변경할지 계획**을 확인할 때 사용합니다.

예:

```
이 기능을 수정하려면 어떤 작업이 필요한지 계획만 작성해줘.
```

### Agent

Bob이 **실제 파일을 수정하거나 명령을 실행**해야 할 때 사용합니다.

이번 Lab에서는 `/init` 실행 시 Agent Mode를 사용합니다.

---

## 5-2. Permission

Bob Chat의 **Permission** 설정을 확인합니다.

Permission은 Bob이 파일 수정이나 명령 실행을 제안했을 때 자동으로 실행할지, 개발자에게 승인을 요청할지를 결정합니다.

### 권장 방식

| 작업 | 권장 설정 |
| --- | --- |
| 파일 읽기 | Auto-Approve 허용 가능 |
| 파일 수정 / 생성 | 개발자 확인 후 승인 |
| 명령 실행 | 개발자 확인 후 승인 |
| 외부 Tool | 필요한 경우에만 승인 |

> **실습 포인트**
> 
> 
> Bob에게 모든 권한을 주는 것이 목적이 아닙니다.
> 
> 처음에는 파일 변경과 명령 실행 내용을 직접 확인하면서 Bob이 어떤 작업을 수행하는지 익히는 것이 좋습니다.
> 

---

# 6. 로컬 프로젝트 폴더 구성

실습 폴더를 다음과 같이 구성합니다.

Windows 예시:

```
C:\IBM-Bob-Lab\
└── Menu.html
```

복잡한 프로젝트를 사용하지 않는 이유는 Lab 01에서는 코드 구현보다 **Bob 설치, 프로젝트 열기, Context 초기화 과정**에 집중하기 위해서입니다.

---

# 7. 실습용 `Menu.html` 다운로드

이번 Hands-on에서는 간단한 Café 웹페이지인 `Menu.html`을 사용합니다.

이 파일 하나에 HTML, CSS, JavaScript가 함께 포함되어 있어 별도의 패키지 설치 없이 실습할 수 있습니다.

### 실습 파일

GitHub:

[https://github.com/suh1027/IBM_Bob_Enablement/tree/main/Lab_1/file](https://github.com/suh1027/IBM_Bob_Enablement/tree/main/Lab_1/file)

사용할 파일:

```
Menu.html
```

---

## 방법 A. GitHub에서 직접 다운로드

1. GitHub에서 `Menu.html`을 엽니다.
2. **Raw** 또는 **Download raw file**을 선택합니다.
3. 파일명을 `Menu.html`로 저장합니다.

> 첫 번째 Lab에서는 Git 명령 자체가 학습 목표가 아니므로 가장 단순한 이 방법을 권장합니다.
> 

---

## 방법 B. PowerShell에서 파일 다운로드

Windows PowerShell을 사용하는 경우 아래와 같이 하나의 파일만 내려받을 수도 있습니다.

먼저 실습 폴더를 생성합니다.

```powershell
mkdir C:\IBM-Bob-Lab
cd C:\IBM-Bob-Lab
```

이후 `Menu.html`의 Raw URL을 사용해 파일을 다운로드합니다.

```powershell
Invoke-WebRequest `
  -Uri "https://raw.githubusercontent.com/suh1027/IBM_Bob_Enablement/main/Lab_1/file/Menu.html" `
  -OutFile "Menu.html"
```

다운로드 결과를 확인합니다.

```powershell
dir
```

다음 파일이 보이면 정상입니다.

```
Menu.html
```

---

# 8. Bob IDE에서 프로젝트 열기

1. IBM Bob IDE 실행
2. **Open Folder** 선택
3. `C:\IBM-Bob-Lab` 폴더 선택
4. Explorer에서 `Menu.html` 확인

### 확인 포인트

- Bob IDE가 `IBM-Bob-Lab` 폴더를 Workspace로 열었는가?
- Explorer에 `Menu.html`이 표시되는가?

> 파일 자체를 하나만 여는 것이 아니라 **`IBM-Bob-Lab` 폴더 전체를 Workspace로 여는 것**이 중요합니다.
> 

---

# 9. `/init`으로 프로젝트 초기화

이제 Bob에게 현재 프로젝트를 먼저 파악하도록 합니다.

## `/init`이란?

`/init`은 현재 프로젝트를 분석하고 Bob이 이후 작업에서 참고할 프로젝트 정보를 초기화하는 명령입니다.

쉽게 표현하면:

> **`/init` = “이 프로젝트가 어떤 구조이고 어떤 기준으로 작업해야 하는지 먼저 파악해 둬.”**
> 

Bob은 프로젝트 파일과 구조를 확인하고 이후 작업에서 참고할 `AGENTS.md` 등의 Context 파일을 생성하거나 갱신할 수 있습니다.

---

## Step 1. Agent Mode 선택

Bob Chat 하단에서 **Agent Mode**를 선택합니다.

`/init` 과정에서는 프로젝트 파일을 읽고 Context 파일을 생성해야 하므로 파일 생성 권한이 필요할 수 있습니다.

---

## Step 2. `/init` 실행

Bob Chat에 아래 명령을 입력합니다.

```
/init
```

Bob이 파일 읽기 또는 파일 생성을 요청하면 수행할 내용을 확인한 뒤 승인합니다.

> **강사 포인트**
> 
> 
> 여기서 바로 승인 버튼을 누르기보다 “Bob이 어떤 파일을 읽고 무엇을 생성하려고 하는지” 참가자가 한 번 확인하도록 합니다.
> 
> Session 1에서 설명한 **Human-in-the-Loop**를 실제로 경험하는 첫 지점입니다.
> 

---

# 10. 생성된 Context 파일 확인

`/init`이 완료되면 Explorer에서 새롭게 생성된 파일을 확인합니다.

환경이나 Bob 버전에 따라 생성되는 파일 구조는 달라질 수 있습니다.

예:

```
IBM-Bob-Lab/
├── Menu.html
├── AGENTS.md
└── .bob/
    └── ...
```

핵심은 정확히 같은 폴더 구조를 만드는 것이 아니라, **Bob이 프로젝트를 분석한 뒤 이후 작업에서 참고할 Context를 구성했다는 것**입니다.

---

# 11. `AGENTS.md` 확인

생성된 `AGENTS.md`를 열어 내용을 확인합니다.

이번 프로젝트는 `Menu.html` 하나로 구성되어 있기 때문에 구조는 단순합니다.

아래 내용을 중심으로 살펴봅니다.

- 프로젝트가 웹페이지 프로젝트임을 인식했는가?
- 주요 파일로 `Menu.html`을 인식했는가?
- HTML, CSS, JavaScript 구성을 파악했는가?
- 이후 Bob이 참고할 프로젝트 설명이나 작업 기준이 작성되어 있는가?

---

# 12. 실습 — Bob에게 프로젝트 설명 요청

시간이 남는 경우 Ask Mode로 전환하고 아래 질문을 입력합니다.

```
현재 프로젝트의 구조와 Menu.html의 역할을 간단하게 설명해줘.
아직 코드는 수정하지 마.
```

### 확인할 내용

- Bob이 `Menu.html`을 정상적으로 인식하는가?
- 현재 프로젝트의 구조를 설명할 수 있는가?
- 코드를 변경하지 않고 분석만 수행하는가?

> 이 단계는 다음 Lab에서 진행할 **Ask → Plan → Agent → Verify** 흐름을 미리 경험하기 위한 선택 실습입니다.
> 

---

# 13. Lab 01 완료 확인

아래 항목이 모두 완료되면 Lab 01이 끝납니다.

- [ ]  Bob 로그인 / Trial 확인
- [ ]  IBM Bob IDE 설치
- [ ]  Bob IDE 기본 화면 확인
- [ ]  Ask / Plan / Agent Mode 확인
- [ ]  Permission 위치 확인
- [ ]  `Menu.html` 다운로드
- [ ]  `IBM-Bob-Lab` 로컬 폴더 구성
- [ ]  Bob IDE에서 프로젝트 Open
- [ ]  Agent Mode에서 `/init` 실행
- [ ]  `AGENTS.md` 등 Context 파일 확인

---

# 14. Lab 01 정리

이번 Lab에서는 아직 코드의 오류를 찾거나 수정하지 않았습니다.

먼저 Bob과 개발 작업을 수행하기 위한 기본 환경을 준비했습니다.

```
개발 환경 준비
      ↓
기존 소스 가져오기
      ↓
Bob에서 프로젝트 열기
      ↓
프로젝트 Context 초기화
```

### 핵심 메시지

> **Bob을 사용하는 개발은 바로 코드를 수정하는 것에서 시작하지 않습니다.**
> 
> 
> 먼저 프로젝트를 열고, Bob이 프로젝트 구조와 Context를 이해할 수 있도록 준비한 뒤 실제 분석과 구현 작업을 시작합니다.
> 

---

# 참고 자료

- IBM SkillsBuild — Use IBM Bob to Troubleshoot Your Code
    
    [https://github.com/academic-initiative/skillsbuild/blob/main/ibm-bob/troubleshoot-your-code/troubleshoot-your-code.md](https://github.com/academic-initiative/skillsbuild/blob/main/ibm-bob/troubleshoot-your-code/troubleshoot-your-code.md)
    
- IBM SkillsBuild — Menu.html
    
    [https://github.com/academic-initiative/skillsbuild/blob/main/ibm-bob/troubleshoot-your-code/file/Menu.html](https://github.com/academic-initiative/skillsbuild/blob/main/ibm-bob/troubleshoot-your-code/file/Menu.html)
    
- IBM Bob Download
    
    [https://bob.ibm.com/ko/download](https://bob.ibm.com/ko/download)
    
- IBM Bob Login
    
    [https://bob.ibm.com/login](https://bob.ibm.com/login)
    
- IBM Bob Trial
    
    [https://bob.ibm.com/ko/trial](https://bob.ibm.com/ko/trial)
    
- IBM Bob Docs
    
    [https://bob.ibm.com/ko/docs](https://bob.ibm.com/ko/docs)