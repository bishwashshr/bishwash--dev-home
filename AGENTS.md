# Repository Guidelines

## Project Structure & Module Organization

This personal portfolio uses React, TypeScript, and Vite, with the application rooted in this directory.

- `src/main.tsx` mounts React; `src/App.tsx` contains the main interface.
- `src/App.css` holds component styles; `src/index.css` holds global styles.
- `src/assets/` contains imported images and SVGs. `public/` contains assets served directly by path.
- `index.html` is the HTML entry point. Root configuration files control Vite, TypeScript, and ESLint.
- `dist/` is generated build output. No test directory currently exists.

## Build, Test, and Development Commands

Run commands from the repository root:

- `npm ci`: install dependencies using the committed lockfile.
- `npm run dev`: start the Vite development server with hot reload.
- `npm run build`: run TypeScript checks and generate production files in `dist/`.
- `npm run lint`: check TypeScript and TSX files with ESLint, including React Hooks and refresh rules.
- `npm run preview`: serve an existing production build locally; run the build first.

## Coding Style & Naming Conventions

Follow existing code: two-space indentation, single-quoted TypeScript strings, no semicolons, and double-quoted JSX attributes. Use function components and hooks. Name components and their files in PascalCase, such as `ProjectCard.tsx`; use camelCase for functions and variables and `use` prefixes for custom hooks. Keep imported assets under `src/assets/`. ESLint is configured; no dedicated formatter is installed.

## Testing Guidelines

No automated test framework, test script, or coverage threshold is configured. For code changes, run `npm run lint` and `npm run build`. Check affected interactions and responsive layouts in the browser. If adding automated tests, document the chosen runner, commands, and naming convention before treating them as required checks.

## Commit & Pull Request Guidelines

History uses short, descriptive subjects, such as `Scaffold React TypeScript portfolio with Vite`; no enforced commit prefix convention exists. Keep changes focused. Pull requests should explain the change, list validation performed, link relevant issues, and include screenshots for visual changes.

**Agents must ask the user for the commit message before creating any commit.**

## Security & Configuration

Keep dependencies, build output, caches, and local environment files out of Git using `.gitignore`. Commit `package-lock.json` with dependency changes. Only put placeholder values in shared `.env.example` files; never include secrets in browser code or client-exposed environment variables.
