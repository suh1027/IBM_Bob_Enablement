# Session 2-1. Lab 1 — IBM Bob 설치 및 프로젝트 초기 구성

> **실습 목표**  
> IBM Bob을 설치하고 기본 설정을 확인한 뒤, 기존 `Menu.html` 예제 파일을 로컬 프로젝트로 가져와 Bob에서 열고 `/init` 명령으로 프로젝트 Context를 초기화합니다.
>
> **예상 시간:** 약 30분  
> **난이도:** 입문  
> **다음 Lab 연결:** Lab 2에서 동일한 `Menu.html`을 사용해 오류 분석 → 계획 → 수정 → 검증을 진행합니다.

---

## 0. Lab 구성

이번 Lab에서는 코드를 수정하지 않습니다.

```text
IBM Bob 설치
    ↓
IBMid 로그인
    ↓
기본 Permission 확인
    ↓
Menu.html 다운로드
    ↓
로컬 프로젝트 폴더 생성
    ↓
Bob IDE에서 프로젝트 열기
    ↓
/init 실행
    ↓
AGENTS.md 확인
```

### 이 Lab에서 기억할 것

1. **Bob IDE**는 개발 프로젝트를 열고 AI Agent와 함께 작업하는 개발 환경입니다.
2. **Permission**은 Bob에게 어떤 작업을 자동으로 허용할지 결정합니다.
3. **`/init`**은 현재 프로젝트를 분석해 Bob이 지속적으로 참고할 프로젝트 Context를 생성합니다.

---

# 1. 사전 준비

실습 전에 아래 항목을 확인합니다.

- 인터넷 연결
- IBMid
- IBM Bob 사용 권한
- IBM Bob 설치가 가능한 PC
- GitHub 접속 가능

### IBM Bob 권장 환경

- Windows / macOS / Linux
- 최소 4 GB RAM
- 8 GB RAM 이상 권장
- 최소 500 MB의 여유 디스크

> 교육 환경에서는 설치 문제를 줄이기 위해 IBMid 생성과 Bob 사용 권한을 교육 전에 확인하는 것을 권장합니다.

---

# 2. IBM Bob 설치

## Step 1. IBM Bob 다운로드

IBM Bob 공식 설치 페이지에서 사용 중인 운영체제에 맞는 설치 파일을 다운로드합니다.

**IBM Bob 설치 문서**

https://bob.ibm.com/docs/ide/getting-started/install

Windows 환경에서는 `.exe` 설치 파일을 다운로드합니다.

---

## Step 2. IBM Bob 설치

다운로드한 설치 프로그램을 실행합니다.

Windows 기준:

1. 다운로드한 `.exe` 파일 실행
2. 설치 Wizard 진행
3. 특별한 요구사항이 없다면 기본 설치 경로 사용
4. 설치 완료 후 IBM Bob 실행

### 완료 확인

IBM Bob IDE가 정상적으로 실행되면 다음 단계로 이동합니다.

---

# 3. IBMid 로그인

IBM Bob을 처음 실행하면 IBMid 인증을 요청합니다.

1. **Sign in** 선택
2. 브라우저에서 IBMid 로그인
3. 인증 완료
4. IBM Bob IDE로 돌아오기

### 완료 확인

Bob IDE가 열리고 Bob Chat을 사용할 수 있으면 정상입니다.

---

# 4. 기본 Permission 확인

코드를 수정하기 전에 Bob의 실행 권한을 간단하게 확인합니다.

Bob Chat 하단의 **Permissions** 메뉴를 확인합니다.

이번 교육에서는 처음부터 모든 작업을 자동 승인하지 않습니다.

### 교육용 권장 설정

| 작업 | 권장 설정 |
|---|---|
| Read | Auto-Approve 허용 |
| Edit / Write | 개발자 승인 |
| Execute | 개발자 승인 |
| 기타 외부 Tool | 필요 시 승인 |

> **실습 포인트**  
> Bob에게 모든 권한을 주는 것이 목적이 아닙니다.  
> 읽기 작업은 편리하게 허용하되, 실제 파일 변경이나 명령 실행은 개발자가 확인하는 방식으로 시작합니다.

---

# 5. 실습용 HTML 파일 다운로드

이번 Hands-on에서는 IBM SkillsBuild의 **Use IBM Bob to Troubleshoot Your Code** 예제에서 사용하는 `Menu.html` 파일을 사용합니다.

이 파일은 HTML, CSS, JavaScript가 하나의 파일에 포함된 간단한 Café 웹페이지입니다.

### 원본 예제

**Troubleshoot Your Code Lab**

