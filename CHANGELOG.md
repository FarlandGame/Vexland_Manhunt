# Version history

## 2.0.0 — supplied combined package

The public release/file is 2.0.0; the unchanged embedded descriptor is **1.9.11-grim.1**. The provided integration deliberately uses Manhunt 1.9.11 as its gameplay foundation, not the spectator-enabled 1.13.1 branch.

- One flattened JAR combines Manhunt, modified GrimAC 2.3.73 and bundled PacketEvents under a shared Bukkit plugin instance; the descriptor provides GrimAC. No separate GrimAC or PacketEvents installation is needed for this package. Three original Grim classes are modified; this is not the unchanged standalone upstream Grim artifact.
- Adds administrator `/vexintegration`, reporting Grim ACTIVE/INACTIVE, Bukkit owner, VexAC status, PacketEvents status and tracked players. Native `/grim` and `/grimac` registration is verified by the integrated module.
- Requires exact Minecraft 1.21.11 and Paper configuration API, Java 21, and a full normal startup. Hot loading with online players and a separately loaded GrimAC instance are rejected. Startup failure disables the integrated plugin and logs inactive protection while the server can remain online.
- First-load migration backs up existing Manhunt and Grim data trees, copies old Grim data only if the integrated destination is absent, preserves original folders, warns rather than merging/overwriting when both destinations exist, and refuses symbolic links. Integrated Grim data lives under plugins/VexLandManhunt/grim/.
- Movement correction ownership is controlled by plugins/VexLandManhunt/integration.properties: legacy by default, or grim. The latter suppresses VexAC setback/teleport paths while its checks, alerts and evidence remain; it does not disable all legacy punishments. Invalid ownership values abort startup.
- Retains the flat five-row /mhgui, Runner/Hunter role cycling, VexAC menu, Smart Hunter Kit V3, spawn movement, pause/resume, reconnect/recovery, progress/rewards/results and utilities from the 1.9.11 foundation. The VexAC GUI controls the legacy engine, separately from integrated Grim.
- Has 17 public Manhunt/integration command registrations and ten game languages with 683 translated keys per bundled translation.
- Does **not** contain the dedicated Spectator role, /mspectator, /mhspectate, categorized control center, exact four-way role chooser, 30-second confirmation pages, preset/reconnect GUI selectors, new SmartKitPlanner or sealed recovery system from 1.13.1. That branch remains separately downloadable with its own manual and both required JARs.

Fresh gameplay defaults remain Smart Kit ON, auto spawn OFF and reconnect 15 minutes; confirmed legacy Reset Settings selects ON / 15m / 15m. Original bytes are preserved. The source-only companion retains all supplied source code, build scripts, dependency inputs and notices; 50 local test/runtime evidence files were excluded without modifying source payloads. GPLv3 text and component notices accompany the artifact. No independent rebuild or live-server/anti-cheat performance test was run during publication.

## 1.13.1

Compared with the supplied 1.9.11 build:

- Dedicated ghost Spectator role, administrator assignment with `/mspectator <player>`, and a paginated participant teleport menu using `/mhspectate` or the spectator compass. Protected hidden Adventure-mode flight, blocked gameplay interaction, persistent state and restoration on administrator role reassignment. No self-enroll/self-exit command and no vanilla through-block camera movement.
- Categorized `/mhgui`: Match Controls, Player Roles, Match Settings, Player Management, GrimAC Security, Global Language and guidebook. Exact Runner/Hunter/Spectator/No Team chooser replaces cycling; named target selection replaces target cycling.
- Reconnect-duration selector (1/5/10/15/20/30 minutes) and Classic/Fast/Hardcore/Custom presets. All retain a random head start. Classic: Kit ON / Spawn 15m / Reconnect 15m; Fast: ON / 5m / 10m; Hardcore: OFF / OFF / 5m; Custom keeps manual settings.
- Separate Confirm/Cancel screens expire after 30 seconds for Reset Match, teleport-all, Reset Settings, clear target inventory, kill target, clear dropped items and final-Runner GUI role change. Direct role commands still apply immediately and can end the match when the last Runner changes role. The old five/eight-second repeated-click instructions apply to the archived guide, not this UI.
- Required GrimAC dependency and a bridge requiring API 2.3.73. The active startup path initializes GrimAC instead of VexAC; legacy VexAC classes remain bundled. Movement, Combat, Packets, Velocity/AntiKB and World/Scaffold groups, master, admin alerts and explicit monitor controls are available. Paper Anti-Xray remains independent and needs restart after changes.
- Grim bridge fresh defaults are enabled, all groups enabled, alerts enabled and **monitor-only false**, so enforcement is ON. Eligible Grim kick commands can become localized reconnectable disconnects; no permanent-ban policy is established. Evidence is queued with bounded capacity; movement exemptions include spectators, paused/frozen play and a three-second join/teleport/respawn grace.
- New Smart Hunter Kit planner profiles gear/enchantments, nearest Runner, team counts, nearby Hunters, distance, dimension and terrain. It preserves stronger existing items, avoids duplicate tools and gates supply top-ups with a 30-second history. The old fixed “below Runner average” description is not an exact statement of the new algorithm.
- Recovery snapshots gain SHA-256 integrity seals, schema/state validation and valid-backup fallback; invalid/newer-format data is preserved without overwriting it. Spectator state is persisted separately. Reset can skip a teleport when no safe spawn surface is available.
- Translation resources expand from 683 to 762 keys per bundled translation; ten selectable game languages remain. Public command registration grows to 18. `/mhnone` remains unregistered.

**Installation:** use Paper 1.21.11 / Java 21 and both supplied JARs: `VexLandManhunt-1.13.1.jar` and `grimac-bukkit-2.3.73.jar`. Preserve server data, retain one JAR per plugin, and restart fully. The numbers are plugin release identifiers.

Fresh Manhunt fallbacks remain Kit ON, Auto Spawn OFF and Reconnect 15 minutes. Confirmed Reset Settings chooses ON / 15m / 15m. The [current manual](README.md) explains every public submenu and spectator operation; the complete [1.9.11 / 1.6.4 guide](docs/archive/1.9.11/README.md) is archived with all 18 documentation editions.

Co-created by Bardiya/Farland_game and Ali/Alivexor. GrimAC is a separate upstream project by GrimAC/DefineOutside and contributors. The release includes unchanged binaries, checksums, the matching upstream source snapshot, GPLv3 text and component notices. Static inspection and file-integrity checks were performed; no live Minecraft server or anti-cheat accuracy/performance test was run.

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

## Future supplied builds

Each future supplied build will receive its own download, checksum and feature-change notes after comparison with the previous build. The dedicated spectator build has been received and is documented above as 1.13.1.
