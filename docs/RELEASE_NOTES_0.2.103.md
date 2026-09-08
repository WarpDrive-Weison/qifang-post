# 齐放Post v0.2.103

Release channel: public pre-release / QA  
Release date: 2026-09-08

## Highlights

- Builds both platform packages from one source snapshot and bundles FFmpeg 9.0.1 LGPL-only executables with matching source and build metadata.
- Public QA packages omit the private managed-AI gateway and require a user-provided DeepSeek or OpenAI-compatible API for AI copy generation.
- Retains bounded same-page repair when a verified upload is complete but a cover or platform option is still transient. The repair keeps the same account, task, page, and uploaded video; it never refreshes, re-uploads, or performs the final publish click.
- Stabilizes workbench and platform-window sizing when returning from fullscreen or takeover views.
- Removes the unused AI refinement-preference field.
- Enforces a 20-character master-title limit and a 60-character short-body limit, generated from the full transcript rather than copied wholesale.
- Keeps only the current domestic platform scope: Douyin, WeChat Channels, Xiaohongshu, and Kuaishou.
- Supports first-frame or uploaded-image covers, with separate 3:4 and 4:3 crops and platform-side cover confirmation.
- Maintains native-topic selection and readback instead of treating plain `#text` as an accepted platform topic.

## Safety behavior

- Same-page automatic repair requires the same account, task fingerprint, and uploaded video, `finalClickCount = 0`, and no login/captcha/risk-control gate.
- Any change to a fingerprinted form value invalidates the previous final confirmation.
- A platform final-publish control is triggered at most once per task.
- Submission, review, management-list match, and public publication remain separate states.

## Known limitations

- macOS: Apple Silicon only, macOS 12+. The package is ad-hoc signed and not Apple-notarized.
- Windows: Windows 10/11 x64. The package was cross-built and structurally verified on macOS, but has not completed native Windows launch/install/login/publishing acceptance. It is not Authenticode-signed.
- Platform web pages can change without notice. Login, captcha, verification, risk control, agreement, or account-permission prompts may require user action.
- Automated tests do not constitute a new public post on any platform.

## Verification results

- Full Node regression: 668/668 passed.
- Electron/DOM regression: all 19 scripts passed, including 57/57 upload-entry structures.
- Real local-media pipeline and packaged macOS media/cover smoke: passed.
- macOS DMG: 161,421,301 bytes; all 20 packaged Mach-O files are arm64; `codesign --deep --strict` passed; SHA-256 `b33ad009f55cdd7fe1c205868c175f877fe9f7277d18cbe8083a5a6626f4cff4`.
- Windows Setup: 132,781,036 bytes; x64 application, FFmpeg, FFprobe, and sharp payload verified after NSIS extraction; SHA-256 `0a7e83196d1d939c78c7780aec67ec25dd4e6b53c1245f618018aff80e11fe6d`.
- Codex skill archive: extracted and validated; SHA-256 `c352abd28e9e82dc7ff4d9c9fe4c308d8b0137a2f091cc13aca11839756fe484`.
- The authoritative digest list is `SHA256SUMS-0.2.103.txt`.

## Downloads

- `齐放Post-0.2.103-macOS-QA-arm64.dmg`
- `齐放Post-0.2.103-Windows-QA-x64-Setup.exe`
- `qifang-post-skill-0.2.103.zip`
- `ffmpeg-9.0.1.tar.xz`
- `ffmpeg-9.0.1.tar.xz.asc`
- `SHA256SUMS-0.2.103.txt`
