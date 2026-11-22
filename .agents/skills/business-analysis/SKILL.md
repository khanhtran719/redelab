---
name: business-analysis
description: Specify approved-direction business workflows, functional requirements, rules and acceptance intent during authorized Product Definition.
---

# Business Analysis

## Trigger and purpose

Use after a real SELECT plus explicit Product Definition authorization, or for bounded requirement clarification.

## Inputs

Founder decision/reference, selected concept, source evidence, authorized scope, current version and constraints.

## Procedure

1. Recover approved direction, unresolved decisions and term definitions; separate APPROVED / PROPOSED / OPEN / REJECTED.
2. Model actors, preconditions, triggers, core/alternate/error flows, states/invariants, data behavior and recovery for each MUST feature.
3. Assign stable FR/BR/UX/AC and decision references; never invent a business answer to close a gap.
4. Ensure journeys, rules and acceptance criteria agree; link dependencies and scope exclusions.
5. Freeze draft revision for cross-department review, respond to named PM/TL/QA findings and revise affected normative artifacts.
6. Build source-of-truth and Dev Studio handoff with PCR process. Stop at Founder approval gate.

## Required output

Lean Product Blueprint and requirement traceability, uncertainties, reviewer replies, changes and handoff brief.

## Evidence and uncertainty

Apply [evidence policy](../../../protocols/evidence-policy.md). Classify material empirical claims VERIFIED / INFERENCE / HYPOTHESIS / UNKNOWN; label other behavioral or technical verification dimensions separately. Cite claim/source IDs and dates where material. Use the compact [finding and assignment contract](../../../protocols/agent-contracts.md) when invoked by a council; do not replace actual reasoning with checkboxes.

## Failure conditions

Blocking unresolved business semantics or contradictory mandatory behavior: mark PARTIAL/BLOCKED rather than READY.

## Authorization and collaboration

No product code, detailed architecture or Founder approval. Use [Product Definition](../../../protocols/product-definition.md) and [cross-department review](../../../protocols/cross-department-review.md).
