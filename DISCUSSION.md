# DISCUSSION.md — Strength Code OS · The "Why" Behind the Plan

This is the plain-language record of the reasoning behind the app, so the thinking survives even if the original chats are gone. `COACH.md` is the spec; this file is the story.

---

## The starting picture
38yo, post-op right shoulder (multiple dislocations over ~15 years, stabilization surgery 18 months ago). Reported symptoms: right knee squeezes/strains in the squat; right tricep fails early on the bench; can't sit a deep squat without a ~25 mm heel lift; right knee aches after ~15 min walking; right hip + ankle chronically tight; right foot tilts downward at rest when lying on the back. Goal: lean, athletic, durable body, fat loss from ~32% toward ~15%, safe return to cricket and pickleball.

## The biggest correction: it's not one chain
The owner's working model was a single top-down chain: shoulder → scapula → spine → hip → knee → ankle, all driven by the shoulder. That model is roughly right for the **upper-right quadrant** but mostly wrong for the lower body (~70–75% confidence, reasoned from biomechanics + base rates).

The better model is **2–3 semi-independent problems**:
- **Upper-right quadrant (the real cascade):** the guarded shoulder → weak rear delt / lost external rotation → scapular winging → the early-failing tricep on bench. This *is* a chain, and it traces back to the shoulder.
- **The ankle is local, not descended.** A ~25 mm dorsiflexion restriction is almost always a local issue (tight gastroc-soleus, joint restriction, old sprains) — it did not come down from the shoulder.
- **The right knee is the victim, not the cause.** It's squeezed between a stiff ankle below and a weak/uncontrolled hip above — bottom-up / middle-out, not top-down.

**Why this matters:** semi-independent problems can be worked **in parallel**, which directly answered the owner's main question ("can I do this all at once?") — yes.

## Parallel training: what runs now, what waits
Run most compound lifting concurrently with rehab. Two carve-outs:
- **Overhead press waits** — it loads the shoulder near the apprehension/dislocation position; highest-risk move on the board. Landmine press is the eventual substitute.
- **Heavy ankle-loaded squat / leg press waits** behind ankle range + single-leg control. (Leg press is sneaky-bad: the back support removes the feedback that would expose the compensation.)

Everything else runs in parallel: trap-bar/conventional deadlift, rows, lat pulldown (lower-risk than the original gating implied), and **dumbbell** bench instead of barbell — DBs expose and correct the right-side asymmetry, and the early-failing tricep is a *signal* the shoulder isn't sharing load (fix via cuff/serratus work, not by hammering triceps).

## The clinical flag (not alarmist, just honest)
Two signs deserve **one** physio / sports-doc screen: (a) the supine foot-tilt — quick self-test: can you actively dorsiflex the foot against gravity? Yes → trainable tightness; No → see a doctor (possible nerve/foot-drop issue). (b) Knee strain at ~15 min of walking — low-load pain deserves a real diagnosis. Claude is a coach/analyst, not a clinician, and can't assess this remotely.

## Fat loss: the owner's instinct was right
"Just eat less, no fancy diet, protect BMR" is correct on the evidence — energy balance dominates and adherence is the real variable. Honest math: ~57–59 kg lean mass → 15% body fat ≈ ~67–68 kg ≈ ~17 kg of fat ≈ roughly a year at a safe pace. Two non-negotiable additions (not noise):
1. **Protein ~100 g/day.** In a deficit the body burns muscle unless protein is high and you're lifting; lost muscle drops BMR — the exact thing the owner feared. The self-imposed ~40 g ceiling was the real risk. Solution = no calorie math: one positive rule (a protein anchor every meal) + one negative rule (smaller portions of everything else). Veg anchors for Chennai: soy chunks (~25 g/50 g dry — the cheapest big lever), paneer, hung/Greek curd, dal/rajma/chana, tofu, milk, a second whey scoop.
2. **One instrument: a weekly weigh-in**, read as a 3–4 week trend. Down = deficit working, do nothing. Flat = trim non-protein portions. No daily counting.

BMR fear addressed: adaptive thermogenesis is real but modest, and it's blunted by protein + lifting + walking, not by diet hacks.

## The app's philosophy (what makes it a coach, not a tracker)
Test-gated phase progression (you level up on numbers, not time), a "why" behind every exercise, red-flags and success cues, a reasoned change log, and equipment chosen by need (bench replaces a box). Bodyweight/GMB mobility counts fully.

## Program changes made (with reasons)
1. **Added rotator-cuff & serratus work before pressing** — the original plan ignored the shoulder, the actual root cause.
2. **Smith RDL → Cable RDL** — the fixed bar path let the right side cheat invisibly; the cable forces honest bilateral stabilization.
3. **Duplicate hinge → Single-Leg RDL (R)** — removed redundancy, added a unilateral hinge that also trains the balance test.
4. **Box squat uses the bench** — no box to buy; equipment follows need.
5. **Lat pulldown & 1-arm press parked in Phase 1** — foundation before load; pulldown returns in Phase 2.
6. **Added Ankle Rock (Knee-to-Wall)** — there was a heel-lift *test* but nothing *training* it. The stiff ankle is the bottom-up driver under the right knee; unloaded drills plateau, so loaded end-range work was added to both Lower days. (~80% this was the single highest-value change.)
7. **Box Squat → Lateral Step-Down (P1) / Loaded Lateral Lunge (P2)** — the whole program was sagittal + anti-rotation, with **zero frontal-plane work** — the exact plane cricket/pickleball live in and the plane the right knee fails in (caving inward). Box squat was also a duplicate bilateral squat. The step-down doubles as a knee-tracking drill. (~70% confidence; the main risk is frontal-plane loading on the knee, so it's low, slow, and pain-gated.) Lat pulldown deliberately kept parked — restraint, not oversight.
8. **Added the Fuel tab** — fat loss had no support in the app. Two rules + weekly weight, gamified into the same XP/streak engine as training so nutrition consistency levels you up too.

## What was deliberately NOT changed
The Upper days, the hinge selection, the single-leg work, and the test gates were already well-built. Churning them would have been theater. The discipline here is doing the few changes that are defensible on first principles and naming the restraint out loud.

## Falsification triggers (when to rethink)
- If Ankle Rock runs consistently for 3–4 weeks and the heel-lift test doesn't drop, the restriction may be structural (bony block / old fusion) → physio/imaging, not more load.
- If Lateral Step-Down provokes right-knee pain > 3/10, regress the height or pull it.
- If the daily-rotating program ever drifts from movement-quality-first, stop and re-anchor on the principles.

## Hosting / tooling note
The app moved from Netlify to **GitHub Pages**. Because browser storage is tied to the site's address, training data does not auto-transfer between hosts — it's migrated once via in-app Export → Import backup. Future development can happen by discussing changes with Claude (here), taking the updated `index.html`, and uploading/pushing it to the repo; GitHub Pages redeploys automatically.
