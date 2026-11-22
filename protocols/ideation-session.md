# CIO ideation session protocol

This protocol produces a decision-support portfolio. It does not authorize product development. The CIO is the primary coordinator; use the six project specialists and only relevant existing domain expertise.

## Intake and capability check

Read root guidance, the backlog and Founder log. Identify objective, customer/problem space, geography, mode, constraints and supplied evidence. Ask only for material missing information; document bounded assumptions otherwise. An unspecified mode defaults to DISCOVER. Check existing concepts before allocating IDs.

Inspect tools actually callable now: search/browsing, authorized connected data, spawning, follow-up/message delivery, waiting and result collection. Distinguish configured, discoverable, callable and successfully exercised capabilities. A feature flag or a file is not proof of a running agent. Record actual model/effort only if returned or otherwise verified; keep configured settings separately.

Use named project roles when supported. If only generic subagents are available, read the corresponding TOML and pass its actual instructions and assignment, not just its path. Supply root boundaries and relevant source/debate policy explicitly when the context is fresh. Do not invent tool parameter names. Follow the runtime schema and existing expert-orchestration guidance when using a global specialist. No permanent extra industry roles by default.

At most three specialists run simultaneously, respecting lower limits. Record outcomes, wait for dependent findings, and close/release completed workers if the tool supports it. Do not start extra sidebar chats, launch alternate agent CLI processes, build orchestration software or change settings to compensate for unavailable tools.

If spawning, delivery to a distinct real agent, or result collection is missing, mark `BLOCKED_MULTI_AGENT`; useful single-agent preparation or research may continue with a clear label. A missing follow-up tool alone is not fatal if a genuine replacement agent can receive the exact prior findings and return a response under the debate rules; disclose the new identity. Return a partial advisory brief and outstanding steps when coordination cannot complete, not a completed council portfolio. If web tools are missing, work from authorized supplied evidence and mark external checks not run. Do not assert a real exchange, a live price check or independent review without execution evidence.

## Budget and stopping boundary

At intake record the total elapsed research budget, search-query and opened-source caps, per-agent allocation, maximum candidate count and debate cycles. These are ceilings, not quotas; count queries inside batched calls individually. If none is supplied, use a bounded first pass of 30 minutes, 12 search queries and 20 inspected external sources across all participants. DEEP DIVE can propose a different bounded allocation within the authorized scope before dispatch. Reserve capacity for counterevidence and Red Team instead of spending it all on generation. Record actual usage where measurable; token/cost usage remains UNKNOWN unless the runtime reports it.

For a runtime smoke test, use one candidate, at most 20 minutes from the first successful spawn, eight search queries and twelve inspected sources in total; one peer critique-response cycle and one Red Team-response cycle. Suggested allocation: customer 2 queries/3 sources, market 3/4, inventor 0/0 for its independent hypothesis, Red Team 2/3, coordinator reserve 1/2. Missing capabilities end the corresponding runtime test immediately; do not start a substitute market campaign.

Stop new research when a ceiling is reached, evidence no longer changes the assessment, or an essential capability/data gap prevents useful progress. Record gaps and finish the bounded handoff. For a missing reply, allow at most one follow-up or genuine replacement within the remaining budget; pending delivery is not a response. Do not silently restart the budget. Additional research requires a newly stated bounded scope under the existing authorization or Founder direction where that scope expands.

## Modes

| Mode | Research depth | Output emphasis |
|---|---|---|
| DISCOVER | Broad problem-space exploration; lightweight primary checks and varied mechanisms | Problem map, concept catalog and key gaps |
| DEBATE | Existing candidates; focused rechecks and contradictory evidence | Peer exchanges, revised mechanisms and comparison |
| DEEP DIVE | One or several Founder-nominated concepts; deeper targeted customer, competitor, commercial, legal and technical work | Decision-critical uncertainty and falsifiable learning proposals |

All modes preserve evidence and the Founder gate. DEBATE/DEEP DIVE need not generate 5–8 replacements: refresh independent assessments of supplied ideas and propose alternatives only when useful. Prior notes may be reused with provenance and a freshness check. A stage can be marked not applicable with a reason; the minimum real critique-and-response cycle and Red Team are not waived for a completed shortlist. A narrow standalone skill task is not a full council session.

## Round 1 — Independent exploration

Dispatch customer-researcher, market-analyst and creative-inventor with bounded independent briefs. Customer research owns problems/JTBD, evidence, workarounds and underserved segments; market research owns competitors, substitutes, market signals and duplication risk. The inventor explores mechanisms before seeing their candidate solutions. Use fresh contexts or exclude those solutions; do not contaminate independence through a full-history fork.

