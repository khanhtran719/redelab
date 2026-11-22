# 08 — Proposed MVP boundary

Version 0.2 · 22/11/2026 · **PROPOSED; not Founder-approved scope or build authorization**.

One primary segment: university student independently studying a small exercise/topic with their own legitimate material and a comparison method. One problem: ending a bout without a clear conclusion about what they could do and what remains uncertain. One workflow: commitment→learning→self-attempt/comparison→qualified conclusion→readable gap. One proposed benefit: a useful self-reported conclusion that can guide the next bout with acceptable effort. No learning/business evidence is fabricated.

| Priority | Scope | Why essential / dependency |
|---|---|---|
| MUST | FR-001 draft/commitment and FR-002 explicit Start | A result needs a prior goal; freeze avoids rewriting goal to claim success |
| MUST | FR-003 manual workflow controls, source-not-ready/unassessed exit and goal-change split | Real sessions are interrupted and goals change; no forced pass/fail or trapped form |
| MUST | FR-004/005 self-check and qualified conclusion | This is the product's core loop, including sufficient basis, assistance and uncertainty rather than timer-based completion |
| MUST | FR-006 acknowledged save, whole actions and recovery | A lost/half goal-result or duplicate restart invalidates the record's meaning |
| MUST | FR-007 readable history and withdrawal correction | A gap must be findable, and a mistakenly entered assessed conclusion must stop appearing current without inventing a new bout |
| MUST | FR-009 scoped deletion/reset | Local personal learning content needs truthful user-controlled retention and failure behavior |
| MUST quality | NFR-001–006 and NFR-009; UX common behaviors | Offline, privacy, accessibility, durability, honest backup/retention and update behavior are quality requirements, not optional polish |
| SHOULD | FR-008 use past goal/gap as a reviewed new draft | Can reduce re-entry; not necessary for the user to manually begin a fresh bout. Only include after explicit scope approval; AC-031/032 then apply |
| COULD | No additional feature proposed | No quota to fill and no unspecified feature implied |
| OUT OF SCOPE | Timer/Pomodoro/countdown/alarms; app blocking/usage capture; focus-minute/attention claims; accounts/Fokus backup/sync; AI/content generation/grading; question bank/spaced repetition; photos/voice/upload; social/leaderboard/pets/streaks; parent/teacher portal; payments/ads/analytics SDK; full task/course manager | These add dependencies or a different product without establishing the selected loop's incremental value. They are council-proposed exclusions, not invented Founder REJECT decisions |

Past research considered a timer as an optional aid in conversation; it was never approved. Current proposal explicitly excludes it. No feature that disappeared in peer review is silently reintroduced through NFR, screen inventory or handoff.

## Functional dependency and review order

First establish the meaning of commitment/result, single slot and whole saved actions (BR-001–009/FR-006). Then demonstrate the whole FR-001→002→003→004→005 workflow including unassessed exit. Complete readable history/withdrawal/deletion and all recovery/accessibility/privacy cases; these are still MUST, not postponed safeguards. Only then consider the separately approved SHOULD convenience. This is a dependency explanation and high-level functional order, not engineering sprints or a delivery commitment.

Complexity **INFERENCE, relative**: small local text scope is lower than blocker/social/tutoring systems; two OS, state integrity, backup boundaries and assistive technology still require competent engineering/verification. Team capability/cost/calendar estimate UNKNOWN. Do not interpret “small” as production ready or permission to skip tests.

## Proposed acceptance boundary

Every MUST FR must meet its AC plus shared crash/failure/duplicate/privacy/accessibility scenarios. NFR-007/008 support/performance qualification must be resolved before claims or future sign-off; thresholds are not guessed here. Learning efficacy, app increment over worksheet/Anki/RemNote and commercial viability require separate evidence, not an added grading system or automated analytics in this MVP.

Founder approval of a scope later would still not initiate Dev Studio. Separate explicit implementation authorization and bounded scope are required.
