# Privacy notice

## Local data

齐放Post stores platform sessions, account descriptors, the imported video's absolute local path and media fingerprint, draft metadata, cover assets, task state, and append-only publishing evidence in the current operating-system user's application-data area. The app records the path so it can identify and reuse the selected local file; it does not copy the original video into its application-data directory. Installers do not contain account sessions, and copying an installer to another computer does not copy login state.

The app does not record platform passwords. Login, QR scan, captcha, verification, risk control, and platform agreements are completed directly in each platform's embedded Chromium page.

## Video and cover data

Imported videos and generated/uploaded cover assets are processed locally before the selected platform receives them. The selected publishing platform receives the video and metadata when the user starts that platform's upload.

The 0.2.107 QA package includes an HTTPS managed text-generation endpoint. Managed media upload and cloud transcription are disabled in this package; the text-generation request does not contain the complete video or cover file.

## Optional AI copy generation

When the user requests AI copy generation through the default service, the app sends the transcript, title context, duration, media SHA-256, locale, installation identifier and client version to 齐放Post's HTTPS server. The server calls the upstream AI provider and returns text. Upstream API credentials are server-side rather than bundled in the client configuration. Service availability and quota are controlled by the server; a configured endpoint is not a guarantee of uninterrupted access.

If the user instead configures a personal DeepSeek or OpenAI-compatible API, the transcript and other necessary prompt context may be sent to that provider. A user-provided API key is stored with Electron's operating-system-backed secure storage when available and is not intentionally written to logs. Manual copy entry does not require an AI request.

## Publishing evidence

The local ledger records task state, platform, account descriptor, media fingerprint, final-click count, receipt/status evidence, and timestamps. It is designed not to store platform passwords or raw API keys.

## Retention and deletion

Removing the macOS application bundle leaves its per-user data so that accounts, drafts, generated assets, and task evidence can survive a reinstall. The current public package uses:

- macOS: `~/Library/Application Support/齐放Post`

To remove the app's retained data, first quit 齐放Post and close every platform window it opened. Then use Finder's **Go to Folder** to locate and delete only the exact `齐放Post` directory shown above. This removes the app's local sessions, encrypted API-key files, drafts, derived media/cover assets, and publishing ledger. It does not delete the original video at the absolute path recorded by the app. Back up anything needed for audit or recovery before deletion.

Windows distribution was withdrawn on 2026-09-11. Withdrawing its download does not remotely delete existing installations or their locally retained data.

## User responsibility

Review the privacy terms of every selected publishing and AI platform. Do not publish media without the necessary rights and consent. Before sharing diagnostics, remove account identifiers, personal data, cookies, tokens, QR codes, and private media paths.
