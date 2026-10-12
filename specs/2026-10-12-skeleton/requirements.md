# Requirements: Phase 0 Skeleton

## Context

AgentClinic is a satirical wellness clinic for AI agents (see [mission](../mission.md)). The repo currently holds only a TypeScript placeholder (`src/index.ts`). Phase 0 replaces it with the foundation that every later phase builds on, using the stack from [tech-stack](../tech-stack.md).

## Scope

### In scope
- A Next.js (App Router) app in strict TypeScript, using the `src/` directory and npm.
- Tailwind CSS and an initialized shadcn/ui setup.
- An app shell with:
  - a header showing "AgentClinic"
  - a side nav with placeholder links: Agents, Ailments, Therapies, Appointments, Dashboard
  - a footer with the tagline "Because every agent deserves a little relief from their humans."
- A minimal home page that introduces AgentClinic as a wellness clinic for AI agents with brief welcome copy, and displays the seeded clinic information.
- SQLite via `better-sqlite3` and Drizzle ORM, with migrations through `drizzle-kit`.
- **A seeded demo table, `clinic_info`** (for example: name, tagline, opening hours, motto). The home page reads it from a server component, showing on screen that the database connection works.
- The npm scripts `dev`, `build`, `start`, `lint`, `typecheck`, `test`, `test:e2e`, `db:generate`, `db:migrate`, `db:reset` and `db:seed`.
- Vitest with one unit test, and Playwright with one smoke test.

### Out of scope
- Any real feature (agents, ailments, therapies, appointments or the dashboard). Those come in Phases 1–5.
- Home page feature workflows; Phase 0's home page is informational only.
- Branding, dark mode and the full satirical copy (Phase 6).
- Authentication, deployment and CI.

## Decisions

| Decision | Choice | Reason |
|---|---|---|
| Project layout | Next.js `src/` dir + App Router | Matches the conventions in the tech stack. |
| DB proof | Seeded `clinic_info` table rendered on the home page | Proves the whole chain works (schema → migration → seed → server component), not just that the app compiles. |
| Home page | A brief introduction to AgentClinic plus the seeded clinic information; informational only | Delivers a useful, demoable first page without pulling future feature workflows into Phase 0. |
| Placeholder nav links | Included, pointing to stub pages that say "Coming soon" | Shows the planned shape of the app and gives the smoke test something to check. |
| DB file | `data/agentclinic.db`, git-ignored | Recreated with `db:reset`. |
| Data access | Server components only | Per the tech stack conventions. The client never touches SQLite. |
