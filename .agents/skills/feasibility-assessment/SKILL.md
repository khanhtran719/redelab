---
name: feasibility-assessment
description: Assess small-team opportunity feasibility, technical dependencies and ongoing operational burden without detailed architecture.
---

# Feasibility Assessment

## Trigger and purpose

Use for deciding whether a product mechanism is feasible; technical architecture belongs to Dev Studio after authorization.

## Inputs

Minimal core workflow, platform/region, required data/permissions, team constraints, primary sources.

## Procedure

1. Describe smallest complete value loop and explicit exclusions.
2. Build dependency ladder: REQUIRED/OPTIONAL, documented capability, actual access, policy/rights, cost units, failure impact, fallback and verification needed.
3. Separate UNKNOWN, DOCS_VERIFIED, ACCESS_VERIFIED and EXERCISED; checking docs does not prove user-account access or successful device behavior.
4. Examine privacy/security, vendor lock-in, failure/recovery, support and maintenance across changes.
5. Identify what makes the lean MVP infeasible, and a targeted verification step without implementation.
6. Review product-level NFRs for an authorized Blueprint; leave architecture to Dev Studio TL.

## Required output

Lean scope, data/access table, operational burden, feasibility confidence, conditional blockers, alternatives and evidence gaps.

## Evidence and uncertainty

Apply [evidence policy](../../../protocols/evidence-policy.md). Classify material empirical claims VERIFIED / INFERENCE / HYPOTHESIS / UNKNOWN; label other behavioral or technical verification dimensions separately. Cite claim/source IDs and dates where material. Use the compact [finding and assignment contract](../../../protocols/agent-contracts.md) when invoked by a council; do not replace actual reasoning with checkboxes.

## Failure conditions

Essential inaccessible data, unsupported APIs, missing lawful rights or unbounded operating effort: mark conditional/blocking, not positive feasibility.

## Authorization and collaboration

No product code, architecture diagrams, deployments or account changes. Route detailed design to authorized Dev Studio.
