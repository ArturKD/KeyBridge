# Publication Copy

Use the text below for Reddit or another community. Check its self-promotion
rules before posting. This copy describes Alpha 2; Alpha 1 does not include
in-app feedback or the updater. Do not claim end-to-end validation is complete.

## Suggested Title

KeyBridge for Windows: an early alpha for Magic Keyboard modifier and media keys

## Post

I am building KeyBridge, an independent Windows companion app for Apple keyboards.
It provides modifier presets, a configurable Fn shortcut, and model-aware
function-row actions for volume, media, brightness, and Windows shortcuts.

This is an early alpha, not an official Apple or Microsoft product.
**I have physically tested it only with Magic Keyboard with Numeric Keypad
A1843 (Lightning).** Other models have detection/layout profiles but have not
been physically tested by me. Citrix and NVIDIA GeForce NOW compatibility is
not guaranteed. Modifier remapping currently affects other keyboards too.

### Download And Install

1. Open https://github.com/ArturKD/KeyBridge/releases.
2. Open the newest alpha release and scroll to **Assets**; expand it if needed.
3. Click the **`-x64-Setup.exe`** file. Alpha 2 is
   `KeyBridge-1.1.0-alpha.2-x64-Setup.exe`.
4. Run the file from your browser's Downloads list or Windows Downloads folder.
5. Follow Setup and launch KeyBridge. Choose a modifier preset and an Fn shortcut.

Do not download **Source code (zip/tar.gz)** or **Code > Download ZIP**.
You do not need a GitHub account, Git, a .NET SDK, or a keyboard driver.
Windows 10 1809+ / Windows 11 x64 and .NET Framework 4.8+ are required.

The installer is unsigned, so Windows may show a SmartScreen warning.
Do not disable antivirus or system protection. Installation/upgrade validation
is still in progress. If updating an existing copy, use **Exit** in its system
tray menu first, then install the newer package without uninstalling.

Windows System mapping is optional and separately requires administrator
permission and a Windows restart; normal installation does not.

In Alpha 2, click **Send feedback**, write what went wrong, and press **Send**.
No browser or account is required. Basic version/keyboard/mapping metadata is
included; an optional event-log attachment is unchecked by default. Reports are
stored privately on Cloudflare for 90 days. Do not include personal information.
If sending fails, use https://github.com/ArturKD/KeyBridge/issues.
Do not upload unreviewed raw logs or complete settings files.

Alpha 2 also checks for newer releases and offers an **Update** button inside
the installed app. Alpha 1 users need one manual installation of Alpha 2 first.
Feedback and the full update flow are still undergoing real-PC testing.

Optional support: https://ko-fi.com/keybridgehelp. The app does not require a donation.

