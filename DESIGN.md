# DESIGN.md - Native HTML UI Kit

## Product Intent
브라우저 네이티브 HTML 기능으로 UI kit을 구성하는 한국어 실험 저장소다. 사용자는 popover, dialog, details, form validation의 기본 계약을 확인한다.

## Design Authority
우선순위는 접근성, native HTML semantics, no-JS 제약, 이 문서, CSS semantic token, 외부 참고 순서다.

## Visual Character
```txt
Native
Precise
Quiet
Reusable
```

- true white shell과 neutral border를 기준으로 한다.
- navy는 primary control, blue는 focus/interactive state, green/red는 validation semantic에만 사용한다.
- UI kit은 marketing page가 아니라 component reference처럼 읽혀야 한다.

## Typography
- UI: Inter, Pretendard, system-ui
- Display: 48-96px
- Section title: 28-36px
- Body: 18/31
- Control: 14/20

## Layout
- Sticky header와 component grid를 유지한다.
- Component card는 8px radius, 1px border, moderate shadow만 허용한다.
- Form field height는 44px 이상이다.

## Component Rules
- Native element의 semantic role을 유지한다.
- Button, input, select는 browser default typography에 의존하지 않는다.
- Invalid/valid state는 color-only가 아니라 border와 native validation을 함께 사용한다.
- `commandfor`는 progressive enhancement로 문서화한다.

## Interaction Model
```txt
Open component -> Inspect native behavior -> Validate state -> Add example PR
```

## Anti-patterns
- runtime JavaScript
- framework component clone
- over-styled controls that hide native semantics
- brand-specific design clone
