# FY27 Goals — Senior Front-End, Competence Growth Plan

> **Draft — bound to change.** This is a working plan, not a commitment. Goals, metrics,
> and milestones will be revised as baselines are captured in Q2 and as circumstances
> evolve through the year.

**Role:** Senior Front-End Developer on the current project
**Horizon:** 2026-04 → 2027-04. **Q1 is ramp-up** (planning, shortlisting, enrolment). Active
execution runs **Q2–Q4** with quarterly check-ins.
**Anchor themes:** (1) AI Engineering Excellence · (2) Frontend Quality & Architecture
**Detail:** see [fy27-goals-detail.md](./fy27-goals-detail.md)

---

## Results & Outcomes

**1. Code-Health Tooling Evaluation**
Research, pilot, and compare code-health tooling for the current project; deliver a written
business-case recommendation at Q4. No production rollout this year.
- **Metrics:** ≥ 7 tools scored (≥ 2–3 per category), ≥ 2 piloted hands-on, ~15-item labeled sample, 1 recommendation doc (≤ 10 pages), 100% of shortlist scored on all 4 dimensions.
- **Milestones:** **Q1 (ramp)** read up on the landscape · **Q2** plan + scorecard template + labeled sample + initial landscape map + shortlist + pilot 2 dedicated platforms · **Q3** AI-review pilot + compare vs. custom pipeline + cost/licensing outreach · **Q4** write & circulate recommendation with "recommend / not / revisit" verdicts.

**2. Versioned Code-Quality Skill Library**
Build a benchmarked, semver-tagged Claude skills library focused on code quality & review,
with a deterministic precision/recall harness.
- **Metrics:** precision ≥ 75%, recall ≥ 55%, false-positive rate ≤ 25%, tokens/task −20%, cost/task −20%, ≥ 3 skills versioned, ≥ 25 labeled fixture PRs, harness adopted by ≥ 1 other FE engineer.
- **Milestones:** **Q1 (ramp)** draft versioning convention + scout labeled-fixture candidates · **Q2** harness MVP + 10 labeled fixtures + baseline + version existing skills + first A/B upgrade (≥ 10pp precision delta) · **Q3** ship first new skill + pick reporting format + ≥ 3 minor-version upgrades with regression gate · **Q4** hit KPIs + 1 other-engineer adoption + publish reusable preset for sister products.

---

## Behaviors & Impact

**3. Cross-Product FE Architecture Contributions**
Make the current project's shared components extraction-ready, drive proper adoption of the
shared MUI theme, and establish an ADR (Architecture Decision Record) practice.
*Note: a full cross-product component library may be owned by another team; my focus is on
extraction-readiness, which is no-regret.*
- **Metrics:** ≥ 5 components tagged extraction-ready, theme violations −50% vs. Q2 baseline, 0 new violations merged on changed lines from Q4, Theme Usage Guide referenced in ≥ 8 PRs, ≥ 6 new ADRs (`docs/adr/` from 2 → ≥ 8) each reviewed + linked from implementing PR.
- **Milestones:** **Q1 (ramp)** draft ADR template + sketch extraction-ready checklist · **Q2** ADR-0003 "Extraction-Ready Shared UI Strategy" + theme audit baseline + checklist doc + tag 2 components + Theme Usage Guide + ESLint rule (warn) + ADR-0004 theme strategy + ADR-0005 shared-UI API · **Q3** tag 3 more components + ESLint rule → error-mode + ≥ 25% remediation + ADR-0006 shadcn status + ADR-0007 if cross-product coordination becomes real · **Q4** ≥ 50% remediation + coordinate on contribution path if a shared library exists + ADR-0008 year-end decisions.

**4. Internal AI Event Session + Developer-Facing Companion Skill**
Present once at an internal AI-focused event + ship a developer-pulled code-quality companion
skill (self-review / review-helper / PR-packaging modes).
- **Metrics:** 1 talk delivered + ≥ 3 follow-up adoption conversations + write-up, companion skill benchmarked via Goal 2's harness, ≥ 4 FE engineers adopt skill, ≥ 40 invocations, ≥ 60% "improved my workflow" survey, 3 modes shipped (self-review → PR-packaging → review-helper sequence).
- **Milestones:** **Q1 (ramp)** outline talk proposal + sketch skill modes · **Q2** submit talk proposal + skill design spike + test on ~5 historical PRs + ship v0.x (self-review + PR-packaging) + 2-teammate pilot · **Q3** v1.0 (all 3 modes) + broaden to ≥ 4 users + deliver the talk (or prep for H2 date) + publish write-up + v1.1 · **Q4** ≥ 40 invocations + post-pilot survey + usage report + consider transfer to sister products.

---

## Skills & Competencies

