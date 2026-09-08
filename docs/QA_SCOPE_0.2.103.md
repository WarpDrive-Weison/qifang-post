# v0.2.103 QA scope

QA date: 2026-09-08 (Asia/Shanghai)

## Required release checks

- Full Node regression.
- Electron/DOM platform-structure regression.
- Real local-media pipeline smoke using the packaged executables.
- Package-source parity and architecture checks.
- FFmpeg/FFprobe license and configuration readback proving neither `--enable-gpl` nor `--enable-nonfree` is present.
- SHA-256 verification after final artifact creation.

## Platform-specific evidence

- macOS: DMG verification, ZIP integrity, application parity, arm64 checks, ad-hoc signing integrity, install/launch check, and preservation counts.
- Windows: Setup and portable extraction, AMD64 checks, package-source parity, NSIS structure, UTF-8 path verification, and checksum readback.

## Evidence boundary

The macOS checks include local packaging and app acceptance on the build Mac. The Windows checks are structural cross-build checks only; no Windows machine or virtual machine was available for native acceptance.

Neither set of automated checks proves a new public post. A progress percentage proves upload transport only. `FORM_READY`, final submission, platform review, management-list match, and public publication require separate evidence.

Final numeric results and hashes are published in the GitHub Release after the rebuilt artifacts pass.
