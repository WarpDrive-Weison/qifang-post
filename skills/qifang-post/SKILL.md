---
name: qifang-post
description: Use the 齐放Post desktop app to prepare, publish, recover, and verify short-video tasks for Douyin, WeChat Channels, Xiaohongshu, and Kuaishou. Trigger for operating or troubleshooting 齐放Post; do not use it to bypass platform login, captcha, risk-control, account-permission, or final-confirmation gates.
metadata:
  version: "0.2.103"
---

# 齐放Post

Use 齐放Post as the system of record for a multi-platform publishing task. Keep the app task, the embedded platform page, and the platform management list aligned; do not substitute an unrelated browser session for an app-owned session.

## Verify version and session ownership

Before operating, read the app version shown by 齐放Post. This workflow requires version `0.2.103` or newer. If the version is older or cannot be verified, report the mismatch and do not assume that the cover, repair, fingerprint, or one-click protections described here are available.

Operate publishing forms only in Chromium windows opened and owned by 齐放Post for the current task. A takeover or management window opened by the app remains inside that task boundary and may be inspected or completed according to the confirmation rules below. Treat the same platform opened independently in another browser as read-only corroborating evidence unless the user explicitly requests otherwise and the account, media fingerprint, task identity, and final-click count are all reconciled. Never use an unrelated external page to recreate or resubmit the task.

## Start from the requested outcome

Confirm the finished local video, selected platforms, title/body/topic intent, cover choice, originality, location, download permission, collection, visibility, and timing. Preserve user-edited values. If an option was not requested, read the current app value instead of inventing a preference.

Open the relevant reference only when needed:

- For the normal end-to-end flow, read [references/workflow.md](references/workflow.md).
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
- `SUBMITTED`, `SCHEDULED`, `REVIEWING`, management-list match, and `PUBLISHED` are distinct states. Report only the strongest state actually evidenced.

## Finish cleanly

Record one outcome per platform, including the account, task identity, video fingerprint, final-click count, receipt or list evidence, and any remaining user gate. When all selected platforms have a terminal evidenced state, return a concise per-platform ledger instead of a single blended success claim.
