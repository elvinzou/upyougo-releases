# Requirements and acceptance criteria

**English** | [日本語](../ja/REQUIREMENTS.md) | [한국어](../ko/REQUIREMENTS.md) | [简体中文](../../docs/REQUIREMENTS.md) | [繁體中文](../zh-Hant/REQUIREMENTS.md)

Baseline: UpYouGo 1.2.3, 2026-09-28. This document covers the current Windows desktop product. Proposed work is listed in the [roadmap](ROADMAP.md). Hardware work in historical PRDs is outside this release.

## Product goal and user flow

Provide unobtrusive sit–stand reminders for people working on Windows for extended periods. Users confirm their actual posture; the app does not use a camera or sensors to detect standing.

First launch → set durations and schedule → start timer → reminder beside the cat → confirm standing/sitting → next cycle. Outside working hours, during lunch, while away, and in quiet mode, the corresponding rules prevent duplicate or poorly timed reminders.

## Implemented requirements

| ID | Capability | Acceptance criteria |
| --- | --- | --- |
| R01 | Sit–stand timers | Configurable durations; start, pause, resume, restart; change posture phase only after confirmation |
| R02 | Unobtrusive reminders | Bubbles appear near the cat without taking input focus; appearance is consistent with the main panel |
| R03 | Snooze | Delay by 2/5/10 minutes; per-second refreshes preserve the snooze state |
| R04 | Work schedule | Working hours, weekdays, optional lunch break; time outside the schedule is not counted as effective sitting/standing time |
| R05 | Chinese holiday calendar | Chinese holidays and adjusted working days, plus today's override; keep cached data on sync failure and use weekday rules for uncovered years |
| R06 | Time away | Freeze on Windows lock/sleep; combine overlapping events; resume after short absences and await a choice after long ones |
| R07 | Do Not Disturb | Manual and optional automatic fullscreen quiet modes are independent; ending automatic quiet does not cancel manual quiet |
| R08 | Local statistics | Day/week/month/year views, effective intervals and reminder-response feedback; do not upload these records |
| R09 | Desktop pet | Draggable pixel cat, idle/interactive animations and reminder poses; account for reduced-motion preferences |
| R10 | Startup settings | Optional Windows startup and automatic timer start; closing the panel does not quit; tray menu can quit |
| R11 | Installation | Choose a dedicated writable folder; create stable launcher and shortcuts; continue using existing personal data |
| R12 | Update discovery | Check public stable releases at startup and every 6 hours; notify only for newer versions; ignore prereleases; show a manual download link if the update window cannot start instead of an unhandled exception |
| R13 | Online updates | Show release notes; download on user action, verify ZIP checksum and internal manifest, then save, exit, and start the new app |
| R14 | Local updates | Accept a complete ZIP; reject missing files, path traversal, duplicates, checksum failures, and different contents under an existing version number |
| R15 | Rollback | Confirm only after main-panel loading and a short liveness check; restore old state on failure; recover interrupted updates on next launch; support manual rollback |
| R16 | Language switching | Version 1.2.0 adds Chinese / English interface switching. Choose a language at the top right of the main panel. It applies immediately and is remembered at the next launch. Existing users keep Chinese by default. Switching preserves the timer, posture and statistics, and does not change the Chinese work calendar or schedule. |
| R17 | Personal data export | Export settings, time statistics, behavior records and existing `.bak` copies into one `.upyougo` file from the tray; save current statistics first and avoid incomplete exports on save failure |
| R18 | Restore from backup | Validate structure and SHA-256; retain current files before restoring and reload data; remove old statistics and `.bak` files absent from the backup to prevent mixed histories |

The work-calendar cache can be downloaded again and is not included in personal backups. The Windows startup registry entry is not transferred. Restore brings back settings and history, not the previous timer phase.

## Outside the current release

A production mobile app, cross-device sync, cloud accounts, automatic posture detection, forced online updates, countdown restoration after updates, and a complete uninstaller are not delivered. ESP8266 and old bridge code remain historical projects and are not compiled into this release.

## Update failures and data boundaries

- Download and package validation finish before the old app exits; failures do not switch the active version.
- If saving fails, keep the old process running rather than forcibly terminating it.
- Startup validation times out after 30 seconds; terminate only a failed process started by this updater.
- Rollback does not migrate, delete, or restore personal data. Future incompatible data formats require a backup and compatibility plan first.
- Ask users to exit early portable builds through the tray if they lack the update shutdown interface.
- For insufficient permissions or conflicting files, prompt for another folder without automatic elevation.

## Validation and metrics

See release notes for validation coverage. Response statistics reflect user confirmations, not measured physical activity or health outcomes. Retention, health benefits, and public user counts have not been validated and are not claimed as achieved results.