**5. Code-Health Tooling Depth + A11y + AI-Tool Evaluation**
Build real depth in the tools piloted under Goal 1, master accessibility engineering, and
evaluate AI code-quality tools.
- **Metrics:** 2 deep-dive notes (≤ 5 pages each), 0 Critical/Serious axe violations on critical paths, 2 team pairing sessions, strict `eslint-plugin-jsx-a11y` config merged, WAS (or equivalent) cert, ≥ 3 AI tools scored, AI-tool comparison doc published.
- **Milestones:** **Q1 (ramp)** scout WAS (or equivalent) courses + draft deep-dive + eval templates · **Q2** axe audit of top-10 pages + triage + WAS enrollment (2h/week) + deep-dive #1 + a11y batch 1 (wizard focus, DataGrid keyboard nav) + jsx-a11y strict · **Q3** deep-dive #2 + a11y batch 2 (color contrast, aria-live) + AI-tool comparison + WAS exam · **Q4** feed deep-dives into Goal 1 recommendation + publish a11y patterns.

**6. Forensic Code-Analysis Pipeline**
Build a code-as-crime-scene pipeline (hotspots, churn × complexity, co-change, bus factor) for
the current project's frontend and use it to drive targeted refactors.
- **Metrics:** top-10 hotspot complexity −25%, bus factor ≥ 2 on top-5 feature slices, cross-layer co-change pairs > 0.7 coupling −40%, ≥ 4 hotspot-driven refactor PRs with pre/post complexity deltas.
- **Milestones:** **Q1 (ramp)** start Tornhill ch. 1–7 notes · **Q2** local CLI prototype + top-20 hotspots baseline + scripted repeatable pipeline + decide storage/access + 1st refactor PR citing hotspot rank · **Q3** pick surfacing format + Steiger/ESLint rule proposal blocking PRs that push top-5 hotspots past a complexity ceiling + 2 refactors · **Q4** 4 total refactors with complexity + bug-incidence deltas + experimental adoption on another product's frontend.

---

## Growth & Development

**7. FE Architecture Conference + Applied Takeaways**
Attend one conference (React Conf / JSConf / React Summit / React Advanced / MUI Connect or
equivalent) and merge the learnings back as concrete PRs.
- **Metrics:** 1 conference attended, 1 trip report (≤ 2 pages), 2–3 applied-takeaway PRs/ADRs merged, each with "from session X" note in the PR body.
- **Milestones:** **Q1 (ramp)** shortlist 3 candidates + pitch to EM + register + pre-read prior-year talks · **Q2** attend (if Q2 event) + trip report within 2 weeks + 1st takeaway PR, OR continue prep · **Q3** ship remaining takeaway PRs (if Q2 event), OR attend + trip report + 1st PR (if Q3 event) · **Q4** all committed takeaways merged + retrospective.

**8. One AI-Engineering Course + One Applied Project**
Complete one course end-to-end and ship one project applying what I learned.
*Candidates: Anthropic Claude API / Agent SDK / skills track; Karpathy "AI for Devs"; DeepLearning.AI agentic systems or evals short courses.*
- **Metrics:** 1 course completed (cert or all modules done), 1 course-notes doc (≤ 3 pages), 1 applied project merged tied to the course in its PR body (likely feeds Goals 2 / 4 / 6).
- **Milestones:** **Q1 (ramp)** shortlist 3 courses + pick + enroll + notes outline · **Q2** ≥ 60% modules done + populate notes + pick applied-project idea · **Q3** finish course + ship project MVP · **Q4** v1.0 merged + publish notes + short retrospective.

---

## Why This Plan Hangs Together

- **Code quality is the anchor.** Goals 1, 5, 6 line up on understanding, measuring, and
  improving code health — each from a different angle (evaluation, depth, original analysis).
- **AI amplifies the anchor.** Goals 2, 4, 8 build AI tooling specifically tuned to code
  quality & review — not generic AI adoption.
- **Cross-product influence stays tractable.** Goal 3 commits to extraction-readiness and an
  ADR practice without depending on another team's timeline.
- **Growth is personal and scoped.** Goals 7 and 8 are single, concrete investments with
  visible artifacts — no mentoring, no multi-quarter roadmaps.

---

## Improvement Areas from FY26 Addressed

| FY26 improvement area | Addressed by |
|---|---|
| Earlier cross-team alignment | Goal 3 (ADR practice makes decisions legible ahead of time) |
| AI tool cost / efficiency / quality | Goals 2, 4, 8 (benchmarked skills, companion skill, course) |
| Planning & workload discipline | Q2 baseline capture on every goal; quarterly checkpoints |
| More active process contribution | Goal 3 (ADR practice), Goal 4 (internal AI event + companion skill rollout) |
| Backend-adjacent / end-to-end understanding | Goal 1 (evaluation touches CI, integration cost, procurement) |
| Keeping up with evolving tech | Goals 7 (conference) + 8 (AI course) |

---

## Quarterly Check-In Template

Each quarter, 30 minutes:
1. Update metrics per goal (what moved, what didn't).
2. Review milestones hit / missed / deferred.
3. Adjust Q+1 milestones if baselines or circumstances changed.
4. Note one thing to stop, one to keep, one to start.
