# Recovery and troubleshooting

## Upload stuck at 0%

Separate the failure layers before retrying:

1. Confirm the local file still exists, is readable, and matches the task fingerprint.
2. Inspect whether the embedded page has a usable file input or upload target.
3. Distinguish "file not injected" from "request started but progress unavailable" and "transport finished but platform processing pending".
4. Preserve the current page and account session while inspecting errors.
5. Re-upload only when there is evidence that the platform never accepted the file and the task has zero final clicks.

Do not display a synthetic percentage. Show an indeterminate state when the platform does not expose measurable progress.

Douyin's optional AI recommended-cover generation can remain pending after the video is uploaded. Distinguish that local recommendation panel from actual upload/transcoding indicators. Continue only with independent upload-completion evidence and no real upload failure/active-transfer gate; do not infer success from an unclassified API code such as 2000. Required user-selected cover upload and readback still apply.

## Cover dialog remains open

Treat a visible platform cover modal as an unfinished form step. Locate the modal's own Confirm/Upload control, activate it once, then verify:

- the modal closed;
- the page preview changed to the intended cover;
- no crop/ratio validation message remains;
- the task still points to the same uploaded video.

If a click reports success but the modal remains, re-observe the active document, nested frame, overlay, and disabled state. Do not advance to final publish.

## Source file changed at the same path (Mac 0.2.120)

A matching filename is not a matching video. If the app reports 需重新准备 because video bytes changed, do not keep clicking 恢复任务 or reuse the old confirmation. Confirm with the user that the current file is intended, then use 重新校验视频 on the eligible task, or 重新校验当前视频 in the workbench. These controls preserve manual copy, topics and cover choices while rebuilding media metadata; they do not upload, publish, or revive stopped tasks. Prepare again and obtain a fresh confirmation for changed content. If the file, cover, account or task changes during validation, resolve that change before retrying. Never revive a cancelled task or resend another platform merely because the source was refreshed.

## "Repair unfinished items" on an unchanged source

Automatic repair is safe only on the same page when the account, task fingerprint, and uploaded video are unchanged, there is no login/captcha/risk gate, and `finalClickCount` is zero. Repair may re-read or reapply unfinished form controls, but must not refresh, re-upload, or submit.

If bounded repair is exhausted, expose the takeover page with a precise unfinished-item list. After the user or agent closes the platform page, re-read the form before regenerating the final confirmation.

## Duplicate title candidates

In Mac 0.2.120 post-submit verification, one complete matching title in the current account's visible management work item satisfies the app's 发布成功 rule even when repeated. Record that this is title presence, not unique attribution or public visibility. Before upload, preserve strict duplicate checks. Never resend to clarify a receipt. Windows may use this same business label only with the title-match evidence boundary explicitly recorded.

## Existing task is not visible

Clear or inspect task filters, then reconcile active task IDs against the ledger. Provide explicit continue/stop/delete actions for the exact old task. Never silently stop an unrelated task to start a new one.

## App or platform window changes size

Focus or reveal the intended window without forcing fullscreen or restoring a saved size from another platform. Leave fullscreen only if that specific platform window is actually fullscreen; wait for the native transition before hiding it.
