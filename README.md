# IBM Bob Enablement Hands-on Labs

IBM Bob의 주요 개발 워크플로를 직접 실습하기 위한 Hands-on Repository입니다.

총 3개의 Lab으로 구성되어 있으며, **설치 및 프로젝트 초기화 → Rules/Skills를 활용한 UI 재구성 및 검증 → 자율 웹페이지 구현** 순서로 진행합니다.

---

## Hands-on Labs

| Lab | 주제 | 주요 내용 | 가이드 |
|---|---|---|---|
| **Lab 1** | **설치와 시작** | IBM Bob IDE 설치, Mode/Permission 확인, 프로젝트 열기, `/init`, 프로젝트 Context 초기화 | [Lab 1 가이드](./Lab_1/IBM%20Bob%20Hands-on%20Lab%2001.md) |
| **Lab 2** | **UI 재구성** | Company Rules와 Carbon Builder Skill 적용, Ask/Plan/Agent를 활용한 UI 재구성, 브라우저 확인 및 `html-validate` 검증 | [Lab 2 가이드](./Lab_2/IBM%20Bob%20Hands-on%20Lab%2002.md) |
| **Lab 3** | **회원가입 페이지** | 요구사항을 바탕으로 `create-plan` Skill을 활용해 계획을 만들고, Agent Mode로 간단한 회원가입 페이지를 자유롭게 구현 | [Lab 3 가이드](./Lab_3/IBM%20Bob%20Hands-on%20Lab%2003.md) |

---

## 전체 실습 흐름

```text
Lab 1
IBM Bob 설치 및 프로젝트 준비
        ↓
Lab 2
Rules + Skills 기반 UI 재구성 및 검증
        ↓
Lab 3
요구사항 기반 자율 구현
```

각 Lab은 약 **30분**을 기준으로 구성되어 있습니다.

---

## Lab 1 — 설치와 시작

IBM Bob을 처음 사용하는 참가자를 위한 기본 실습입니다.

주요 내용:

- IBM Bob IDE 설치 및 실행
- Mode / Permission 확인
- 실습 프로젝트 구성
- `Menu.html` 가져오기
- Bob IDE에서 프로젝트 열기
- `/init` 실행
- `AGENTS.md`를 통한 프로젝트 Context 확인

➡️ [IBM Bob Hands-on Lab 01](./Lab_1/IBM%20Bob%20Hands-on%20Lab%2001.md)

---

## Lab 2 — UI 재구성

기업 내부 개발 규칙과 전문 Skill을 Bob 프로젝트에 적용하고, 기존 Café 웹페이지를 분석·계획·수정·검증합니다.

주요 내용:

- `company-standards.md` 적용
- Carbon Builder Skill 적용
- Ask Mode를 통한 기존 코드 분석
- Plan Mode를 통한 Visual Redesign 계획
- Agent Mode를 통한 실제 UI 수정
- 브라우저에서 결과 확인
- `html-validate`를 활용한 정적 검증
- 최초 요구사항 기준 최종 Verify

Lab 2에서 사용하는 추가 리소스:

```text
Lab_2/
├── company-rules/
│   └── company-standards.md
└── skills/
    └── carbon-builder/
        ├── SKILL.md
        └── references/
```

➡️ [IBM Bob Hands-on Lab 02](./Lab_2/IBM%20Bob%20Hands-on%20Lab%2002.md)

---

## Lab 3 — 회원가입 페이지

앞선 Lab에서 학습한 Plan과 Agent Workflow를 자유롭게 활용하는 자율 실습입니다.

간단한 회원가입 페이지를 주제로 요구사항을 해석하고, 구현 계획을 작성한 뒤 직접 기능을 완성합니다.

주요 내용:

- 회원가입 페이지 요구사항 확인
- Plan Mode에서 `create-plan` Skill 활용
- Plan 검토 및 자유로운 수정
- Agent Mode를 통한 HTML / CSS / JavaScript 구현
- 입력값 Validation
- Responsive Layout
- 브라우저 확인 및 추가 개선

> Lab 3는 정해진 구현 방식보다 **Bob을 어떻게 계획하고 활용할 것인지 직접 결정하는 것**에 초점을 둡니다.

➡️ [IBM Bob Hands-on Lab 03](./Lab_3/IBM%20Bob%20Hands-on%20Lab%2003.md)

---

## 권장 진행 순서

처음 실습하는 경우 아래 순서대로 진행하는 것을 권장합니다.

1. **Lab 1**에서 Bob IDE와 프로젝트 Context 구성 방법을 익힙니다.
2. **Lab 2**에서 Rules와 Skills를 적용해 기존 코드를 구조적으로 개선합니다.
3. **Lab 3**에서 요구사항만 가지고 Plan → Agent → 구현 과정을 자유롭게 수행합니다.

---

## 핵심 학습 포인트

이 Hands-on에서는 단순한 코드 생성을 넘어 다음 개발 흐름을 경험합니다.

```text
Analyze
   ↓
Plan
   ↓
Human Check
   ↓
Agent
   ↓
Validation
   ↓
Verify
```

- **Rules** — 조직에서 지켜야 하는 개발 기준
- **Skills** — 특정 작업을 수행하기 위한 전문 작업 지침
- **Plan** — 코드 변경 전 구현 방향과 영향 범위 정의
- **Agent** — 파일 수정 및 개발 도구 실행
- **Permission** — 실제 변경과 명령 실행에 대한 개발자 통제
- **Validation / Verify** — 코드와 최종 요구사항을 다시 확인

---

## Repository

- Repository: https://github.com/suh1027/IBM_Bob_Enablement
- IBM Bob: https://bob.ibm.com/

