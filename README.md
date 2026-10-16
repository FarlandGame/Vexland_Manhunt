# Vexland_Manhunt

[English](README.md) | [日本語](docs/README.ja.md) | [فارسی](docs/README.fa.md) | [Deutsch](docs/README.de.md) | [Français](docs/README.fr.md) | [Español](docs/README.es.md) | [Português (Brasil)](docs/README.pt-BR.md) | [Italiano](docs/README.it.md) | [Nederlands](docs/README.nl.md) | [Polski](docs/README.pl.md) | [Українська](docs/README.uk.md) | [Türkçe](docs/README.tr.md) | [Русский](docs/README.ru.md) | [简体中文](docs/README.zh-CN.md) | [繁體中文](docs/README.zh-TW.md) | [한국어](docs/README.ko.md) | [हिन्दी](docs/README.hi.md) | [Bahasa Indonesia](docs/README.id.md)

**A complete Minecraft Runner-versus-Hunter experience, co-created by [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) and [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt brings match setup, team roles, the opening chase, tracking, progression, rewards, results, and administration into one Paper server plugin. Runners try to defeat the Ender Dragon while Hunters try to eliminate the final Runner. The plugin supports multiple Runners and keeps the chase moving through deaths, respawns, dimension changes, and reconnects. Its `/mhgui` control center lets administrators manage a match through menus, with localized messages and guidebooks for the players.

## Downloads and compatibility

| File / version | Download | Purpose |
|---|---|---|
| **1.13.1 — current** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Manhunt plugin by Bardiya and Ali |
| **GrimAC 2.3.73 — required** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | Separate third-party anti-cheat dependency |
| 1.9.11 — archived | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Previous Manhunt build |
| 1.6.4 — archived | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Earlier Manhunt build |

**Target: Paper 1.21.11, Java 21.** The numbers 1.6.4, 1.9.11 and 1.13.1 are plugin releases, not supported Minecraft versions. In 1.13.1, GrimAC is a hard dependency and the bridge requires the 2.3.73 API. Download **both current JARs**. These are server plugins; players do not install them in a client mods folder.

These are original personal-server builds with creator-specific elevated administrative access, preserved exactly as supplied. This manual covers the public Manhunt controls.

## The Manhunt experience

- **Runner and Hunter teams:** assign online players to either side. A match needs at least one Runner and a Hunter or an unassigned online player. Surviving Runners continue if a teammate dies; a fallen Runner becomes a Hunter unless that death ends the match.
- **Cinematic match start:** inventories and game modes are prepared, teams are introduced, and a roulette chooses the Runner head start. Hunters are frozen during that countdown, with title and sound feedback. The head start is randomized; administrators can release Hunters early.
- **Target-selecting tracker compass:** Hunters receive a special compass. Right-click it to choose a Runner from the target menu and change the target during the chase. Across dimensions, tracking follows the relevant portal route until direct tracking becomes possible. Hunters receive their tracker again after respawning.
- **Progress displays:** bossbars and match information follow Runner equipment and progression through Nether resources, blaze rods, pearls, Eyes of Ender, the stronghold, and the End. The newer build adds finer stages and dragon-health-aware progress visuals.
- **Rewards for Runner kills:** when a Runner kills a Hunter during an active match, a progression-aware weighted reward pool of 50 entries is used. Animated rolls, double/triple rewards, streak announcements, and rare-item celebrations are included.
- **Victory and results:** the final Runner's death gives Hunters victory; defeating the Ender Dragon gives Runners victory. Match-end titles, celebrations, kill/death information, and temporary-item cleanup are included. The newer build also reports MVP, damage, and distance results.
- **Team communication and utilities:** private teammate messages with `/teammsg`, a 54-slot disposable trash inventory with `/trash`, and personal night vision with `/nv`.
- **Administration through menus:** roles, start/reset, early Hunter release, friendly fire, server lock, teleport-all, heal/feed, language, protection settings, status, and guidebooks are available through the control center. Freezing and a full reset help prepare the next match.
- **Localized guides:** Runner, Hunter, and administrator books explain objectives, tracker use, deaths, setup, and commands. Version 1.9.11 gives players a role-aware guide through `/mhhelp`.
- **Paper Anti-Xray integration:** menu controls configure Paper's world-level protection; changes need a server restart to take effect.

## What is new in 1.13.1?

Compared with the supplied 1.9.11 build:

- **Ghost spectators:** a separate role, administrator assignment, protected flight, hidden players, saved/restored state and a paginated participant-teleport menu.
- **Redesigned control center:** categorized menus, explicit four-way role selection, named target picker, reconnect-duration selector, Classic/Fast/Hardcore/Custom presets and dedicated 30-second confirmation screens.
- **GrimAC integration:** required GrimAC 2.3.73 replaces the active VexAC startup path. Master, five check groups, alerts and monitor/enforcement controls are exposed in the GUI. Paper Anti-Xray remains independent.
- **New Smart Hunter Kit planner:** adapts equipment and supplies to Runner gear/enchantments, nearest Runner, team numbers, distance, dimension and terrain. It preserves stronger existing gear, avoids duplicate tools and limits consumable top-ups with a 30-second history. This is not a guarantee of a fixed gear gap or measured balance.
- **Validated recovery:** SHA-256-sealed snapshots, schema/state checks and valid-backup fallback; invalid or newer-format snapshots are preserved without overwriting them. Spectator state has its own persistence.
- **Expanded messages:** translated keys grow from 683 to 762 per bundled translation, still across the same ten in-game languages. Two new public commands are registered: `/mspectator <player>` and `/mhspectate`.
- **Reset fallback:** if no safe surface near Overworld spawn is found, reset can skip that teleport instead of forcing it.

## Full setup and use with `/mhgui`

Stop the server and keep a backup of worlds and plugin data. Put both current JARs in `plugins/`, retaining only one Manhunt JAR and one GrimAC JAR there. Keep existing `plugins/VexLandManhunt/` settings/data when upgrading. Start the Paper 1.21.11 / Java 21 server fully; use a full restart when replacing builds. GrimAC must load successfully. The internal plugin name remains `VexLandManhunt`.

This guide describes plugin release **1.13.1** with English labels. Labels follow the server-wide language. Positions count rows from top to bottom and columns from left to right. Use a normal left-click unless a special action is stated. This guide comes from static inspection; no Minecraft server was run.

### Set up a match

1. Use `/mhgui` with `vexland.admin` (default: OP).
2. Open **Player Roles**, click a named player tile, then choose **Runner**, **Hunter**, **Spectator** or **No Team**. This opens an exact-role selector; clicking the player does not cycle their role.
3. Assign at least one Runner and one Hunter. Unassigned online players can become Hunters when a match starts; spectators do not fill either team's required slot.
4. Review **Match Settings**, **GrimAC Security** and **Global Language**. Switch Server Freeze off before starting.
5. Open **Match Controls → Start Match**. Participant inventories are prepared/cleared, the introduction plays, and the roulette chooses the Hunter head start.

### Home: `/mhgui` (five rows)

| Position | Button | Action |
|---|---|---|
| R2 C2 | Match Controls | Start, pause/resume, release and reset. |
| R2 C4 | Player Roles | Open the online-player role list. |
| R2 C6 | Match Settings | Friendly fire, kits, spawn, reconnect and presets. |
| R2 C8 | Player Management | Choose a target and use player/world tools. |
| R4 C2 | GrimAC Security | Open protection settings. |
| R4 C4 | Global Language | Choose the language used for everyone. |
| R4 C6 | Administrator Guide | Add the localized admin book to your inventory. |
| R5 C5 | Close | Close the menu. |

The beacon at R1 C5 reports match state and Runner/Hunter counts.

### Match Controls (five rows)

| Position | Button | Action |
|---|---|---|
| R2 C2 | Start Match | Start the complete sequence. |
| R2 C4 | Pause Match / Resume Match | Pause or resume gameplay and match timers; available for a RUNNING match. |
| R2 C6 | Release Hunters | End the current Hunter waiting period early. |
| R2 C8 | Reset Match | Open confirmation, then fully reset the match. |
| R4 C2 | Server Freeze | Toggle the global non-OP player freeze. |
| R4 C4 | Teleport Everyone | Open confirmation, then bring all online players to you. |
| R4 C6 | Match Info | Send the match and team report. |

**Back** is R5 C1; **Close** is R5 C9. Server Freeze is separate from Pause Match: use Pause when the clock and gameplay systems must stop together.

### Player Roles

The six-row player list shows up to 45 named role tiles, ordered by player name, across its first five rows. Runner uses lime concrete, Hunter red concrete, Spectator an Ender Eye, and No Team gray concrete. The bottom row has **Previous Page** at C1, page/online information at C3, **Back to Control Center** at C5 and **Next Page** at C9.

Click a player to open **Choose Player Role** (three rows):

| Position | Exact role |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

The player's name/current role appears at R1 C5; **Back** is R3 C1 and **Close** R3 C9. Roles can change during a match. Changing the final assigned Runner away from Runner during RUNNING opens **Last Runner: the match will end** confirmation. Applying it can give Hunters the win. Direct role commands apply immediately, so use them deliberately. No Team can be assigned here; ordinary start/join synchronization can turn an unassigned player into a Hunter during an active match.

### Spectators

An administrator assigns `/mspectator <player>` or chooses **Spectator** in Player Roles. The command checks administrator access even though its descriptor has no permission line. Players do not enroll themselves by running `/mhspectate`.

A spectator receives a **Spectator teleport** compass in their first hotbar slot. Hold it in the main hand and right-click, or use `/mhspectate`, to open the six-row teleport menu. The menu works only while the player has the Spectator role. Its first five rows contain up to 45 living online Runners/Hunters, sorted by name; click a named role tile to teleport to that player's current location, including another world. The bottom row has **Previous Page** at C1, **Close** at C5 and **Next Page** at C9. With no suitable participant, R3 C5 says **No players available**. Closing this menu leaves you a spectator.

Spectators fly, are hidden from other players, do not collide, and are protected from damage. The implementation uses Adventure mode with flight; it does not grant vanilla Spectator camera or through-block movement. It blocks attacks, block breaking/placement, ordinary block/entity interactions, item pickup/drop, offhand swapping, inventory clicks/drags, armor-stand manipulation and experience pickup/gain. Mobs cannot target them, and hunger changes are canceled. `/teammsg <message>` reaches other players with the Spectator role. Do not pass participant locations or other outside assistance to competitors.

To leave, an administrator assigns **Runner**, **Hunter** or **No Team**, or uses `/mrunner <player>` or `/mhunter <player>`. There is no dedicated self-exit command/button. Leaving restores saved inventory/cursor, location, game mode, flight, collision and immunity state, then applies the new role's match behavior. Spectator state is saved for rejoining. Full Match Reset restores spectator state, clears roles and moves online players to a safe Overworld spawn when one is available. Normal match-end cleanup leaves spectators outside participant item/flight handling.

### Match Settings (five rows)

| Position | Button | Action |
|---|---|---|
| R2 C2 | Friendly Fire | Toggle teammate damage. |
| R2 C4 | Smart Hunter Kit | Toggle adaptive Hunter respawn kits. |
| R2 C6 | Auto World Spawn | Open interval selection. |
| R2 C8 | Reconnect Grace | Open the Runner reconnect-duration selection. |
| R4 C2 | Match Preset | Choose Classic, Fast, Hardcore or Custom. |
| R4 C4 | Reset Settings | Confirm balanced settings: Kit ON, Spawn 15m, Reconnect 15m. |
| R4 C6 | Random Head Start | Information tile; roulette still chooses the delay. |

**Back** is R5 C1; **Close** R5 C9.

The three-row **Reconnect Grace** selector offers **1, 5, 10, 15, 20, 30 minutes** at R2 C2–C7, in that order. Clicking saves the value and keeps the selector open. Back is R3 C1; Close R3 C9.

The three-row **Match Preset** selector puts **Classic**, **Fast**, **Hardcore**, **Custom** at R2 C2, C4, C6, C8. Classic: Kit ON, Spawn 15m, Reconnect 15m. Fast: ON, 5m, 10m. Hardcore: OFF, OFF, 5m. Custom keeps current manual settings. Presets preserve the random head start. Selection keeps this menu open; Back is R3 C1, Close R3 C9.

**Auto World Spawn** offers OFF, 5m, 10m at R2 C2, C3, C4 and 15m, 20m, 30m at R2 C6, C7, C8. Back is R3 C5. Select an interval or use `/mhspawn <off|5|10|15|20|30|status>`. It moves Overworld spawn near a suitable Overworld Runner; it can skip when none is suitable. `/mhkit <on|off|toggle|status>` controls kits directly.

### Player Management (six rows)

| Position | Button | Applies to |
|---|---|---|
| R1 C5 | Target Player | Open a named-player picker. |
| R2 C2 | Full Heal | All online players. |
| R2 C4 | Full Hunger | All online players. |
| R2 C6 | Clear Effects | All online players. |
| R2 C8 | Freeze Target | Selected player. |
| R4 C2 | Clear Target Inventory | Selected player; confirmation required. |
| R4 C4 | Kill Target | Selected player; confirmation required and normal match outcomes apply. |
| R4 C6 | Set Day | Your current world. |
| R4 C8 | Clear Weather | Your current world. |
| R5 C2 | Clear Dropped Items | Your current world; confirmation required. |
| R5 C4 | Emergency Sync | Refresh role/runtime systems for online players. |
| R5 C6 | Freeze Team | Left: Runners; right: Hunters; shift-click: clear these team/individual freezes. |

Back is R6 C1; Close R6 C9. Target selection does not change roles. Its picker offers 28 other online players per page, in rows 2–5, columns 2–8; click a name to select and return. Previous/Back/Next are R6 C1/C5/C9. Recheck the displayed target before applying an action.

### Confirmation screens

Reset Match, Teleport Everyone, Reset Settings, Clear Target Inventory, Kill Target, Clear Dropped Items and the final-Runner GUI change use a separate three-row **Confirm Action** screen. Read the action/target at R1 C5, then click green **Confirm** at R2 C3 or red **Cancel** at R2 C7. Confirmation expires after **30 seconds**. Changed/offline targets or changed roles require a fresh selection. This replaces the old guide's five/eight-second repeated-click instructions for these new menu paths.

### GrimAC Security and language

The six-row Grim menu has status at R1 C5; toggles at R2 C2 **GrimAC Master**, C4 **Movement**, C6 **Combat**, C8 **Packets**; R4 C2 **Velocity / AntiKB**, C4 **World / Scaffold**, C6 **Anti X-Ray**, C8 **Admin Alerts**; and R5 C5 **Monitor mode**. Back is R6 C1 and Close R6 C9. Monitor mode controls alerts/evidence versus enforcement. Paper Anti-Xray is independent and needs a restart after changes. These are GrimAC controls; the older VexAC/AutoClick menu description does not describe this release.

Global Language applies to everyone and refreshes menus/items. Click the named language; Back is R3 C5. `/mhlang` opens the same selector, and `/mhhelp` supplies the localized player/admin guide.

### Current defaults, reconnect and moderation

Fresh configuration fallbacks in `plugins/VexLandManhunt/config.yml` are:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` means automatic spawn movement is off. Reset Settings and Classic instead choose 15 minutes. During a Runner's reconnect window their slot is retained; a timely return provides ten seconds of protection. Saved server downtime is excluded. Expiry can turn the Runner into a Hunter or end the match for Hunters. Pause/Resume freezes gameplay systems and adjusts active match timing. Recovery files are managed by the plugin.

Grim bridge settings are persisted in `plugins/VexLandManhunt/grim-settings.yml`. Fresh defaults are Master ON, all five groups ON, Admin Alerts ON and **Monitor mode OFF: enforcement is enabled**. Monitor mode queues evidence/alerts and cancels qualifying flags. In enforcement mode the bridge can turn a Grim kick command into a localized disconnect that permits reconnecting; it does not establish a permanent-ban policy. Actual thresholds also depend on Grim's configuration. Evidence is queued to `plugins/VexLandManhunt/anticheat/grim-evidence.log`; bounded queues can drop entries under load. The bridge exempts spectators, paused/frozen play and certain vehicle contexts, with three-second grace after join, teleport and respawn. No anti-cheat accuracy or performance benchmark is claimed.

## Public command reference — 1.13.1

Administrator access means OP or `vexland.admin` (default OP). The `/mspectator <player>` handler checks this despite lacking a descriptor permission line. Direct role commands apply immediately; changing the final Runner during RUNNING can finish the match. The GUI provides a confirmation for that situation.

| Command | Purpose | Access |
|---|---|---|
| `/mhgui` | Open categorized control center | Administrator |
| `/mhstart` | Start full match sequence | Administrator |
| `/mhreset` | Fully reset match | Administrator |
| `/mhrelease` | Release waiting Hunters | Administrator |
| `/mrunner <player>` | Assign Runner | Administrator |
| `/mhunter <player>` | Assign Hunter | Administrator |
| `/mspectator <player>` | Assign Spectator | Administrator; new |
| `/mhspectate` | Open participant teleport menu | Current Spectator; new |
| `/teammsg <message>` | Send to your own role/team | Player |
| `/trash` | Disposable 54-slot inventory; aliases `/mhtrash`, `/vextrash` | Player |
| `/nv` | Toggle personal night vision | Player |
| `/mhlang` | Open global language selector | Administrator |
| `/mhkit <on\|off\|toggle\|status>` | Configure adaptive Hunter kits | Administrator |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Configure spawn movement | Administrator |
| `/mhhelp` | Receive localized role/admin guide | Player / administrator |
| `/mhpause` | Pause running match | Administrator |
| `/mhresume` | Resume paused match | Administrator |
| `/mhdebug` | Internal diagnostics | Administrator |

`/mhnone` is not registered in this release; use the GUI's No Team role. Hunters right-click their tracker compass to choose a Runner; this is separate from spectator teleporting and the administrator's target picker. Runners win by defeating the Ender Dragon; Hunters win when no Runner remains. A fallen Runner becomes a Hunter if other Runners remain.

## Languages, history and third-party credits

The original plugin offers **10 in-game languages**: English, Persian, Arabic, Spanish, French, German, Russian, Simplified Chinese, Hindi and Portuguese. `/mhlang` selects one language for the whole server, persisted in `language.txt`. The GitHub manual has **18 languages**, excluding an Arabic documentation edition. Japanese and other extra README languages do not add in-game translations to the unchanged JARs.

[Version history](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) records each supplied build. The complete older 1.9.11 / 1.6.4 manual is retained in the [versioned archive](docs/archive/1.9.11/README.md). The dedicated spectator build has now been supplied and published as 1.13.1; its features should not be attributed to the older downloads.

**GrimAC is an independent project by the GrimAC contributors, distributed under GPL-3.0.** Bardiya and Ali created Vexland_Manhunt and its integration; they are not credited as GrimAC's authors. The supplied Grim JAR matches the official Modrinth 2.3.73 Bukkit artifact's SHA-512 and SHA-1. Its embedded source commit matches [upstream v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73). The release includes unchanged binaries, checksums, the upstream source snapshot, license and [third-party notices](THIRD_PARTY_NOTICES.md). These component notices do not assign a license to the separate Manhunt project.

## A playful challenge to Dream

A little Minecraft banter from Bardiya 😄

> "Sigh... Ali and I made a Manhunt plugin a hundred times better than Dream's, but Dream's scared and won't play ours!"

## Creators and project scope

**Co-created by [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) and [Ali · Alivexor](https://github.com/Alivexor).** Both handles are also recorded as authors in the original plugin descriptors.

This repository presents the original compiled releases, their documentation, and version notes as a shared portfolio project. Feature descriptions are based on static inspection of the supplied JARs. Live-server compatibility, recovery performance, balance, and anti-cheat accuracy have not been tested in this publication workflow.

[Bardiya's GitHub portfolio](https://github.com/FarlandGame) · [Ali's GitHub](https://github.com/Alivexor) · [All releases](https://github.com/FarlandGame/Vexland_Manhunt/releases)
