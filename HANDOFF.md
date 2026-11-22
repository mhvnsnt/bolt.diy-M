# HANDOFF — bolt.diy-M

**Last updated: 2026-11-22 (America/New_York).**
**Repo:** `mhvnsnt/bolt.diy-M` (PUBLIC), default branch `main`.
**Purpose of this file:** any agent that picks up work here reads this FIRST, then the linked docs. It states what we've done, where we're at, and what we're working toward — so the owner can say "go to this repo, pick up the work" and you just know. Update this file in the same PR whenever the state changes (add, don't delete).

## 1. What this repo is

bolt.diy-M — the owner's fork of bolt.diy: "Prompt, run, edit, and deploy full-stack web applications using any LLM you want!" Created 2026-07-22 (forked from upstream bolt.diy). Public. Electron + web: `app/`, `electron/`, `worker-configuration.d.ts`, `wrangler.toml`, `docker-compose.yaml`, `Dockerfile`, `playwright.config.preview.ts`, `docs/`, `PROJECT.md`, `FAQ.md`, `CHANGES.md`.

## 2. Where we're at

### DONE
- **No-data-loss rules + deletion guard (2026-02-07 era work, open PR #1):** the owner-law rules doc — still open as a PR, not merged.
- **AGENTS.md with anti-clobber laws (open PR #2):** the anti-clobber rules doc — still open as a PR, not merged.
- **Working method statement (2026-10-27):** `WORKING-METHOD.md` landed.
- **Web URL content fetcher for chat context (2026-02-07, `2e254ac`):** the last feature commit on main.

### IN PROGRESS
- Nothing is actively in progress in this repo that the repo itself records. Last push was the 2026-10-27 sweep commit. The two law PRs (#1, #2) are the only open PRs — both are docs, both unmerged.

### BLOCKED
- Nothing recorded as blocked in this repo. No releases. Note: as a fork, this repo can drift from upstream bolt.diy — the repo does not record when it was last synced with upstream, so do not assume it is current.

## 3. What we're working toward

A prompt-to-app builder that runs any LLM the owner wants and deploys full-stack apps. The bar: prompt in, working app out, deployed — verified live in the preview, not described. Upstream drift should be checked before any big feature: if upstream fixed it, pull it — don't rebuild it.

## 4. Standing rules that apply here

- **Branch → PR → merge, always.** Never push to main directly. Add-only, zero-conflict PRs, no force pushes.
- **Checkpoint-and-save law:** CHECKPOINT.md first, update after every step; the repo is the save; resume, never restart.
- **No-temp-storage law:** nothing in /tmp or any wipeable location, ever.
- **Real-source-only:** build from the real sources, wired up fully — pull from upstream rather than rebuilding what upstream already fixed.
- **Anti-clobber:** never wipe or overwrite another lane's work.
- **Never kill in-progress work.**

## 5. Key files and paths

| What | Where |
|---|---|
| App / worker | `app/`, `worker-configuration.d.ts` |
| Electron shell | `electron/`, `electron-builder.yml` |
| Deploy / containers | `wrangler.toml`, `docker-compose.yaml`, `Dockerfile` |
| Project notes / FAQ / changes | `PROJECT.md`, `FAQ.md`, `CHANGES.md`, `changelog.md` |
| Docs | `docs/` |
| Preview tests | `playwright.config.preview.ts`, `test-workflows.sh` |
| Open PRs | #1 (NO-DATA-LOSS rules + deletion guard), #2 (AGENTS.md anti-clobber laws) |
| Related builder | `mhvnsnt/Neon-App-Builder` (the other app builder — check which is live before duplicating work) |

## 6. Open decisions needing the owner

- **bolt.diy-M vs Neon-App-Builder:** two app builders in this batch. Which one is the live builder is his call — lanes do not pick it or merge the two.
- **Upstream sync:** whether to sync with upstream bolt.diy and when. His call.
- No other decisions are recorded in this repo.

## 7. How to pick up

1. Read this HANDOFF.md first, then `PROJECT.md`, `README.md`, and `WORKING-METHOD.md`.
2. Check `Neon-App-Builder` too — do not duplicate builder work across the two repos.
3. Check what other agents are already doing before starting anything.
4. Resume from the stated next step — never restart, never re-derive finished work.
5. Land work branch → PR → merge, add-only. Stage finished work to the repo as it lands.
6. Update this HANDOFF.md in the same PR when the state changes. Verify with your own eyes before claiming anything built.
