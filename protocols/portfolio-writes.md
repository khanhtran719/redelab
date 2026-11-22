# Shared record write ownership

This is a cooperative local-filesystem procedure, not a service, database transaction or permission boundary. It applies to all sessions using this workspace. The CIO of each session owns its notes; only one CIO at a time may allocate session/idea/decision IDs or update `portfolio/idea-backlog.md`, `portfolio/decision-log.md` and `sessions/README.md`. Specialists return findings and never acquire shared write ownership.

## Acquire and publish

1. Prepare findings in the exclusively assigned session artifact. For a new session, reserve its ID/path under this lock first; create the file exclusively so an existing record is never replaced.
2. From the workspace root, acquire `.portfolio-write-lock` with a single atomic `mkdir .portfolio-write-lock` (without `-p`). Only success grants ownership. If it already exists, do not touch shared files or take over; keep a pending update in the session artifact and finish other bounded work.
3. Immediately write `owner.md` inside the acquired directory: session ID, actual owner/chat locator if available, acquisition time/timezone and intended files. An absent owner record means uncertain ownership, not a free lock. Never invent a runtime ID.
4. While holding the lock, re-read the current backlog, decision log and relevant session/index. Record SHA-256 hashes or the exact base contents and the proposed changes in the session artifact. Reconcile new evidence and deduplicate before allocating monotonically increasing IDs. A pre-lock draft is not the current base.
5. Recheck the bases immediately before writing. If any changed unexpectedly, stop the write and reconcile; do not overwrite or retry from stale contents. Only explicit human decisions can enter the decision log. When a decision is authorized, append its authoritative record before updating the backlog projection. Ordinary research and runtime tests do not add decision rows.
6. Apply a minimal edit, verify intended rows, unique IDs, links and the resulting contents, then record the result in the session artifact. If interrupted between files, compare the log and session evidence to the backlog before continuing; this is not a multi-file atomic commit.
7. Release only your own lock after verifying completion or recording a pending partial update: remove your `owner.md`, then `rmdir .portfolio-write-lock`. Do not recursively delete an unfamiliar lock or remove another session's ownership.

## Contention and recovery

Do not use elapsed time alone to expire a lock: a paused writer could resume. A leftover lock blocks publication until its recorded owner releases it, or a human explicitly confirms the previous writer has stopped and authorizes recovery. Re-read the authoritative files and reconcile partial writes before removing a stale lock. No background retries, takeover leases or extra service are needed.

This protects cooperating sessions on the same local filesystem. A writer ignoring the protocol, another copy of the workspace, unreliable network-filesystem semantics or direct human edits can defeat it; the base check detects some drift but is not an atomic compare-and-swap. If ownership cannot be established, leave the update pending rather than claim concurrent-write safety.

Validate contention only in an isolated temporary fixture with two contenders; verify exactly one acquisition, an unchanged artifact after the loser, successful handoff after release and refusal to auto-clear an orphan lock. Such a test demonstrates the filesystem primitive and the scripted sequence, not agent compliance or crash-safe multi-file publication. Keep fixtures out of the real backlog and decision log.
