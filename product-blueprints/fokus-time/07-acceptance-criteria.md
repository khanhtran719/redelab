# 07 — Acceptance criteria and scenario matrix

Version 0.2 · 22/11/2026 · **PROPOSED; every application scenario NOT RUN**. This is a product test contract, not a passing test report. All 8 MUST FRs have observable scenarios; shared integrity/failure cases apply to each mutation. FR-008 is SHOULD and conditional. No learning-efficacy, payment or empirical non-inferiority claim follows from passing these scenarios.

Dev Studio later chooses test implementation after separate authorization. Expected results come from the fixed [BR](05-business-rules-and-data.md) truth table, known before/after record fixtures and visible data after a fresh read/restart, not only the same UI success message or production predicate reused as its own oracle. Failure/crash injections are future test methods, not performed work here.

## Preparation — FR-001

### AC-001 — Save an incomplete draft
**Given** no open record, **when** learner saves a draft with a goal missing or a READY plan lacking source, **then** exactly one DRAFT is saved with values, marked not start-ready; no started/closed result is invented. **Oracle:** fresh reopen shows same draft, not a session outcome. BR-001/002; UX-J01/J03.

### AC-002 — Field boundaries and text preservation
**Given** each field's BR-002 limit N, **when** saving N scalar values, N+1, whitespace-only and valid Vietnamese/combining text, **then** N is accepted where field otherwise valid, N+1 rejected inline without truncation/input loss, whitespace counts as empty, internal newlines/Unicode content remain readable after save/reopen. Empty goal may save draft but cannot Start. **Oracle:** known input and fresh record comparison. BR-002; NFR-005; UX-S02/S04.

### AC-003 — Start validation is not semantic grading
**Given** DRAFT, **when** goal is blank, comparison plan unset or READY has blank reference and Start is tapped, **then** stay DRAFT with specific errors and existing input. A syntactically valid goal may Start without the app asserting pedagogical quality/source correctness. BR-002; FR-002; UX-S02.

### AC-004 — Slot guard at every entry point
**Given** an open DRAFT/LEARNING/CHECKING, **when** New or any past-goal/gap/create-draft entry is chosen, **then** existing record is offered or action canceled; no second open record or silent closure. **Oracle:** complete record set before/after; each entry tested. BR-001; FR-002/003/008; UX-J07.

## Start — FR-002

### AC-005 — Freeze the exact commitment
**Given** valid DRAFT, **when** Start succeeds, **then** same record enters LEARNING with original goal/material/plan and start event; later check fields do not overwrite them. No timer/permission/network is required. BR-003/008; UX-J01; NFR-001.

### AC-006 — Source not ready is a legitimate start
**Given** nonempty goal and NOT_READY plan, **when** Start is chosen offline, **then** LEARNING opens with comparison-not-ready notice, without forced source search. Later adequate actual source may be recorded without rewriting original plan; without it only unassessed closure is available. BR-002/005; FR-004/005; UX-J02.

### AC-007 — Start duplicate and uncertain acknowledgment
**Given** valid DRAFT, **when** Start is double-tapped, retried after a lost acknowledgment or encountered on a stale draft screen, **then** at most one started record/open slot exists. Reopen presents actual prior or complete started state, never a second start event/record. BR-001/008; FR-006; NFR-002.

## Open workflow — FR-003

### AC-008 — Leave without an invented phase change
**Given** LEARNING/CHECKING with acknowledged data, **when** app backgrounds, locks, loses network, is killed or reboots, **then** reopening shows same saved phase/data, with no inferred pause/failure/success and no continuous-focus claim. Screen Back only navigates. BR-004/008; FR-006; UX-J03.

### AC-009 — Return to learning discards only after consent
**Given** CHECKING with saved and unsaved draft details, **when** Return to learning is selected, **then** warning identifies both sets of check content; Cancel preserves both. Confirmed successful action yields LEARNING with original commitment unchanged and check draft cleared; failure does not clear half the data. BR-004/008; UX-J04.

