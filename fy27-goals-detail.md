# FY27 SMART Goals — Senior Front-End, Competence Growth Plan (Detail)

> **Draft — bound to change.** This is a working plan, not a commitment. Goals, metrics,
> and milestones will be revised as baselines are captured in Q2 and as circumstances
> evolve through the year.

**Role:** Senior FE, AA26 DSPM (Netwrix)
**Horizon:** 2026-04 → 2027-04. **Q1 is ramp-up** (planning, shortlisting, enrolment, light
pre-reading). Active execution runs **Q2–Q4** with quarterly check-ins.
**Anchor themes:** AI Engineering Excellence + Frontend Quality & Architecture
**Summary:** see [fy27-goals.md](./fy27-goals.md)

**Baseline posture:** Q2 of every goal includes baseline capture.

---

# Results & Outcomes

## 1 — Code-Health Tooling Evaluation & Business-Case Recommendation

Year-long evaluation → Q4 written recommendation. No production rollout this year.

**Specifics** — Score candidates across 3 categories (dedicated platforms like
SonarQube / CodeScene / Codacy; AI review tools like CodeRabbit / Greptile / Qodo; our
custom forensic pipeline from Goal 6) on 4 dimensions: signal quality, integration cost,
cost / licensing, team friction / DX.

**Metrics (Q4 targets)**
- ≥ 7 tools scored (≥ 2–3 per category) · ≥ 2 piloted hands-on
- ~15-item labeled sample (AA26 files/PRs with known issues tagged)
- 1 recommendation doc (≤ 10 pages) at `docs/ai-engineering/code-health-tooling-evaluation.md`
- 100% of shortlist scored on all 4 dimensions

**Quarterly**
- **Q1 (ramp)** read up on the tooling landscape; no deliverables committed
- **Q2** plan + scorecard template + labeled sample + initial landscape map + shortlist + pilot 2 dedicated platforms
- **Q3** AI-review pilot + compare against custom pipeline + cost/licensing outreach
- **Q4** write & circulate recommendation with "recommend / not / revisit" verdicts

**Evidence** — Recommendation doc, labeled sample, pilot notes, scorecard, vendor cost
summaries.

**Risks** — Shallow "tool review blog post" → commit to ≥ 2 hands-on pilots. Vendor sales
cycles → start procurement outreach early Q3. Scope creep to rollout → "evaluation" is in the
title; Q4 deliverable is a doc, not a CI change. Compressed execution (3 active quarters) →
keep scorecard shallow on clearly-unfit candidates; depth only where it matters.

---

## 2 — Versioned Claude Skill Library for Code Quality & Review

Semver-tagged skill library with a deterministic precision/recall harness. Exact skill list
decided iteratively from any pre-existing review-oriented skills, adding new skills only
where a clear gap is visible in the labeled sample.

**Specifics** — Harness replays fixed prompts + labeled PR inputs, asserts pass via existing
oracles (`typecheck`, `lint`, `test:run`, `test:architecture`) + precision/recall for review
skills. JSONL results; reporting format (CSV / dashboard / PR comment / etc.) decided later.

**Metrics (Q4 targets)**
- Review skills: precision ≥ 75%, recall ≥ 55%, false-positive rate ≤ 25% (held-out labeled PRs)
- Tokens/task −20%, cost/task −20% vs. Q2 baseline
- ≥ 3 code-quality skills versioned + changelog · ≥ 25 labeled fixture PRs
- Harness adopted by ≥ 1 other FE engineer; reusable preset for 1Secure

**Quarterly**
- **Q1 (ramp)** draft versioning convention + scout labeled-fixture candidates from merged PRs
- **Q2** harness MVP on 1 existing review skill + 10 labeled fixtures + baseline + version/benchmark existing skills + first A/B upgrade (≥ 10pp precision delta)
- **Q3** ship first new skill where a gap is confirmed + pick reporting format + ≥ 3 minor-version upgrades with regression gate
- **Q4** hit KPIs + 1 other-engineer adoption + publish preset for 1Secure

**Evidence** — Git history on `.claude/skills/` with semver tags + CHANGELOGs; harness
source; labeled fixture set; JSONL logs; reusable preset package.

