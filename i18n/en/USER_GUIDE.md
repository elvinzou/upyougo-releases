# User guide

**English** | [日本語](../ja/USER_GUIDE.md) | [한국어](../ko/USER_GUIDE.md) | [简体中文](../../USER_GUIDE.md) | [繁體中文](../zh-Hant/USER_GUIDE.md)

## First installation and migration

Download UpYouGo-Setup.exe from Releases and choose a dedicated, writable folder. Older versions with the update interface save and exit automatically. Earlier portable builds must be closed using the cat's system tray menu first. Installation preserves existing settings and statistics.

## Daily reminders

Set sitting and standing durations and working hours, then start the timer. When reminded, confirm that you have stood up or sat down to enter the next phase. Use snooze or Do Not Disturb if the timing is inconvenient. You confirm your posture manually; the app does not detect body movements.

Schedule settings include weekdays, Chinese public holidays and adjusted working days, a working/rest-day override for today, and an optional lunch break. Locking or sleeping freezes the timer. After a long absence, choose whether to continue or restart. Automatic fullscreen quiet mode can be disabled.

The statistics entry on the main panel shows local time records and behavioral feedback. Closing the panel leaves the tray icon and desktop cat running. To quit completely, use the tray menu.

## Updates and rollback

Open the tray menu → “版本与更新” (Version & Updates) to check for updates, read release notes, and download a new version. You can also select a complete local update ZIP. The installer verifies files before saving and exiting the app. If the new version fails its startup check, the previous installation state is restored. Rolling back the app does not roll back personal data.

Version 1.1.1 moves the old default private update source to this public repository. Run this release's Setup when first migrating to this channel so the maintenance program is updated too.

## Troubleshooting

- **No update found:** Check that the repository is `elvinzou/upyougo-releases` and GitHub is reachable. Prereleases do not trigger automatic notifications.
- **Download failed:** The current app remains usable. Retry later, or download the complete ZIP manually and choose a local update.
- **Main panel failed to initialize:** Check that Microsoft Edge WebView2 Runtime is installed. Extract the entire portable package; do not copy only the EXE.
- **No permission to install:** Choose a dedicated folder writable by your current user. The installer does not request elevation automatically.
- **Reminders continue after closing the window:** Closing the panel does not quit the app. Exit through the tray menu.
- **Countdown resets after an update:** Restoring the previous countdown is not implemented yet. Startup settings determine what happens after restarting.

Settings and records: `%APPDATA%\LumbarReminder`. WebView2 cache: `%LOCALAPPDATA%\UpYouGo\WebView2Data`. Quit the app and back up the original files before editing data.

## Language switching

Version 1.2.0 adds Chinese / English interface switching. Choose a language at the top right of the main panel. It applies immediately and is remembered at the next launch. Existing users keep Chinese by default. Switching preserves the timer, posture and statistics, and does not change the Chinese work calendar or schedule.

Covers the main panel, reminder settings, tray and cat menus, reminder bubbles, statistics and in-app update notices. Open statistics windows update immediately; English bubble titles fit the available space.

The standalone installer and maintenance tool remain in Chinese. Updating or restarting the app still starts a new timer according to startup settings; switching languages requires no restart.