### AC-010 — End without a forced diagnosis
**Given** LEARNING or incomplete CHECKING, **when** learner chooses end without assessment, **then** CLOSED/UNASSESSED is possible without mode/source/reason/gap, never default fail. Retain valid optional details; if unsaved invalid text cannot be stored, offer fix or explicitly discard it and close, not an inescapable validation loop. BR-006/008; FR-005; UX-J02/J04.

### AC-011 — Goal change does not shrink the past
**Given** started goal “tự giải5câu” and check details, **when** Change goal is confirmed to prepare a smaller goal, **then** old record closes UNASSESSED(reason changed goal), original5-câu commitment remains; one editable DRAFT has setup only, no attempt/comparison/verdict/gap. It is not started automatically. Cancel preserves original phase/data including unsaved check fields. BR-003/004; UX-J04.

### AC-012 — Goal-change interruption/duplicate
**Given** goal change is saving, **when** failure/kill/retry occurs across save boundary, **then** observe old open record with no new draft **or** old closed plus exactly one new draft. Never closed-old without draft, two successor drafts or two open records. **Oracle:** independent pre/post fixture plus fresh record set. BR-001/008; FR-006; NFR-002.

## Self-check — FR-004

### AC-013 — Help timing and selection changes
**Given** learner independently attempts and afterward views answer only to compare, **when** declaring mode, **then** this is eligible for INDEPENDENT; help used to solve before/during the attempt is ASSISTED. No mode preselected. Changing an eligible draft to ASSISTED/NOT_CONFIRMED clears an assessed selection visibly but preserves notes. BR-005; UX-J01/J02.

### AC-014 — Insufficient comparison cannot pass
**Given** INDEPENDENT and actual source text, **when** comparison is NOT_CONFIRMED, DONE_INSUFFICIENT or unset, **then** MEETS/PARTIAL/NOT_YET cannot be committed. Only DONE_SUFFICIENT plus nonempty actual reference enables self-assessed options; app does not verify the rubric itself. ASSISTED remains unassessed even with sufficient comparison. BR-005; FR-005; UX-J02.

### AC-015 — Actual source differs from plan
**Given** a frozen planned source or NOT_READY plan, **when** learner later uses another source, **then** save actual reference/status separately and display the distinction; original goal/plan unchanged. Empty actual reference prevents assessed conclusion even when status says sufficient. BR-003/005; UX-S04/S05.

### AC-016 — Partial check save and return
**Given** CHECKING with incomplete mode/status/outcome/gap, **when** Save for later is used, **then** basic valid partial fields save and phase stays CHECKING; final Close validation is not applied. Restart recovers the partial draft and never presents it as a closed assessment. BR-008/009; FR-006; UX-J03/J05.

## Conclusion — FR-005

### AC-017 — Eligible self-assessed result
**Given** INDEPENDENT + DONE_SUFFICIENT + actual source, **when** MEETS is explicitly chosen and saved, **then** CLOSED stores full conclusion once; summary states “Tự đánh giá sau đối chiếu” with mode/source and original goal, no mastery/score claim. Optional gap/note may be empty. BR-005/006; UX-J01.

### AC-018 — Gap required without forcing invention
**Given** eligible PARTIAL or NOT_YET, **when** gap text is empty and unknown-gap not chosen, **then** close stays CHECKING with error/input preserved. Nonempty valid gap **or** explicit unknown-gap allows close; selecting both is not allowed, switching from entered text warns before discard. No compulsory next-study date or generated diagnosis. BR-006; UX-S04.

### AC-019 — Close once and free the slot
**Given** valid conclusion, **when** Save conclusion succeeds/repeats, **then** one CLOSED record keeps goal/result/gap together, slot becomes free once, no automatic successor session. Duration/opening check never performs Close. BR-001/006/008; FR-006; UX-S05.

### AC-020 — Assisted and uncertain conclusions stay truthful
**Given** ASSISTED with DONE_SUFFICIENT or DONE_INSUFFICIENT, **when** closing UNASSESSED, **then** useful optional gap remains and summary says comparison occurred with help, retaining insufficient-basis qualifier when relevant. With not-confirmed comparison, do not claim comparison occurred. Independent but uncertain may also close UNASSESSED without excuse, retry or pass/fail. BR-005/006; UX-J02.