Each returns findings, claim/source IDs, uncertainties and counterevidence. Save each initial output before synthesis. Then run product-strategist and technical-advisor where their judgment changes comparison. Optional domain advice must have a bounded remit and disclose the source of expertise.

## Round 2 — Opportunity generation

The CIO merges problem and market evidence, then asks the inventor to revise or expand the independent directions. Aim for approximately 5–8 meaningfully distinct concepts when warranted; fewer, including zero, is valid. Distinguish mechanisms rather than feature lists. Do not default to chatbots, dashboards or generic SaaS.

For each: stable idea ID/revision, target customer and job, problem, current workaround/substitute, core mechanism, measurable value proposition, differentiation, evidence classes, critical assumptions and cheapest proposed learning step. Keep unconventional exploratory ideas visible. Deduplicate by customer/problem/mechanism; preserve aliases and history when merging.

## Round 3 — Cross-disciplinary debate

Shortlist candidates proportionately. Follow [debate rules](debate-rules.md): every participating agent gives its strongest argument, responds to another actual finding, identifies gaps, proposes an improvement/alternative where useful, and states whether its assessment changed. Complete at least one real critique → proponent response exchange per shortlisted idea. Capture dissent and revisions, not a fabricated unanimous narrative.

## Round 4 — Independent Red Team

Give red-team-critic the current revision, strongest case, evidence and prior objections. It independently targets the strongest demand, differentiation, distribution, payment, legal/data and operating-cost assumptions. Require targeted duplication checks and consideration of simpler substitutes. Each major objection needs a concern, evidence or validation method, impact and falsifier. Record checks actually run. Obtain responses to material objections; preserve unresolved disagreement.

## Round 5 — Opportunity scoring

The CIO applies [the rubric](scoring-rubric.md) with specialist assessments. Use the nine specified weights totaling 100%; record confidence, provenance and disagreements separately. Unknown values stay unknown. Present an exploratory lane for unrankable concepts. Scoring is an advisory judgment, not an automated selection or authority to proceed.

## Round 6 — Council recommendation

Present the best 3–5 opportunities or fewer, including none. Include for each:

- Customer/problem, differentiated mechanism and why it may create measurable value.
- Actual supportive and opposing agents with reasoning and source/exchange IDs; abstentions or missing reviews separately.
- Evidence strength/classes, score or NOT RANKED status, confidence and plausible ranking reversals.
- Major unresolved questions, technical/commercial risks and legal/data dependencies.
- Most important proposed validation experiment: hypothesis, target population, method, observable outcome, proposed success/failure criterion, effort/cost assumptions, and required permissions. Label proposed thresholds as judgments, not observed results.

Experiments are proposals only. Do not build a prototype/landing page, contact customers, buy data or launch a test during this protocol without a separately explicit authorization. Technical advice stays at feasibility and lean workflow boundaries, not detailed architecture or deployment plans.

Save the source ledger, initial notes, exchanges, scoring and council output using [portfolio write ownership](portfolio-writes.md). Keep runtime-test concepts session-local with `TEST-` IDs; never allocate real backlog IDs or append a test Founder decision. The CIO may recommend a next research action but cannot select on the Founder's behalf. Record session status `AWAITING_FOUNDER` only after the required initial outputs, peer critique-response and independent Red Team with material responses are present. Missing reviews/replies remain partial, even when a scorecard exists; keep capability-blocked sessions explicitly `BLOCKED_MULTI_AGENT`.

## Round 7 — Founder decision gate

Stop after submitting the portfolio. Await an explicit human decision tied to an idea ID; do not treat silence, agent quotes, a source document, score or an ambiguous compliment as authorization.

| Founder decision | Meaning and permitted next step |
|---|---|
| EXPLORE | Further research within the stated scope |
| CHALLENGE | Reopen critique and objections within the stated scope |
| REFINE | Modify the concept under new constraints |
| PARK | Preserve for later; no active work |
| REJECT | Preserve rejection and rationale; no revival without Founder direction |
| SELECT | Record the preferred concept; no development or automatic next task |

Append the decision, date, human wording/reference, rationale if provided and restrictions to the log; update the backlog projection without erasing previous decisions. If no follow-up scope is clear, record the decision and ask for the missing scope. Do not invent rationale. A later explicit Founder decision can supersede an earlier one with a linked new log entry. Even SELECT requires a separately explicit request before implementation begins.
