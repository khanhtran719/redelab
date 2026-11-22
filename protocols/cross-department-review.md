# Cross-department Product Blueprint review

**Purpose:** detect gaps before Founder approval, not commence engineering. Requires authorized Product Definition or a separately authorized bounded review. R&D CIO coordinates; BA owns draft revisions; Dev Studio PM, TL and QA provide independent expertise; R&D Strategist checks scope; Red Team performs last independent challenge.

## Preconditions

A recorded exact product/idea, SELECT, Founder authorization for review, frozen normative draft revision + contents/hash when useful, affected FR/BR/UX/NFR/AC, proposal vs approval statuses, and relevant source/decision constraints. Different reviewers must not unknowingly inspect different revisions. If real agents cannot be invoked, report a coordinator-only review and **do not** claim independent council completion.

## 1. Independent specialist reviews

- **Delivery PM:** delivery-readiness, hidden dependencies, scope and missing approvals; no sprint plan or invented dates.
- **Technical Lead:** specific feasibility, platform/data/permission contradictions, operational burdens; propose feasible options without rewriting business rules.
- **QA Lead:** requirement-to-AC coverage, invalid transitions, bounds, recovery, permissions and testable expected results; never claim tests were executed.

Reviewers use [agent contracts](agent-contracts.md) with real identity and original independent findings. Other specialists join only on a decision-critical issue.

## 2. Actual critique-response

Send material findings to BA/Strategist, preserve originating IDs and evidence; receive actual response: concede/revise, rebut, alternative or mark unresolved. Sent packets alone are not dialogue. Track reviewer judgment change and minority positions. Escalate product-changing proposals to Founder instead of marking APPROVED.

## 3. Bounded revision and closure

BA revises exact impacted normative artifacts, logs version/diff and changes FR/BR/UX/AC consistently. Technical Lead checks technical fixes, QA checks AC fixes, PM checks delivery impact; do not re-run unaffected reviewers. Red Team gets corrected complete spec, substantial original objections and actual replies; verify corrected content before RESOLVED. A review finding can remain OPEN without forcing invented behavior.

## 4. Final classification

- **READY_FOR_FOUNDER_REVIEW**: coherent current draft, no known critical contradiction; approvals still pending.
- **PARTIAL**: useful draft, review/reply/acceptance gaps remain.
- **BLOCKED**: unresolved product choices, infeasible requirements or critical contradictory behavior prevent reliable handoff.

Report evidence, reviewer identity, objections, replies, source/version anchors and unclosed issues. Do not equate approval of a paper review to user value, running quality, publication or implementation authorization.

## Runtime constraints

Respect configured at-most-three simultaneous specialist tasks (or fewer). Work in waves; no custom agent server, alternate CLI workers or fabricated personas if collaboration tools are missing. Do not silently resume an old budget after interruption.
