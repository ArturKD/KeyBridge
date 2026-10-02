# Installation And Updates

## Before Installing

Use an x64 Windows 10 1809+ or Windows 11 PC with .NET Framework 4.8 or newer.
Download the installer from [KeyBridge Releases](https://github.com/ArturKD/KeyBridge/releases),
not a third-party mirror. Public alpha builds are for testing, not production use.
If the release includes a SHA256 checksum, verify it with PowerShell:

```powershell
Get-FileHash .\KeyBridge-1.1.0-alpha.1-x64-Setup.exe -Algorithm SHA256
```

A matching checksum confirms the downloaded file matches the release asset;
it is not a digital signature or a guarantee that software is safe.

## Fresh Installation

1. Exit any running KeyBridge copy through its system tray menu.
2. Run the installer under your normal Windows account.
3. The app installs into `%LOCALAPPDATA%\Programs\KeyBridge`.
4. Launch KeyBridge from the Start menu and check the detected keyboard model.
5. Review your modifier mapping, Fn shortcut, and startup preference.

The installer does not install drivers or change Windows keyboard mappings.
Using Windows System mapping inside the app is a separate action that requires
administrator permission and a Windows restart.

## Upgrade

1. Download a newer release for the same Windows user.
2. Exit KeyBridge through the tray menu. Do not just close its window.
3. Run the newer installer; do not uninstall first.
4. Open KeyBridge and verify the version in About.

Settings, backups, and logs remain in `%LOCALAPPDATA%\KeyBridge`.
Pending administrator/restart state is stored with the settings. The system
mapping recovery journal remains in the Windows registry. Setup replaces
neither location. A pending system change still needs the indicated action;
updating or restarting the app does not substitute for a Windows restart.

Existing KeyBridge startup entries are redirected when recognized. The
installer does not enable a missing startup entry or override a Windows
Startup Apps disabled choice. On launch, KeyBridge reconciles startup with
your saved preference.

If you previously used a portable EXE, stop launching the old copy after
verifying the installed one. Both copies share settings and a single-instance
guard. Downgrading to an older alpha is not supported.

## Uninstall

1. If you want to remove a Windows System mapping, reset it in KeyBridge first
   and follow the administrator/restart instructions. Do this before uninstalling.
2. Exit KeyBridge from the system tray.
3. Remove KeyBridge in Windows Installed apps.

User settings are retained for future installation. Uninstalling does not undo
a Windows System mapping, erase its recovery journal, or reboot Windows.

## Installation Problems

- **App is running:** use Exit in its tray menu, then retry.
- **.NET Framework missing:** install .NET Framework 4.8 or newer from Microsoft,
  then retry; end users do not need the .NET SDK.
- **Security warning:** current alpha packages are unsigned. Verify the release
  source and checksum. Do not disable antivirus or system protection.
- **Unexpected behavior:** report the version and reproduction steps through
  Issues. Review and redact logs before sharing them.
