# Cross-agent debate

Use actual subagent outputs. The CIO can relay messages when peer-to-peer messaging is unavailable; a relay must identify the originating agent, output/finding ID and any summarization. Relay is genuine exchange only when a different agent actually receives and responds to it.

## Independence and assignments

Give each specialist the objective, mode, constraints, relevant facts, deliverable, source policy, deadline/budget if supplied, and edit ownership. Do not provide the CIO's preferred answer. Round 1 uses a fresh context or a prompt that excludes other agents' candidate solutions and rankings, especially for the inventor. Do not use a full-history fork containing candidates and call it independent exploration.

Record returned runtime IDs and initial findings before showing other solutions. Sequential fresh agents are acceptable when concurrency is low. For later rounds, reuse a real agent via follow-up when supported; otherwise start a genuine replacement with the exact prior record and disclose the identity change. Do not claim unavailable model overrides were applied.

Specialists normally return messages; the CIO writes the shared records. An exclusive notes path may be assigned to one agent. No concurrent writes to the backlog, decision log or synthesis. No further delegation unless specifically assigned by the CIO.

## Critique-and-response cycle

For each shortlisted idea:

1. Assign at least two relevant specialists, with different remits, actual candidate/evidence records and each other's substantive findings.
2. Each returns: strongest argument for or against; response to at least one named finding from another agent; missing evidence; improvement/alternative where useful; assessment before and after, including why it changed or remained unchanged.
3. Relay each material objection to the original proponent or responsible specialist. Obtain an actual response: concede, revise, rebut with evidence, or leave unresolved with a proposed test. Capture at least one complete objection → response exchange for every shortlisted idea.
4. Freeze the resulting candidate revision and evidence packet for the independent Red Team. The Red Team receives the strongest case and contrary evidence, without a requirement to agree. After its critique, obtain a proponent response for material objections before final scoring, or record the missing response as incomplete debate.

An agent may retain dissent. A count of supporters is descriptive, not evidence, voting authority or consensus. The CIO must not write missing replies on an agent's behalf. If there is only one active role or no reply capability, mark `BLOCKED_MULTI_AGENT`/partial review and explain what did not occur.

## Traceable exchange

Record exchange ID, idea ID/revision, source agent/runtime ID, target agent/runtime ID, originating finding IDs, objection, response, evidence IDs, assessment change and unresolved question. Use verbatim quotations only for actual text, otherwise identify a paraphrase. Keep initial notes immutable; append revisions.

For each delivery, preserve the actual sent packet (or a faithful excerpt with its artifact locator), originating claim, sender/recipient runtime IDs, tool name, returned message/task ID when available, send/result time and returned response locator. If the runtime omits message IDs, say so and preserve the exact payload plus tool-returned agent identity and output; never invent an ID. Distinguish `PREPARED`, `SENT`, `RESPONDED` and `FAILED_OR_UNKNOWN`. An acknowledged send or a timeout does not establish that the peer processed the finding. An exchange is complete only when a different real agent's response explicitly addresses the named originating finding and the proponent actually answers the objection. Record assessment before/after, including unchanged assessments. These are record states, not an orchestration service.

A major objection states the underlying concern, why it could defeat the opportunity, supporting evidence or a feasible validation method, and what observation would reduce the concern. Skepticism must be falsifiable; automatic negativity is not independent review.

## Stop rules

One complete cycle is the minimum for a shortlist when tools are available. Add another only for material new evidence or a resolvable consequential disagreement. Stop unproductive repetition; preserve uncertainty. No forced winner, fabricated consensus, implementation assignment or Founder decision by an agent. Submit the portfolio and await the Founder.
