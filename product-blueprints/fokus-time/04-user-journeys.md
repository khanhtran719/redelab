# 04 — Journeys and interface responsibilities

Version 0.2 · 22/11/2026 · **all UX behavior PROPOSED**. Screen IDs identify responsibilities, not prescribed routes/layout/components. There are no approved Figma/Stitch references, visual mockups or assets. Exact guards and saved-state semantics are in [BR](05-business-rules-and-data.md); this file cannot override them.

## Common interaction contract — UX-001

Display whether edits are unsaved, saving, saved on device, known not saved or result unknown. Only explicit save boundaries guarantee recovery. New opens an unsaved form without persisted record/slot; Back with no edits returns Home. App-controlled navigation with dirty fields offers Save and leave / Keep editing / Discard edits. When no save is pending/submitted and no record exists, Discard leaves no record; after a saved draft it discards only newer edits and retains saved draft/slot. Unknown acknowledgment is not evidence nothing saved: reconcile actual state before discard/delete/new/command replay, including when a past-gap entry would replace an unsaved form. OS kill may bypass any dialog. Never imply continuous focus from phase. Inline errors name a field, retain text and expose screen-reader feedback; source links are plain references, not auto-opened. Every destructive action has a named-scope confirmation and cancel; state-changing success waits for the whole save. Use neutral learning language, no guilt or achievement grade.

## UX-J01 — A complete self-reported learning bout

- **Entry/objective/initial state:** Home, no open record; learner wants to know whether they can independently do a small task.
- **Actions/steps:** New opens unsaved form→write observable goal, optional material and comparison plan→Save draft or first Start directly after first-save information→study outside app→choose Self-check→declare independent attempt, actual comparison and source→choose self-assessed result/gap→Save conclusion. No acknowledged save means no persisted draft/slot is promised.
- **Validation/state:** FR-001/002/004/005 guards; DRAFT→LEARNING→CHECKING→CLOSED. PARTIAL/NOT_YET requires a gap or explicit unknown-gap; no timer threshold.
- **Success:** Summary pairs frozen goal with self-report, reference and gap; no mastery claim. **Failure:** invalid close stays CHECKING with inputs; save failure is not completion.
- **Recovery/exit/return:** retry in place; Save for later keeps phase. History opens exact saved result, does not automatically start the next bout. UX-S01–S05; AC-001/005/013/017–020.

## UX-J02 — Missing source, uncertainty or help

- **Entry/objective/state:** Setup or CHECKING, learner cannot currently establish independent performance.
- **Actions/steps:** choose NOT_READY at setup if needed→still Start with limitation visible→at check declare mode and whether comparison actually occurred→save UNASSESSED, optionally retain useful gap.
- **Validation/state:** no assessed result unless BR-005 independent+DONE_SUFFICIENT+source guard. If later an adequate source is obtained, actual source can be recorded separately without changing original plan. A comparison done with inadequate basis is retained as such, not a pass. Help during the attempt differs from viewing the answer afterward to compare; an assisted comparison has its own accurate qualifier.
- **Success:** CLOSED with “Chưa có kết luận về tự làm”, or “Chưa xác nhận tự làm — đã đối chiếu có trợ giúp” when applicable; not pass/fail. **Failure:** trying MEETS with assisted/missing comparison is prevented and explained, notes retained.
- **Recovery/exit/return:** no compulsory retry/excuse or rubric search; may return to learning, save partial check, or close unassessed. A closed unassessed record cannot be upgraded by editing later. UX-S02/S04/S05; AC-006/014–016/020/021.

## UX-J03 — Leave, interrupt and resume

- **Entry/objective/state:** Any DRAFT/LEARNING/CHECKING; learner needs to leave without claiming success.
- **Actions/steps:** Save draft/Save for later if editing; leave; return from Home to same open record/phase. In LEARNING with no edits, leaving requires no timer/pause operation.
- **Validation/state:** saving partial CHECKING does not require final assessment fields; Back does not conclude or change phase. Lock/background/call/reboot/offline does not automatically pause, fail or complete.
- **Success:** last acknowledged content/phase restored. **Failure:** writing failed gives retry while input remains in process; force-kill may lose only unacknowledged edits on ordinary restart.
- **Recovery/exit:** show actual recovered state; never replay Start/Close blindly or promise all keystrokes. User can continue or deliberately end unassessed. UX-S01–S04; AC-008/016/022–024.

## UX-J04 — Return to learning or change the goal

- **Entry/objective/state:** CHECKING when learner wants more study, or started record whose goal must change.
- **Actions/steps:** Return to learning explicitly→warn saved+unsaved check draft will be discarded→confirm or cancel. Alternatively Change goal→warn original closes unassessed and check draft discarded→confirm→new prefilled DRAFT→edit/review→Start separately.
- **Validation/state:** return CHECKING→LEARNING clears check draft, keeps commitment; goal-change closes old UNASSESSED and creates exactly one new DRAFT as a whole. No result/mode/gap transfers; source plan may be prefilled as an editable plan.
- **Success:** correct record and phase displayed; original goal never silently easier. **Failure:** partial new draft/closure not allowed; retry/kill yields intact old or complete new pair.
- **Recovery/exit:** cancel preserves saved and in-memory content. New draft can be edited/saved/deleted; old record stays closed and unassessed. UX-S02/S03/S04/dialogs; AC-009/011/012/023.

## UX-J05 — Save failure or unreadable data

