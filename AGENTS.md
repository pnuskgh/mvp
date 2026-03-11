# AGENTS.md

## Project overview
개인 재무 관리 AI 서비스

## Setup commands
- Install: `npm install`
- Build: `npm run build`
- Test: `npm test`

## Dev environment tips
- `pnpm dlx turbo run where <project_name>`을 사용해 원하는 패키지로 빠르게 이동.
- `pnpm install --filter <project_name>`으로 특정 패키지를 워크스페이스에 추가해 Vite, ESLint, TypeScript에서 인식 가능.
- `pnpm create vite@latest <project_name> -- --template react-ts`로 React + TypeScript 패키지 생성.
- 각 패키지의 `package.json`의 name 필드를 확인.

## Code style
- TypeScript strict mode
- ESLint + Prettier 사용
- 함수형 패턴 선호
- Always add JSDoc comments for public APIs

## CI/CD 실행 방법

## Testing instructions
- `.github/workflows` 폴더에서 CI 계획 확인.
- `pnpm turbo run test --filter <project_name>`으로 테스트 실행.
- 패키지 루트에서 `pnpm test` 실행.
- 특정 테스트 실행 시: `pnpm vitest run -t "<test name>"`.
- 모든 테스트가 통과해야 머지 가능.
- 파일 이동이나 import 변경 시 `pnpm lint --filter <project_name>` 실행.
- 코드 변경 시 반드시 테스트 추가/갱신.
- PR 전에 반드시 `npm test` 실행
- 새 기능은 테스트 필수

## PR instructions
- 제목 형식: `[module] Description`
- 커밋 메시지는 conventional commits 따름

## 보안 관련 주의사항
