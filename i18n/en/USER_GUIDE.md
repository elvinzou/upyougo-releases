# User guide · UpYouGo 1.4.0

[Product overview](README.md) · [简体中文](../../USER_GUIDE.md)

## Installation and upgrades

Download the latest **UpYouGo-Setup.exe**, select a dedicated writable folder, then set your durations and work schedule. Windows x64, .NET Framework (4.8 recommended) and Microsoft Edge WebView2 Runtime are required. The installer does not bundle the full WebView2 Runtime.

Portable users must extract the entire ZIP. If an old update window cannot open, run the latest installer directly. Existing settings and records are retained; the previous countdown is not resumed.

## Timers and reminders

Start the timer after configuring your sitting/standing durations. Confirm **I am standing** or **I am sitting** only after changing posture. Confirmation begins the next phase. You can snooze for 2, 5 or 10 minutes or use Do Not Disturb.

Configure workdays, working hours, lunch breaks, Chinese holiday adjustments and today's override in the schedule panel. Lock and sleep events follow the app's away rules.

## Pet settings

Open **Pet settings** at the bottom of the main panel. Select a card, preview actions, set a name and size, choose edge docking, then click the apply button.

| Action | Result |
| --- | --- |
| Single click | Pet the companion |
| Double click | Open the main panel |
| Drag | Reposition the companion |
| Right-click snack/play | Play one short interaction |
| Drop near either screen edge | Retract when edge docking is enabled |
| Pointer arrives / reminder is due | Expand the companion |
| Recover pet | Undo hiding/current docking and return it to a visible work area |

Interactions and previews do not change real timer records. Reminders take priority over normal interactions. Reduced-motion preferences stop autonomous loops and retain necessary static responses.

## Import ZIP or folder

Both buttons import the same character format:
- ZIP: select a compatible pack file.
- Folder: select the directory directly containing `character.json`.
- After import, select the character and **apply it to the desktop**.

A pack contains JSON configuration and transparent PNG artwork. Ordinary photo archives, GIFs, videos and packs from other programs need conversion; import does not generate animation from photographs.

A ZIP may contain the configuration at its root or one enclosing character folder. Imported packs are copied to `%APPDATA%\LumbarReminder\characters\<id>`. Duplicate IDs are rejected without overwriting existing packs. [Format and limits](../../docs/CHARACTER-PACKS.md).

## Recover a hidden pet

Use the recovery button in Pet settings or the tray menu. It restores visibility and a position within a screen's work area, keeping the selected character, size and timer. It does not create another companion.

During genuine fullscreen use it waits to show the pet. After fullscreen ends the pet can return immediately while reminder grace continues. Version 1.4.0 removes the extra ten-second hide after temporary fullscreen windows close. Capture behavior in specific WeChat versions still needs confirmation.

## Backup and updates

The tray menu exports settings and records to a `.upyougo` file and restores validated backups. The app retains a pre-restore copy under `%APPDATA%\LumbarReminder\backups`.

Backups do not include custom artwork, calendar cache, browser cache or the Windows startup registry entry. Keep imported packs separately.

The installed app checks stable releases at startup and every six hours. Review and choose an update from the tray menu, or select a complete local ZIP. Files are verified before the app exits and activates the new version. A failed startup can roll back the application; personal data is not rolled back.

Closing the main panel leaves the app running. Use the tray menu to quit.

[Changelog](CHANGELOG.md) · [Data statement](../../docs/PRIVACY.md) · [Issues](https://github.com/elvinzou/upyougo-releases/issues)
