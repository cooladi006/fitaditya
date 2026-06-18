# COACH.md — Strength Code OS · Continuity File

**Purpose of this file:** so this project survives anything — a deleted chat, a new device, a year from now. Keep it in the `fitaditya` GitHub repo next to `index.html`. To resume coaching in any new conversation, upload **this file + your latest `strength-backup-*.json` + the current `index.html`** and say: *"Resume my Strength Code OS coaching from this file."* The new chat will have full context.

Last updated: Phase 1 live, Phase 2 built, Phase 3–4 outlined.

---

## 1. Who this is for
- Male, 38 · 180 cm · 84.5 kg · ~30–32% body fat at start.
- **Right shoulder:** multiple dislocations + surgery. This is the root cause of a right-side kinetic-chain compensation: reduced rear-delt → scapular winging → lost external rotation → altered trunk → right hip → right knee → right ankle → right tricep/elbow.
- **Goal:** lean, athletic, durable body (Virat-Kohli-style) with usable strength and longevity, healthy body-fat %. Return safely to **cricket and pickleball**. Movement quality is the primary metric; strength is the tool.
- **Training:** 3 sessions/week, 20–30 min each.
- **Equipment:** Inspire FT2 functional trainer (dual cables + Smith), adjustable bench, dumbbells, EZ curl bar, rope + handle attachments. **GMB mobility** subscription (use bodyweight/mobility freely). **No plyo box** — use the bench.
- **Baselines:** push-ups 4 · pull-ups 0 · right-leg balance 15 s · walking tolerance 15–20 min · deep squat needs ~25 mm heel elevation.

## 2. Non-negotiable principles (first principles)
1. **Movement quality > load > volume > intensity.** Quality gates everything.
2. **Foundation before progression** — never skip a floor. Don't build the 10th on a missing 9th.
3. **Equipment follows need, not the reverse.** Don't buy gear for one lift if an owned tool meets the goal (e.g., bench instead of a box). Bodyweight/GMB counts fully where it serves the goal.
4. **Educate every change.** Any exercise added/removed/replaced, or any phase change, must come with a first-principles reason (logged in §6 and in the app's "Why your plan looks like this").
5. **The one progression rule:** add load only when **all target reps hit · form ≥ 7/10 · pain ≤ 3/10 · RIR ≥ 2 · compensation not worse.** Otherwise hold or regress.
6. **Progress is proven by tests, not by time elapsed** (see §4).
7. **Right shoulder safety:** no loaded external rotation at 90° abduction (the apprehension/dislocation position) until cleared by surgeon/physio.

## 3. The phase model (the staircase)
- **Phase 1 — Restore & Stabilize (Floor 1):** rebuild rotator cuff, scapular control, single-leg stability, ankle mobility. No heavy load on an unstable base.
- **Phase 2 — Build & Integrate (Floor 2):** real load, unilateral strength, reintroduce vertical pulling + push-up/pull-up progressions, controlled rotation.
- **Phase 3 — Athletic Return (Floor 3):** power, rotational power, locomotion/agility, sport prep. *Authored from real test data on arrival.*
- **Phase 4 — Sport & Longevity (Floor 4+):** maintain + periodize for life; goals can evolve (power, body comp, sport peaks) without losing the base.

## 4. Measurable tests + progression gates
Re-test every 2–4 weeks. All gates for a phase must pass to advance.

| Test | Goal it proves | Baseline | P1 gate | P2 gate | P3 gate |
|---|---|---|---|---|---|
| Right-leg balance (s) | CNS + right-side stability | 15 | 30 | 45 | 60 |
| Deep-squat heel lift (mm, lower=better) | Ankle/hip mobility | 25 | 15 | 5 | 0 |
| Push-ups (reps) | Press strength + shoulder | 4 | 8 | 12 | 15 |
| Walk tolerance (min) | Capacity / sport return | 20 | 25 | 35 | 45 |
| Pull-ups (reps) | Pull strength | 0 | 0 | 1 | 2 |
| Loaded-ER shoulder pain (/10, lower=better) | Right shoulder integrity | 5 | 2 | 1 | 0 |

## 5. Current programs
Full cues live in `index.html`. Rotation is **Lower → Upper → Athletic** (not weekday-bound; carry-forward — the next undone session waits).

**Phase 1 — Restore**
- *Lower:* CB Cable Squat · Cable RDL · Assisted Split Squat · Farmer Carry
- *Upper:* Wall Slide + Serratus Punch · Cable External Rotation (R) · Face Pull · Incline DB Press · Seated Cable Row
- *Athletic:* Box Squat (to bench) · Single-Leg RDL (R) · Low Step-Up · Pallof Press
- *Daily:* R/L balance (3:2) · Crawling · Deep-squat hold · Ankle dorsiflexion drill · Walking progression

**Phase 2 — Build** (unlocks when P1 gates pass)
- *Lower:* Goblet/Cable Squat · DB RDL · Bulgarian Split Squat · Loaded Step-Up
- *Upper:* Cable ER (R) · Push-up Progression · Seated Cable Row · Lat Pulldown · Face Pull
- *Athletic:* Box Squat (heavier) · Single-Leg RDL (R) · Cable Chop + Lift · Assisted Pull-up Negative

**Phase 3–4:** directions only in-app; finalized from real data on arrival.

## 6. Change log (decisions + reasons)
1. **Added rotator-cuff & serratus work** (Wall Slide+Serratus, Cable ER, Face Pull), placed *before* pressing — the original plan ignored the shoulder, the actual root cause.
2. **Smith RDL → Cable RDL** — a fixed bar path hides right-side asymmetry; cable exposes and corrects it.
3. **Duplicate Smith RDL → Single-Leg RDL (R)** — removed redundancy, added a unilateral hinge that trains the balance test.
4. **Box squat → uses the bench** — no box to buy; equipment follows need.
5. **Parked Lat Pulldown & 1-Arm Press in Phase 1** — deferred until the cuff foundation passes its tests; reintroduced in Phase 2.

## 7. Tech architecture (how it all persists)
- **App:** one self-contained file `index.html` (vanilla JS PWA) + `sw.js` (offline cache). No build step.
- **Source of truth:** GitHub repo **`fitaditya`** (files at root). Every commit is a restore point.
- **Hosting:** Netlify connected to that repo → auto-deploys on every commit. Roll back instantly via Netlify → Deploys → Publish an older deploy.
- **User data:** browser `localStorage` key `scos_v1`, tied to the Netlify origin → survives every deploy automatically. **Never stored in git or the chat.**
- **Backups:** in-app Progress → *Export backup* → `strength-backup-YYYY-MM-DD.json`. Do this monthly and before any major change. *Import* restores it into any version.
- **State schema (v3):** `{rotationIndex, xp, history[], exHistory{}, activeDates[], bestStreak, drafts{}, habits{}, phase, assessments{}}`.

## 8. How to resume after a lost chat
1. Open a new conversation.
2. Upload: **this `COACH.md`**, your latest **`strength-backup-*.json`**, and the current **`index.html`** from the `fitaditya` repo.
3. Say: *"Resume my Strength Code OS coaching from these files. Here's where I am."*
4. The assistant rebuilds full context from §1–§7 and continues iterating under the same principles. Re-import the backup into the app if you ever switch devices.

*Optional convenience:* in Claude's Settings you can enable memory / "search & reference past chats" so continuity is automatic — but this file is the guarantee that doesn't depend on any single feature or chat.
