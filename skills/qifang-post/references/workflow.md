# Mac app workflow

## 1. Establish the task identity

Identify the exact local MP4/MOV and selected platform accounts. Let 齐放Post compute or display the media fingerprint. Do not reuse an older task merely because the title is similar.

If the app reports an existing active task, inspect the task ledger before starting a replacement. Continue, stop, or delete only the exact task selected by the user. A hidden filter is not proof that no task exists.

## 2. Prepare copy and topics

Import the finished video, obtain the transcript, then let the app produce a concise master title and short body. Read the generated values back before continuing:

- AI-generated Chinese title: at most 20 Unicode characters; AI-generated body: at most 60.
- Preserve manual edits in full, including longer text and line breaks. Check each platform's actual limits separately; warn and request adjustment instead of silently truncating.
- Platform copies may differ when requested by the user.
- Do not paste a long transcript into the body merely because transcription succeeded.

In app 0.2.120, check the local save status before preparing publication. If saving fails, keep the current window and use its retry control; do not regenerate AI copy or reload simply to clear the message. AI and master-sync proposals apply only after persistence; newer manual edits remain owned by the user. Unsaved settings or API keys require explicit handling when closing, rather than being silently saved.

For topics, type the intended term, wait for suggestions, prefer an exact match and otherwise choose the first applicable visible native topic candidate when ambiguous. Verify the selected chip/token; do not choose unrelated controls or duplicate tokens.

## 3. Bind covers

Confirm both domestic cover canvases:

- Vertical cover: 3:4, normally 1080 x 1440.
- Horizontal/share cover: 4:3, normally 1440 x 1080.

The cover may come from the video's first frame or an uploaded PNG/JPG/WebP/TIFF. Preserve the user's crop. After 齐放Post enters a platform cover editor, verify the intended image is visible, activate the platform's own Confirm/Upload control, and read back the closed dialog or changed cover preview.

## 4. Prepare each platform form

Wait for video transport and platform processing. Then read back title/body, native topics, cover, visibility, timing, and every requested platform option. Do not call the form ready while a cover dialog, agreement, spinner, or validation message remains open.

If the app performs a bounded same-page repair, allow it only when all of the following still match: account, task fingerprint, uploaded video, and zero final clicks. It must not refresh the page, re-upload the video, or press the final publish button.

## 5. Confirm and submit

New Mac configurations default to secondary confirmation off; preserve existing saved settings. Use the batch confirmation fingerprint when confirmation is enabled, only after every selected platform reaches `FORM_READY`. If any fingerprinted field changes, regenerate the confirmation.

After the applicable app authorization checks, submit no more than once. Capture the immediate receipt/status before closing or hiding the platform page. This setting does not grant separate AI tools permission to publish unrequested content.

## 6. Verify independently

After submission, the app accepts a complete matching title in a visible work item of the current account's management list. Time, review state and candidate uniqueness are not required. Record title-match evidence, including the possibility of an old same-title item; do not treat a search field, editor or truncated title as a match. Keep pre-upload deduplication strict.

Return one result per platform. “发布成功” describes this app rule, not public availability or review approval. Never resubmit just to get clearer evidence.
