# Privacy notice

## Local data

齐放Post stores platform sessions, account descriptors, the imported video's absolute local path and media fingerprint, draft metadata, cover assets, task state, and append-only publishing evidence in the current operating-system user's application-data area. The app records the path so it can identify and reuse the selected local file; it does not copy the original video into its application-data directory. Installers do not contain account sessions, and copying an installer to another computer does not copy login state.

The app does not record platform passwords. Login, QR scan, captcha, verification, risk control, and platform agreements are completed directly in each platform's embedded Chromium page.

## Video and cover data

Imported videos and generated/uploaded cover assets are processed locally before the selected platform receives them. The selected publishing platform receives the video and metadata when the user starts that platform's upload.

The public QA build does not include 齐放Post's private managed-AI gateway or managed media-upload service.

## Optional AI copy generation

When the user configures a DeepSeek or OpenAI-compatible API and requests AI copy generation, the transcript, filename context, duration, and user-supplied copy prompt needed for the request may be sent to that provider. A user-provided API key is stored with Electron's operating-system-backed secure storage when available and is not intentionally written to logs.

## Publishing evidence

The local ledger records task state, platform, account descriptor, media fingerprint, final-click count, receipt/status evidence, and timestamps. It is designed not to store platform passwords or raw API keys.

## Retention and deletion

Uninstalling 齐放Post removes the application but intentionally leaves its per-user data so that accounts, drafts, generated assets, and task evidence can survive a reinstall. The default Electron user-data locations are:

- macOS: `~/Library/Application Support/齐放Post`
- Windows: `%APPDATA%\齐放Post` (normally `C:\Users\<user>\AppData\Roaming\齐放Post`)

To remove the app's retained data, first quit 齐放Post and close every platform window it opened. Then use Finder's **Go to Folder** or Windows File Explorer to locate and delete only the exact `齐放Post` directory shown above. This removes the app's local sessions, encrypted API-key files, drafts, derived media/cover assets, and publishing ledger. It does not delete the original video at the absolute path recorded by the app. Back up anything needed for audit or recovery before deletion.

## User responsibility

Review the privacy terms of every selected publishing and AI platform. Do not publish media without the necessary rights and consent. Before sharing diagnostics, remove account identifiers, personal data, cookies, tokens, QR codes, and private media paths.
