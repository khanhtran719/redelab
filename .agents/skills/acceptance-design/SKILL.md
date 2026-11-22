---
name: acceptance-design
description: Review verifiable acceptance criteria, state transitions and test coverage without claiming tests have run.
---

# Acceptance Design

## Trigger and purpose

Use for QA-led specification review; actual QUALITY_REVIEW needs existing product artifacts and authorization.

## Inputs

Frozen product version, FR/BR/UX/NFR and proposed AC, relevant platform constraints.

## Procedure

1. Build requirement→AC coverage matrix with observable positive and negative scenarios.
2. Check boundary, invalid transition, permission, offline/recovery, interrupted persistence and platform-specific expectations where relevant.
3. Identify undefined expected outcomes or contradictory conditions, linking exact requirement IDs.
4. Propose Given/When/Then scenarios where valuable; avoid generic pass criteria.
5. Return findings to BA and inspect corrected exact revision before closure.
6. Distinguish TEST_DESIGNED vs NOT_RUN vs PASS/FAIL only with executed evidence; don't infer implementation quality from a good specification.

## Required output

Coverage matrix, missing scenario register, suggested observable AC, open decisions and verified artifact revision.

## Evidence and uncertainty

Apply [evidence policy](../../../protocols/evidence-policy.md). Classify material empirical claims VERIFIED / INFERENCE / HYPOTHESIS / UNKNOWN; label other behavioral or technical verification dimensions separately. Cite claim/source IDs and dates where material. Use the compact [finding and assignment contract](../../../protocols/agent-contracts.md) when invoked by a council; do not replace actual reasoning with checkboxes.

## Failure conditions

MUST without testable outcome or conflict between AC/BR/UX: block readiness or escalate; never assume a rule.

## Authorization and collaboration

QA review is advisory until actual authorized tests execute. See [Dev Studio lifecycle](../../../protocols/dev-studio-lifecycle.md).
