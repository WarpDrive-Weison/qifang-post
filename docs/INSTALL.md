# Installation and verification

## Verify downloads

Download the installer and `SHA256SUMS-0.2.103.txt` from the same GitHub Release.

macOS:

```bash
shasum -a 256 "QifangPost-0.2.103-macOS-QA-arm64.dmg"
```

Windows PowerShell:

```powershell
Get-FileHash ".\QifangPost-0.2.103-Windows-QA-x64-Setup.exe" -Algorithm SHA256
```

The calculated value must match the checksum list exactly.

## macOS

Requirements: macOS 12 Monterey or later on Apple Silicon.

1. Open the DMG.
2. Drag 齐放Post to Applications.
3. Open the installed application.

The current QA build is ad-hoc signed but not Apple-notarized. macOS may block the first launch. Review the warning and checksum before using System Settings > Privacy & Security to allow an app you trust. Do not disable Gatekeeper globally.

## Windows

Requirements: Windows 10 or 11 x64.

Run `QifangPost-0.2.103-Windows-QA-x64-Setup.exe`. It installs for the current user and creates Start menu and desktop shortcuts.

The current QA build has no Authenticode signature. Windows may show an unknown-publisher or SmartScreen warning. Continue only after verifying the checksum and source of the download.

Windows speech transcription may require the Simplified Chinese speech feature in Windows Settings.

## Update and uninstall behavior

Replacing the application is designed to preserve per-user accounts, drafts, media assets, and task records. Uninstalling the Windows application removes program files and shortcuts but intentionally leaves user data for a later reinstall. Back up important material before any upgrade.
