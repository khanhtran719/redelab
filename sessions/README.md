# Session records

Phiên [SES-20261120-01 — broad discovery](2026-11-20-01-broad-discovery.md) đã bắt đầu ngày 2026-11-20, trạng thái **BLOCKED_MULTI_AGENT**. Hồ sơ hiện là nghiên cứu một agent; chưa hoàn thành hội đồng độc lập.

[SES-20261120-02 — Phase 2 runtime validation](2026-11-20-02-runtime-validation.md): audit và kiểm tra vận hành, không phải phiên chọn sản phẩm. Kết luận và bằng chứng thực thi nằm trong hồ sơ riêng.

Use one Markdown file `YYYY-MM-DD-NN-short-slug.md` per session, with stable ID `SES-YYYYMMDD-NN`. Dates use Asia/Ho_Chi_Minh. The CIO is the sole owner of the synthesis and portfolio updates. Create optional adjacent notes only when a long investigation needs them; assign one writer per notes file.

Across sessions, reserve the session ID/path and serialize shared updates under [portfolio write ownership](../protocols/portfolio-writes.md). A CIO per chat is not a global mutex. Only the assigned owner edits a session's notes; all writers use the shared lock for backlog, decision log and this index. Never put validation fixtures or TEST concepts in the real backlog.

Use the following outline when a real session starts. Empty sections should say not run/not applicable/unknown with a reason, never pretend work occurred. Replace example notation with actual data; do not copy this template into the backlog as evidence.

## Session outline

### Objective and constraints

Session ID/date; mode; question and decision informed; customer/geography; Founder restrictions; supplied evidence; research stopping condition and disclosed assumptions; existing idea IDs and relevant Founder log entries.

Record planned and observed elapsed time, search queries, inspected sources and debate cycles, plus the stop reason. Mark unreported token/cost usage UNKNOWN. A runtime-validation record uses executed/static/not-run labels for every check and cannot inherit a previous session's PASS as fresh execution evidence.

### Capability and participation record

Session status: `IN_PROGRESS`, `BLOCKED_MULTI_AGENT`, `AWAITING_FOUNDER` or `CLOSED`. Record partial completion separately from a delivered council. Available and unavailable tools, checks actually exercised, access limitations, role configuration source, configured model/effort versus verified runtime settings, actual runtime agent IDs, assignments, rounds, artifacts/messages and completion/failure status. List skills actually loaded, not all installed skills. Do not list an unspawned role as a participant.

### Source and claim ledgers

| Source ID | Title / publisher | URL or local path / locator | Publication/event date | Verified/accessed date | Type / limits | Relevant finding |
|---|---|---|---|---|---|---|

| Claim ID | Claim / applicable context | VERIFIED / INFERENCE / HYPOTHESIS / UNKNOWN | Sources and reasoning | Counterevidence | Confidence and reason |
|---|---|---|---|---|---|

Include important search queries, dates, markets/languages and stopping scope. Apply [evidence policy](../protocols/evidence-policy.md).

### Independent initial findings

For each actually participating agent: runtime identity, assignment/context boundaries, dated initial findings and finding IDs, source/claim links, uncertainties. Preserve the original output or an identified faithful excerpt with the runtime artifact locator. Append later revisions; do not rewrite the initial view to manufacture independence or consensus.

### Concept catalog and revisions

Idea ID/revision; name; customer/job/problem; existing workaround; mechanism; measurable value; differentiation; critical assumptions; evidence state; aliases/related ideas. Include exploratory concepts and reason for inclusion/exclusion from the shortlist. No invented products enter the backlog during setup validation.

### Debate and Red Team exchanges

| Exchange ID / idea revision | Origin and target agent IDs | Finding IDs and objection | Actual response / evidence | Assessment change | Unresolved disagreement |
|---|---|---|---|---|---|

Use [debate rules](../protocols/debate-rules.md). Include the Red Team's strongest objections, targeted checks, falsifiers and the proponent's response. Identify paraphrases. A missing reply stays missing.

Link the actual delivery/response receipts, originating claim and initial output. Track PREPARED/SENT/RESPONDED/FAILED_OR_UNKNOWN separately from whether the complete critique-response cycle passed. With no spawned agent, leave the exchange table empty and state NOT RUN; do not create placeholder participants.

### Scoring and comparison

For each candidate, record all nine [rubric](../protocols/scoring-rubric.md) rows: weight, score or UNKNOWN, rationale, claim IDs, confidence, dissent and plausible interval where useful. Show assessed weight, evidence coverage, weighted total or NOT RANKED, ranking sensitivity and critical blockers. Keep exploratory ideas separate from provisional commercial ranking.

Record research priority separately using the rubric's learning-question table. Priority never changes Founder status. A validation portfolio remains session-local and may be empty when the test is blocked; this does not establish that no viable product exists.

### Council portfolio

Best 3–5 or fewer, possibly zero. For each include actual supporters/opponents and reasoning, differentiated mechanism, evidence strength, unresolved questions, technical/commercial/legal/data risks and the most important proposed validation experiment. Record council recommendation separately from any Founder decision. Link minority positions rather than flattening them.

### Founder gate and handoff

State that the portfolio is awaiting a Founder decision; no implementation is authorized. For a blocked session, state incomplete rounds and the capability needed to resume. After an explicit decision, link the append-only decision log entry and authorized follow-up scope. On a later session, carry constraints, unresolved disagreements and source freshness forward. Do not create an autonomous follow-up task.

[SES-20261120-03 — independent DISCOVER council](2026-11-20-03-independent-discovery.md): **AWAITING_FOUNDER**; bảy cơ chế, bốn ứng viên hoàn tất peer + Red Team response; hai hướng khám phá có điều kiện, không có xếp hạng thương mại. Tám job hoàn thành; ba job lỗi được ghi riêng. Nguồn do CIO thu thập, worker phản biện độc lập.

[SES-20261120-04 — Fokus Time Product Discovery & Strategic Debate](2026-11-20-04-fokus-time.md): **IN_PROGRESS**; research only, MCP agent-hub.

[SES-20261121-01 — Fokus Time discovery & debate](2026-11-21-01-fokus-time.md): **AWAITING_FOUNDER**; sáu chuyên gia gpt-6.1-sol, sáu hướng ban đầu, peer critique/reply và Red Team/rebuttal/final review thực; chín deliverables. Hai phương án khám phá IDEA-0013/IDEA-0014 NOT RANKED; Inventor rút standalone-app endorsement, không có winner hoặc Founder decision. Giữ nguyên phiên cũ đang dở.

Continuation 2026-11-22, same SES-20261121-01: Founder SELECT IDEA-0014 (DEC-0001), exact direction ‘Fokus Time — giúp sinh viên biến một buổi tập trung thành tiến bộ học tập có thể tự kiểm tra.’ Product definition/specification review at [Product Blueprint](../product-blueprints/fokus-time/README.md); detailed scope PROPOSED, implementation NONE. Prior research conclusions preserved.

Completed product-definition continuation22/11/2026 for SES-20261121-01 / selected IDEA-0014 / DEC-0001: [Fokus Time Blueprint v0.2](../product-blueprints/fokus-time/README.md), **READY FOR FOUNDER REVIEW**,11docs,8MUST+1SHOULD FR,40AC; real six-role review/RedTeam/replies/final audit. Detailed scope PROPOSED; app/device/outcome tests NOT RUN; implementation NONE.
