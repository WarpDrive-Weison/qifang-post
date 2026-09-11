# v0.2.109 QA scope

## Scope

- Human-authored title/body preservation across native text input, renderer/preload IPC, disk persistence, restart and synchronization to four platform drafts.
- AI normalization continues to enforce Chinese title/body generation limits of 20/60 Unicode characters. Human edits after generation are preserved without those caps.
- Platform-specific publish limits are checked separately; drafts remain intact on failure.
- Default manual confirmation and opt-out automatic confirmation use offline four-platform fixtures with one-click and window-size assertions.

## Regression results

- Node test suite: 691 passed, 0 failed.
- Native text-input regression covers a title longer than 20 characters and a multiline body longer than 6,000 characters, disk reopen, four-platform synchronization, platform-limit warnings, and unrestricted edits after AI generation.
- The AI fixture calls the application normalizer and checks that generated title/body remain within 20/60 characters. It is not a live model-service test.
- All 19 browser DOM fixture scripts, cover recovery, and both four-platform confirmation/window fixtures passed; both confirmation fixtures recorded zero native resize events.
- Packaged media smoke test passed on a 31.633333-second 1080×1920 local video, including four cover formats and alternate-source checks.
- DMG checksum verification, strict deep ad-hoc signature verification, arm64 executable check, and packaged-code hashes passed. The managed-AI endpoint remains enabled without an embedded upstream credential.
- Local replacement from 0.2.108 to 0.2.109 was opened successfully; original draft/settings/account entries, task IDs, assets and final-click totals were preserved. UI labels now explicitly distinguish AI limits from manual editing.

## Evidence boundary

These are local regression and package checks, not a new public post. No online AI-service availability or quota guarantee is made. The package is ad-hoc signed, without Apple notarization or another-Mac installation acceptance. Windows distribution remains withdrawn.

The optional skill stays at 0.2.103 and retains its manual-confirmation workflow. No proprietary application source is published; GitHub source archives contain public documentation and the skill only.
