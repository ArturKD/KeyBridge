# KeyBridge for Windows

Make compatible Apple keyboards feel natural on Windows.

KeyBridge is an independent Windows utility for modifier-key mapping and
model-specific function-row shortcuts. This repository contains application
downloads, documentation, and issue reports, not the application source code.

**Alpha software:** behavior may change, and compatibility is not guaranteed.
KeyBridge is not affiliated with Apple, Microsoft, Citrix, or NVIDIA.

## Download

Open [Releases](https://github.com/ArturKD/KeyBridge/releases), select the newest alpha, and
download the file ending in `-x64-Setup.exe` from **Assets**.
GitHub's automatically generated source ZIP/TAR archives are not the app.

Requirements: Windows 10 1809 or newer, or Windows 11, on an x64 PC, with
.NET Framework 4.8 or newer. ARM64 is not supported by this installer.
No .NET SDK or keyboard driver is required.

## Features

- Modifier presets and custom Control, Option, and Command mappings.
- Live Layer while KeyBridge runs, or Windows System mapping after restart.
- Model-specific function-row actions: brightness, volume, media playback,
  Task View, and other Windows shortcuts.
- A configurable Fn shortcut key; compact keyboards can also assign a
  Print Screen shortcut. Full-size keyboards use Fn + F13 for Print Screen.
- Device information, connection status, and battery information when available.
- System tray operation and optional launch at Windows sign-in.

## Keyboard Models

| Model | Format | Connector | Function Row |
| --- | --- | --- | --- |
| A1644 | Compact | Lightning | Old |
| A1843 | Numeric keypad | Lightning | Old |
| A2449 | Compact, Touch ID | Lightning | Modern |
| A2450 | Compact, Lock key | Lightning | Modern |
| A2520 | Numeric keypad, Touch ID | Lightning | Modern |
| A3118 | Compact, Touch ID | USB-C | Modern |
| A3119 | Numeric keypad, Touch ID | USB-C | Modern |
| A3203 | Compact, Lock key | USB-C | Modern |

These models have detection and function-row profiles in KeyBridge.
This is not a claim that every model, transport, or firmware has been tested.
Touch ID authentication on Windows is not provided by KeyBridge.

## Install And Update

The installer uses `%LOCALAPPDATA%\Programs\KeyBridge` for the current user.
Normal installation does not request administrator permission.

Exit a running copy using **Exit** in the system tray before installing or
updating. Closing the main window may only hide it.
Run the newer installer without uninstalling the old version first.
Your settings and pending restart state are retained.

See [Installation and updates](INSTALLATION.md) for details, including removal
of an existing Windows System mapping.

## Alpha Limitations

- Both Live Layer and Windows System mapping affect other keyboards too.
- Windows System changes require administrator permission and a Windows restart.
  Restarting only KeyBridge does not apply them.
- Windows-reserved shortcuts, including Win+L, may keep their original behavior.
- Citrix and NVIDIA GeForce NOW input compatibility is not guaranteed.
- Left Win and Right Win cannot be assigned as Fn or Print Screen shortcuts.
- Some settings pages are unavailable in the alpha.
- Brightness and battery availability depend on the connected hardware.
- Updates are manual. Downgrades are not supported.
- Alpha installers are currently unsigned; Windows may show a SmartScreen warning.
  Do not disable antivirus or system protection to install KeyBridge.

## Feedback

Use [Issues](https://github.com/ArturKD/KeyBridge/issues) and the bug-report template.
Include the app version from **About**, Windows version, keyboard model,
connection type, mapping mode, and steps to reproduce.
Do not publish passwords, personal information, complete settings, or unreviewed
logs. Logs may contain local paths and device identifiers.

## Support

Optional support: [Support KeyBridge on Ko-fi](https://ko-fi.com/keybridgehelp).
Support does not unlock features or require payment to report a problem.

## Distribution Status

The first public alpha is available for testing. Installation and upgrade
validation is still in progress. This repository does not grant an
open-source license or redistribution rights for the application.
Explicit application distribution terms have not been finalized.
