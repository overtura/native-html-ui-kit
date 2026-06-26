# Native HTML UI Kit

popover, details, command/commandfor, dialog, form validation 같은 브라우저 네이티브 기능만으로 구성하는 no-JS UI kit입니다. 앱 런타임에는 JavaScript를 넣지 않습니다.

## 목적
- 프레임워크 없이 native HTML interaction 패턴을 축적한다.
- 최신 HTML 기능의 사용성과 fallback을 한국어 예제로 검증한다.
- self-improving bot이 컴포넌트 예제, 문서, workflow 개선을 자동 PR로 제안하고 merge한다.

## 사용자 flow
1. 메뉴, form, dialog, accordion 예제를 확인한다.
2. 브라우저 기본 validation과 popover 동작을 확인한다.
3. 후속 PR에서 컴포넌트와 fallback 문서를 확장한다.

## 실행 방법
```bash
pnpm install
pnpm dev
```

## 검증
```bash
pnpm check
```

`pnpm check`는 source와 build output 모두에서 런타임 JavaScript가 없는지 검사한다.

## 자가 개선
```bash
pnpm self-improve:context
pnpm self-improve:guard
```

## 디자인 시스템
- 기준 문서: `DESIGN.md`
- 실행 토큰: `design-system/base.css`
- 참고 기록: `docs/design/`

## 범위 밖
- 런타임 JavaScript
- framework 컴포넌트 라이브러리
- 실제 secret 또는 credential 저장