https://github.com/academic-initiative/skillsbuild/blob/main/ibm-bob/troubleshoot-your-code/troubleshoot-your-code.md

**Menu.html**

https://github.com/academic-initiative/skillsbuild/blob/main/ibm-bob/troubleshoot-your-code/file/Menu.html

---

## Step 1. Menu.html 다운로드

GitHub에서 `Menu.html` 파일을 엽니다.

1. `Menu.html` 페이지 접속
2. **Raw** 또는 **Download raw file** 선택
3. 파일을 PC에 저장

파일명은 다음과 같이 유지합니다.

```text
Menu.html
```

> **주의**  
> 아직 코드의 오류를 찾거나 수정하지 않습니다.  
> 동일한 파일을 다음 Lab에서 Troubleshooting 실습에 사용합니다.

---

# 6. 로컬 프로젝트 폴더 구성

실습용 폴더를 하나 생성합니다.

Windows 예시:

```text
C:\IBM-Bob-Lab\
```

폴더 안에 다운로드한 `Menu.html`을 이동합니다.

최초 상태는 다음과 같이 매우 단순합니다.

```text
IBM-Bob-Lab/
└── Menu.html
```

> 복잡한 프로젝트를 사용하지 않는 이유는 첫 번째 Lab에서 Bob 설치와 프로젝트 초기화 과정 자체에 집중하기 위해서입니다.

---

# 7. Bob IDE에서 프로젝트 열기

IBM Bob IDE에서 방금 만든 프로젝트 폴더를 엽니다.

1. Bob IDE 실행
2. **Open Folder** 선택
3. `IBM-Bob-Lab` 폴더 선택
4. Explorer에서 `Menu.html`이 표시되는지 확인

예상 구조:

```text
IBM-Bob-Lab/
└── Menu.html
```

### 확인 포인트

- Bob IDE가 올바른 폴더를 Workspace로 열었는가?
- Explorer에 `Menu.html`이 보이는가?

---

# 8. `/init`으로 Bob 프로젝트 초기화

이제 Bob에게 현재 프로젝트의 Context를 생성하도록 합니다.

## `/init`이란?

`/init`은 현재 프로젝트를 스캔하고 **`AGENTS.md`** 파일을 생성하는 Bob의 초기화 명령입니다.

`AGENTS.md`에는 Bob이 이후 작업에서 참고할 수 있도록 프로젝트 구조, 기술 구성, 개발 규칙 등의 Context가 정리됩니다.

즉, 쉽게 말하면:

> **`/init` = Bob에게 “이 프로젝트가 어떤 프로젝트인지 먼저 파악해 둬”라고 하는 초기화 작업**

---

## Step 1. Agent Mode 선택

Bob Chat 하단에서 **Agent Mode**를 선택합니다.

> `/init`은 프로젝트 파일을 읽고 `AGENTS.md` 파일을 생성해야 하므로 파일 생성 권한이 필요합니다.

---

## Step 2. `/init` 실행

Bob Chat에 아래 명령을 입력합니다.

```text
/init
```

Bob이 프로젝트 파일을 읽거나 파일 생성을 요청하면 내용을 확인한 후 승인합니다.

---

## Step 3. 생성 결과 확인

`/init` 실행이 완료되면 프로젝트에 `AGENTS.md`와 `.bob` 관련 파일이 생성됩니다.

예상 구조는 다음과 같습니다.

```text
IBM-Bob-Lab/
├── Menu.html
├── AGENTS.md
└── .bob/
    ├── rules-code/
    │   └── AGENTS-code.md
    ├── rules-plan/
    │   └── AGENTS-plan.md
    └── rules-ask/
        └── AGENTS-ask.md
```

> Bob 버전에 따라 생성 구조나 명칭은 달라질 수 있습니다.  
> 핵심은 루트의 `AGENTS.md`와 각 Mode에서 사용할 프로젝트 Context가 생성되는지 확인하는 것입니다.

---

# 9. AGENTS.md 확인

생성된 `AGENTS.md`를 열어봅니다.

이번 프로젝트는 `Menu.html` 하나로 구성되어 있기 때문에 내용은 복잡하지 않습니다.

확인할 내용:

- 프로젝트가 HTML 기반 웹페이지임을 인식했는가?
- CSS와 JavaScript가 HTML 내부에 포함되어 있음을 파악했는가?
- 주요 파일로 `Menu.html`을 인식했는가?

### 강사 설명

`AGENTS.md`는 개발자를 위한 README라기보다 **Bob이 프로젝트를 이해하기 위한 지속적인 Context 문서**라고 설명하면 쉽습니다.