**Risks** — Fixture cost → seed from merged PR review comments, +5/quarter. Precision vs.
recall trade-off → precision first. Over-expanding skill set → only add when labeled sample
shows a real gap.

---

# Behaviors & Impact

## 3 — Cross-Product FE Architecture Contributions

Three tracks: extraction-ready components, Netwrix MUI theme adoption, ADR practice.

> **Note on `@netwrix/ui` ownership.** Graduating `@netwrix/theme` (v0.1.27) into a full
> cross-product library may be owned by another team. My commitment is extraction-readiness
> — no-regret whether or not `@netwrix/ui` ships this year.

**Specifics**
- **Extraction-ready components** — written checklist (theme-first; minimal deps; stable
  public API; Storybook-ready demo; usage notes). List maintained in
  `services/frontend/webapp/docs/extraction-ready-components.md`.
- **Theme adoption** — audit 4 violation categories (hardcoded colors, spacing, ad-hoc `sx`
  vs. variants, ad-hoc typography). Publish Netwrix MUI Theme Usage Guide. Ship ESLint rule
  that flags new violations on changed lines.
- **ADRs** — extend `docs/adr/` with a template, review expectation, and sequential numbering
  for every significant FE architecture decision.

**Metrics (Q4 targets)**
- ≥ 5 components tagged extraction-ready (candidates: AppBreadcrumbs, Nav, FormDrawer,
  FormSection, StatusIndicator, DeleteConfirmationDialog, Toaster, WizardProgressIndicator)
- Theme violations −50% vs. Q2 baseline; 0 new violations merged on changed lines from Q4
- Theme Usage Guide referenced in ≥ 8 PR descriptions/reviews
- ≥ 6 new ADRs (`docs/adr/` from 2 → ≥ 8); each reviewed + linked from implementing PR

**Quarterly**
- **Q1 (ramp)** draft ADR template + sketch extraction-ready checklist; no components tagged yet
- **Q2** ADR template + README + ADR-0003 "Extraction-Ready Shared UI Strategy" + theme audit
  baseline + checklist doc + tag 2 components + publish Theme Usage Guide + ESLint rule (warn)
  + ADR-0004 theme strategy + ADR-0005 shared-UI API conventions
- **Q3** tag 3 more components + ESLint rule → error-mode on changed lines + ≥ 25% remediation
  + ADR-0006 shadcn status + ADR-0007 if cross-product coordination becomes real
- **Q4** ≥ 50% remediation + coordinate on contribution path if `@netwrix/ui` exists + ADR-0008
  year-end decisions

**Evidence** — Extraction-ready list + tagged components, theme audit report + trend,
Netwrix MUI Theme Usage Guide, ESLint rule source + CI config, ADRs 0003–0008+, component PRs.

**Risks** — No `@netwrix/ui` this year → extraction-ready work is no-regret anyway. MUI ↔
shadcn split → tag only MUI components extraction-ready. Remediation fatigue → "no new
violations" first, then PR-sized batches paired with feature work. ESLint false positives →
warn-mode for one quarter (Q2) before error-mode (Q3). ADR paperwork → ≤ 1-page template,
ADR-worthy bar defined in README.

---

## 4 — AIdeas Session + Developer-Facing Companion Skill

Two coupled deliverables: one AIdeas talk + a developer-pulled code-quality companion skill
(not an auto-commenting PR bot).

**Specifics**
- **AIdeas session** — 30–45 min on code-quality AI tooling in AA26 (Goals 1, 2, 6 +
  companion skill). Deck, recording, and write-up at `docs/ai-engineering/aideas-session.md`.
- **Companion skill** — first-class skill in `.claude/skills/` with three dev-invoked modes:
  - Self-review mode — runs on staged diff before push; surfaces code-health, FSD boundary
    issues, test gaps, duplication, complexity hotspots.
  - Review-helper mode — runs on a target PR branch; structured review briefing (risky
    files, complexity deltas, coverage of changed lines, suggested questions).
  - PR-packaging mode — generates PR description + self-review checklist tailored to the
    change (hotspot? shared component? new dep?).

