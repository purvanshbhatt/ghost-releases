# Ghost downloads

Ghost is an AI copilot for interviews, practice and meetings: a live
transcript and suggested answers while you talk. Bring your own AI key
(OpenAI, Anthropic, Gemini, Groq or a local Ollama server).

This repository only holds the installers. **[Download the latest release](https://github.com/purvanshbhatt/ghost-releases/releases/latest)**

| Device | File | Needs |
|---|---|---|
| Mac | [Ghost-macOS.dmg](https://github.com/purvanshbhatt/ghost-releases/releases/latest/download/Ghost-macOS.dmg) | macOS 26 Tahoe, Apple silicon or Intel |
| Windows | [Ghost-Windows-Setup.exe](https://github.com/purvanshbhatt/ghost-releases/releases/latest/download/Ghost-Windows-Setup.exe) | Windows 10 or 11, 64-bit |
| Android | [Ghost-Android.apk](https://github.com/purvanshbhatt/ghost-releases/releases/latest/download/Ghost-Android.apk) | Android 8.0 or later |
| iPhone and iPad | [Ghost-iOS-unsigned.ipa](https://github.com/purvanshbhatt/ghost-releases/releases/latest/download/Ghost-iOS-unsigned.ipa) | iOS 26, installed by sideloading (below) |
| Linux (Debian, Ubuntu) | [Ghost-linux-amd64.deb](https://github.com/purvanshbhatt/ghost-releases/releases/download/v0.2.6/Ghost-linux-amd64.deb) | 64-bit; version 0.2.6 |
| Linux (any distro) | [Ghost-linux-x86_64.AppImage](https://github.com/purvanshbhatt/ghost-releases/releases/download/v0.2.6/Ghost-linux-x86_64.AppImage) | 64-bit; version 0.2.6 |
| Chrome, Edge, Brave | [ghost-chrome-extension.zip](https://github.com/purvanshbhatt/ghost-releases/releases/download/v0.2.6/ghost-chrome-extension.zip) | Unzip, then **Load unpacked** in `chrome://extensions`; version 0.2.6 |

These builds are not signed with a paid Apple or Microsoft certificate yet,
so your computer asks you to confirm the first time. The steps below show
where to click.

## Mac

1. Open `Ghost-macOS.dmg` and drag **Ghost** into **Applications**.
2. Open Ghost. macOS says it can't check the app for malicious software.
   Click **Done**.
3. Open **System Settings > Privacy & Security**, scroll down, and click
   **Open Anyway** next to Ghost. Confirm with your password.
4. Ghost lives in the menu bar (top right), not in the Dock.
5. When you start a session, allow **Microphone** and **Screen & System
   Audio Recording**. Ghost records audio only; it needs the second one to
   hear the other side of a call.

Use headphones on calls so your speakers don't leak into the microphone.

## Windows

1. Run `Ghost-Windows-Setup.exe`.
2. If you see "Windows protected your PC", click **More info**, then
   **Run anyway**.
3. Ghost installs for your user only (no admin password) and adds a Start
   menu and desktop shortcut. Uninstall it from **Settings > Apps >
   Installed apps**.

## Android

1. On the phone, open this page and tap `Ghost-Android.apk`.
2. When asked, allow your browser to install unknown apps, then tap
   **Install**.
3. If an older Ghost from another source is installed and the install fails,
   uninstall the old one first.

## iPhone and iPad (sideloading)

Apple only lets App Store apps install directly, so the `.ipa` is unsigned and
you sign it with your own Apple ID. A free Apple ID works; the app then runs
for 7 days before it has to be signed again, and you can sideload up to 3 apps.

**With Sideloadly (Windows or Mac, USB cable):**

1. Install [Sideloadly](https://sideloadly.io) on your computer and connect
   the iPhone with a cable. On Windows, install iTunes from Apple's website
   first.
2. Drag `Ghost-iOS-unsigned.ipa` into Sideloadly, enter your Apple ID, and
   click **Start**.
3. On the iPhone, open **Settings > Privacy & Security > Developer Mode**,
   turn it on, and restart when asked.
4. Open **Settings > General > VPN & Device Management**, tap your Apple ID,
   and tap **Trust**.
5. Open Ghost. Sign it again with Sideloadly every 7 days (free Apple ID).

**With AltStore (refreshes itself over Wi-Fi):**

1. Install AltServer on your computer from [altstore.io](https://altstore.io)
   and use it to install AltStore on the iPhone.
2. Open the `.ipa` from the Files app with AltStore, or tap **+** in AltStore's
   My Apps tab.
3. Keep AltServer running on the same Wi-Fi so AltStore can refresh the app
   before the 7 days run out.

With a paid Apple Developer account the signature lasts a year.

## What each version can hear

- **Mac:** your microphone (you) and the computer's sound (them).
- **Windows:** your microphone and the computer's sound.
- **Android:** the microphone, and phone calls on speaker.
- **iPhone and iPad:** the microphone only. iOS doesn't let any app hear
  phone calls or other apps, so use it for in-person conversations or calls
  on another device. The latest answer also shows on the Lock Screen and in
  the Dynamic Island.

## Linux

Install the `.deb` with `sudo apt install ./Ghost-linux-amd64.deb`, or make
the AppImage executable (`chmod +x Ghost-linux-x86_64.AppImage`) and run it.
Linux and the Chrome extension are still on version 0.2.6.

## Checking a download

Every release includes `SHA256SUMS.txt`. On Mac or Linux:
`shasum -a 256 <file>`. On Windows: `certutil -hashfile <file> SHA256`.

This repository holds release files only. Ghost is licensed under GPL 3.0 or
later; see `LICENSE`.