### AC-021 — Reject stale/forbidden conclusion mutations
**Given** record already CLOSED/deleted or input gates became ineligible, **when** a stale screen tries assessed Close or Resume, **then** no rewrite/new result happens; actual current state is shown. Invalid phase/action does not change commitment. BR-004/005/008; UX-S04/S05.

## Persistence — FR-006

### AC-022 — Acknowledged versus unsaved edits
**Given** an acknowledged draft/check save followed by new unsaved text, **when** ordinary process death occurs, **then** acknowledged data survives; edits since that boundary may be absent and are not falsely said saved. App-controlled leaving offers save/discard/keep-editing; external kill is not promised preventable. BR-008; NFR-002/003; UX-J03/J05.

### AC-023 — Whole action under failure
**Given** known records before Start, Close, return-and-clear, goal split, withdrawal, delete-one or delete-all, **when** save failure/kill is injected before/during/after each commit boundary, **then** fresh read yields coherent full pre-action or full post-action state; no half result/split/deletion, accidental record loss or duplicate retry. Success feedback is not the only oracle. BR-008; every mutating FR; NFR-002.

### AC-024 — Failed writes, stale UI and future update
**Given** a readable dataset and current inputs, **when** write fails or another saved action invalidates a stale UI action, **then** no false success/app-controlled loss; current input remains while process lives and retry is deliberate. A future app update must preserve readable acknowledged records or report a data error without clearing them. BR-008/010; NFR-002/003/009.

### AC-025 — Older OS snapshot is not latest sync
**Given** an OS snapshot predates later deletes/withdrawals/edits, **when** OS restores it, **then** app shows coherent recovered data as local data, no claim latest changes restored and no automatic old-session completion. It need not detect restore or erase external copies; data information warns old content may reappear. BR-010; NFR-006; UX-J05.

### AC-026 — Offline read failure and no silent reset
**Given** cold start offline, **when** data reads successfully, **then** all core local actions work without account/sensitive permissions. **When** reading is corrupted/unavailable, **then** show data error and retry, not empty history or automatic reset. Do not overwrite recoverable dataset to bypass error. BR-009/010; NFR-001/003; UX-J05.

## History and withdrawal — FR-007

### AC-027 — History is context, not a learning score
**Given** assessed, unassessed, open and withdrawn records, **when** listing/opening them, **then** each shows true phase/result qualifiers and original commitment; no mastery total/streak or implication all closed sessions met goals. Stable recorded creation order does not reshuffle from clock change or withdrawal; open record routes to current phase. BR-003/007; UX-S01/S05.

### AC-028 — Withdraw a mistaken assessed conclusion
**Given** CLOSED assessed record not withdrawn, **when** user confirms withdrawal with optional note, **then** original goal/result/start/close retained, one withdrawal timestamp/annotation added, every surface marks original no longer current. No new verdict, reopened session or fake study bout. BR-007; UX-J06.

### AC-029 — Withdrawal eligibility and no upgrade
**Given** open, UNASSESSED, assisted/unassessed or already withdrawn record, **when** withdrawal/new-verdict editing is attempted, **then** action is unavailable/rejected without changing record or another assessment. No undo or unassessed→assessed correction path. Valid privacy deletion remains available. BR-007/011; UX-J06.

### AC-030 — Withdrawal cancel/failure/retry
**Given** eligible original, **when** Cancel before submission or known uncommitted failure occurs, **then** original remains unchanged, no false withdrawn marker. For a pending/unknown result, reconcile actual saved state before further destructive action; a committed action whose acknowledgment was lost appears once after reopen/retry, not duplicate annotations or an invented rollback. BR-007/008; FR-006; UX-J06.

## Optional next draft — FR-008 (if approved/included)

### AC-031 — New context, never copied success
**Given** closed context and free slot, **when** user chooses use old goal/gap, **then** one editable DRAFT receives only chosen setup text, no mode/actual comparison/outcome/gap-success state; user reviews source readiness and Starts separately. Original unchanged. BR-001/003/007; UX-J07.

### AC-032 — Optional action obeys the slot
**Given** an occupied slot or failed create, **when** past-gap action is tapped/retried, **then** do not replace/close existing work or create duplicate drafts; offer current work/cancel. Absence of this optional feature does not fail MUST baseline. BR-001/008; UX-J07.

