# v0.2.112 QA scope

Release channel: Mac QA prerelease, Apple Silicon / arm64. Ad-hoc signature, not Apple Developer ID notarization. No Windows EXE is distributed.

## Source regression

- 723 Node tests and all Electron suites in the release build, followed by build-input validation.
- Actual renderer/preload and isolated local state: unlimited manual copy, AI-only 20/60 limits, delayed AI/manual edit conflicts, failed persistence and explicit retry, master-sync races, focus/selection preservation.
- Failed pending manual writes continue to block publishing preparation. Closing preserves unsaved edits; settings/credentials do not silently save on close.
- Settings whole-request validation, independent provider drafts, late replies, background refresh and empty states.
- Offline platform DOM fixtures, cover binding/recovery, manual/automatic confirmation-window modes, ledger filtering, notifications and cancellation boundaries.

## Packaged application

Passed: arm64 binary/version, ad-hoc signature integrity, DMG verification, SHA-256, packaged-source match, dependency/legal inventory and runtime-package privacy allowlist (236 archive entries and 64 unpacked files). Packaged local synthetic-video tests passed for portrait/social/horizontal/landscape outputs, source pixel mapping, image replacement and immutable prior assets.

Native startup was observed from the extracted package and the installed application, using separate empty test profiles: version 0.2.112, zero signed-in accounts, and an empty task ledger. Screenshots were retained privately. Real publishing tasks were not resumed. No author profile, account sessions, draft database, task ledger, API-key files or private media are release assets. The configured managed HTTPS relay is not a private upstream key.

## Skill

Skill 0.2.112 aligns its Mac target and documented publishing rules with the release. Frontmatter, references and ZIP/source byte integrity are checked. It remains a workflow, not an executable or browser-control engine. Mac APP UI/save improvements do not claim equivalent functionality in Windows browser mode.

## Not covered

- New live platform publication, long-running network uploads or real-account changes: NOT_RUN.
- Paid AI calls, real API-key storage and live relay availability testing: NOT_RUN.
- Windows native browser end-to-end publishing: NOT_RUN.
- Other Mac models/OS installations, Developer ID notarization, exhaustive accessibility or native IME certification: NOT_RUN.

Historical QA reports are retained unchanged. Local source archives are private; this repository and its tag archives contain public documentation/skill material, not proprietary APP source.
