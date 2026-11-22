# 03 — Functional specification

Version 0.2 · 22/11/2026 · **PROPOSED**. Primary user throughout: the individual student. Common precondition: current local dataset readable, no account/network/sensitive permission required. [BR](05-business-rules-and-data.md) is authoritative for shared guards, limits and states; [AC](07-acceptance-criteria.md) specifies observable tests. An implementation remains unauthorized.

## FR-001 — Prepare and save a commitment

- **Purpose/priority/status:** state an actionable self-test goal with little input; MUST/PROPOSED.
- **Precondition/trigger:** no open record, or editing current DRAFT; learner chooses new/continue draft. With an open LEARNING/CHECKING record, show that record instead (BR-001).
- **Inputs/outputs:** goal; optional material locator; comparison plan READY/NOT_READY and planned reference when ready. Output is one editable DRAFT and truthful saved/unsaved feedback.
- **Primary workflow:** New opens one unsaved form, no persisted record/slot yet → explicitly Save draft creates DRAFT, or first Start creates LEARNING directly (FR-002). No compulsory personal profile, subject taxonomy, answer, photo, duration or schedule. Show first-save/OS-backup information before either save action; New never reports saved.
- **Alternative:** save incomplete draft for later; delete draft with FR-009; NOT_READY can later Start with visible assessment limitation.
- **Rules/states/validation:** BR-001/002/008; save DRAFT→DRAFT, incomplete allowed, type/length limits still apply. Choosing READY with missing source is an incomplete draft, not start-ready. No semantic quality certification.
- **Errors/recovery/cancel:** inline field error preserves input. Known uncommitted save failure does not navigate or say saved. Back/Discard with no save submitted/pending and no saved record leaves no record; an unknown save outcome must be reconciled first under BR-008, then existing saved DRAFT Discard retains original draft/slot. Unsaved navigation uses save/discard/keep-editing dialog; a submitted/pending save cannot be blindly canceled/replayed. External kill can lose unacknowledged preparation/edits only (FR-006).
- **Dependencies/acceptance:** FR-006/009; UX-S01/S02; AC-001–004 and AC-040.

## FR-002 — Start the committed session once

- **Purpose/priority/status:** establish what this attempt is about before doing the work; MUST/PROPOSED.
- **Precondition/trigger:** current DRAFT or one unsaved preparation form with no saved open record; learner taps Start. An existing open record cannot be bypassed through history/new-draft entry points.
- **Inputs/outputs:** draft fields; output immutable original commitment, start event, same saved record LEARNING (or exactly one newly created LEARNING record if first save is Start).
- **Primary workflow:** validate BR-002 → save commitment+phase as a whole → acknowledge and show goal with “khi sẵn sàng, tự thử rồi đối chiếu”.
- **Alternative:** NOT_READY allowed, show comparison not ready; learner can save draft/leave instead. Start is never a hidden side-effect of opening setup.
- **Rules/states/validation:** DRAFT→LEARNING; BR-001/002/003/008. No timer/minimum study duration; Start not evidence of attention or ability.
- **Errors/recovery/cancel:** invalid start keeps DRAFT and values; failure/interrupt produces full pre/post state only; repeated tap/retry/return cannot start another record. Cancellation before action leaves draft.
- **Dependencies/acceptance:** FR-001/006; UX-S02/S03; AC-005–007.

## FR-003 — Continue, check, stop or change goal

- **Purpose/priority/status:** control a real learning bout without a rigid timer; MUST/PROPOSED.
- **Precondition/trigger:** LEARNING or CHECKING; user chooses check, leave, return to learning, end without conclusion or change goal.
- **Inputs/outputs:** action and confirmation where destructive; optional new goal later in created DRAFT. Outputs follow BR-004, never an inferred successful session.
- **Primary workflow:** LEARNING→CHECKING explicitly. Save and leave keeps current phase. Screen Back only navigates; return opens that same record/phase.
- **Alternatives:** direct end without assessment→CLOSED/UNASSESSED; change goal confirms closing original UNASSESSED and creating one prefilled DRAFT; CHECKING→LEARNING confirms deleting saved+unsaved check draft. No PAUSED/CANCELED state, no automatic resume/close.
- **Rules/states/validation:** BR-001/003–006/008. Original goal cannot be overwritten after Start. Goal-change clears attempt/actual comparison/verdict/gap from the new draft. Close unassessed never requires an excuse; no old “pass” transfers.
- **Errors/recovery/cancel:** cancel confirms no change, including in-memory check text; write failure no partial split/clearing. Restart shows old intact state or complete intended state. Repeated goal-change creates at most one successor draft.
- **Dependencies/acceptance:** FR-004/005/006; UX-S03/S04; AC-008–012.

