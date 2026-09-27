# Carbon Design Project Rules

> **Purpose**  
> 이 문서는 Lab 02의 Café 웹페이지를 IBM Carbon Design System 기준으로 리디자인할 때 적용하는 프로젝트 전용 규칙입니다.  
> Lab 02에서는 이 파일을 **Workspace Rule**로 적용합니다.

---

## 1. Project Scope

- 현재 Café 웹페이지의 기존 콘텐츠와 메뉴 데이터는 유지한다.
- UI 구조와 스타일은 변경할 수 있지만, 기존 JavaScript 기능은 가능한 한 유지한다.
- 리디자인과 관계없는 비즈니스 로직은 수정하지 않는다.
- 새로운 Backend, Database 또는 별도 Framework는 추가하지 않는다.

---

## 2. Carbon Design Principles

- UI 변경 시 IBM Carbon Design System의 구성 원칙을 우선 참고한다.
- Button, Tile, Grid, UI Shell 등 Carbon Component로 표현 가능한 영역은 Carbon 패턴을 우선 검토한다.
- 임의의 색상 값을 반복해서 추가하기보다 Carbon의 Color Token과 디자인 체계를 우선 고려한다.
- Typography, Spacing, Alignment는 페이지 전체에서 일관되게 유지한다.
- Primary Action은 화면에서 명확하게 구분한다.

---

## 3. Layout

리디자인 시 아래 구조를 우선 고려한다.

1. Header / Navigation
2. Hero Section
3. Menu Section
4. About 또는 Café Information Section
5. Call-to-Action 또는 Footer

- Desktop과 Mobile 환경을 모두 고려한다.
- 작은 화면에서는 콘텐츠가 자연스럽게 한 열 구조로 배치되도록 한다.
- 불필요하게 복잡한 Layout이나 Animation은 추가하지 않는다.

---

## 4. Accessibility

- 이미지에는 의미 있는 `alt` 속성을 제공한다.
- Button과 Link의 목적이 텍스트만으로도 이해되도록 작성한다.
- Keyboard 사용자가 주요 기능을 사용할 수 있도록 기본 HTML 동작을 유지한다.
- 색상만으로 상태나 의미를 전달하지 않는다.
- 충분한 텍스트 대비를 유지한다.

---

## 5. Implementation Constraints

- 기존 파일 구조를 최대한 유지한다.
- Lab 환경에서는 HTML, CSS, JavaScript 중심으로 구현한다.
- 외부 Library나 Package 설치가 필요하면 먼저 사용자 승인을 요청한다.
- 기존 Café 메뉴와 텍스트 콘텐츠를 임의로 삭제하지 않는다.
- 요청하지 않은 기능 추가는 최소화한다.

---

## 6. Development Workflow

실제 파일을 수정하기 전에 다음 순서로 진행한다.

1. 현재 HTML 구조와 기존 기능을 분석한다.
2. Carbon Design System 기준에서 개선할 영역을 정리한다.
3. 수정할 HTML 구조와 CSS 변경 계획을 먼저 작성한다.
4. 사용자가 계획을 확인한 뒤 실제 코드를 수정한다.
5. 수정 후 기존 기능과 화면 동작을 검증한다.

---

## 7. Validation Checklist

작업 완료 후 아래 항목을 확인한다.

- [ ] 기존 메뉴 데이터가 유지되었는가?
- [ ] 기존 JavaScript 기능이 정상 동작하는가?
- [ ] Carbon Design 원칙이 UI에 반영되었는가?
- [ ] Desktop과 Mobile에서 레이아웃이 깨지지 않는가?
- [ ] 주요 Button과 Link가 정상 동작하는가?
- [ ] 접근성을 해치는 변경이 없는가?
- [ ] 리디자인과 관계없는 코드가 변경되지 않았는가?

---

## 8. Final Response

작업 완료 후 아래 내용을 설명한다.

1. 적용한 Carbon Design 요소
2. 변경한 HTML 구조
3. 변경한 스타일
4. 유지한 기존 기능
5. 검증 결과
