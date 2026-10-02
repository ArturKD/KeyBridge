# Installation And Updates

## Before Installing

Use an x64 Windows 10 1809+ or Windows 11 PC with .NET Framework 4.8 or newer.
Download the installer from [KeyBridge Releases](https://github.com/ArturKD/KeyBridge/releases),
not a third-party mirror. Public alpha builds are for testing, not production use.
If the release includes a SHA256 checksum, verify it with PowerShell:

```powershell
Get-FileHash .\KeyBridge-1.1.0-alpha.2-x64-Setup.exe -Algorithm SHA256
```

A matching checksum confirms the downloaded file matches the release asset;
it is not a digital signature or a guarantee that software is safe.

## Fresh Installation

1. Open [KeyBridge on GitHub](https://github.com/ArturKD/KeyBridge).
2. Click **Releases** on the right side of the repository page. On a phone or
   narrow window, scroll below the file list to find it. You can also go
   [directly to Releases](https://github.com/ArturKD/KeyBridge/releases).
3. Open the newest alpha release. Scroll to **Assets** and expand it if collapsed.
4. Click the file ending in **`-x64-Setup.exe`**. For Alpha 2 this is
   **`KeyBridge-1.1.0-alpha.2-x64-Setup.exe`**. Do not click **Code > Download ZIP**
   or **Source code (zip/tar.gz)**: those are not the Windows installer.
5. Open your browser's Downloads list, or the Windows Downloads folder, and
   run the downloaded Setup file under your normal Windows account. No GitHub
   account, Git installation, or source-code build is needed.
6. If KeyBridge is already running, select **Exit** from its system tray menu
   first. Closing its window may only hide it.
7. Follow Setup and leave **Launch KeyBridge** selected. The app installs into
   `%LOCALAPPDATA%\Programs\KeyBridge`. You can reopen it from the Start menu.
8. Check the detected keyboard model, then choose your modifier preset and Fn shortcut.

The installer does not install drivers or change Windows keyboard mappings.
Using Windows System mapping inside the app is a separate action that requires
administrator permission and a Windows restart.

## Hardware Test Coverage

This alpha has been physically tested only with **Magic Keyboard with Numeric
Keypad, model A1843 (Lightning)**. Other listed models have detection and
function-row profiles but have not been physically tested by the author.
USB/Bluetooth recognition does not imply that every transport/firmware combination
has been validated. Report unexpected behavior with other models as alpha feedback.

## Upgrade

### From Alpha 1 Or A Portable Copy

Alpha 1 has no updater. Follow these manual steps once to install Alpha 2.

1. Download a newer release for the same Windows user.
2. Exit KeyBridge through the tray menu. Do not just close its window.
3. Run the newer installer; do not uninstall first.
4. Open KeyBridge and verify the version in About.

### From An Installed Alpha 2 Or Newer

KeyBridge checks for updates at startup and every six hours. You can also click
**Check for updates** in **About**. When a newer compatible release exists,
an **Update** button appears. Click it to download, verify, install, and reopen
KeyBridge. Run the app normally, not as administrator, for in-app updating.
Do not close it during the download. No Windows restart is requested by updating.
This is an alpha feature and still needs end-to-end testing on an installed copy.
If updating fails, use the manual installation steps above. There is no automatic
rollback after a partially completed installation.

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
- **Unexpected behavior:** click Send feedback in Alpha 2 and describe what happened.
  Diagnostic event-log attachment is optional; private reports expire after 90 days.
  If sending fails, use Issues. Review and redact raw logs before sharing them publicly.

