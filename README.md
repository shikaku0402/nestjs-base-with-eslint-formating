# NestJS API Boilerplate (Config & Tooling) 🚀

This repository serves as a highly-configured NestJS starter template, fully optimized for developer experience, strict type safety, automatic code formatting, and streamlined imports resolving.

---

## 🛠️ Project Tooling & Configurations

### 1. 🛡️ ESLint Flat Configuration (v9)

The project utilizes the modern **ESLint Flat Config** format (`eslint.config.mjs`) to ensure high code quality, robust standards, and strict TypeScript rules:

- **Core Plug-ins Integrated:**
  - `@darraghor/eslint-plugin-nestjs-typed` — Flat configuration for NestJS strict rules.
  - `typescript-eslint` — Comprehensive TypeScript type-checking guidelines.
  - `eslint-plugin-prettier/recommended` — Seamless coordination with Prettier rules.
- **Custom Rules Enforced:**
  - Strict unused variables checking (`@typescript-eslint/no-unused-vars` set to `error`).
  - Warning on unhandled promises (`@typescript-eslint/no-floating-promises` set to `warn`).
  - Custom end-of-line checking tailored for smooth cross-platform collaboration.

### 2. 🎨 Prettier Code Formatter

A `.prettierrc` configuration file ensures a standardized code style across all contributors:

- Single quotes for strings (`singleQuote: true`).
- 2-space tab indentation (`tabWidth: 2`).
- Trailing commas where valid (`trailingComma: "all"`).
- Standard print width limit and automatically handled line endings for compatibility.

### 3. 💻 VS Code Workspace Integration

An optimized `.vscode/settings.json` is bundled to make code standards active instantly on save without manual commands:

- **Format on Save:** Automatically applies Prettier styling to TypeScript files on file save.
- **Code Actions on Save:**
  - Automatic ESLint fix resolution (`source.fixAll.eslint`).
  - Automatic import organizing and sorting (`source.organizeImports`).
- **Standard Line Endings:** Enforces standard LF (`\n`) formatting to prevent cross-platform whitespace conflicts.

### 4. 🧩 TypeScript Path Aliases & Jest Mapping

Avoid complex relative pathing (e.g., `../../../../common`). Absolute paths are fully configured under `tsconfig.json`:

- `@src/*` maps directly to `src/*`
- `@test/*` maps directly to `test/*`
- **Jest Mapping:** `package.json` contains matching configurations (`moduleNameMapper`) to ensure path aliases resolve cleanly in testing suites.

---

## 📂 Project Configuration Structure

```bash
nest-basic-api/
├── .vscode/               # Workspace specific editor settings
│   └── settings.json      # Auto-formatting & Auto-import actions on save
├── eslint.config.mjs      # Strict ESLint flat configuration (v9)
├── .prettierrc            # Code formatter style rules
├── tsconfig.json          # TS compilation & Path aliases (@src/*)
└── package.json           # Jest path mappings, Scripts & Dependencies
```

---

## ⚙️ Development Guide

### Prerequisites

Make sure you have [Node.js](https://nodejs.org/) installed and the [pnpm](https://pnpm.io/) package manager:

```bash
npm i -g pnpm
```

### Installation

```bash
pnpm install
```

### Compile and Run

```bash
# Development (with watch mode)
pnpm run start:dev

# Debug mode
pnpm run start:debug

# Production build
pnpm run build
pnpm run start:prod
```

### Quality Assurance

```bash
# Run ESLint validation and auto-fix violations
pnpm run lint

# Format codebase using Prettier
pnpm run format
```

### Testing Suite

```bash
# Unit tests
pnpm run test

# End-to-end (E2E) tests
pnpm run test:e2e

# Code coverage report
pnpm run test:cov
```

---
