# Native HTML UI Kit

popover, details, command/commandfor, dialog, form validation 같은 브라우저 네이티브 기능만으로 구성하는 no-JS UI kit입니다. 앱 런타임에는 JavaScript를 넣지 않습니다.

## 목적
- 프레임워크 없이 native HTML interaction 패턴을 축적한다.
- 최신 HTML 기능의 사용성과 fallback을 한국어 예제로 검증한다.
- 중앙 maintainer bot이 컴포넌트 예제와 문서 개선을 target profile 기반 PR로 제안한다.

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
`scripts/no-js-lint.mjs`는 `<script>` 태그와 inline event handler를 모두 실패로 처리한다.

## Vercel 배포
- 배포 설정: `vercel.json`
- framework: Vite
- build command: `pnpm build`
- output directory: `dist`
- production deploy: Vercel CLI 로그인 또는 `VERCEL_TOKEN` 설정 후 `npx vercel --prod --yes`

현재 저장소는 Vercel 정적 배포 설정까지 준비되어 있다. 이 Codex 실행 환경에서는 Vercel CLI/커넥터 인증이 확인되지 않아 production URL 발급은 인증 후 진행한다.

## 최근 업데이트
- 밝은 톤 네이티브 HTML UI kit 디자인 시스템을 정리했다.
- details, dialog, popover, form 상태를 JavaScript 없이 보여주는 컴포넌트 예시를 확장했다.
- 중앙 maintainer bot은 네이티브 HTML 컴포넌트 맥락과 최근 PR 이력을 기준으로 독립적인 개선 후보를 찾는다.

## 자가 개선
이 저장소에는 자가 개선 엔진을 두지 않는다. 중앙 control plane인 `okorion/self-improving-maintainer-bot`이 `profiles/overtura/native-html-ui-kit.json` profile로 이 저장소를 target repo로 다룬다.

Target 설정은 `maintainer-bot/`에 둔다. 런타임 JavaScript, `.github/workflows/**`, credential, auth/security, infra, migration 변경은 R3로 취급하며 draft/proposal only로 처리한다.

## 디자인 시스템
- 기준 문서: `DESIGN.md`
- 실행 토큰: `design-system/base.css`
- 참고 기록: `docs/design/`

## 범위 밖
- 런타임 JavaScript
- framework 컴포넌트 라이브러리
- 실제 secret 또는 credential 저장
