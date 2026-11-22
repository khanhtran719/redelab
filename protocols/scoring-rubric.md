# Opportunity scoring

Use scores to expose judgments, not to disguise missing evidence. Evaluate the current candidate revision after peer debate and Red Team review. The Founder is not bound by scores.

| Criterion | Weight | 1 — weak | 5 — mixed | 10 — strong |
|---|---:|---|---|---|
| Customer problem severity | 20% | Minor inconvenience | Recurring material friction | Severe frequent loss or blocked essential work |
| Evidence of demand | 15% | Observed disinterest or failed behavior test | Relevant pain with some action | Repeated credible behavioral commitment in the target segment |
| Meaningful differentiation | 15% | Comparable substitutes already suffice | Useful distinction with uncertain outcome gain | Distinct mechanism with demonstrated customer advantage |
| Distribution feasibility | 15% | No credible affordable access | Plausible reachable channel, untested conversion | Repeatable demonstrated access and adoption route |
| Small-team technical feasibility | 10% | Critical inaccessible dependency or excessive burden | Feasible with material unresolved risks | Core workflow/data access supported with manageable upkeep |
| Monetization potential | 10% | Buyer/value capture contradicted | Plausible buyer and payment hypothesis | Credible payment behavior and sustainable economics |
| Legal and data feasibility | 5% | Evidenced barrier to necessary lawful access/use | Plausible path with specific unresolved constraints | Relevant rights and requirements verified for the context |
| Long-term defensibility | 5% | Easily substituted with no retention advantage | Plausible but unproven durable advantage | Evidence-backed compounding advantage and customer retention |
| Fit for a lean MVP | 5% | Value requires a large complete system | Narrow useful boundary with dependencies | Small coherent workflow can test core value independently |
| **Total** | **100%** | | | |

## Per-criterion record

Use integer scores 1–10 when a reasoned assessment is possible; intermediate values interpolate between anchors. Each row records score, rationale, evidence/claim IDs, evidence class, confidence (`LOW`, `MEDIUM`, `HIGH` with reason), opposing view and any plausible score interval. A high-confidence unfavorable finding is different from a favorable low-confidence hypothesis.

Use `UNKNOWN` instead of a number when there is no defensible assessment. Unknown is neither zero nor five. A speculative score is allowed only as an explicitly labeled scenario (`HYPOTHESIS`), never as observed commercial evidence.

## Calculation and missingness

For fully assessed candidates, `weighted score (1–10 scale) = sum(weight_percent × score) / 100`. Report at most one decimal place. Do not conflate this index with a success probability.

For incomplete candidates, report assessed weight and evidence coverage, leave the total `NOT RANKED`, and keep the candidate in an exploratory lane. Do not renormalize remaining weights to 100%. Optionally display the possible total interval by assigning 1 and 10 to each unknown row, explicitly labeled a bound, not a prediction. For example, an unknown 20% criterion contributes between 0.2 and 2.0 points to the /10 index. No test ideas or invented values enter the real backlog.

Separate evidence coverage (weight supported by VERIFIED claims or traceable INFERENCE) from assessed weight (weight with numeric scores). Hypotheses can increase assessed weight but do not establish evidence coverage. A complete hypothetical score remains exploratory, not evidence-qualified for commercial ranking.

A candidate enters a provisional commercial comparison only when all rows have defensible assessments, demand, differentiation and distribution are supported beyond speculation, and critical data/legal dependencies have been examined. Record any remaining hypothesis and confidence. Absence of demand evidence belongs in the exploratory lane; verified negative demand evidence can justify a low numeric score. This eligibility rule is a council convention, not Founder approval.

## Interpretation

Show how uncertain high-weight criteria could reverse the order; call near-overlapping candidates a tie or uncertain ordering. Do not reward fashionable technology, artificial precision or a pile of dependent citations. Flag evidenced legal/data blockers or essential inaccessible dependencies separately; a weighted total cannot cancel them. A blocker may lead the CIO to recommend PARK/REJECT, but only the Founder records that decision.

Keep promising exploratory mechanisms visible with their key falsification experiment. Present fewer than 3–5 recommendations, including zero, when warranted. Confidence and evidence strength accompany every recommendation, independent of score.

## Research priority is separate

Commercial comparison uses only the eligibility and scoring rules above. Separately, the CIO may prioritize a learning question for an unranked idea: decision-critical uncertainty, result that would change the assessment, accessible authorized evidence, expected effort/cost and reason to investigate now. Use `HIGH`, `MEDIUM`, `LOW` or `UNKNOWN` with a rationale; this is an advisory judgment, not a second commercial score or a success probability. If access or effort is unknown, make priority conditional or UNKNOWN. High research priority can coexist with low commercial viability when a cheap falsifier would resolve a consequential uncertainty. Do not turn priority into EXPLORE/SELECT or execute a proposed experiment without its required authorization.

| Idea/revision | Commercial eligibility / score | Research priority / confidence | Decision-changing question | Proposed evidence / effort / access | Reason and stopping condition |
|---|---|---|---|---|---|