## Deletion — FR-009

### AC-033 — Delete exactly one
**Given** multiple records including an open one, **when** a named record deletion is confirmed and succeeds, **then** only that record/annotations disappear from current app views; others unchanged; deleting open frees slot. Copy warns irreversible current-dataset scope and historic OS copies not erased. BR-010/011; UX-J08.

### AC-034 — Delete all learning data
**Given** draft/open/history/withdrawals, **when** separate Delete all confirmation succeeds, **then** all learning data in current dataset is absent, no hidden open slot or derived result remains. App does not promise OS copies erased or disable future restore. BR-008/010/011; UX-J08.

### AC-035 — Destructive cancel, failure and duplicate
**Given** selected delete scope, **when** Cancel/write failure/double-confirm occurs, **then** cancel has no effects, failed save has no false success, successful retry deletes only intended scope once and never the next record after navigation. Fresh read follows whole-action rule. BR-008/011; FR-006; UX-J08.

### AC-036 — Explicit reset after unreadable data
**Given** read-error state, **when** learner chooses reset, **then** separate confirmation warns all current data may be lost and cannot be recovered by Fokus. Cancel preserves dataset/error; successful reset creates a genuinely empty readable dataset; failed reset stays error, not fake first use. BR-010/011; FR-006; UX-J05/J08.

## Cross-cutting qualification

### AC-037 — Privacy boundary
**Given** text-only baseline with no account/telemetry, **when** completing core flows and exercising errors, **then** no Fokus content upload/AI/ads/analytics, no raw learning text in support/logs by default, no sensitive permission prompt required, no content notification. First-save/data information accurately distinguishes device saves and OS backup. **Oracle:** future network/log/storage inspection plus visible copy, not a privacy slogan. NFR-004/006; FR-001–009.

### AC-038 — Accessible complete workflow
**Given** supported iOS/Android devices with VoiceOver/TalkBack and largest supported text setting, **when** traversing all MUST screens, error and confirm dialogs, **then** every action/field/status/error is reachable and meaningfully read, no essential control clipped, no color/sound/motion/time-limit dependence, Vietnamese entry preserved. NFR-005; UX001, UX-S01–S05.

### AC-039 — Platform/performance sign-off remains separate
**Given** no approved support matrix/numeric performance profile yet, **when** preparing future implementation/release qualification, **then** mark those checks OPEN/NOT RUN, obtain proposed OS/device/dataset thresholds through OPEN-003/004 and PCR before claiming support/performance PASS. Business behavior cannot be silently changed to pass. This is a handoff qualification rule, not an executed product benchmark. NFR-007/008/009.

### AC-040 — First New, discard and first save boundary
**Given** no open saved record and no save submitted/pending, **when** New opens then Back without edits, or type→Discard, **then** dataset/history/slot remains unchanged; no ghost empty draft. Repeated New reuses the unsaved form. First successful Save creates one DRAFT, or first Start creates one LEARNING directly after validation; device-save/OS-backup information precedes both. **When** first Save/Start is pending or acknowledgment lost and Back/Discard/Retry/New is requested, **then** resolve actual durable state first, never assume no record or undo a commit: full-new-record stays, known no-commit may retry/discard, unreadable uses data-error. **Given** an acknowledged DRAFT (including goal-change/past-gap successor), **when** newer edits are discarded, **then** saved draft/slot remain; deletion is separate. An unsaved form cannot be overwritten by past-gap action: Save/Keep/Discard first; saving occupies slot. **Oracle:** empty/existing-draft fixtures, pending/commit/no-commit failures, fresh reopen and all create entry points. FR-001/002/006/008; BR-001/008; UX001/J01/S02; NFR-002/006.

## Traceability and execution status

Registry02 maps allFRs to these IDs; BR/UX/NFR references above are dependencies, not circular test evidence. Reuse failure scenario AC-023 for every data mutation, including the optional FR-008 if included. Independent expected state must also confirm unrelated records unchanged.

**Current status:** all application scenarios NOT RUN; no application exists in this scope. Specification review can establish completeness/consistency and traceability, never implementation correctness or user outcome. No generated software tests, test framework or infrastructure is part of this package.
