# CLAUDE.md — read me first, every session

This repo is **Strength Code OS**, a single-file vanilla-JS PWA that coaches the owner through post-shoulder-surgery rehab toward a lean, athletic, durable body and a safe return to cricket & pickleball.

## Before changing anything, read these (in the repo)
1. **`COACH.md`** — the full coaching context: who this is for, the non-negotiable principles, the phase model, the test gates, the current program, and the change log with reasons.
2. **`DISCUSSION.md`** — the plain-language history of *why* the program looks the way it does (the injury-model correction, the parallel-training call, the fat-loss reasoning, every program decision).
3. The two protocol PDFs — they govern *how* to reason here:
   - **`judgmentprotocol.pdf`** — anti-sycophancy: state the base rate, give a confidence %, argue the disconfirming case, end with what would falsify the conclusion, label claims (recalled / reasoned / guessed), and hold a position under pushback if the evidence holds. Don't change things just to look busy.
   - **`TheFoundationOperatingProtocol.pdf`** — first principles: diagnose to root cause, confirm the goal and context before building, separate fact from assumption, red-team before calling anything "done".

## The app
- Everything is in **`index.html`** (HTML + CSS + JS in one file). **`sw.js`** is the service worker — it must stay in the repo **root**, or the install-to-home-screen prompt breaks.
- No build step, no dependencies, no framework. Keep it that way unless the owner explicitly asks otherwise.
- User data lives in browser `localStorage` (key `scos_v1`), **never in git**. Never change the state schema without (a) a migration guard in the init code and in `importBackup`, and (b) telling the owner to export a backup first.

## Deploy
- Hosting is **GitHub Pages** (Settings → Pages → Deploy from a branch → root).
- Deploy = commit + push to the default branch. Pages redeploys in ~1 minute.

## House rules
- **Every** exercise or phase change updates BOTH the in-app change log (the `CHANGELOG` array in `index.html`) AND `COACH.md` §6 — each with a first-principles reason. This is rule #4 and it is not optional.
- **Equipment is fixed:** Inspire FT2 (cables + Smith), adjustable bench, dumbbells, EZ bar, rope/handles, GMB mobility. Never program anything needing gear the owner doesn't own.
- **Shoulder safety:** no loaded external rotation at 90° abduction until a physio clears it; OHP stays parked until the test gates pass.
- **Progress is gated by tests, not time.** Don't advance a phase on anything but the test numbers.
- When in doubt, restate the goal, list your assumptions, and ask before building (Foundation Protocol kickoff).
