# Recovery and troubleshooting

## Upload stuck at 0%

Separate the failure layers before retrying:

1. Confirm the local file still exists, is readable, and matches the task fingerprint.
2. Inspect whether the embedded page has a usable file input or upload target.
3. Distinguish "file not injected" from "request started but progress unavailable" and "transport finished but platform processing pending".
4. Preserve the current page and account session while inspecting errors.
5. Re-upload only when there is evidence that the platform never accepted the file and the task has zero final clicks.

Do not display a synthetic percentage. Show an indeterminate state when the platform does not expose measurable progress.

## Cover dialog remains open

Treat a visible platform cover modal as an unfinished form step. Locate the modal's own Confirm/Upload control, activate it once, then verify:

- the modal closed;
- the page preview changed to the intended cover;
- no crop/ratio validation message remains;
- the task still points to the same uploaded video.

If a click reports success but the modal remains, re-observe the active document, nested frame, overlay, and disabled state. Do not advance to final publish.

## "Repair unfinished items"

Automatic repair is safe only on the same page when the account, task fingerprint, and uploaded video are unchanged, there is no login/captcha/risk gate, and `finalClickCount` is zero. Repair may re-read or reapply unfinished form controls, but must not refresh, re-upload, or submit.

If bounded repair is exhausted, expose the takeover page with a precise unfinished-item list. After the user or agent closes the platform page, re-read the form before regenerating the final confirmation.

## Duplicate title candidates

Repeated titles in the management list create an identity problem, not permission to resend. Compare platform account, submission time, task ID/fingerprint, receipt, status, and any platform content ID. Keep the current task at `SUBMITTED` or `REVIEWING` when publication cannot be attributed confidently.

## Existing task is not visible

Clear or inspect task filters, then reconcile active task IDs against the ledger. Provide explicit continue/stop/delete actions for the exact old task. Never silently stop an unrelated task to start a new one.

## App or platform window changes size

Focus or reveal the intended window without forcing fullscreen or restoring a saved size from another platform. Leave fullscreen only if that specific platform window is actually fullscreen; wait for the native transition before hiding it.
