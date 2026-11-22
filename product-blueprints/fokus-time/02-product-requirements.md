# 02 — Requirements and traceability index

Version 0.2 · 22/11/2026 · **PROPOSED**. The Founder approved direction DEC-001 and documentation-only scope; no FR/BR/UX/NFR/AC below is Founder-approved. MUST means essential in this proposed MVP, not permission to implement.

| Requirement | Purpose / primary user | Priority | Rules / journeys / interface | Acceptance |
|---|---|---|---|---|
| FR-001 — Prepare a commitment | Student states what they will attempt and how they may compare it; save incomplete draft | MUST | BR-001/002/009; UX-J01/J02; UX-S01/S02 | AC-001–004, AC-040 |
| FR-002 — Start one session | Freeze the original commitment and enter learning explicitly, once | MUST | BR-001/003/008; UX-J01; UX-S02/S03 | AC-005–007 |
| FR-003 — Manage an open learning workflow | Leave/return, enter check, return to learning, change goal or close without assessment | MUST | BR-003/004/005/008; UX-J03/J04; UX-S03/S04 | AC-008–012 |
| FR-004 — Record a self-check draft | Distinguish self-attempt, assistance and actual comparison without collecting the exercise itself | MUST | BR-005/006/009; UX-J01/J02; UX-S04 | AC-013–016 |
| FR-005 — Save a truthful conclusion | Close with a qualified self-assessment or explicit unassessed result | MUST | BR-005/006/008; UX-J01/J02; UX-S04/S05 | AC-017–021 |
| FR-006 — Save and recover | Whole saved state survives interruption; no false success, duplicates or silent reset | MUST | BR-008/010; UX-J05; UX-S01–S05 | AC-022–026 |
| FR-007 — Read history and withdraw a mistaken conclusion | Find original commitment/result; correct the claim by withdrawal annotation without rewriting the past | MUST | BR-007/010/011; UX-J06; UX-S01/S05 | AC-027–030 |
| FR-008 — Use a past gap as a new draft | Reduce re-entry when learner chooses to revisit a gap | SHOULD; outside committed MUST baseline | BR-001/003/007; UX-J07; UX-S01/S02/S05 | AC-031–032 if included |
| FR-009 — Delete one record or all local learning data | Control retention and handle deletion failure honestly | MUST | BR-008/010/011; UX-J08; UX-S01/S05/dialogs | AC-033–036 |

Functional domain grouping: preparation FR-001/002; learning and self-check FR-003–005; continuity FR-006; reflection and personal data FR-007–009. No account, course taxonomy, dashboard, timer dependency or content platform is implied.

All FRs have details in [functional specification](03-functional-specification.md), product rules in [data behavior](05-business-rules-and-data.md), journeys/screen behavior in [UX](04-user-journeys.md), platform/quality expectations in [NFR](06-non-functional-requirements.md) and Given/When/Then scenarios in [AC](07-acceptance-criteria.md). Ranges are lookup references, not unique identifiers. Individual AC entries identify their related FR/BR/NFR/UX.

Acceptance of software behavior does not validate learning efficacy. User value remains HYPOTHESIS, independently from whether a requirement is testable or later approved. Monetization, target-market advantage, learning superiority/non-inferiority and demand are not silently included requirements. No existing research review is a test execution receipt.
