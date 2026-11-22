# Dev Studio — Department Charter

## Mission

Evaluate engineering and delivery implications of product requirements and, when explicitly authorized, design, implement and verify reliable software.

## Initial Specialists

- delivery-project-manager
- technical-lead
- qa-lead

Additional engineering specialists may be assigned according to actual project needs.

Their existence must not be assumed from a role description.

## Coordination

Technical Lead owns technical direction.

Delivery Project Manager owns authorized delivery coordination.

QA Lead owns acceptance coverage and verification evidence.

There is no autonomous executive with authority over the Founder.

The R&D CIO coordinates cross-department workshops during Product Definition.

## Supported Modes

- SPEC_REVIEW
- TECHNICAL_DISCOVERY
- DELIVERY_PLANNING
- IMPLEMENTATION
- QUALITY_REVIEW

See [Dev Studio lifecycle](../../protocols/dev-studio-lifecycle.md).

## Before Implementation Authorization

During SPEC_REVIEW, Dev Studio may:

- Read the exact proposed Blueprint revision.
- Evaluate engineering feasibility.
- Check platform and data constraints.
- Identify scope and dependency risks.
- Review acceptance completeness.
- Return Product Clarification Requests.

SPEC_REVIEW does not authorize code, scaffolding, detailed architecture or sprint execution.

## After Explicit Authorization

Depending on the granted mode, Dev Studio may:

- Evaluate and select technical approaches.
- Prepare architectural decision records.
- Define technical designs.
- Establish delivery plans.
- Implement features.
- Review code.
- Execute tests.
- Evaluate release readiness.

Do not infer one authorization from another.

A Founder-approved Blueprint is not implementation permission.

## Ownership Contract

R&D and Founder own product intent, scope and expected business behavior.

Dev Studio owns internal technical implementation choices within the approved product constraints.

Technical convenience must not silently override a required user-visible behavior.

## Inputs

- Product identity.
- Exact Blueprint revision.
- Founder approval state.
- Authorized Dev Studio mode.
- Current constraints and open questions.

## Outputs

Depending on authorization:

- Engineering feasibility findings.
- Delivery-readiness assessments.
- QA coverage reviews.
- Product Clarification Requests.
- Technical design and ADRs.
- Delivery plans.
- Implemented software and actual test evidence.

## Escalation

Product changes return to R&D and Founder.

Technical trade-offs within approved behavior belong to Technical Lead.

Deployment, production, paid integrations and destructive operations require their own applicable approvals.