## FR-004 — Save a partial self-check

- **Purpose/priority/status:** distinguish independent attempt, assisted work and uncertainty from actual comparison; MUST/PROPOSED.
- **Precondition/trigger:** CHECKING; learner records current self-test situation or chooses Save for later.
- **Inputs/outputs:** attempt mode, comparison status (not confirmed / done but insufficient / done and sufficient), actual source reference, optional note and draft outcome/gap. Output remains a **draft self-check**, not an assessment.
- **Primary workflow:** display original goal/plan → learner self-attempts outside app → declares help used during that attempt → compares outside app and states whether it provides sufficient basis → names source if able → chooses proposed conclusion in FR-005. Looking at the answer afterward only for comparison does not itself make the attempt assisted.
- **Alternatives:** source was not ready or inadequate; helped attempt; not sure; no attempted work. Save any incomplete draft respecting basic type/length, or close unassessed. Do not demand full answer, photo, source import or reteaching.
- **Rules/states/validation:** BR-005/006/009. No attempt mode/verdict preselected. Assessed options only if eligible; changing a gate to ineligible clears assessed selection visibly, retains notes. Partial saves never run final-close validation or claim learning.
- **Errors/recovery/cancel:** field limits preserve input; save failure retry in place. Process interruption restores last acknowledged partial draft; unsaved edits not guaranteed. Explicit return to learning warns before clearing the entire check draft.
- **Dependencies/acceptance:** FR-003/005/006; UX-S04; AC-013–016.

## FR-005 — Conclude a session honestly

- **Purpose/priority/status:** pair the original commitment with a useful, explicitly self-reported conclusion; MUST/PROPOSED.
- **Precondition/trigger:** CHECKING with final user choice, or direct unassessed close from LEARNING. User taps Save conclusion or End without assessment.
- **Inputs/outputs:** eligible MEETS/PARTIAL/NOT_YET, or UNASSESSED; relevant attempt/comparison/source/gap/unknown-gap/note. Output CLOSED with complete result and freed slot.
- **Primary workflow:** validate exact BR-005/006 conditions → save result+close event together → show original goal, attempt mode, comparison used, self-reported result and gap if supplied.
- **Alternative:** independent but uncertain, assisted, missing source or not attempted closes UNASSESSED; do not mark failed. PARTIAL/NOT_YET may explicitly say gap not identified. No forced next session.
- **Rules/states/validation:** eligible means independent self-attempt + comparison DONE_SUFFICIENT + nonempty actual reference. DONE_INSUFFICIENT is never eligible despite source text. PARTIAL/NOT_YET requires gap text or unknown-gap choice. UNASSESSED needs neither a fabricated diagnosis nor compulsory reason. Assisted comparison is labeled accurately, not simply “chưa tự kiểm”.
- **Errors/recovery/cancel:** invalid close stays CHECKING with inputs; duplicate close no duplicate record. Write/crash outcome all-or-none; no CLOSED without its result. Cancel close leaves saved phase and in-memory draft unchanged.
- **Dependencies/acceptance:** FR-004/006/007; UX-S04/S05; AC-017–021.

## FR-006 — Durable saves and recovery

- **Purpose/priority/status:** avoid silent loss, half-states and success feedback that did not happen; MUST/PROPOSED.
- **Precondition/trigger:** any draft save, transition, conclusion, withdrawal, deletion, retry or app return.
- **Inputs/outputs:** current action/content; output acknowledged durable result or explicit unsaved/error status; resume from actual saved state.
- **Primary workflow:** acknowledge only a whole saved action. Reopening restores the latest acknowledged phase and data in the current dataset. No state transition from app background/lock/kill/reboot, elapsed time or offline status.
- **Alternatives:** crash before acknowledgment may yield full old or full new state; reconcile without replay duplicates. OS restore can yield an older coherent snapshot (BR-010), not latest-sync claims.
- **Rules/states/validation:** BR-008/010 across all FRs, including two-record goal change and delete-all. Saves of incomplete drafts are allowed; no forced final validation. Stale action cannot overwrite current closed/deleted/newer record.
- **Errors/recovery/cancel:** known uncommitted failure keeps in-memory edits while process lives with retry/discard; unknown save outcome instead offers reconciliation before discard/delete/new/replay. A committed save with lost acknowledgment is not rolled back or treated as unsaved. No app-controlled navigation loses unresolved input; OS force-kill cannot be prevented and only edits since last acknowledgment may be lost on ordinary restart. Read/corruption error never silently creates empty dataset; retry or explicit warned reset. No invented salvage/restore guarantee.
- **Dependencies/acceptance:** all data-mutating FRs; NFR-001–004/006; AC-022–026 plus each FR's failure scenarios. Choice of storage/atomicity implementation belongs to Dev Studio.

