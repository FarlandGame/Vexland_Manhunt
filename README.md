# Vexland_Manhunt


[English](README.md) | [日本語](docs/README.ja.md) | [فارسی](docs/README.fa.md) | [Deutsch](docs/README.de.md) | [Français](docs/README.fr.md) | [Español](docs/README.es.md) | [Português (Brasil)](docs/README.pt-BR.md) | [Italiano](docs/README.it.md) | [Nederlands](docs/README.nl.md) | [Polski](docs/README.pl.md) | [Українська](docs/README.uk.md) | [Türkçe](docs/README.tr.md) | [Русский](docs/README.ru.md) | [简体中文](docs/README.zh-CN.md) | [繁體中文](docs/README.zh-TW.md) | [한국어](docs/README.ko.md) | [हिन्दी](docs/README.hi.md) | [Bahasa Indonesia](docs/README.id.md)

**A complete Minecraft Runner-versus-Hunter experience, co-created by [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) and [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt brings match setup, team roles, the opening chase, tracking, progression, rewards, results, and administration into one Paper server plugin. Runners try to defeat the Ender Dragon while Hunters try to eliminate the final Runner. The plugin supports multiple Runners and keeps the chase moving through deaths, respawns, dimension changes, and reconnects. Its `/mhgui` control center lets administrators manage a match through menus, with localized messages and guidebooks for the players.

## Downloads and compatibility

| Supplied release | Download | Installation |
|---|---|---|
| **2.0.0 — combined package** | [VexLandManhunt-2.0.0.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0.jar) | **One JAR**, including integrated GrimAC 2.3.73 |
| **1.13.1 — spectator branch** | [Release and both JARs](https://github.com/FarlandGame/Vexland_Manhunt/releases/tag/v1.13.1) | Manhunt plus separate GrimAC 2.3.73 |
| 1.9.11 / 1.6.4 — older | [All releases](https://github.com/FarlandGame/Vexland_Manhunt/releases) | Historical standalone builds |

**Paper 1.21.11 / Java 21.** These are server plugins, not client mods. The supplied filename and public release are **2.0.0**, but the unchanged descriptor reports **`1.9.11-grim.1`** and identifies the gameplay baseline as 1.9.11. This combined package does **not** contain the dedicated Spectator role, `/mspectator <player>`, `/mhspectate`, categorized menus or other 1.13.1 additions. Keep using the separately listed 1.13.1 branch if you need those features.

Original personal-server builds with creator-specific elevated administrative access are preserved as supplied. The guide covers the public controls.

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

## What changed in the supplied 2.0.0 package?

- **One integrated JAR:** Manhunt, modified GrimAC 2.3.73 and bundled PacketEvents share one Bukkit plugin instance. No separate GrimAC or PacketEvents installation is needed for this package. The descriptor provides `GrimAC`; the archive is flattened, not a nested unchanged Grim JAR.
- **Module status:** administrator command `/vexintegration` reports Grim ACTIVE/INACTIVE, the Bukkit owner, VexAC status, PacketEvents status and tracked-player count. Native `/grim` and `/grimac` commands are registered by the integrated module.
- **Controlled startup:** the loader requires Paper's configuration API and exactly Minecraft 1.21.11. It rejects hot loading with online players and a separate GrimAC instance. If integrated startup fails, the plugin is disabled and logs that Grim protection is inactive; the server itself can continue. Verify status before starting a match.
- **Existing data migration:** on the first integrated load, the migration backs up both old plugin data trees and copies old GrimAC data only when the integrated destination does not exist. Existing integrated data wins if both exist; no merge/overwrite is performed. Original data is retained.
- **Movement correction ownership:** `plugins/VexLandManhunt/integration.properties` defaults to `movement-correction-owner=legacy`. The supported alternative is `grim`; other values abort startup. Choosing grim suppresses VexAC setback/teleport correction paths, while VexAC checks, alerts and evidence remain. It does not disable every legacy punishment.
- **Gameplay baseline:** the flat `/mhgui`, Runner/Hunter role cycling, VexAC controls, Smart Hunter Kit V3, pause/resume, recovery and 683 translated keys follow 1.9.11. This is a combined packaging/integration release, not the spectator-enabled 1.13.1 feature set.

## Gameplay retained from the 1.9.11 foundation

The following systems were added to the 1.9.11 foundation and are retained by this combined package. They are inherited gameplay features, rather than new 2.0.0 spectator features.

| Addition or change | Behavior in 1.9.11 |
| --- | --- |
| **Smart Hunter Kit V3** | Adaptive respawn kits consider Runner equipment, teams, and match context. The system aims to keep Hunter kits below the Runner equipment average and can be toggled with `/mhkit` or the GUI. |
| **Automatic Overworld Spawn** | Move world spawn near an eligible Overworld Runner at a chosen interval: off, 5, 10, 15, 20, or 30 minutes. The system selects a safe surface candidate and skips unsuitable cases. |
| **Pause and resume** | `/mhpause` freezes gameplay and match-related timers, tracking, and spawn movement; `/mhresume` continues. Paused time is offset from active match timing. |
| **Restart/crash recovery** | A recovery layer restores match state, roles, tracker targets, progress, reward/death timers, and reconnect state using primary/backup snapshots, periodic saves, and shutdown saves. |
| **Runner reconnect settings** | A configurable reconnect window replaces the earlier fixed 60-minute window. Fresh default: 15 minutes, with 10 seconds of rejoin protection. Server downtime is excluded; expiry can convert the Runner to a Hunter or finish the match. |
| **Expanded administration** | Change roles during a live match while preserving the final Runner; selected-player actions, team teleport/freeze, runtime resynchronization, and shortcuts improve match management. |
| **Confirmed settings reset** | Two clicks within eight seconds apply Smart Kit ON, auto spawn every 15 minutes, and reconnect 15 minutes. This differs from a fresh installation's auto-spawn OFF default. |
| **VexAC 3.0** | Movement, combat, AutoClick, velocity/knockback, and world-building checks; group/master controls, evidence logging, administrator alerts, and environment/lag exemptions. |
| **Ultra Deep Debug v4** | `/mhdebug` provides state-machine, GUI, synthetic kit/stress, language-placeholder, recovery round-trip, and integrity diagnostics. |
| **Expanded displays** | More progression detail, dragon-health visuals, MVP/damage/distance results, and TAB ping information. |
| **Command changes** | Adds `/mhkit`, `/mhspawn`, `/mhpause`, `/mhresume`, and `/mhdebug`; removes `/mhnone`; makes `/mhhelp` player/admin aware and adds `/trash` aliases. |
| **More localized messages** | Translation resources expand from 446 message keys per language to 683. |

VexAC's packaged checks cover Fly, Speed, Timer, Phase, Step, NoSlow, GroundSpoof, Reach, KillAura, AimAssist, wall-hit, BadPackets, AutoClick timing patterns, altered knockback, Scaffold, Tower, FastPlace, Nuker, and block reach. Its UI uses a monitor-only label, while compiled code also contains kick paths; confirm the actual moderation behavior on a test server before relying on that label. The earlier build contains legacy Anti AutoClick and Anti Fly controls instead.

## Full setup and use with `/mhgui`

### 1. Install the combined build

1. Stop the **Paper 1.21.11 / Java 21** server fully and back up worlds and plugin data.
2. Put only `VexLandManhunt-2.0.0.jar` from this release in `plugins/`. Move older Manhunt and standalone GrimAC JARs out of the active plugins directory. Preserve their data folders; do not delete them. Players do not install this JAR on the client.
3. Start normally rather than using `/reload`. The integrated loader manages its Grim and PacketEvents lifecycle.
4. As OP or with `vexland.admin`, run `/vexintegration`. Check `Grim=ACTIVE` and `PacketEvents=true` before proceeding to `/mhgui`. Inactive protection is a startup problem, not a successful integrated installation.

Grim configuration lives in `plugins/VexLandManhunt/grim/` (`config.yml`, `messages.yml`, `punishments.yml`, `discord.yml`), with optional `violations.sqlite` history. First migration backups go to `plugins/VexLandManhunt-integration-backups/`; `plugins/VexLandManhunt/integration-migration-v1.txt` marks completion. If old and integrated Grim data both exist, the integrated destination is preserved and a warning is logged. Migration refuses symbolic links.

Review movement ownership in `plugins/VexLandManhunt/integration.properties`; preserve other settings. Fresh default:

```properties
movement-correction-owner=legacy
```

The complete public menu guide below follows this package's 1.9.11 gameplay baseline. The spectator branch has its own archived guide.

### 2. Open the control center

Join the server as an administrator with **OP** or the **`vexland.admin`** permission and enter:

```text
/mhgui
```

The instructions below cover the public interface in plugin release **2.0.0**, using its English button labels. Labels follow the selected server language. For complete GUI use, use a trusted **OP** account: the descriptor permission allows opening the command, while some supplied GUI handlers apply stricter OP checks. The main inventory has five rows of nine slots. Hover over a button to read its description and current setting. Most buttons use a normal click; special mouse actions and confirmations are explained below. The smaller 1.6.4 menu is covered at the end.

#### Set up your first match

1. Open **Player Roles**. Click each participant's player head until its displayed role is correct. In 2.0.0 the role cycles between **Runner** and **Hunter**; a previously unassigned participant becomes a Runner on the first click. Left/right/shift-click are not separate role-selection shortcuts. Use **Previous Page**, **Next Page** and **Back to Control Center** when needed.
2. Assign at least one Runner and at least one Hunter. The start routine can turn remaining unassigned online players into Hunters, so assigning every participant explicitly makes the teams clear.
3. Click **Friendly Fire** to choose whether teammates can damage each other. Check the ON/OFF indicator after clicking.
4. Click **Language** to choose the server-wide language. This setting affects messages, interfaces, notices and guidebooks for everyone, not just your own player.
5. Review **Smart Hunter Kit**, **Auto World Spawn** and **Anti-Cheat**. Read the administrator guide from the book button if you need an in-game explanation.
6. Make sure **Server Freeze** is off, then click **Start Match**. Starting prepares the players and their inventories, runs the introduction and random Hunter head-start roulette, then begins the hunt. Keep anything you need outside participant inventories before starting.

#### Main control-center buttons

Positions below count rows from top to bottom and columns from left to right. They describe the final decorated 2.0.0 layout.

| Position | English button | What it does |
|---|---|---|
| Row 2, column 2 | Player Roles | Opens the paginated Runner/Hunter player-head menu. |
| Row 2, column 3 | Target Player | Cycles through other online players for selected-target admin actions. Check the current target name. |
| Row 2, column 4 | Friendly Fire | Toggles damage between teammates. |
| Row 2, column 5 | Match Info | Sends a quick report of match state, teams, friendly fire and the selected target. |
| Row 2, column 6 | Start Match | Runs the normal match start and random head-start sequence. |
| Row 2, column 7 | Full Heal | Restores health for all online players. |
| Row 2, column 8 | Reset Match | Performs the full match reset. This is different from Reset Settings. |
| Row 3, column 2 | Full Hunger | Restores food and saturation for all online players. |
| Row 3, column 3 | Release Hunters | Releases waiting Hunters before their head start expires. |
| Row 3, column 4 | Clear Effects | Removes potion effects from all online players. |
| Row 3, column 5 | Server Freeze | Toggles the global server freeze; ordinary non-OP players are frozen. |
| Row 3, column 6 | Clear Target Inventory | Clears the selected player's inventory, armor and offhand after confirmation. |
| Row 3, column 7 | Teleport Everyone | Brings all online players to your current position. |
| Row 3, column 8 | Kill Target | Kills the selected player after confirmation; normal death rules can affect the match. |
| Row 4, column 2 | Anti-Cheat | Opens the VexAC Security controls. |
| Row 4, column 3 | Freeze Target | Toggles the selected player's individual freeze. |
| Row 4, column 4 | Emergency Restore | Restores health, food and saturation for everyone online. |
| Row 4, column 5 | Freeze Team | Left-click toggles Runners; right-click toggles Hunters; shift-click clears individual/team freezes. |
| Row 4, column 6 | Set Day | Sets your current world to daytime. |
| Row 4, column 7 | Clear Weather | Stops rain and thunder in your current world. |
| Row 4, column 8 | Language | Opens the global language selector. |
| Row 5, column 2 | Smart Hunter Kit | Toggles adaptive Hunter respawn kits; displays ON/OFF. |
| Row 5, column 3 | Clear Dropped Items | Removes dropped item entities in your current world. |
| Row 5, column 4 | Pause Match / Resume Match | Stops or resumes active gameplay and match timers. |
| Row 5, column 5 | Emergency Sync | Re-syncs player roles, trackers and related runtime state. |
| Row 5, column 6 | Reset Settings | Restores the balanced settings after two-click confirmation. |
| Row 5, column 7 | Close | Closes the control center. |
| Row 5, column 8 | Auto World Spawn | Opens the automatic Overworld spawn interval selector. |
| Row 5, column 9 | Manhunt Administrator Guide | Supplies the localized administrator guidebook. |

The decorative glass and title/status items are not gameplay buttons.

#### Roles and selected targets

**Player Roles** changes a participant's actual Manhunt team. Click their head and read the updated role. During STARTING/RUNNING, the interface permits Runner/Hunter changes but refuses to convert the final Runner to Hunter. This preserves the ongoing match's Runner side. Use role changes deliberately because team runtime and trackers are synchronized after a change.

**Target Player** is separate: it selects someone for actions such as Freeze Target, Clear Target Inventory or Kill Target without changing their team. Cycle until the intended online player's name is shown. If a saved target becomes unavailable, the code can fall back to the first other online player, so always confirm the name immediately before a selected-target action. If nobody else is online, it reports that no target is available.

**Clear Target Inventory** and **Kill Target** require clicking the same action for the same target twice within **five seconds**. The first click arms confirmation and identifies the target; the second performs the action. Changing targets or waiting too long requires a new confirmation. Clearing an inventory deletes its contents; killing a Runner can end or change the match under normal death rules.

**Freeze Team** has the only team-specific mouse shortcuts in this menu: ordinary left-click selects the Runner team, ordinary right-click selects the Hunter team, and shift-click clears all individual/team freezes managed by this tool. The global Server Freeze switch is a separate control and should be switched off separately if players remain frozen.

#### Smart Hunter Kit

Click **Smart Hunter Kit** to turn adaptive Hunter respawn kits on or off. The button shows its current state. With it on, a respawning Hunter can receive a kit adapted to Runner gear and match context; the shipped player guide describes the kit as weaker than the Runner average. With it off, Hunters get no automatic kit after death. This does not switch off the tracking compass.

For a direct setting instead of a toggle, use `/mhkit on`, `/mhkit off` or `/mhkit status`. The inspected fresh configuration fallback is ON.

#### Auto World Spawn

Click **Auto World Spawn**, then choose **OFF**, **5 minutes**, **10 minutes**, **15 minutes**, **20 minutes** or **30 minutes**. Selecting an option saves it and returns to `/mhgui`; **Back** returns without selecting a new interval.

When enabled, the system periodically searches for a safe Overworld surface near an active Overworld Runner and moves the world spawn there. It skips movement if no Runner is in the Overworld or no safe candidate is found. The fresh configuration fallback is OFF. For the same controls by command, use `/mhspawn off`, `/mhspawn 15`, or `/mhspawn status`, with any supported interval in place of 15.

#### Pause, reconnect and recovery

**Pause Match** is available while the match is RUNNING. It freezes gameplay systems, movement/interactions, match timers, tracking and spawn movement. **Resume Match** continues those systems and compensates for paused time. Server Freeze only freezes players and should not be used as a substitute when you need the match clock to pause.

The Runner reconnect window is configurable, with a fresh fallback of **15 minutes**. A timely rejoin restores Runner state and provides ten seconds of rejoin protection. Server downtime does not consume the saved reconnect time. Expired Runner slots become Hunters; the final Runner's timeout can give Hunters the win.

There is **no separate reconnect-duration selector in the supplied 2.0.0 GUI**. To customize it, stop the server, edit `plugins/VexLandManhunt/config.yml`, preserve its other settings and set:

```yaml
features:
  custom-reconnect-minutes: 15
```

Restart after editing. Values below one minute are clamped to one. **Reset Settings** restores this value to 15 minutes. The compiled build also saves match/reconnect state and backup snapshots for recovery after server restarts/crashes; let the plugin manage those files rather than editing them during play.

#### Reset Settings and Reset Match

**Reset Settings** requires clicking the button twice within **eight seconds**. The first click arms confirmation; the second restores **Smart Kit ON**, **Auto Spawn every 15 minutes**, **Reconnect 15 minutes** and a **random head start**. This differs from a fresh installation, where Auto World Spawn falls back to OFF. It changes configuration; it does not replace the full match reset.

**Reset Match** performs the existing match reset, clearing temporary match state/items and returning players to the Overworld spawn for another round. Its main button does not use the Reset Settings two-click confirmation. **Start Match** can prepare/clear participant inventories. Review which reset/start control you intend to use before clicking.

#### Language and anti-cheat controls

**Language** opens the global selector. Click the named language you want. Both supplied builds contain English, Persian, Arabic, Spanish, French, German, Russian, Simplified Chinese, Hindi and Portuguese. The selected language is shared by the server and persisted. Japanese README documentation does not add Japanese to the plugin's in-game selector.

**Anti-Cheat** opens **VexAC Security**. Click **VexAC Master** to enable/disable the internal engine, or click **Movement**, **Combat**, **AutoClick**, **Velocity / AntiKB** or **World / Scaffold** to toggle that group. **Anti X-Ray** toggles Paper's configured Anti-Xray; restart the server to apply that change. Status, evidence-log and detection-model tiles explain the current systems. **Back to Control Center** returns to the main menu.

The build's interface describes monitor-only moderation, but static inspection retains a threshold-based kick path. Treat the menu's no-kicks wording as an implementation/documentation discrepancy and confirm moderation behavior on a controlled server before depending on it.

#### Integrated GrimAC and legacy VexAC

The existing **VexAC Security** GUI controls the legacy VexAC engine; its Master/group buttons are not a new Grim control panel. Integrated GrimAC runs alongside it. Use `/vexintegration` for module status and native `/grim` or `/grimac` for Grim's own commands and permission-controlled tools. Grim's settings and punishment rules are in `plugins/VexLandManhunt/grim/`.

The 1.13.1 GrimBridge monitor/groups menu and `grim-settings.yml` do not describe this package. Do not assume that switching VexAC off also disables integrated GrimAC, or that a monitor label establishes a no-kicks policy. Paper Anti-Xray remains an independent restart-requiring setting.

#### In-game guide and troubleshooting

Click **Manhunt Administrator Guide** or use `/mhhelp` for a localized guidebook. Players can use `/mhhelp` for their role-aware guide in 2.0.0. Hunters right-click their compass to select a Runner; this tracker interface is separate from the administrator's Target Player selector.

If a role or tracker appears out of sync, **Emergency Sync** refreshes related runtime state. **Match Info** helps check the current teams and state. If a requested start fails, check that the match is ready, the server freeze is off, and a Runner/Hunter team exists. After changing the JAR, use a full server restart rather than `/reload`. `/mhdebug` is an administrator diagnostic command included in 2.0.0; its presence is not a claim that these releases passed live server tests.

#### Using the older 1.6.4 control center

1.6.4 retains **Player Roles**, **Friendly Fire**, **Start Match**, **Reset Match**, **Release Hunters Now**, **Server Lock**, **Teleport Everyone To Me**, **Heal & Feed Everyone**, **Match Status**, language selection, **Anti Cheat**, and an administrator guide. Its roles cycle **None → Runner → Hunter**, and role changes are locked while a match is starting/running.

Its anti-cheat menu contains legacy **Anti AutoClick** (30-CPS rule with warning/kick handling), **Anti Fly** and Paper **Anti X-Ray**. Its Runner reconnect window is fixed at **60 minutes**. The newer Smart Hunter Kit V3 toggle, Auto World Spawn selector, pause/resume, Reset Settings confirmation and expanded selected-target/world tools described above belong to 2.0.0 and should not be expected in the older menu.

This guide was derived from the supplied JAR metadata, bundled language/help text and static disassembly. The interface was not executed on a live Minecraft server during this inspection.

### 3. Play the chase

Runners escape during the randomized head start and progress toward defeating the Ender Dragon. Hunters wait for release, then right-click their tracker compass to select a Runner. Targets can be changed during play, including when the chase crosses dimensions. Use `/teammsg <message>` to speak only to your team and `/mhhelp` for the localized role guide in 2.0.0.

If a Runner dies, the remaining Runners keep playing and the fallen player becomes a Hunter. A Hunter can respawn and continue tracking. The final Runner's death or Runner disconnect expiry can finish the match for Hunters; Ender Dragon defeat finishes it for Runners.

### 4. Pause, finish, and prepare another match

In 2.0.0, pause with `/mhpause` and continue with `/mhresume`. Use `/mhrelease` if Hunters should be released before the head-start countdown ends. For a fresh match, use the control center's full reset or `/mhreset`; reset clears temporary match state and items and returns players to the Overworld spawn. Changing Paper Anti-Xray settings needs a restart.

## Default settings in the combined 2.0.0 package

The inspected fresh-config fallback values are:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` means automatic spawn movement is off. The GUI's confirmed settings-reset action sets the spawn interval to 15 minutes instead. Use the GUI or `/mhkit` and `/mhspawn` for the corresponding settings.

## Public command reference — combined 2.0.0

Administrator commands require OP or `vexland.admin` (default OP). Team chat, trash and night vision are player utilities; `/mhhelp` gives the role-aware guide. The table lists the 17 Manhunt/integration commands; native Grim commands have their own permissions. `/mhnone` is not registered here.

| Command | Purpose |
| --- | --- |
| `/vexintegration` | Report integrated Grim, VexAC, PacketEvents and shared Bukkit-owner status |
| `/mhgui` | Open the control center |
| `/mhstart` | Run the full match-start sequence |
| `/mhreset` | Fully reset the current match |
| `/mhrelease` | Release Hunters early |
| `/mrunner <player>` | Assign a Runner |
| `/mhunter <player>` | Assign a Hunter |
| `/teammsg <message>` | Send a private teammate message |
| `/trash` | Open the disposable 54-slot inventory |
| `/nv` | Toggle personal night vision |
| `/mhlang` | Open the global language selector |
| `/mhhelp` | Receive a localized guidebook |
| `/mhkit <on\|off\|toggle\|status>` | Configure Smart Hunter kits |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Configure automatic spawn movement |
| `/mhpause` | Pause the running match |
| `/mhresume` | Resume the paused match |
| `/mhdebug` | Run internal diagnostics |

## In-game languages and documentation

This package retains **10 game languages**: English, Persian, Arabic, Spanish, French, German, Russian, Simplified Chinese, Hindi and Portuguese. Each bundled translation has **683 keys**, following 1.9.11. `/mhlang` sets one server-wide language, saved in `language.txt`.

Project documentation has **18 languages**, excluding an Arabic documentation edition. These translations do not add Japanese or other extra in-game languages to the unchanged binary.

## Version history, source and credits

[CHANGELOG.md](CHANGELOG.md) records each supplied release. The full [1.13.1 spectator guide](docs/archive/1.13.1/README.md) and [older 1.9.11 / 1.6.4 guide](docs/archive/1.9.11/README.md) remain available. Every supplied version keeps its own download and checksum.

**Manhunt is co-created by Bardiya / Farland_game and Ali / Alivexor. GrimAC is a separate project by GrimAC / DefineOutside and contributors.** This integrated artifact modifies three Grim classes; it is not the unchanged official Grim binary from the older two-file release. The companion [source package](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0-source.zip) retains supplied sources, build scripts, dependency inputs and notices, with test/runtime evidence omitted and source code unchanged. The release also includes GPLv3 text, checksums and [third-party notices](THIRD_PARTY_NOTICES.md). No live-server or reproducible-build test was performed during this publication.

## A playful challenge to Dream

A little Minecraft banter from Bardiya 😄

> "Sigh... Ali and I made a Manhunt plugin a hundred times better than Dream's, but Dream's scared and won't play ours!"

## Creators and project scope

**Co-created by [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) and [Ali · Alivexor](https://github.com/Alivexor).** Both handles are also recorded as authors in the original plugin descriptors.

This repository presents the original compiled releases, their documentation, and version notes as a shared portfolio project. Feature descriptions are based on static inspection of the supplied JARs. Live-server compatibility, recovery performance, balance, and anti-cheat accuracy have not been tested in this publication workflow.

[Bardiya's GitHub portfolio](https://github.com/FarlandGame) · [Ali's GitHub](https://github.com/Alivexor) · [All releases](https://github.com/FarlandGame/Vexland_Manhunt/releases)
