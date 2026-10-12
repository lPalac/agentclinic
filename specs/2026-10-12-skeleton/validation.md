# Validation: Phase 0 Skeleton

This branch can be merged when **every** item below passes.

## Automated
- [ ] `npm install` completes cleanly.
- [ ] `npm run lint` passes with no errors.
- [ ] `npm run typecheck` passes.
- [ ] `npm run build` succeeds.
- [ ] `npm run db:reset && npm run db:seed` succeed on a fresh clone, creating `data/agentclinic.db`.
- [ ] `npm test` (Vitest) passes.
- [ ] `npm run test:e2e` (Playwright smoke test) passes.

## Manual
- [ ] `npm run dev` serves the app at http://localhost:3000.
- [ ] The header shows "AgentClinic", and the footer shows the tagline.
- [ ] The home page briefly introduces AgentClinic as a wellness clinic for AI agents and shows the seeded `clinic_info` record read from SQLite.
- [ ] Each nav link (Agents, Ailments, Therapies, Appointments, Dashboard) opens a "Coming soon" stub page.
- [ ] The layout looks correct in a modern browser at desktop width (≥1280px) and mobile width (~375px), with no horizontal scrolling.

## Repo hygiene
- [ ] The SQLite database file isn't committed.
- [ ] The placeholder `src/index.ts` is gone.
- [ ] The README explains how to install, reset and seed the database, and run the app.
