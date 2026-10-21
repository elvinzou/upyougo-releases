# Changelog

## 1.4.0 · Desktop companions — 2026-10-21

- Four built-in characters: pixel cat, Jiu Qian Sui, hand-drawn capybara and chibi companion.
- Pet settings with independent previews, names, 70%–150% sizing and edge docking.
- Petting, feeding, ball play and short responses; real reminders take priority.
- JSON + PNG character packs imported from folders or ZIP, with validation and separate user storage.
- Jiu Qian Sui retains its reference appearance and uniform proportions, with continuous interaction and stand/sit body transitions.
- Matching rounded speech bubbles with placement above/below the companion and screen-edge handling.
- Pet visibility is separated from the fullscreen exit reminder grace, removing an extra ten-second hide. Recognition is added for capture-tool overlays.
- Existing backup/restore and updater fixes from 1.2.1–1.2.3 are retained.

Verification covers installer/update/backup, timing and schedules, real window rendering, characters/imports, animations, languages and focus. Specific WeChat versions and physical mixed-DPI/multi-monitor setups need environment-specific confirmation. Updates still do not resume the old countdown; installer and maintenance UI remain in Chinese. This release updates the GitHub standalone channel.

## 1.2.3 — 2026-09-28

Fixes the maintenance executable inheriting the installer's download-origin mark.

## 1.2.2 — 2026-09-28

Handles Windows cancellation or blocking when opening the updater, with a manual download path instead of an unhandled exception.

## 1.2.1 — 2026-09-28

Adds tray-menu personal settings/records backup and restore with validation and a pre-restore local copy.

## 1.2.0 — 2026-09-23

Adds immediate Simplified Chinese/English switching without resetting timer progress.

## 1.1.1 — 2026-09-22

Moves public distribution to this repository and provides online/local updating with rollback.

[Detailed Chinese changelog](../../CHANGELOG.md)
