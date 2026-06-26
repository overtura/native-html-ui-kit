# Native HTML UI Kit Maintainer Bot Backlog

중앙 control plane은 `okorion/self-improving-maintainer-bot`이다. 브라우저 기본 HTML 기능을 우선하고 런타임 JavaScript를 추가하지 않는다.

## 운영 검증
- 모든 변경은 `pnpm check`를 통과해야 한다.
- 자동 merge 기본값은 꺼져 있다.
- GitHub Actions는 dry-run/check/report automation 용도로만 사용한다.
- `.github/workflows/**`, credential, auth/security, infra, migration 변경은 R3로 취급하고 코드 변경 없이 proposal only로 다룬다.

## R0 Report
- native control 추가 기준과 사용성 기준의 빈 부분을 분석 리포트로 정리한다.
- 각 컴포넌트 예제가 보여줘야 할 상태와 fallback 기준을 정리한다.

## R1 PR 후보
- 작은 native HTML control 예제를 추가한다.
- 기존 예제의 label, helper text, 상태 설명을 보강한다.
- 밝은 UI kit 톤을 유지하며 control spacing과 focus ring을 개선한다.

## R2 Draft 후보
- build tooling, dependency, lint script 변경은 draft PR로만 제안한다.

## R3 Proposal only
- workflow, credential, security, infra, migration 관련 변경은 코드 변경 없이 proposal로만 다룬다.
