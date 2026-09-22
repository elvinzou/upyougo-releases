# Roadmap

**English** | [日本語](../ja/ROADMAP.md) | [한국어](../ko/ROADMAP.md) | [简体中文](../../docs/ROADMAP.md) | [繁體中文](../zh-Hant/ROADMAP.md)

These are proposals, not implemented features or committed dates. See [requirements](REQUIREMENTS.md) for the current baseline.

| Priority | Proposal | Value and acceptance direction |
| --- | --- | --- |
| P1 | Restore countdown after updates | Preserve phase, remaining time, snooze and pause state across update/rollback; handle expired sessions explicitly |
| P1 | Data export and recovery | Export settings and statistics; validate imports and back up existing data before restoring |
| P1 | Installation maintenance | Add uninstall, old-version cleanup and installation-folder migration; retain personal data by default |
| P2 | Cancel/resume downloads | Allow cancellation; retry weak connections without interrupting the timer or leaving unused temporary files |
| P2 | Update preferences and channels | Disable automatic checks, skip a release, and define a compatible maintenance-program update protocol |
| P2 | Release trust and compatibility | Executable signing and broader DPI, multiple-monitor and Windows-environment validation |
| P2 | Separate core rules further | Extract timer, schedule and record boundaries from WinForms for future mobile reuse |
| To validate | Production mobile app | Validate background reminders, notification permissions and interactions before committing scope; do not replicate desktop windows or installer |

Prioritize reliable distribution and recoverable data before expanding features and platforms. Hardware integration remains a historical project outside this default development order.
