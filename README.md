# NestJS Boilerplate

Production-ready NestJS boilerplate with TypeORM (PostgreSQL), Docker, and team collaboration tooling.

## Quick Start

### 1. Install dependencies

```bash
npm install
```

### 2. Environment setup

```bash
cp .env.example .env
# Edit .env with your values - app will NOT start without required variables
```

### 3. Local development (PostgreSQL in Docker)

```bash
npm run docker:dev        # Start PostgreSQL
npm run start:dev         # Start NestJS app
```

### 4. Full stack in Docker

```bash
npm run docker:up
```

## Scripts

| Script | Description |
|--------|-------------|
| `npm run start:dev` | Start with hot reload |
| `npm run build` | Build for production |
| `npm run start:prod` | Run production build |
| `npm run lint` | Run ESLint |
| `npm run format` | Format with Prettier |
| `npm run docker:dev` | Start PostgreSQL for local dev |
| `npm run docker:up` | Start app + PostgreSQL |

## Project Structure

```
src/
├── common/           # Guards, filters, decorators
├── config/           # Environment validation, configs
├── modules/          # Business logic modules
│   └── health/       # Example health check module
├── app.module.ts
└── main.ts
```

## Git Hooks (Husky)

- **pre-commit**: Runs `lint-staged` (ESLint + Prettier on staged files)
- **commit-msg**: Enforces Conventional Commits via Commitlint

Valid commit types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`, `revert`

Example: `feat: add user authentication`
