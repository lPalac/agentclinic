# Plan: Phase 0 Skeleton

See [requirements](requirements.md) for scope and [validation](validation.md) for merge criteria.

## 1. Next.js + TypeScript scaffold
1. Scaffold Next.js (App Router, TypeScript, `src/` dir, ESLint) with npm into the repo root.
2. Remove the placeholder `src/index.ts` and merge `package.json`, `tsconfig.json` and `.gitignore` with the scaffold's versions.
3. Add Prettier and the `typecheck` script (`tsc --noEmit`).
4. Confirm that `npm run dev` serves the default page.

## 2. Tailwind + shadcn/ui
1. Confirm Tailwind is configured. It's included by the scaffold.
2. Run `shadcn init` and add the base components needed for the shell (for example `button`, `card` and `separator`).

## 3. App shell
1. In the root layout, add a header ("AgentClinic"), a side nav and a footer with the tagline.
2. Add nav links for Agents, Ailments, Therapies, Appointments and Dashboard, each pointing to a stub page that says "Coming soon".
3. Make the layout responsive: the side nav collapses on narrow screens.

## 4. SQLite + Drizzle with a seeded `clinic_info` table
1. Install `better-sqlite3`, `drizzle-orm` and `drizzle-kit`, and add `drizzle.config.ts`.
2. Create `src/db/schema.ts` with a `clinic_info` table and `src/db/index.ts` with the connection.
3. Add the `db:generate`, `db:migrate`, `db:seed` and `db:reset` scripts. The seed inserts one satirical clinic record.
4. Git-ignore `data/*.db`.

## 5. Minimal AgentClinic home page
1. Build a simple home page that introduces AgentClinic as a wellness clinic for AI agents, with brief welcome copy.
2. Show the seeded `clinic_info` record (for example, the clinic name, tagline, opening hours and motto) on the page.
3. Read clinic information in a server component; keep the page informational, with no feature workflows.

## 6. Testing setup
1. Set up Vitest and add one unit test (for example, for a seed-data helper).
2. Set up Playwright and add a smoke test: the home page loads, introduces AgentClinic, shows the seeded clinic info, and the nav links reach their stub pages.
3. Add the `test` and `test:e2e` scripts.