## FR-007 — History, detail and a withdrawn conclusion

- **Purpose/priority/status:** revisit the actual conclusion and recover from entering a mistaken verdict without rewriting learning history; MUST/PROPOSED.
- **Precondition/trigger:** dataset readable, user opens home/history/detail; withdrawal requires CLOSED assessed record not already withdrawn.
- **Inputs/outputs:** selected record; optional withdrawal note and confirmation. Output unchanged original record plus at most one withdrawal annotation.
- **Primary workflow:** open any saved record → see phase/commitment/result/gap and accurate qualifiers; for mistaken assessed conclusion choose Withdraw → confirm consequence/no undo → save annotation.
- **Alternative:** UNASSESSED has no assessment to withdraw; can view/delete/new draft. Already withdrawn is read-only with visible original. History opening an unfinished record routes to its current phase, not a stale result screen.
- **Rules/states/validation:** BR-007/010/011; no CLOSED→LEARNING, no correction-to-new-verdict, no upgrade assisted/unassessed into independently assessed. Withdrawal stays visible wherever the old result appears. Original/withdrawal times distinct; no progress totals.
- **Errors/recovery/cancel:** wrong/stale record action rejected with current state, no effect on another record. Cancel is no-op. Failure no false withdrawal. Retry yields one annotation. No undo/revision engine; privacy deletion remains available.
- **Dependencies/acceptance:** FR-006/009; UX-S01/S05; AC-027–030.

## FR-008 — Create a draft from past context

- **Purpose/priority/status:** optional reduction of re-entry for the next bout; SHOULD/PROPOSED, excluded from minimum MUST acceptance unless Founder includes it.
- **Precondition/trigger:** free open slot; user explicitly chooses use past goal/gap as next draft.
- **Inputs/outputs:** selected prior context; output one editable DRAFT. Goal may be prefilled from learner's chosen gap or original goal; no automatic Start.
- **Primary/alternative workflow:** review the proposed goal and source readiness before starting; may edit/save/discard. If slot occupied, offer current record or cancel, never replace it.
- **Rules/states/validation:** BR-001/002/003/007/008; no attempt, actual comparison, outcome or withdrawal copied. New session does not resolve old gap or rewrite old result.
- **Errors/recovery/cancel:** no duplicate draft on retry, no original modification, standard save failures. Unavailable optional action does not prevent a complete core session.
- **Dependencies/acceptance:** FR-001/002/006/007; UX-J07; AC-031–032 only if included. No spaced-repetition scheduler/task manager implied.

## FR-009 — Delete personal learning records

- **Purpose/priority/status:** user controls local retention; MUST/PROPOSED.
- **Precondition/trigger:** record or data-management controls available; delete one, delete all or reset unreadable dataset selected explicitly.
- **Inputs/outputs:** named scope + confirmation; output current dataset without targeted content, or truthful failure. Delete open also clears slot; delete all includes draft/history/withdrawals.
- **Primary workflow:** explain irreversible current-dataset deletion and OS-backup limitation → confirm → whole deletion → success only when absent from app views.
- **Alternatives:** cancel preserves all data; unreadable data uses separate reset flow with total-loss warning, never masquerades as empty first use.
- **Rules/states/validation:** BR-008/010/011; no recycle bin/undo or erasure-of-all-backups claim. Repeated confirmation cannot target another record; stale record already deleted yields truthful already-absent state.
- **Errors/recovery/cancel:** failed deletion retains actual last state and retry option; process interruption shows full prior or deleted state, not partly-cleared history/open slot. Do not log learning content to support.
- **Dependencies/acceptance:** FR-006/007; UX-J08; AC-033–036. No login/password requirement invented for a local accountless app.
