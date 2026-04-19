# FY27 Growth Plan — Feasibility at 4h/week

> **Draft — bound to change.** This is an honest capacity analysis done against the
> current plan. Numbers are estimates, not commitments. Q2 baseline review is the right
> moment to lock in what actually ships.

**Summary:** see [fy27-goals.md](./fy27-goals.md)
**Detail:** see [fy27-goals-detail.md](./fy27-goals-detail.md)

---

## Time budget

| | Hours |
|---|---|
| 4h/week × 52 weeks | 208h |
| Realistic after PTO / sick / context-switching (~10% loss) | **~185h/year** |
| Q1 (ramp, ~50% activity) | ~23h |
| Q2–Q4 (active execution) | ~55h each, ~165h combined |
| **Total effective, active execution** | **~190h** |

---

## Plan vs. capacity

The current plan as written totals roughly **~630h of work across 8 goals** (rough order of
magnitude, not a hard estimate — most goals are 60–110h each given what's listed as
"Specifics" and "Quarterly milestones" in the detail doc).

At 4h/week (~190h/year), that's about **3× overcommitted**. Something has to give — either
scope, timeline, or time budget.

---

## What feels achievable at 4h/week

Realistically, 4h/week supports **3–4 goals at reasonable depth**, or 5–6 goals if several
are deliberately lightweight. 8 goals at the current depth is not feasible.

Two usable framings:

### Framing 1 — Four focused goals (recommended)

Keeps one goal per category, accepts depth over breadth.

| # | Goal | Effort | What actually lands |
|---|------|--------|----------------------|
| 1 | **Code-Health Tooling Evaluation** (Results & Outcomes) | ~60h | 5 tools scored, 1–2 piloted, written recommendation (≤ 10 pages) at Q4. Smaller labeled sample (~10 items). |
| 3 | **Architecture Contributions — ADRs + theme adoption only** (Behaviors & Impact) | ~50h | Drop the "extraction-ready components" track for this year. Keep ADR practice (≥ 4 new ADRs) + theme audit + Theme Usage Guide + ESLint rule in warn-mode. Flip to error-mode in FY28. |
| 6 | **Forensic Pipeline (reduced)** (Skills & Competencies) | ~45h | CLI prototype + repeatable pipeline, Tornhill reading notes, **1–2 hotspot refactor PRs** (not 4). No Steiger rule this year; propose as FY28 follow-up. |
| 8 | **AI Course + Applied Project** (Growth & Development) | ~35h | 1 course + 1 applied project (likely feeds Goal 6). Candidate: a focused Anthropic / DeepLearning.AI short course, not a multi-book curriculum. |
| | **Total** | **~190h** | Fits. |

**What this costs:** drops Goals 2, 4, 5, 7. The AI-skill-library work (Goal 2) partially
folds into Goal 1 (labeled sample + basic skill versioning) or Goal 8 (applied project
could *be* a skill harness). The a11y work (Goal 5) can become a single ADR in Goal 3 if
a priority emerges.

### Framing 2 — Eight goals, lighter touch

Keeps all 8 goals but shrinks every target by ~⅔. Fits the budget but nothing lands with
real depth; risk is that none of them produce a clear promo-legible artifact.

Sketch of what it looks like:

- Goal 1 — eval 3–4 tools, pilot 1, doc 3 pages
- Goal 2 — harness MVP + 1 skill versioned; no labeled fixtures this year
- Goal 3 — **one** of the three tracks (e.g. ADRs only)
- Goal 4 — talk only, drop the companion skill
- Goal 5 — a11y audit only, no deep-dives, no WAS cert
- Goal 6 — 1 hotspot refactor, no pipeline infra
- Goal 7 — attend conference + short trip report, 0–1 applied PRs
- Goal 8 — finish course, small demo instead of a project

Only recommended if breadth matters more than depth for your review.

---

## Per-goal feasibility call-outs

| # | As-written size | At 4h/week honest take |
|---|----|---|
| **1 Code-Health Eval** | ~80h | ✅ Feasible at reduced scope (~60h). Smallest at-risk item is the labeled sample — keep it small (~10). |
| **2 Skill Library** | ~80h | ⚠️ Harness MVP alone is ≥ 30h of real engineering. Either make this the whole year's AI goal, OR drop. Can't be a side quest at 4h/week. |
| **3 Cross-Product Architecture** | ~110h | ❌ Not feasible as 3 tracks. Pick one — ADRs + theme is the realistic pair (~50h). Extraction-readiness goes to FY28. |
| **4 AI Event + Companion Skill** | ~85h | ❌ Companion skill with 3 modes at 4h/week would eat Q2+Q3+Q4 alone. Pick either the talk (~15h) or a single-mode skill (~40h), not both. |
| **5 Tool Depth + A11y + AI-Tool Eval** | ~80h | ⚠️ WAS cert alone is 40–60h of study. Pick one sub-track at most this year. |
| **6 Forensic Pipeline** | ~90h | ⚠️ Refactor PRs at "≤ 5 days each" × 4 = 4 weeks. Cut to 1–2 refactors (~45h). |
| **7 Conference + Takeaways** | ~50h | ✅ Mostly one conference week + light follow-up. Doable. Drop if cut needed elsewhere. |
| **8 AI Course + Project** | ~65h | ✅ Doable at ~35h for a ≤ 20-hour course + small applied project. Don't pick a multi-book curriculum. |

---

## Hidden costs not in the 4h/week

These exist whether you like it or not:

- **Conference** (Goal 7): travel + attendance = a full week ≠ 4h
- **WAS exam** (Goal 5 if kept): $300ish + ~50h study time
- **Vendor procurement calls** (Goal 1 Q3): slow in enterprise contexts
- **Manager / peer review cycles** on ADRs and written recommendations: extra elapsed
  time, even if low clock time
- **Q1 ramp reality**: "4h/week" starting month 1 is optimistic — account for a slow
  start

---

## My honest recommendation

1. **Bring this doc to your next 1:1** before committing. The 4h/week assumption is the
   load-bearing number in the whole plan; confirm it's realistic (and ask whether
   conference time, course time, and similar should come out of the 4h or be separate).
2. **Prefer depth over breadth** — pick **Framing 1 (four focused goals)**. A promo
   conversation lands better with 3–4 substantial artifacts than 8 shallow ones.
3. **Treat Q1 as a scoping quarter**, not a kickoff quarter. By end of Q1, you should
   have re-baselined the plan based on what actually fits.
4. **Revisit this doc every quarter** at the regular check-in. If the 4h/week assumption
   holds, confidence grows. If it slips, cut earlier not later.

---

## If you want to explore other budgets

| Budget | Realistic scope |
|---|---|
| **2h/week** (~95h/year) | 2 goals max. Pick Goal 1 (recommendation doc) + Goal 8 (course). |
| **4h/week** (~190h/year) | **4 focused goals** (Framing 1 above). |
| **6h/week** (~285h/year) | 5 goals. Add back a second goal from {2, 4, 5, 6, 7}. |
| **8h/week** (~380h/year) | 6 goals. Full Framing 1 + a simplified Goal 2 or 5. |
| **As-written plan** | ~12h/week of focused investment. Not sustainable alongside normal delivery. |
