# v0.2.118 QA scope

Mac arm64 QA prerelease, ad-hoc signed, not Apple notarized. Windows EXE is not distributed.

The reported Douyin page was inspected read-only. Its task audit already contained a remote playable video (readyState 4, no media error) and a ready form, while the uploader observer classified the optional AI recommendation spinner as video processing. No final click had occurred.

Regression covers optional recommended-cover generation, actual concurrent transfer/transcoding/failure, hidden recommendation text and conservative unknown cover processing. Ignoring recommendations alone never proves upload completion. No classification of generic code 2000 as success was added.

Passed: 735 Node tests and the complete Electron release regression suite, including four-platform manual/automatic confirmation with zero window-resize events. The final narrowed observer also passed the updated upload-phase fixture and old-versus-new reproduction. Package privacy checks passed (236 archive entries, 64 unpacked files); bundled synthetic-media checks passed. No new real-account publication, paid AI call, Windows native end-to-end run, other Mac hardware certification or Apple notarization is claimed.

发布成功 remains the app's post-submit title-presence business result, not review approval or independently verified public visibility. Duplicate old titles can satisfy this user-selected rule. Upload-before-submit and duplicate prevention checks remain separate.
