# 09 — Authority, product decisions and open questions

Version 0.2 · 22/11/2026 · draft for Founder. `DEC-001` etc below are **product-local decision IDs**; portfolio `DEC-0001` is the append-only human SELECT record. Approval status and evidence confidence are separate.

## Decision register

| ID | Status | Decision / provenance |
|---|---|---|
| DEC-001 | **APPROVED** | Exact direction: “Fokus Time — giúp sinh viên biến một buổi tập trung thành tiến bộ học tập có thể tự kiểm tra.” Founder current message, [portfolio DEC-0001](../../portfolio/decision-log.md), IDEA-0014/F3 direction |
| DEC-002 | **APPROVED** | Continue current Innovation Lab chat/session; product definition/specification review/handoff documents only; implementation NONE; no Dev Studio activation, source code, prototype/UI assets, architecture/infrastructure/deployment |
| DEC-003 | **APPROVED scope intent** | Original brief specifies iOS and Android and VN/SEA/international exploration; no exact OS minimum, release geography/language plan or support matrix thereby approved |
| DEC-004 | PROPOSED | Primary segment university student with own material and self-comparison method; Vietnamese-first text, no course/cohort/multi-step-math pivot approved |
| DEC-005 | PROPOSED | One open local record including draft; four phases DRAFT/LEARNING/CHECKING/CLOSED; no timer/pause/cancel state; “phase” never measured focus |
| DEC-006 | PROPOSED | Original commitment frozen at Start; explicit goal change closes old UNASSESSED and creates a reviewed new draft as a whole action |
| DEC-007 | PROPOSED | NOT_READY source may start; assessed verdict requires declared independent attempt + sufficient comparison + reference; helped/uncertain attempts may retain gaps but are not independent-performance verdicts |
| DEC-008 | PROPOSED | Partial saves allowed; explicit Save/transition acknowledgment, no every-keystroke autosave promise; input limits BR-002 are design choices pending approval |
| DEC-009 | PROPOSED | Closed original immutable, correction via one withdrawal annotation of assessed conclusion; no replacement verdict/undo/revision engine |
| DEC-010 | PROPOSED | No Fokus cloud/account/sync/telemetry; allow OS backup/transfer under OS/user control with no latest restore or all-backup deletion guarantee |
| DEC-011 | PROPOSED | User-controlled retention until delete; current-dataset scoped delete-one/delete-all; no recycle bin or auto-expiry |
| DEC-012 | PROPOSED | MUST FR-001–007/009; SHOULD FR-008 only if included; timer/AI/content/grading/blocker/social/monetization/analytics outside MVP |
| DEC-013 | PROPOSED measurement boundary | Functional success means correct self-report/save/flow, not learning proof. Superiority or efficiency/non-inferiority is separately designed research, NOT RUN |

No previous council recommendation is retrospectively APPROVED. The Founder did not explicitly REJECT any of the prior directions/features; council withdrawals and this proposed OUT OF SCOPE remain accurately labeled. F1 not selected is not the same as Founder REJECT/PARK.

## Meaningful open choices and recommended defaults

These defaults make the draft deterministic; alternatives are not simultaneously normative. They do **not** block completing documentation or require Dev Studio to guess. Approval of proposed behaviors is still pending.

| ID | Question / options / trade-off | Council/CIO recommendation and impact | Blocking scope |
|---|---|---|---|
| OPEN-001 | Approve the self-report MVP boundary? A: independent-only assessed verdict + assisted/unassessed gaps, four phases and no timer. B: permit qualified assisted verdict. C: add timer with separate rules | **A** is the normative draft. B can be useful but changes meaning of “tự làm” and must update every summary/AC. C adds timing/background/notification semantics. Inventor retains B preference; no false consensus | Founder scope approval before any future implementation; no ambiguity within this draft |
| OPEN-002 | OS backup policy: A allow user/OS backup/transfer; B exclude where supported | **A** normative proposal: possible recovery, historic copies/deleted/withdrawn content may return. B reduces copies but increases loss risk and needs platform-specific capability/disclosure verification. Neither adds Fokus backup service | Meaningful privacy/recovery decision before implementation; current behavior/copy is defined under A |
| OPEN-003 | Which OS versions/devices/form factors can be claimed supported? | Dev Studio later proposes matrix from target users, feasibility and resources; Product/Founder reviews meaningful coverage/cost. Do not ask Founder to choose SDK/API internals | Before platform support/implementation qualification claims, not before Founder specification review |
| OPEN-004 | Numeric latency, history/dataset capacity and resource targets? | Measure representative supported devices/data first, propose targets via PCR; no invented numbers or “unlimited”. Current field limits and error behavior remain explicit | Before quantitative performance sign-off; no missing core state behavior |
| OPEN-005 | Monetization and distribution? | No payment/ads/subscription in this MVP proposal. Real buyer/channel/WTP UNKNOWN; separate business decision/research if authorized | Not blocking core blueprint; no launch economics claim |
| OPEN-006 | Which actual learning cohort and evidence of incremental value? | Preserve selected general direction; observe real workflow before claims. No superiority/non-inferiority threshold invented; self-report correctness is separately testable | Blocks efficacy/business claims, not definition or selected direction |
| OPEN-007 | Exact publication/jurisdiction/privacy policy obligations and future support access? | Product-specific legal/store review before publication; user text/OS backups disclosed; no legal clearance claimed now | Before publication, no production action authorized here |
| OPEN-008 | Correction strength: withdrawal vs replacement result? | **Withdrawal** normative baseline: makes old verdict not-current with small state. Full replacement may be more convenient but needs original/latest semantics and constraints; Inventor preference preserved | Founder may change proposed baseline; current rules/AC are complete |

## Preserved disagreements and applied changes

Actual Customer/Strategy peer exchange changed opinions on assisted work in both directions; later Customer and Strategy chose conservative independent-only, Inventor kept a qualified-assisted alternative. This was not resolved by empirical evidence. CIO chose a single proposed default and retained OPEN-001.

Inventor IP2 led to dropping PAUSED/CANCELED; Strategy accepted. Customer challenged delete-only correction, Inventor proposed editable result, Strategy later accepted withdrawal as sufficient minimal correction; preference dissent remains OPEN-008. Technical required partial-check save and whole-state recovery. Market required distinct adequate/inadequate comparison declarations and accurate assisted wording. Inventor distinguished help during attempt from later comparison. See [review record](reviews/review-record.md) for actual identities, packets, responses and final issue status; no invented dialogue.

## Authority and change procedure

Only explicit human instructions change APPROVED decisions. A reviewer recommendation or READY FOR FOUNDER REVIEW is not approval. Record future decisions/version changes and their source; do not overwrite prior research or implied past approval. Product Clarification Requests follow [handoff](10-dev-studio-handoff.md); technical preferences cannot silently modify business behavior. No downstream execution is authorized by SELECT or this package.
