# Product Definition — R&D Lab

**Entry gate:** a real Founder SELECT for the named direction **and** a separate explicit Founder instruction to define the product. A SELECT by itself never begins this process. If the current conversation includes that extra instruction, a second redundant authorization is not required. Recover context from the active session and durable records; do not ask to repeat known selections. Incomplete context is labeled OPEN rather than invented.

**Owner:** R&D CIO. **Normative draft owner:** Business Analyst with Product Strategist for product scope; Customer Researcher and Technical Advisor consult when necessary. **Dev Studio reviewers:** PM, TL and QA via [cross-department review](cross-department-review.md). **Independent challenger:** Red Team.

## Lifecycle and outputs

1. **Recover:** exact decision ID/wording; selected idea revision; source ledger, dissent, rejected alternatives, technical blockers, Founder constraints; label freshness and missing information.

2. **Consolidate:** product promise, segment, primary value loop, exclusions, success hypotheses. Separate Founder APPROVED from council PROPOSED, OPEN and REJECTED; do not automatically carry all brainstormed features.

3. **Specify:** BA maps functional domains only as deeply as needed; for MUST features define actors, trigger/precondition, main + alternate paths, validation, forbidden states, data behavior, errors/recovery and user-facing feedback. Stable FR/BR/UX/NFR/AC identifiers as appropriate.

4. **Prioritize:** Strategist + BA propose MUST/SHOULD/COULD/OUT_OF_SCOPE, with a coherent full value loop, key dependencies, privacy/accessibility and measurable benefit. Estimates require grounded assumptions, not fake SLA figures.

5. **Review:** freeze exact draft baseline, consult Dev Studio PM/TL/QA in SPEC_REVIEW. Receive actual objections, obtain BA/Strategist responses and update affected IDs. Apply targeted re-review. Run independent Red Team on revised draft; record unresolved dissent.

6. **Quality gate:** every MUST has observable AC and key failure/recovery paths; traceability and referenced docs consistent; scope approved status explicit; important PCRs resolved or open/blocked. Outcome READY_FOR_FOUNDER_REVIEW / PARTIAL / BLOCKED. This is review of documentation, not verification of a running product.

7. **Founder gate:** present current proposed exact revision with unresolved product choices and their consequences. Stop. Only explicit Founder acceptance approves a normative baseline; no Dev Studio activation or implementation is implied.

## Lean Product Blueprint contract

Use as many documents as necessary, not a fixed ten-file quota. Provide discoverable entrypoint containing approved direction, status, version, authoritative files, proposed MVP, exclusions, decision ledger, business rules, journeys, NFRs, acceptance cross-references, open/blocked questions and Dev Studio handoff expectations. Keep historical raw receipts separate from normative current contract. Existing Fokus Time v0.2 is a reference example, **not** a template to copy or edit as part of organizational setup.

## Authority and disagreement

Product Strategist owns WHY, buyer/value and proposed scope; BA owns explicit WHAT/behavior; Dev Studio TL owns engineering feasibility and implementation choices under a future authorization; QA checks testability; PM checks delivery risks; Red Team independently critiques. Disagreements are actual exchanges with source IDs, not fabricated meeting minutes. Do not mark an unapproved proposal APPROVED. Changes to a Founder-approved business rule require escalation and explicit decision.

## Clarification and traceability

A Product Clarification Request (PCR) identifies product version, impacted IDs, triggering scenario, conflicting or missing behavior, user/technical/quality impacts, feasible alternatives, recommendation, product decision owner, status and affected acceptance tests. Do not allocate fictitious PCRs. After approval, preserve immutable baseline/revision and track superseding Founder choices. Studio receives a pointer to approved baseline, but intake and build authorizations are separate under [Dev Studio lifecycle](dev-studio-lifecycle.md).