새로운 대화를 시작하더라도 Bob이 매번 프로젝트 전체를 처음부터 파악하는 부담을 줄이고, 프로젝트의 구조와 규칙을 일관되게 참고할 수 있게 합니다.

---

# 10. Lab 1 완료 확인

아래 항목이 모두 완료되면 Lab 1이 끝납니다.

- [ ] IBM Bob 설치
- [ ] IBMid 로그인
- [ ] Permission 확인
- [ ] `Menu.html` 다운로드
- [ ] 로컬 프로젝트 폴더 생성
- [ ] Bob IDE에서 프로젝트 열기
- [ ] Agent Mode 선택
- [ ] `/init` 실행
- [ ] `AGENTS.md` 생성 확인

---

# 11. Lab 1 정리

이번 Lab에서는 아직 코드를 작성하거나 수정하지 않았습니다.

Bob과 개발을 시작하기 전에 다음 세 가지를 준비했습니다.

```text
개발 환경 준비
      ↓
기존 프로젝트 가져오기
      ↓
프로젝트 Context 초기화
```

### 핵심 메시지

> **Bob을 사용한 개발은 바로 코드를 수정하는 것에서 시작하지 않습니다.**  
> 먼저 프로젝트를 열고, Bob이 프로젝트 구조와 Context를 이해할 수 있도록 초기화한 뒤 실제 작업을 시작합니다.

---

# 12. 다음 Lab 예고 — Troubleshoot Your Code

Lab 2에서는 방금 준비한 동일한 `Menu.html` 파일을 그대로 사용합니다.

IBM SkillsBuild 원본 Lab의 Troubleshooting 시나리오를 기반으로 다음 흐름을 실습합니다.

```text
Ask
프로젝트와 오류 분석
    ↓
Plan
수정 계획 확인
    ↓
Agent
실제 코드 수정
    ↓
Verify
변경 결과 확인
```

원본 예제에는 웹페이지의 동작을 방해하는 몇 가지 문제가 포함되어 있습니다.

다음 Lab에서는 참가자가 직접 문제를 찾기보다 **Bob에게 구조적으로 분석을 요청하고, 결과를 검토한 뒤 수정 작업으로 연결하는 과정**을 경험합니다.

---

# 강사용 진행 가이드

## 권장 시간 배분 — 총 30분

| 구간 | 시간 |
|---|---:|
| Lab 소개 / 사전 확인 | 2분 |
| Bob 설치 | 7분 |
| IBMid 로그인 및 Permission 확인 | 4분 |
| `Menu.html` 다운로드 | 4분 |
| 로컬 폴더 생성 및 Bob에서 열기 | 4분 |
| `/init` 실행 | 5분 |
| `AGENTS.md` 설명 및 정리 | 4분 |
| **합계** | **30분** |

---

## 강사가 강조할 내용

### 1. 첫 Lab에서는 오류를 수정하지 않습니다

`Menu.html`에는 이후 Troubleshooting에서 사용할 문제가 포함되어 있습니다.

Lab 1에서 Bob에게 다음과 같은 요청은 하지 않습니다.

```text
이 코드의 오류를 찾아줘.
```

```text
이 파일을 수정해줘.
```

오류 분석과 수정은 Lab 2의 학습 목표입니다.

---

### 2. `/init`의 목적을 기술적으로 너무 어렵게 설명하지 않습니다

교육에서는 다음 정도로 설명하면 충분합니다.

> “Bob이 이후 작업에서 이 프로젝트를 계속 이해할 수 있도록 프로젝트 정보를 정리하는 과정입니다.”

---

### 3. AGENTS.md를 직접 수정하는 실습은 Lab 1에서 제외합니다

이번 Lab의 목적은 **설치와 초기 구성 경험**입니다.

Rules, Skills, Hooks 등의 세부 구성은 이후 실습에서 필요한 기능만 단계적으로 추가하는 것이 좋습니다.

---

# 참고 자료

- IBM SkillsBuild — Use IBM Bob to Troubleshoot Your Code  
  https://github.com/academic-initiative/skillsbuild/blob/main/ibm-bob/troubleshoot-your-code/troubleshoot-your-code.md

- IBM SkillsBuild — Menu.html  
  https://github.com/academic-initiative/skillsbuild/blob/main/ibm-bob/troubleshoot-your-code/file/Menu.html

- IBM Bob — Installing  
  https://bob.ibm.com/docs/ide/getting-started/install

- IBM Bob — Start a project with `/init` and `AGENTS.md`  
  https://bob.ibm.com/docs/ide/tutorials/start-a-project

- IBM Bob — Quickstart  
  https://bob.ibm.com/docs/ide/getting-started/quickstart
