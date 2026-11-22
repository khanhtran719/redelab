---
name: technical-feasibility-review
description: Review precise engineering implications of product requirements; architecture is authorized separately.
---

# Technical Feasibility Review

## Trigger and purpose

Use by TL during SPEC_REVIEW; use for deeper TECHNICAL_DISCOVERY only when explicitly authorized.

## Inputs

Frozen Blueprint version, affected FR/BR/NFR/AC, platform constraints and primary source docs.

## Procedure

1. Review implementation feasibility of exact business behaviors, platform/API constraints, integrity and failure recovery.
2. Distinguish documented capability, actual permitted access and exercised behavior.
3. Identify hidden blockers and offer bounded engineering options, cost/complexity, user-visible trade-offs and unknowns.
4. Raise PCR for product-level changes; never silently narrow an approved requirement.
5. Inspect corrected artifact for closure of feasibility objection.
6. Under separate TECHNICAL_DISCOVERY authorization only, develop technical options/ADRs/architecture to required depth; no implementation automatically.

## Required output

Traceable TL finding register, impacted requirements, evidence and feasible alternatives; authorized ADRs only in technical-discovery mode.

## Evidence and uncertainty

Apply [evidence policy](../../../protocols/evidence-policy.md). Classify material empirical claims VERIFIED / INFERENCE / HYPOTHESIS / UNKNOWN; label other behavioral or technical verification dimensions separately. Cite claim/source IDs and dates where material. Use the compact [finding and assignment contract](../../../protocols/agent-contracts.md) when invoked by a council; do not replace actual reasoning with checkboxes.

## Failure conditions

Requirement infeasible or contradictory and owner response missing: keep unresolved; do not pretend planned changes are delivered.

## Authorization and collaboration

No code/project setup without explicit IMPLEMENTATION authorization. Follow [cross-department](../../../protocols/cross-department-review.md).
