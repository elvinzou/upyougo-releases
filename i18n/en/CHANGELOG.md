# Changelog

**English** | [日本語](../ja/CHANGELOG.md) | [한국어](../ko/CHANGELOG.md) | [简体中文](../../CHANGELOG.md) | [繁體中文](../zh-Hant/CHANGELOG.md)

## 1.2.0 — 2026-09-23

- Version 1.2.0 adds Chinese / English interface switching. Choose a language at the top right of the main panel. It applies immediately and is remembered at the next launch. Existing users keep Chinese by default. Switching preserves the timer, posture and statistics, and does not change the Chinese work calendar or schedule.
- Covers the main panel, reminder settings, tray and cat menus, reminder bubbles, statistics and in-app update notices. Open statistics windows update immediately; English bubble titles fit the available space.

The standalone installer and maintenance tool remain in Chinese. Updating or restarting the app still starts a new timer according to startup settings; switching languages requires no restart.

## 1.1.1 — 2026-09-22

First distribution through a dedicated public release repository; the development source remains private.

- Switch the default update source to `elvinzou/upyougo-releases`, with compatibility for the old default configuration.
- Add requirements, architecture, development/testing, release-process and roadmap documentation.
- Add continuous integration for Windows builds and updater checks.

Includes previously delivered local features: sit–stand reminders, pixel cat, schedule/Chinese holiday adjustments/lunch breaks, time-away and fullscreen quiet handling, local statistics, custom installation paths, new-version notifications, online/local updates, and rollback.

Known limitations: updates do not restore the countdown; the installer does not bundle the full WebView2 Runtime; a complete uninstaller and old-version cleanup are not available; executables are not Authenticode-signed.

## 1.1.0 — 2026-09-22 (local delivery)

- GitHub stable-release checks, tray notifications, release notes, and download verification.
- Custom installation folders and actual-path detection for the launcher.

## 1.0.0 — 2026-09-22 (local delivery)

- Stable launcher, separate version folders, local ZIP updates, save-and-exit, startup validation, and rollback.
- Preserve compatibility with existing personal settings and statistics directories.
