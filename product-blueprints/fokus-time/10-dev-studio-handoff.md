# 10 — Dev Studio handoff entrypoint

Version 0.2 · 22/11/2026 · **PROPOSED, pending Founder review; no execution authorization**. Read this file first. This is a documentation handoff for possible future use, not an instruction to start Dev Studio or build software.

## Product and authority

Approved direction, exact: **“Fokus Time — giúp sinh viên biến một buổi tập trung thành tiến bộ học tập có thể tự kiểm tra.”** Current SES-20261121-01, IDEA-0014, portfolio DEC-0001. Founder authorized product definition/specification review only. All detailed FR/BR/UX/NFR/AC decisions are PROPOSED. There is no approved stack, architecture, repository initialization, database/API contract, sprint/release plan or implementation scope.

Proposed primary user: university student studying one exercise/topic with their own legitimate material. Objective: end a bout with a clear self-reported conclusion/gap and find it later. No externally verified learning, sustained attention, grades, novelty or market fit is claimed. Existing worksheets/Anki/RemNote/current tools remain substitutes, no renewed selection debate required.

## Authoritative reading order

| Document | Owns |
|---|---|
| [09 decisions/open questions](09-decisions-and-open-questions.md) and [portfolio human decision](../../portfolio/decision-log.md) | Approval boundaries, defaults and unresolved meaningful choices |
| [01 vision](01-product-vision.md) | User/problem/value and claim limits |
| [02 requirements index](02-product-requirements.md) | FR/BR/UX/NFR/AC traceability and priorities |
| [05 rules/data](05-business-rules-and-data.md) | Normative states, allowed/forbidden transitions, product data semantics |
| [03 functional specification](03-functional-specification.md) | Preconditions, triggers, paths, validation, errors and recovery for every feature |
| [04 journeys](04-user-journeys.md) | User-facing actions, five interface responsibilities and shared dialogs; no mockup/layout prescription |
| [06 NFR](06-non-functional-requirements.md) | Offline/integrity/privacy/accessibility/platform and qualification gaps |
| [07 acceptance](07-acceptance-criteria.md) | Observable scenarios/independent oracle contract, NOT RUN |
| [08 MVP scope](08-mvp-scope.md) | Minimum complete product, dependencies and exclusions |
| [review record](reviews/review-record.md) and [readiness audit](reviews/readiness-audit.md) | Actual specialist critiques/replies, applied fixes and what audit does/does not prove |

Explicit Founder decisions prevail. Documents should agree; any contradiction among normative rules, UX, FR or AC requires a PCR, **not** choosing the most convenient document by precedence. Reviewer notes explain history, never silently override the published normative baseline.

## Proposed MVP and complete workflows

MUST FR-001–007 and009: save/edit draft; explicit one-time Start; manual learning/check/leave/goal-change/unassessed exit; record self-attempt/comparison status; close truthful conclusion; recover acknowledged saves; read history/withdraw wrong assessment; delete current data. FR-008 past-gap draft convenience is SHOULD and outside minimum commitment unless Founder includes it. Accessibility/privacy/integrity/offline are required quality, not optional later tasks.

Normal journey: draft goal/plan→Start freezes commitment→learn outside app→self-attempt→compare source and sufficiency→qualified self-assessment/gap→close→summary/history. Missing/assisted/uncertain: preserve facts/gaps and close UNASSESSED without pass/fail or forced retry. Interrupted: recover saved phase without inferred progress. Changed goal: old unassessed + new draft saved together. Incorrect assessed result: withdraw annotation, never rewrite original into new learning. Delete: current dataset only with clear OS-copy limitation.

## Critical invariants to carry into design/tests

1. **One open local record**, including draft; every create entry obeys the same guard.
2. **Commitment before outcome:** original goal/plan frozen at Start; actual comparison reference separately recorded; goal-change never shrinks an old success.
3. **Independent assessed eligibility:** explicit independent attempt, DONE_SUFFICIENT comparison and actual reference. Help used while solving differs from answer viewed afterward for comparison. Source text alone never sufficient.
4. **Unassessed is legitimate:** assistance/comparison facts retained truthfully, no automatic fail, no forced explanation or invented gap.
5. **Saving ≠ learning proof:** partial saves do not close, whole state acknowledged only after saved; restart/retry/stale screens never duplicate or fabricate success.
6. **Withdrawal ≠ replacement:** only eligible CLOSED-assessed records, original becomes visibly not-current everywhere, no new verdict/undo or unassessed upgrade.
7. **Data control scope:** user-retained until delete, no Fokus cloud/account/telemetry. OS backups may exist/restore old/deleted/withdrawn snapshots. No erase-every-copy/latest-restore guarantee.
8. **No inferred focus:** no timer baseline or automatically concluding from time/background/return.

These are product contracts, not instructions for database schema, transactions, clocks, idempotency implementation or module organization. Dev Studio chooses how to satisfy them after a separately authorized implementation task.

## Acceptance and known qualification risks

Use [AC-001–040](07-acceptance-criteria.md), especially AC-012/023 whole-action checks, AC-013/014/020 truthful learning-state guards and AC-040 first-New/save-boundary cases. A submitted write with lost acknowledgment may already have committed: resolve actual state before destructive discard/new/replay, never promise rollback. All scenarios NOT RUN. QA must distinguish a valid saved state from a success toast and actual self-report from demonstrated knowledge. Implement test scenarios/independent oracles, not tests that merely mirror a predicate.

Device/save failure/restore/accessibility/privacy behavior has not been exercised. OS/device support matrix, numeric performance/capacity and publication-specific obligations are OPEN-003/004/007. Backup policy OPEN-002 and detailed MVP choices OPEN-001/008 have explicit proposed defaults pending Founder approval. Research validation OPEN-005/006 remains separate; a passing app test cannot close it.

## Explicit exclusions

Timer/Pomodoro/alarms, blocking/usage capture, focus-minute truth claims, account/cloud/sync/custom backup, photo/voice evidence, AI tutor/grading/content bank, spaced repetition, social/pets/streaks, parent/teacher monitoring, payment/ads/analytics, broad course/task manager. No competitor-equivalence or platform API entitlement is assumed. If value later seems to require these, raise a new scope/clarification; don't add them to rescue the draft silently.

## Responsibilities and Product Clarification Request

Innovation Lab/Founder owns product behavior, business rules, user journeys, constraints, proposed scope and acceptance intent. Dev Studio owns later technology selection, architecture/module organization, physical data models/API contracts, implementation/testing approach and deployment/release engineering. The present package prescribes none of those and dispatches no work.

For any ambiguity/infeasibility, submit a **Product Clarification Request (PCR)** containing: affected version and FR/BR/UX/NFR/AC IDs; concrete triggering scenario; current stated behavior and contradiction/evidence; feasible options with user/data/permission/scope trade-offs; recommended product change; tests and documents affected. No invented PCR ID before an actual request. Product/Founder resolves meaningful product change; technical owner documents implementation choice only within approved behavior. Do not silently weaken a guard, change self-assessment wording, add cloud or skip recovery.

Before a future build starts, obtain separate explicit implementation authorization and confirm which proposed baseline/SHOULD items Founder accepted. READY FOR FOUNDER REVIEW never substitutes for approval, release acceptance or implementation permission.