**Metrics (Q4 targets)**
- 1 AIdeas talk delivered + ≥ 3 follow-up adoption conversations + write-up
- Companion skill benchmarked via Goal 2 harness
- Adopted by ≥ 4 FE engineers · ≥ 40 invocations logged · ≥ 60% "improved my workflow" survey
- 3 modes shipped (self-review → PR-packaging → review-helper sequence)

**Quarterly**
- **Q1 (ramp)** outline AIdeas talk proposal + sketch skill modes on paper
- **Q2** submit AIdeas proposal + skill design spike + test on ~5 historical PRs + ship v0.x (self-review + PR-packaging) + 2-teammate pilot + refine talk deck
- **Q3** v1.0 (all 3 modes) + broaden to ≥ 4 users + deliver AIdeas talk (or prep for H2 date if event is later) + publish write-up + v1.1
- **Q4** ≥ 40 invocations + post-pilot survey + usage report + consider 1Secure transfer

**Evidence** — Skill source + changelog, AIdeas deck + recording + write-up, usage-log
excerpts, pilot feedback, survey results.

**Risks** — AIdeas proposal rejected / event slips → fallback is internal FE demo + written
article. Low adoption → Q2 pilot shapes DX first; usage stays voluntary. Scope creep across
modes → ship sequentially, each with a single clear intent.

---

# Skills & Competencies

## 5 — Tool Depth + Accessibility + AI Code-Quality Tooling Eval

Three tracks, all feeding Goal 1's recommendation doc.

**Specifics**
1. **Code-health tooling depth** (tracks Goal 1 pilots) — for each tool piloted, go deep
   on rule system / plugin model, configuration, CI integration, cost/ops model. Written
   "deep-dive" notes; no custom rule shipping — depth for evaluation credibility.
2. **Accessibility engineering** — WCAG 2.2 AA proficiency; axe audit of top-10 pages;
   keyboard + ARIA patterns; strict `eslint-plugin-jsx-a11y`; WAS (or equivalent) cert.
3. **AI code-quality tool eval** — compare ≥ 3 AI review tools (CodeRabbit, Greptile, Codacy,
   Qodo, …) on the same labeled sample using the Goal 2 precision/recall methodology.

**Metrics (Q4 targets)**
- 2 deep-dive notes in `docs/ai-engineering/tool-deep-dives/` (≤ 5 pages each)
- 0 Critical/Serious axe violations on critical paths; 2 team pairing sessions; strict jsx-a11y
  config merged; WAS (or equivalent) cert earned
