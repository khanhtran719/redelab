# Actual CIO response to independent RTD1/RTD2

22/11/2026 · source `/root/ft_define_redteam_sol`, [redteam-initial.md](redteam-initial.md) on frozen0.1 · respondent `/root`. Initial audit preserved. Both findings conceded; current draft is not declared fixed until normative correction and final reviewer receipt.

## RTD1 — accept wrong semantic decision reference

01 used product-local DEC002 for the proposed primary segment while09 used DEC002 for approved documentation authority. This is a synthesis reference error, not evidence the Founder approved the detailed segment. Correction:01 proposed segment→DEC004; DEC002 remains documentation-only authority. Global DEC0001 stays unchanged. Check all canonical refs for unique meaning; no new approval.

## RTD2 — accept first-draft persistence ambiguity

Proposed deterministic correction: New, with no open saved record, opens one **unsaved preparation form**, not an automatically saved empty DRAFT. This is an interaction state, not a fifth persisted lifecycle phase. No “saved” message or local slot exists before a successful explicit save/start. Repeated New returns the same unsaved form; no reset/second form. Back with no edits returns Home; Back after edits offers Save/Keep editing/Discard. Discard before first acknowledgment leaves dataset unchanged/no ghost slot. OS kill before any acknowledged save can lose the form; never claim recovered keystrokes.

First successful Save draft creates exactly one persisted DRAFT (incomplete allowed). First successful Start directly creates one LEARNING record with frozen commitment; separate Save draft not required. Lost acknowledgment can recover prior no-record or full new record, never a ghost/duplicate. First-save privacy/OS-backup information is visible before Save or Start, not after.

For an already saved DRAFT, Discard removes only newer unsaved edits and retains saved draft/slot; deletion is a separate confirmed action. Goal-change and optional past-gap explicit actions create a **saved** successor draft as specified by their whole-action contract, unlike New merely opening a form. Draft entry points all obey slot guard; a transient unsaved form is not silently replaced or duplicated by navigation.

Will update FR001/002/006, BR001/004/008, UX001/J01/S02, registry and add AC040 for first-New empty/type/discard/existing-draft/failed-first-save/lost-ack/privacy cases. No schema/API/algorithm introduced.

## Responsible-specialist response request

Strategy (origin SP2/3/4) and Technical (origin TP2/3) read actual RTD2 and this response; confirm/rebut proposed boundaries and any missing state/duplicate/loss case. Write respectively `strategy-redteam-response.md` / `technical-redteam-response.md`, preserve original. This request is not approval; raise a contradiction rather than rubber-stamp. No new web or build. CIO will relay actual responses and revised exact snapshot to independent reviewer.