- **Entry/objective/state:** any data action, cold start or restore; user wants a truthful recoverable state.
- **Actions/steps:** known uncommitted failure shows not-saved→retry/edit/discard; pending/unknown result shows unconfirmed→check actual saved state before discard/new/retry of command. On read failure use data-error→retry opening or separate warned reset if willing to lose dataset. No unknown acknowledgment is treated as proof of no commit.
- **Validation/state:** no “empty history” substitute for corruption; no silent reset, half conclusion or app-controlled exit losing current edits. Known uncommitted failure differs from unknown save outcome. Unknown/pending results must reconcile before destructive discard/new/replay, without promising rollback of a committed save. Success only from actual whole saved state. External kill cannot be blocked.
- **Success:** read succeeds or deliberate reset creates an empty dataset; failed reset stays an error. **Failure:** unavailable storage/read remains visible; no invented backup rescue.
- **Recovery/exit:** preserve recoverable dataset where possible, no automatic overwrites. OS restore may supply older data, including data deleted/withdrawn since its snapshot; never claim latest sync. UX common/error panel; AC-022–026/036.

## UX-J06 — Read and withdraw a mistaken assessed conclusion

- **Entry/objective/state:** history/detail of CLOSED MEETS/PARTIAL/NOT_YET not withdrawn; learner realizes the entered verdict was wrong.
- **Actions/steps:** inspect original commitment/result→Withdraw conclusion→read no-undo/current-dataset warning→optional note→confirm→see prominent withdrawn marker and original shown as historical only.
- **Validation/state:** no new assessment, no edits to goal/start/close times. UNASSESSED has no assessment to withdraw; already withdrawn cannot repeat or undo.
- **Success:** all surfaces avoid rendering old verdict as a current valid conclusion. **Failure:** unsaved withdrawal not shown as done; stale selection cannot affect a different record.
- **Recovery/exit:** cancel no-op, retry same annotation once; may delete or start a fresh bout. No fake learning session is created just to mark a mistake. UX-S01/S05; AC-027–030.

## UX-J07 — Use a gap next time (SHOULD only)

- **Entry/objective/state:** reading past context, free slot; user wants to revisit a gap.
- **Actions/steps:** explicitly choose source text for new goal→prefilled DRAFT→review/edit comparison plan→Start separately or discard.
- **Validation/state:** no attempt/source-confirmation/verdict copied; no old gap automatically resolved; same BR-001 slot guard from every entry point.
- **Success:** one new draft, original unchanged. **Failure/recovery:** occupied slot routes to current record/cancel; failed create retry no duplicates. UX-S01/S02/S05; AC-031/032. Core MVP remains complete if this optional action is absent.

## UX-J08 — Delete current data

- **Entry/objective/state:** record detail or data controls; learner wants one record or all learning data removed from current app dataset.
- **Actions/steps:** select named scope→see irreversible/no-undo and historic-OS-backup limit→confirm or cancel→save deletion→refresh views/open slot.
- **Validation/state:** delete one leaves others intact; delete all includes current draft/check/history/withdrawals. Read-error reset is separate and warns data may not be inspectable first.
- **Success:** no targeted data remains in app views; **failure:** no false “deleted”, retry available, no next-record deletion from duplicate taps.
- **Recovery/exit:** interruption yields full prior or deleted state; cancel preserves everything. Future OS restore can reintroduce an older snapshot, as disclosed. UX-S01/S05/dialogs; AC-033–036.

## Minimal screen inventory

| Interface | Purpose / displayed information | Available actions and navigation | States/validation/errors | Accessibility and FRs |
|---|---|---|---|---|
| UX-S01 — Home/history | One open record with current phase; past records with self-report/unassessed/withdrawn qualifiers; data information | Continue current; New when slot free; view past; delete-all/data info; optional FR-008 | Empty is genuine only after successful read; loading/saved-data/read-error distinct; no achievement total | Ordered accessible list, full labels beyond color, no content forced into notifications. FR-001/006/007/008/009 |
| UX-S02 — Commitment | Goal example, optional locator, source-ready choice/reference, unsaved form vs saved draft status, privacy/backup note before first save | Edit, Save draft, Start, Back; Delete only for a saved draft | New does not persist; first Save/Start does. Discard before first save leaves no record, after saved draft retains it. Missing/too-long field inline; incomplete drafts allowed; open-slot guard | Labels/input purpose, multiline+large text, errors announced, no required personal profile. FR-001/002/006 |
| UX-S03 — Open learning | Frozen goal and source plan; workflow-open label, no measured attention/time claim | Self-check, leave, end unassessed, change goal | Saving/error/current-record-changed; no countdown/auto advance | Screen-off allowed, no forced orientation/motion/sound or deadline. FR-003/006 |
| UX-S04 — Self-check | Original goal/plan; attempt choices; actual source/comparison status with sufficient/insufficient distinction; verdict/gap/unknown option; partial-save status | Save for later, Save conclusion, end unassessed, return to learning, change goal, Back | No mode/verdict preselection; assessed options conditional; changes clear ineligible verdict, not notes; partial save and final close differ | Form grouping, logical reading order, announced guard/error, assisted label truthful. FR-003/004/005/006 |
| UX-S05 — Summary/detail | Original commitment/time context, attempt/comparison facts, result/gap, withdrawal if any | Home; withdraw eligible conclusion; delete; optional new draft | Closed read-only; original vs withdrawn marker unambiguous; stale/deleted record error | Verdict and qualification in one readable group, not icon alone. FR-005/007/008/009 |

Confirmation dialogs and the data-error/unsaved-edits panels are shared interaction states, not extra product dashboards/screens. Every dialog identifies record/scope, explains discarded data/no-undo if relevant, and has accessible confirm/cancel without time pressure. No layout, visual style, component framework or native navigation implementation is prescribed.
