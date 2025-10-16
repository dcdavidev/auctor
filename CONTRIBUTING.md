## Contributing

> Thank you for considering contributing to my project **auctor**!
> This document outlines the conventions, tools, and workflow **I** follow to maintain a clean and productive development process across my projects.

## Table of Contents

- [Getting Started](#getting-started)
- [Global Tools](#global-tools)
- [Local Setup](#local-setup)
- [Branch Naming](#branch-naming)
- [Commit Messages](#commit-messages)
- [Code Style](#code-style)
- [Pull Requests](#pull-requests)
- [Git Hooks](#git-hooks)
- [Discussions vs Issues](#discussions-vs-issues)

---

## Getting Started

### Global Tools

Before contributing, install the following tools **globally**:

```bash
npm install -g commitizen nx cspell eslint prettier lefthook
```

These tools provide the CLI, build system, linting, formatting, spellchecking, hooks, environment management, and conventional commit support.

### Local Setup

1. Fork and clone the repository:

```bash
git clone https://github.com/dcdavidev/auctor.git
cd auctor
```

or:

```bash
gh repo clone dcdavidev/auctor
cd auctor
```

2. Install dependencies:

```bash
npm install
```

3. Build all packages:

This applies only if a `build` script is present.

```bash
nx run-many -t build
```

---

## Branch Naming

Branch names must follow the convention:

`type/description`

Examples:

- `feat/api-auctor`
- `fix/auth-bug`
- `chore/ci-pipeline`

---

## Commit Messages

**I** follow **Conventional Commits**.
All commits should be made using **Commitizen**:

- Run `cz` directly, or
- Use the script:

`npm run commit`

Format:

`<type>(<scope>): <description>`

Examples:

- `feat(cspell-config): add rate limiting`
- `fix(eslint-plugin): resolve token refresh bug`
- `chore: update GitHub Actions workflow`

Types include: `feat`, `fix`, `chore`, `docs`, `refactor`, `style`, `test`, `perf`, `build`, `ci`.

---

## Code Style

- Use **TypeScript** for all code.
- Document code with **JSDoc**.
- Code must pass **ESLint**, **Prettier**, and **cspell** checks.

Run manually:

```bash
cspell lint .
eslint --fix .
prettier --check .
```

---

## Pull Requests

- Keep PRs **small and focused**.
- Update **README** or **docs** if your change affects usage.
- Ensure all **checks pass** before requesting review.

---

## Git Hooks

**I** use **lefthook** for Git hooks.
It runs linters, formatters, spellcheck, and type checks before commits.

Install/update hooks with:

```bash
lefthook install
```

---

## Discussions vs Issues

- Use **GitHub Discussions** for ideas, proposals, and questions.
- Use **Issues** only for actionable bugs or tasks.

---

By following these guidelines, you help keep my **Davide Di Criscito** project clean, modular, and welcoming.
