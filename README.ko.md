# AGENTS.md

<p align="center">
  <img src="https://agents.md/og.png">
</p>

[AGENTS.md](https://agents.md)는 코딩 에이전트를 안내하기 위한 간단하고 개방적인 형식입니다.

AGENTS.md를 에이전트를 위한 README라고 생각하세요: AI 코딩 에이전트가 여러분의 프로젝트에서 작업하는 데 도움이 되는 컨텍스트와 지침을 제공하는 전용의 예측 가능한 장소입니다.

아래는 AGENTS.md 파일의 최소 예제입니다:

```markdown
# Sample AGENTS.md file

## Dev environment tips
- Use `pnpm dlx turbo run where <project_name>` to jump to a package instead of scanning with `ls`.
- Run `pnpm install --filter <project_name>` to add the package to your workspace so Vite, ESLint, and TypeScript can see it.
- Use `pnpm create vite@latest <project_name> -- --template react-ts` to spin up a new React + Vite package with TypeScript checks ready.
- Check the name field inside each package's package.json to confirm the right name—skip the top-level one.

## Testing instructions
- Find the CI plan in the .github/workflows folder.
- Run `pnpm turbo run test --filter <project_name>` to run every check defined for that package.
- From the package root you can just call `pnpm test`. The commit should pass all tests before you merge.
- To focus on one step, add the Vitest pattern: `pnpm vitest run -t "<test name>"`.
- Fix any test or type errors until the whole suite is green.
- After moving files or changing imports, run `pnpm lint --filter <project_name>` to be sure ESLint and TypeScript rules still pass.
- Add or update tests for the code you change, even if nobody asked.

## PR instructions
- Title format: [<project_name>] <Title>
- Always run `pnpm lint` and `pnpm test` before committing.
```

## 웹사이트

이 레포지토리에는 https://agents.md/ 에서 호스팅되는 기본 Next.js 웹사이트도 포함되어 있으며, 프로젝트의 목표를 간단하게 설명하고 몇 가지 예제를 제공합니다.

### 로컬에서 앱 실행하기
1. 의존성 설치:
   ```bash
   npm install
   ```
2. 개발 서버 시작:
   ```bash
   npm run dev
   ```
3. 브라우저를 열고 http://localhost:3000 으로 이동