- ≥ 3 AI tools scored on labeled sample; comparison doc at
  `docs/ai-engineering/tool-eval-codequality.md` (becomes Goal 1's AI-review scorecard)

**Quarterly**
- **Q1 (ramp)** scout WAS (or equivalent) courses + draft deep-dive + eval templates
- **Q2** axe audit of top-10 pages + triage + WAS enrollment (2h/week) + deep-dive #1 + a11y batch 1 (wizard focus, DataGrid keyboard nav) + jsx-a11y strict
- **Q3** deep-dive #2 + a11y batch 2 (color contrast, aria-live) + AI-tool comparison + WAS exam
- **Q4** feed deep-dives into Goal 1 recommendation + publish a11y patterns

**Evidence** — Deep-dive notes, AI-tool comparison doc, axe CI history + triage reports,
WAS cert, a11y patterns doc.

**Risks** — Shallow deep-dive notes → each must include a "non-obvious finding" only visible
after hands-on use. Overlap with Goal 1 AI-review category → by design; single source of
truth cited from Goal 1. WAS exam slips → fallback to Deque or WebAIM certificate.

---

## 6 — Forensic Code-Analysis Pipeline

Code-as-crime-scene pipeline for the AA26 frontend; drives data-backed refactor prioritization.

**Specifics** — Mine `git log` on `services/frontend/webapp/src/` for per-file churn,
complexity (`eslint-plugin-sonarjs` / `complexity-report`), hotspot score (churn × complexity),
co-change pairs, author knowledge concentration. Storage & surfacing format + automation
frequency decided later based on what's useful — commitment is to the analysis, not a stack.

**Metrics (Q4 targets)**
- Avg cyclomatic complexity on top-10 hotspots −25%
- Bus factor ≥ 2 on top-5 feature slices
- Cross-layer co-change pairs > 0.7 coupling −40%
- ≥ 4 hotspot-driven refactor PRs with pre/post complexity deltas

**Quarterly**
- **Q1 (ramp)** start Tornhill ch. 1–7 notes in `docs/ai-engineering/forensics-notes.md`
- **Q2** local CLI prototype → top-20 hotspots, avg complexity, bus-factor baseline + scripted
  repeatable pipeline + decide storage/access + 1st refactor PR citing hotspot rank
- **Q3** pick surfacing format (dashboard / report / PR comment / digest) + Steiger/ESLint rule
  blocking PRs that push top-5 hotspots past a complexity ceiling + 2 refactors
- **Q4** 4 total refactors with complexity + bug-incidence deltas + experimental adoption on 1Secure

**Evidence** — Pipeline source in `services/frontend/webapp/scripts/forensics/` (or equiv.);
surfacing artifact; refactor PRs with before/after metrics; forensics notes.

**Risks** — Git-log noise (renames, squash-merges) → `--follow`, `--find-renames`, exclude
generated files, validate against manual top-10. Refactor sprawl → ≤ 5 days per PR with a
measurable complexity delta; slice incrementally along FSD boundaries.

---

# Growth & Development

## 7 — FE Architecture Conference + Applied Takeaways

One conference this year (React Conf / JSConf / React Summit / React Advanced / MUI Connect
or equivalent) → translate into merged PRs so the time produces tangible output, not just notes.

**Metrics (Q4 targets)**
- 1 conference attended · 1 trip report (≤ 2 pages) at
  `docs/ai-engineering/conference-trip-report.md`
- 2–3 applied-takeaway PRs/ADRs merged, each with "from session X" note in the PR body

**Quarterly**
- **Q1 (ramp)** shortlist 3 candidates + pitch to EM + register + pre-read prior-year talks
- **Q2** attend (if Q2 event) + trip report within 2 weeks + 1st takeaway PR, OR continue prep
- **Q3** ship remaining takeaway PRs (if Q2 event), OR attend + trip report + 1st PR (if Q3 event)
- **Q4** all committed takeaways merged + retrospective

**Risks** — Budget/time approval slips → shortlist includes ≥ 1 virtual/low-cost option.
Forced takeaways → bar is "genuinely improves something", not "big"; skipping is fine.

---

## 8 — One AI-Engineering Course + One Applied Project

One course end-to-end + one project merged, so learning produces a concrete artifact.

**Candidates** — Anthropic Claude API / Agent SDK / skills track; Karpathy "AI for Devs";
DeepLearning.AI agentic systems or evals short courses.

**Metrics (Q4 targets)**
- 1 course completed (cert or all modules done)
- 1 course-notes doc (≤ 3 pages) at `docs/ai-engineering/course-notes.md`
- 1 applied project merged into the repo, tied to the course in its PR body; likely feeds
  Goals 2 / 4 / 6 so effort compounds

**Quarterly**
- **Q1 (ramp)** shortlist 3 courses + pick + enroll + notes outline
- **Q2** ≥ 60% modules done + populate notes + pick applied-project idea
- **Q3** finish course + ship project MVP
- **Q4** v1.0 merged + publish notes + short retrospective

**Risks** — Course time displaced → recurring weekly block; if it slips, cut project scope,
don't finish at any cost. Project scope creep → cap at ≤ 1 week focused work; split to next
year if bigger.

---

# Critical Files & Anchors

- [services/frontend/webapp/.claude/skills/](services/frontend/webapp/.claude/skills/) — versioning + benchmarking target (Goal 2)
- [services/frontend/webapp/.claude/CLAUDE.md](services/frontend/webapp/.claude/CLAUDE.md) — FSD rules, Container pattern, Metabase workaround
- [services/frontend/webapp/src/shared/ui/AppBreadcrumbs/](services/frontend/webapp/src/shared/ui/AppBreadcrumbs/) — likely first extraction-ready component
- [docs/adr/](docs/adr/) — ADR repo (extend ADR-0001 / ADR-0002 onward)
- [lefthook.yml](lefthook.yml) — integration point for benchmark CI gates
