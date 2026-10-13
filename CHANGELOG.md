# Version history

## 1.9.11

Compared with the supplied 1.6.4 build:

- Smart Hunter Kit V3 with adaptive respawn kits and `/mhkit` controls.
- Configurable automatic Overworld spawn movement with `/mhspawn` (off / 5 / 10 / 15 / 20 / 30 minutes).
- Pause/resume commands with frozen gameplay and adjusted timer accounting.
- Restart/crash recovery with primary/backup snapshots, autosave, and shutdown saving.
- Configurable Runner reconnect window (fresh default 15 minutes), 10-second rejoin protection, and excluded server downtime; replaces the earlier fixed 60-minute window.
- Expanded live role management, team/target actions, runtime resynchronization, and confirmed GUI settings reset.
- VexAC 3.0 group/master controls, evidence logging, alerts, and movement/combat/AutoClick/velocity/world checks.
- Ultra Deep Debug v4 with state-machine, GUI, synthetic kit/stress, localization, recovery, and integrity diagnostics.
- More progression/dragon-health displays, MVP, damage/distance statistics, and TAB ping information.
- `/mhhelp` becomes role-aware for players/admins; `/trash` gains `/mhtrash` and `/vextrash` aliases.
- `/mhnone` is removed from public command registration.
- Bundled localized message keys increase from 446 to 683 per translated language.

Fresh settings: Smart Kit ON, auto spawn OFF, reconnect 15 minutes. Confirmed GUI settings reset instead sets auto spawn to 15 minutes. UI monitor-only anti-cheat labeling must be checked against actual behavior because compiled kick paths remain present.

## 1.6.4

Earlier supplied baseline: Runner/Hunter match lifecycle, multi-Runner teams, randomized head-start sequence, selectable compass tracking across dimensions, role/death/respawn handling, progression bossbars, randomized Runner kill rewards, victory/results, GUI administration, team chat, trash/night-vision utilities, 10 built-in languages, localized rulebooks, Paper Anti-Xray, legacy Anti AutoClick/Anti Fly, and a fixed 60-minute Runner reconnect window.

## Next supplied build

The dedicated spectator build is awaiting receipt. Its new features will be documented from the actual file rather than attributed to these earlier releases.
