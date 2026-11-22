---
name: delivery-planning
description: Evaluate delivery readiness; prepare schedules and delivery breakdown only after specific Founder authorization.
---

# Delivery Planning

## Trigger and purpose

Use in SPEC_REVIEW to assess scope, dependencies and risk; use in DELIVERY_PLANNING for separately authorized planning.

## Inputs

Blueprint revision/authorization, team and workload assumptions if planning, dependencies and readiness questions.

## Procedure

1. In SPEC_REVIEW read frozen normative baseline; flag unclear MVP boundary, missing approvals, dependency/order risk and unstated staffing assumptions.
2. Avoid sprint tasks, estimated dates or commitments during SPEC_REVIEW.
3. When separately authorized for DELIVERY_PLANNING, propose staged deliverables, interfaces/dependencies, estimates with confidence and explicit resource assumptions, risk/mitigation and reporting.
4. Escalate a change that affects product behavior via PCR; keep decisions traceable.
5. Re-review only impacted scope after BA correction.

## Required output

SPEC_REVIEW: bounded readiness and risk register. Authorized planning: staged plan, assumptions, risks and review checkpoints.

## Evidence and uncertainty

Apply [evidence policy](../../../protocols/evidence-policy.md). Classify material empirical claims VERIFIED / INFERENCE / HYPOTHESIS / UNKNOWN; label other behavioral or technical verification dimensions separately. Cite claim/source IDs and dates where material. Use the compact [finding and assignment contract](../../../protocols/agent-contracts.md) when invoked by a council; do not replace actual reasoning with checkboxes.

## Failure conditions

Missing approved baseline or workload data: report uncertainty, not invented deadlines or commitments.

## Authorization and collaboration

Do not create engineering work orders, modify scope or run implementation without explicit authorized mode. See [Dev Studio lifecycle](../../../protocols/dev-studio-lifecycle.md).
