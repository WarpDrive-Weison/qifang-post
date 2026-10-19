---
name: qifang-post
description: Prepare, publish, recover, and verify 齐放Post short-video tasks on four platforms, using the Mac app or a Windows AI-controlled browser workflow without the 齐放 app. Use when the user requests 齐放 publishing or recovery; requires available authorized browser controls for Windows mode.
metadata:
  version: "0.2.120"
---

# 齐放Post

Select the execution mode before acting. On Mac with an app-owned task, use 齐放Post as the system of record and keep its embedded page and ledger aligned. On Windows without the app, read [references/windows-browser.md](references/windows-browser.md) and use an AI-controlled local browser with a separate local task record. Do not apply app-only instructions to Windows browser mode or move an unresolved app task into another browser.

Skill release `0.2.120` aligns with the current Mac release's publishing rules, not its executable code or test results. Windows end-to-end execution is not yet verified by this release.

## Verify version and session ownership

For Mac app mode, read the app version shown by 齐放Post. This revision targets `0.2.120`; do not assume newer controls exist in older versions. Windows mode has no app-version prerequisite; verify the loaded skill version and actual browser-tool capabilities instead.

In Mac app mode, operate publishing forms only in Chromium windows opened and owned by 齐放Post for the current task. A takeover or management window opened by the app remains inside that task boundary and may be inspected or completed according to the confirmation rules below. Treat the same platform opened independently in another browser as read-only corroborating evidence unless the user explicitly requests otherwise and the account, media fingerprint, task identity, and final-click count are all reconciled. Never use an unrelated external page to recreate or resubmit the task.

## Start from the requested outcome

Confirm the finished local video, selected platforms, title/body/topic intent, cover choice, originality, location, download permission, collection, visibility, and timing. Preserve user-edited values. If an option was not requested, read the current app value instead of inventing a preference.

Open the relevant reference only when needed:

- For the Mac app flow, read [references/workflow.md](references/workflow.md).
- For Windows without the app, read [references/windows-browser.md](references/windows-browser.md).
- For platform-specific form and cover checks, read [references/platform-checkpoints.md](references/platform-checkpoints.md).
- For stalled uploads, cover dialogs, recovery, duplicate candidates, or task conflicts, read [references/recovery.md](references/recovery.md).
- For evidence levels and completion language, read [references/evidence.md](references/evidence.md).

## Non-negotiable invariants

- A percentage or upload-complete message proves transport only; it does not prove form readiness, submission, review, or public publication.
- `FORM_READY` means the intended video and required fields were read back on the platform page. It is not permission to submit.
- Treat the final confirmation fingerprint as a safety boundary. If account, video, title/body, topics, cover, platform options, or task identity changes, require a fresh confirmation.
- Trigger a platform's final publish control at most once for a task. If a receipt or management-list match is unresolved, inspect and reconcile; never resend merely to obtain clearer evidence.
- A typed `#topic` is not necessarily a native topic. Verify the platform accepted the suggestion and rendered its selected topic chip/token when the platform supports native topics.
- A front-end cover preview is not proof that the platform uses that cover. Verify the platform cover editor shows the bound image and that its confirmation dialog closes successfully.
- Login, QR scan, captcha, identity check, account permission, risk control, and updated platform agreements are user gates. Pause at the exact gate and keep the task recoverable; never bypass or falsely mark it complete.
- In Mac 0.2.120, `PUBLISHED` displays 发布成功 and means a complete matching title was found in the current account's visible management-list item after submission. It does not prove review approval, public visibility, or unique attribution to this upload; old same-title items can match. Never use this post-submit rule to weaken pre-upload duplicate checks. Windows records must distinguish this title-match business result from independently observed platform public status.

## Finish cleanly

Record one outcome per platform, including the account, task identity, video fingerprint, final-click count, receipt or list evidence, and any remaining user gate. When all selected platforms have a terminal evidenced state, return a concise per-platform ledger instead of a single blended success claim.
