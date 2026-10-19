# v0.2.120 QA scope

Mac arm64 QA prerelease, ad-hoc signed, not Apple notarized. Windows EXE is not distributed.

Final build passed 759 Node tests, the complete Electron release regression suite, packaged synthetic-media smoke checks, and package privacy checks (236 archive entries and 64 unpacked files). Final installed source matched the tested build.

Source-refresh regression covers all four platform task types, duplicate clicks, confirmation cancellation, stopped/submitted tasks, account/media/cover changes and late results. The actual renderer/preload/engine fixture checks success/failure progress-overlay cleanup and zero upload/publish side effects. Native installed-app validation confirmed the refreshed local media fingerprint and preservation of manual copy, covers, task history, accounts and settings within the refresh operation.

Inherited cover regression covers saved-receipt retention, explicit centered crop slots, separate portrait/landscape targets, wrong images, stale documents and cancellation. A save receipt alone is not accepted as cover success.

No new real-account publication, paid AI call, Windows native end-to-end run, other Mac hardware certification or Apple notarization is claimed. Offline regressions do not guarantee that every future platform-page revision will work.

发布成功 is the post-submit title-presence business result, not review approval or independently verified public visibility. Duplicate old titles can satisfy the user-selected rule; pre-upload duplicate checks remain separate.
