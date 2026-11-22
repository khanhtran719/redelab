# Dev Studio modes and authority

Dev Studio is a logical department within Redelab, not a runtime security sandbox. Root Codex configuration and `agents.max_concurrent_threads_per_session` remain applicable. A mode is an authorization scope, not a permission bypass; all external deployment, account, payment and destructive operations require applicable approvals.

| Mode                  | Entry authorization                                                             | Allowed                                                                         | Excluded                                                                    |
| --------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `SPEC_REVIEW`         | Explicit bounded review or part of authorized Product Definition                | Read frozen Blueprint; PM/TL/QA return risks, testability and PCRs              | Code, scaffolding, detailed architecture, sprint plan                       |
| `TECHNICAL_DISCOVERY` | Separate Founder technical investigation instruction                            | Evaluate stack, architecture options, ADRs, data/integration/testing approaches | Product implementation; silent rule changes                                 |
| `DELIVERY_PLANNING`   | Separate Founder delivery planning instruction                                  | Dependencies, slices, work items, estimates with staffing assumptions, risks    | Automatic code, false schedules, new business scope                         |
| `IMPLEMENTATION`      | Explicit Founder implementation request with product baseline and bounded scope | Source code, repo scaffolding, application tests, authorized technical work     | Unrequested features, independent production deploy or paid service changes |
| `QUALITY_REVIEW`      | Access and scoped permission for actual artifacts                               | Code/test review, executed test evidence, regression and release risks          | Fictional PASS, implicit production approval                                |

## Product lifecycle gates

1. R&D publishes PROPOSED Blueprint at exact version for Founder review after [cross-department review](cross-department-review.md).
2. Founder explicitly approves a full or restricted Blueprint revision; register exact approved scope. Missing approval remains PROPOSED.
3. Dev Studio may perform authorized intake against that baseline, acknowledge understanding and create PCRs. Intake is not engineering authorization.
4. Separate Founder instruction activates TECHNICAL_DISCOVERY, DELIVERY_PLANNING or IMPLEMENTATION, each only within its stated scope. These stages may be combined in one explicitly authorized message if each boundary and deliverable is clear; do not demand redundant approvals.
5. QA tests must be linked to actual test commands/artifacts; an AC on paper is not a test result.

## Decision ownership

R&D/Founder controls WHAT/WHY and business/user behavior. Dev Studio TL controls HOW only when technical work is authorized and outcome stays within approved behavior. PM coordinates delivery but cannot approve new scope. QA reports coverage and evidence, not product approval. Unclear or infeasible product behavior → PCR; affected requirements and acceptance criteria remain pending until resolved by correct owner.

## No autonomous transitions

A finished review does not start discovery; completed discovery does not start planning; accepted plan does not start coding; passing tests does not deploy automatically. Explicitly record missing inputs and return decision-ready options.
