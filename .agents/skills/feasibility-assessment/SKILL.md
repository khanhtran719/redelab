---
name: feasibility-assessment
description: Evaluate whether a software opportunity has a credible small-team workflow, data access, integration path and manageable operating burden. Use for comparative ideation feasibility; not detailed architecture, prototypes or implementation.
---

# Feasibility assessment

## Purpose and inputs

Expose technical dependencies that change opportunity choice. Inputs: concept/current workflow, target segment, team capabilities, required data/integrations, jurisdictions and constraints. Missing capabilities remain assumptions.

## Procedure

1. Describe the smallest coherent workflow that delivers the core customer value, plus exclusions. Do not design components or a repository.
2. List necessary data, rights, APIs and third parties. Verify decision-critical capability, access conditions, availability and costs against current primary documentation.
3. Assess complexity, security/privacy constraints, integration volatility, manual operations, failure recovery, maintenance and third-party lock-in.
4. Estimate only useful cost ranges with explicit usage units and dated price assumptions. Name unknowns and thresholds where the idea becomes impractical.
5. Compare simpler approaches and propose targeted verification steps. Flag jurisdiction-dependent questions for bounded specialist advice when necessary.

## Expected outputs

Lean workflow boundary, feasibility judgment/confidence, dependency and data-access table, cost assumptions, maintenance/security constraints, engineering unknowns and proposed evidence needed. No claim of production readiness.

## Evidence requirements

Use [evidence policy](../../../protocols/evidence-policy.md). Never invent an API, permission, integration entitlement, cost or legal clearance. Mark docs verified separately from integration exercised; documentation does not prove access for this account.

## Failure conditions

Essential inaccessible data, unsupported API, unknown rights, unbounded operations or team mismatch: identify a blocker/condition rather than assuming a future fix. Unknown facts are not a positive feasibility result.

## Boundaries

No code, prototype, scaffolding, detailed architecture diagrams, infrastructure, deployment scripts/plans, installations or account changes. Founder decisions are human; SELECT is not build authorization. Return advisory comparisons and follow [debate rules](../../../protocols/debate-rules.md) only for assigned peer review.
