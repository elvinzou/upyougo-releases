<p align="center"><img src="../../assets/brand-cover-en.svg" width="100%" alt="UpYouGo: stay focused, remember to move"></p>

<p align="center"><strong>A better rhythm for your workday.</strong><br>A Windows sit–stand reminder with responsive desktop companions.</p>

<p align="center"><a href="https://github.com/elvinzou/upyougo-releases/releases/latest"><strong>Download 1.4.2</strong></a> · <a href="USER_GUIDE.md">User guide</a> · <a href="CHANGELOG.md">Changelog</a> · <a href="../../README.md">简体中文</a></p>

## Focus, with room to move

UpYouGo pairs a configurable sitting and standing timer with a small companion on your desktop. Confirm your posture when a reminder arrives, snooze when you are busy, and set working hours, lunch breaks and quiet periods to suit your day.

No account is required. Personal settings, statistics and behavioral records stay on your computer.

## Find your desktop companion

<img src="../../assets/desktop-companions.png" width="100%" alt="Pixel cat, Jiu Qian Sui, capybara and a chibi companion">

Choose a pixel cat, Jiu Qian Sui, a hand-drawn capybara or a chibi companion. Click to pet, offer a snack, or play with a ball. Rename your companion, adjust its size, and tuck it against either edge of the screen.

- Four built-in characters, independent animation previews and 70%–150% sizing.
- Petting, feeding, play and short responses.
- Edge docking, pointer-triggered peeking and expansion for reminders.
- Local JSON + PNG character packs, imported from a folder or ZIP.

Changing characters, previewing actions and playing do not change your real timer or statistics. Images use the application's actual renderers.

## A reminder that feels like a conversation

<img src="../../assets/companion-dialogs.png" width="100%" alt="Jiu Qian Sui responding to petting and displaying stand and sit reminders">

Rounded speech bubbles appear near your companion, normally above it, with placement adjusted at screen edges. Confirm that you have stood or sat down, or snooze for 2, 5 or 10 minutes. Reminders do not take keyboard focus.

The app supports manual Do Not Disturb, optional fullscreen quiet mode, lock/sleep handling and Windows reduced-motion preferences. Screenshots show the Simplified Chinese UI with sample times; the app also supports English.

## Built for the workday

| Capability | Details |
| --- | --- |
| Sit–stand timer | Custom durations, pause/resume and explicit posture confirmation |
| Scheduling | Working hours, weekdays, optional lunch break, Chinese holidays and adjusted workdays |
| Companions | Four appearances, names, sizing, action previews and local character packs |
| Local records | Time statistics and reminder-response feedback |
| Backup and restore | Export settings and records; verify before restoring and retain a local pre-restore copy |
| Language | Switch between Simplified Chinese and English without resetting the timer |
| Updates | Custom install folder, online/local updates, integrity checks and failed-startup rollback |

## Get started

1. Download **UpYouGo-Setup.exe** from [Releases](https://github.com/elvinzou/upyougo-releases/releases/latest).
2. Choose a dedicated writable folder and set your sitting/standing durations and schedule.
3. Open **Pet settings** at the bottom of the main panel to choose and customize a companion.

Requires Windows x64, .NET Framework (4.8 recommended) and Microsoft Edge WebView2 Runtime. Windows 10/11 is recommended. The installer does not bundle the full WebView2 Runtime.

For portable use, fully extract **UpYouGo-Windows-x64.zip** and run the included executable. The updater uses the matching **.sha256** file automatically. GitHub's automatically generated Source code archives contain documentation, not the application.

## What changed in 1.4.2?

Pet rendering failures now retain the last frame and retry after a delay, allowing timer updates to continue when graphics resources are temporarily unavailable. Timer progress, manual pause and snooze state can also resume across restarts and updates.

Backup/restore and updater fixes from 1.2.1–1.2.3 are retained. [Full release notes →](CHANGELOG.md)

## Data and current limits

Settings and records live in `%APPDATA%\LumbarReminder`, with custom artwork under `characters`. The app does not upload those settings, statistics or behavioral records. Network access is used for update checks, downloads and calendar synchronization.

- Posture is confirmed by you, not detected through a camera or sensor.
- Short interruptions within the same work period resume automatically; longer gaps or schedule changes ask you to continue or restart. Versions 1.4.0 and earlier have no saved session to recover on first upgrade.
- Personal backup files do not include imported character artwork; retain the original packs separately.
- The app UI supports Simplified Chinese and English. The installer and maintenance tool remain in Chinese.
- Actual WeChat capture behavior and physical multi-monitor/mixed-DPI setups still require testing in the relevant environments.
- This repository distributes the GitHub standalone installer and documentation. Development source is private.

[User guide](USER_GUIDE.md) · [Character pack format](../../docs/CHARACTER-PACKS.md) · [Data statement](../../docs/PRIVACY.md) · [Report an issue](https://github.com/elvinzou/upyougo-releases/issues)
