# v0.2.117 QA scope

Mac arm64 QA prerelease, ad-hoc signed, not Apple notarized. Windows EXE is not distributed.

Passed: 735 Node tests and the complete Electron regression suite, package-input/privacy checks (236 archive entries, 64 unpacked files), and packaged synthetic-media checks. Coverage includes title-presence verification on four platform fixtures, strict pre-upload duplicate detection, topic selection, cover binding, single-submit protection, manual copy preservation, AI retry/error handling, settings and confirmation-window sizing. Both four-platform manual and automatic confirmation fixtures recorded zero resize events. The actual renderer's task badge and published filter were asserted as 发布成功 and captured in an isolated screenshot.

发布成功 is the app's post-submit title-presence business result, not independently verified public availability. Duplicate old titles can satisfy this user-selected rule. Original platform metadata and title-match evidence remain distinct.

No new real video publication, paid AI call, Windows native end-to-end run, other Mac hardware certification or Apple notarization is claimed. Runtime artifacts exclude author accounts, tasks, Cookies, private drafts and keys. The managed HTTPS endpoint is not an upstream secret.

The skill shares documented rules/version only; it is not an execution engine. Historical QA notes are unchanged.
