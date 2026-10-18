# Windows: AI + local browser, without the 齐放Post app

This is a skill-guided workflow, not an EXE, background service, or port of the Mac app. It requires a Windows AI host with authorized local browser control, file upload, and local task-record storage. A text-only chatbot or merely opening Edge does not provide these capabilities. Check the host's actual tools before promising execution; if absent, report `BLOCKED` with the missing capability. Do not invent tool APIs or use another method to evade a denied tool/site permission.

## Establish ownership and inputs

Use the user's chosen installed browser (for example Edge or Chrome) only if the host can control it. Observe the live page, signed-in account, tab/window identity and current draft. The browser owns login state; do not extract, export or copy Cookies. The user handles login, captcha, risk prompts and new agreements.

Identify the exact MP4/MOV and selected accounts; compute its SHA-256 with an available local tool (PowerShell `Get-FileHash -Algorithm SHA256 -LiteralPath <path>` is one option). Record a unique task ID, skill version, media hash, platform/account alias, tab identity, title/body, selected topics, intended cover paths/hashes/crops, options, state, final-click status and evidence timestamps in a user-approved local JSON or Markdown file. Keep credentials and QR images out of it. Check this record and the live platform draft/list before starting a new upload, including after an AI session restart.

## Prepare and verify the form

1. Preserve the user's title/body. Only newly AI-generated Chinese copy uses the 20-character title and 60-character body caps. Do not truncate manual copy; surface platform-specific validation separately. Transcription/copy generation uses the chosen AI host's capabilities, not the Mac app's bundled service.
2. Use the confirmed image covers or extract the requested first frame with an available local media tool. The baseline canvases are 3:4 vertical and 4:3 horizontal/share; preserve the approved crop and verify what each actual platform slot accepts. If required media processing is unavailable, ask for prepared covers rather than substituting a random frame.
3. Upload through the verified tab's supported file-upload mechanism. Wait for both transfer and processing. Never enter local paths into unrelated page fields or assume a progress percentage proves completion.
4. Follow [platform-checkpoints.md](platform-checkpoints.md) for native selected topic tokens, cover-source choice, nested dialogs and requested collection, originality, download, visibility, scheduling and cross-product settings. Mac-preview references mean the user's supplied cover preview in this mode.
   For native topic suggestions, prefer an exact match; if still ambiguous choose the first applicable visible candidate for the intended query, then read back the selected token. Do not treat arbitrary controls or plain hash text as selected topics.
5. After each cover upload/crop, confirm the correct modal and read back closure and the resulting preview. Repair the same page only while identity is unchanged and no final submission has been attempted. If two re-observed attempts make no progress, preserve the page and report the exact unfinished step; do not loop, refresh or re-upload blindly.

## Submit once and reconcile

Persist `FORM_READY` only after actual page readback. Present the account/media/copy/topics/covers/options fingerprint for explicit final confirmation. The Mac app's optional auto-confirm setting does not grant this AI host permission. A changed fingerprint needs fresh confirmation.

Before the final click, persist `submission_attempted` with timestamp and fingerprint. Activate the final publish control once, then persist the observed receipt/content ID/status. If interrupted between recording the attempt and observing the result, treat it as `SENT_UNACK`: inspect the existing tab and management list, never repeat the click merely because the recorded count is unknown. This is a workflow requirement, not an app-enforced transactional guarantee.

Use [evidence.md](evidence.md) to distinguish title-match completion from actual review/public visibility. After submission, a complete same title in a visible management work item for the selected account can be recorded as 发布成功 under the app-aligned business rule; no time or review-state requirement. Record that old same-title items can match. Keep pre-upload duplicate checks and final-click protection strict. Return one result per platform, retain resumable tabs/records and identify user gates; do not promise execution while the AI host is closed or disconnected.
