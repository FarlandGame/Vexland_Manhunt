# Vexland_Manhunt — 1.13.1

> 旧版本归档指南 · [2.0.0 →](../../README.zh-CN.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**完整的 Minecraft 逃亡者对抗猎人体验，由 [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) 与 [Ali · Alivexor](https://github.com/Alivexor) 共同开发。**

Vexland_Manhunt 将比赛设置、队伍角色、开场追逐、追踪、进度、奖励、结果与管理功能整合进一个 Paper 服务器插件。逃亡者试图击败末影龙，猎人则试图消灭最后一名逃亡者。插件支持多名逃亡者，并在死亡、重生、切换维度和重新连接后继续维持追逐。管理员可以通过 `/mhgui` 控制中心的菜单管理比赛，玩家则可以使用本地化消息与指南书。

## 下载与兼容性

| 文件 / 版本 | 下载 | 用途 |
|---|---|---|
| **1.13.1 — 当前版本** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Bardiya 和 Ali 开发的 Manhunt 插件 |
| **GrimAC 2.3.73 — 必需** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | 独立的第三方反作弊依赖 |
| 1.9.11 — 已归档 | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | 上一个 Manhunt 构建版本 |
| 1.6.4 — 已归档 | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | 更早的 Manhunt 构建版本 |

**目标环境：Paper 1.21.11、Java 21。** 1.6.4、1.9.11 和 1.13.1 是插件的发布版本号，不是支持的 Minecraft 版本号。在 1.13.1 中，GrimAC 是强制依赖，桥接层需要 2.3.73 API。请下载**两个当前版本的 JAR**。它们是服务器插件，玩家无需将其安装到客户端的 mods 文件夹。

这些是原始的个人服务器构建，保留了创建者专属的高级管理权限，内容与提供时完全一致。本手册介绍公开的 Manhunt 控制功能。

## Manhunt 体验

- **逃亡者与猎人队伍：**将在线玩家分配到任一阵营。比赛至少需要一名逃亡者，以及一名猎人或一名尚未分配角色的在线玩家。队友死亡后，存活的逃亡者仍会继续比赛；死亡的逃亡者会成为猎人，除非这次死亡使比赛结束。
- **电影式比赛开场：**准备物品栏和游戏模式，介绍队伍，并通过轮盘随机决定逃亡者的领先时间。猎人在倒计时期间被冻结，并收到标题与声音提示。领先时间是随机的；管理员可以提前释放猎人。
- **可选择目标的追踪指南针：**猎人获得一枚特殊指南针。右键点击它，在目标菜单中选择一名逃亡者，并在追逐期间更换目标。跨维度时，追踪会沿相关传送门路线进行，直到可以直接追踪目标。猎人重生后会再次获得追踪器。
- **进度显示：**Boss 栏和比赛信息根据逃亡者装备，以及下界资源、烈焰棒、末影珍珠、末影之眼、要塞和末地等进程更新。新构建增加了更细致的阶段，以及随末影龙生命值变化的进度显示。
- **逃亡者击杀奖励：**在进行中的比赛里，逃亡者击杀猎人时，系统会使用一个随进度变化、包含 50 个条目的加权奖励池。包含抽奖动画、双重／三重奖励、连杀公告和稀有物品庆祝效果。
- **胜利与结果：**最后一名逃亡者死亡，猎人获胜；击败末影龙，逃亡者获胜。包含比赛结束标题、庆祝效果、击杀／死亡信息以及临时物品清理。新构建还报告 MVP、伤害和移动距离结果。
- **队伍交流与实用功能：**通过 `/teammsg` 私下向队友发消息，使用 `/trash` 打开 54 格临时垃圾物品栏，以及通过 `/nv` 切换个人夜视。
- **通过菜单管理：**控制中心提供角色分配、开始／重置、提前释放猎人、友军伤害、服务器锁定、全员传送、治疗／补充饥饿、语言、保护设置、状态和指南书。冻结和完整重置有助于准备下一场比赛。
- **本地化指南：**逃亡者、猎人和管理员指南书解释目标、追踪器用法、死亡、设置与命令。1.9.11 版本通过 `/mhhelp` 向玩家提供与其角色对应的指南。
- **Paper Anti-Xray 集成：**菜单控制 Paper 的世界级保护；更改需要重启服务器才会生效。

## 1.13.1 有哪些新内容？

与提供的 1.9.11 构建相比：

- **幽灵观察者：** 独立角色，由管理员分配；提供受保护的飞行、对其他玩家隐藏、状态保存与恢复，以及分页的参赛者传送菜单。
- **重新设计的控制中心：** 分类菜单、明确的四种角色选择、按名称选择目标、重连时长选择器、Classic/Fast/Hardcore/Custom 预设，以及独立的 30 秒确认界面。
- **GrimAC 集成：** 必需的 GrimAC 2.3.73 替代了原先启用的 VexAC 启动路径。GUI 提供总开关、五个检测组、提醒及监控/执行模式控制。Paper Anti-Xray 仍然独立运行。
- **新的 Smart Hunter Kit 规划器：** 根据 Runner 的装备和附魔、最近的 Runner、队伍人数、距离、维度及地形调整装备与补给。保留已有的更强装备，避免重复工具，并通过 30 秒历史记录限制消耗品补充。这不保证固定的装备差距，也不代表经过实测的平衡性。
- **经校验的恢复：** 使用 SHA-256 封存快照、检查数据结构和状态，并在需要时回退到有效备份；无效或格式更新的快照会保留，不会被覆盖。观察者状态单独持久化保存。
- **更多消息：** 每份内置翻译的消息键从 683 个增加到 762 个，游戏内语言仍为相同的十种。新增两个公开注册命令：`/mspectator <player>` 和 `/mhspectate`。
- **重置后备行为：** 如果主世界出生点附近找不到安全地面，重置可以跳过该次传送，而不强行传送。

## 使用 `/mhgui` 完整设置与操作

停止服务器，并备份世界及插件数据。将两个当前版本的 JAR 放入 `plugins/`，该目录中只保留一个 Manhunt JAR 和一个 GrimAC JAR。升级时保留现有的 `plugins/VexLandManhunt/` 设置与数据。完整启动 Paper 1.21.11 / Java 21 服务器；替换构建版本后应完全重启。GrimAC 必须成功加载。插件的内部名称仍为 `VexLandManhunt`。

本指南介绍插件 **1.13.1**，并使用英文界面标签。实际标签遵循服务器的全局语言。位置按从上到下数行、从左到右数列。除非另有说明，否则使用普通左键点击。本指南基于静态检查，未运行 Minecraft 服务器。

### 设置一场比赛

1. 使用具有 `vexland.admin` 权限的账号执行 `/mhgui`（默认：OP）。
2. 打开 **Player Roles**，点击带玩家名称的图标，然后选择 **Runner**、**Hunter**、**Spectator** 或 **No Team**。这会打开明确的角色选择器；点击玩家不会循环切换角色。
3. 至少分配一名 Runner 和一名 Hunter。比赛开始时，尚未分配角色的在线玩家可能变为 Hunter；观察者不能充当任一队伍所需的成员。
4. 检查 **Match Settings**、**GrimAC Security** 和 **Global Language**。开始前关闭 Server Freeze。
5. 打开 **Match Controls → Start Match**。系统准备/清空参赛者的物品栏，播放开场介绍，并由轮盘决定 Hunter 的延迟出发时间。

### 主页：`/mhgui`（五行）

| 位置 | 按钮 | 操作 |
|---|---|---|
| R2 C2 | Match Controls | 开始、暂停/继续、放行及重置。 |
| R2 C4 | Player Roles | 打开在线玩家角色列表。 |
| R2 C6 | Match Settings | 友军伤害、装备包、出生点、重连及预设。 |
| R2 C8 | Player Management | 选择目标并使用玩家/世界工具。 |
| R4 C2 | GrimAC Security | 打开保护设置。 |
| R4 C4 | Global Language | 选择所有人使用的语言。 |
| R4 C6 | Administrator Guide | 将本地化管理员指南书加入物品栏。 |
| R5 C5 | Close | 关闭菜单。 |

R1 C5 的信标显示比赛状态及 Runner/Hunter 人数。

### Match Controls（五行）

| 位置 | 按钮 | 操作 |
|---|---|---|
| R2 C2 | Start Match | 开始完整流程。 |
| R2 C4 | Pause Match / Resume Match | 暂停或继续游戏及比赛计时；适用于 RUNNING 状态的比赛。 |
| R2 C6 | Release Hunters | 提前结束当前 Hunter 等待时间。 |
| R2 C8 | Reset Match | 打开确认界面，然后完全重置比赛。 |
| R4 C2 | Server Freeze | 切换对全服非 OP 玩家的冻结。 |
| R4 C4 | Teleport Everyone | 打开确认界面，然后将所有在线玩家传送到你身边。 |
| R4 C6 | Match Info | 发送比赛和队伍报告。 |

**Back** 位于 R5 C1；**Close** 位于 R5 C9。Server Freeze 与 Pause Match 相互独立：需要同时停止计时和游戏系统时，请使用 Pause。

### Player Roles

六行的玩家列表在前五行最多显示 45 个带名称的角色图标，按玩家名称排序。Runner 使用黄绿色混凝土，Hunter 使用红色混凝土，Spectator 使用末影之眼，No Team 使用灰色混凝土。底行 C1 是 **Previous Page**，C3 显示页码/在线信息，C5 是 **Back to Control Center**，C9 是 **Next Page**。

点击玩家可打开 **Choose Player Role**（三行）：

| 位置 | 指定角色 |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

玩家名称/当前角色显示在 R1 C5；**Back** 位于 R3 C1，**Close** 位于 R3 C9。比赛期间可以更改角色。在 RUNNING 状态下，将最后一名已分配的 Runner 改为其他角色，会打开 **Last Runner: the match will end** 确认界面。确认后可能判定 Hunter 获胜。直接角色命令会立即生效，请谨慎使用。这里可以分配 No Team；在正在进行的比赛中，正常的开始/加入同步可能将未分配角色的玩家变为 Hunter。

### 观察者

管理员使用 `/mspectator <player>` 或在 Player Roles 中选择 **Spectator** 来分配角色。虽然命令描述文件没有权限行，处理器仍检查管理员权限。玩家执行 `/mhspectate` 不会自行加入观察者。

观察者会在快捷栏第一格收到 **Spectator teleport** 指南针。主手持有它并右键点击，或使用 `/mhspectate`，即可打开六行传送菜单。此菜单仅在玩家具有 Spectator 角色时可用。前五行最多列出 45 名存活且在线的 Runner/Hunter，按名称排序；点击带名称的角色图标可传送到该玩家的当前位置，也支持其他世界。底行 C1 是 **Previous Page**，C5 是 **Close**，C9 是 **Next Page**。没有合适参赛者时，R3 C5 显示 **No players available**。关闭菜单后仍保持观察者角色。

观察者可以飞行、对其他玩家隐藏、无碰撞，并受到伤害保护。实现采用带飞行能力的冒险模式，不提供原版旁观模式的摄像机功能或穿墙移动。系统阻止攻击、破坏/放置方块、普通方块/实体交互、拾取/丢弃物品、副手交换、物品栏点击/拖动、操作盔甲架及拾取/获得经验。生物无法将其设为目标，饥饿值变化也会被取消。`/teammsg <message>` 会发送给其他 Spectator 角色玩家。请勿向参赛者泄露参与者位置或提供其他场外协助。

退出时，管理员分配 **Runner**、**Hunter** 或 **No Team**，或使用 `/mrunner <player>`、`/mhunter <player>`。没有专门的自行退出命令/按钮。退出会恢复保存的物品栏/光标物品、位置、游戏模式、飞行、碰撞及免伤状态，再应用新角色的比赛行为。观察者状态会保存以便重新加入。完整 Match Reset 会恢复观察者状态、清除角色，并在存在安全主世界出生点时将在线玩家传送过去。正常的比赛结束清理不会对观察者执行参赛者的物品/飞行处理。

### Match Settings（五行）

| 位置 | 按钮 | 操作 |
|---|---|---|
| R2 C2 | Friendly Fire | 切换队友伤害。 |
| R2 C4 | Smart Hunter Kit | 切换自适应 Hunter 重生装备包。 |
| R2 C6 | Auto World Spawn | 打开间隔选择器。 |
| R2 C8 | Reconnect Grace | 打开 Runner 重连时长选择器。 |
| R4 C2 | Match Preset | 选择 Classic、Fast、Hardcore 或 Custom。 |
| R4 C4 | Reset Settings | 确认平衡设置：Kit ON、Spawn 15m、Reconnect 15m。 |
| R4 C6 | Random Head Start | 信息图标；延迟仍由轮盘决定。 |

**Back** 位于 R5 C1；**Close** 位于 R5 C9。

三行的 **Reconnect Grace** 选择器在 R2 C2–C7 依次提供 **1、5、10、15、20、30 分钟**。点击后保存数值，并保持选择器打开。Back 位于 R3 C1；Close 位于 R3 C9。

三行的 **Match Preset** 选择器在 R2 C2、C4、C6、C8 放置 **Classic**、**Fast**、**Hardcore**、**Custom**。Classic：Kit ON、Spawn 15m、Reconnect 15m。Fast：ON、5m、10m。Hardcore：OFF、OFF、5m。Custom 保留当前手动设置。预设保留随机延迟出发。选择后菜单保持打开；Back 位于 R3 C1，Close 位于 R3 C9。

**Auto World Spawn** 在 R2 C2、C3、C4 提供 OFF、5m、10m，在 R2 C6、C7、C8 提供 15m、20m、30m。Back 位于 R3 C5。选择间隔或使用 `/mhspawn <off|5|10|15|20|30|status>`。它会将主世界出生点移动到合适的主世界 Runner 附近；没有合适目标时可以跳过。`/mhkit <on|off|toggle|status>` 可直接控制装备包。

### Player Management（六行）

| 位置 | 按钮 | 作用对象 |
|---|---|---|
| R1 C5 | Target Player | 打开按名称选择玩家的界面。 |
| R2 C2 | Full Heal | 所有在线玩家。 |
| R2 C4 | Full Hunger | 所有在线玩家。 |
| R2 C6 | Clear Effects | 所有在线玩家。 |
| R2 C8 | Freeze Target | 选中的玩家。 |
| R4 C2 | Clear Target Inventory | 选中的玩家；需要确认。 |
| R4 C4 | Kill Target | 选中的玩家；需要确认，并适用正常比赛结果规则。 |
| R4 C6 | Set Day | 你当前所在的世界。 |
| R4 C8 | Clear Weather | 你当前所在的世界。 |
| R5 C2 | Clear Dropped Items | 你当前所在的世界；需要确认。 |
| R5 C4 | Emergency Sync | 刷新在线玩家的角色/运行时系统。 |
| R5 C6 | Freeze Team | 左键：Runner；右键：Hunter；Shift 点击：清除这些队伍/个人冻结。 |

Back 位于 R6 C1；Close 位于 R6 C9。选择目标不会更改角色。选择器每页显示另外 28 名在线玩家，位于第 2–5 行、第 2–8 列；点击名称即可选择并返回。Previous/Back/Next 分别位于 R6 C1/C5/C9。执行操作前再次核对显示的目标。

### 确认界面

Reset Match、Teleport Everyone、Reset Settings、Clear Target Inventory、Kill Target、Clear Dropped Items，以及 GUI 中最后一名 Runner 的角色更改，均使用独立的三行 **Confirm Action** 界面。查看 R1 C5 的操作/目标，然后点击 R2 C3 的绿色 **Confirm** 或 R2 C7 的红色 **Cancel**。确认在 **30 秒**后过期。目标发生变化/离线，或角色变化时，需要重新选择。这些新菜单路径取代旧指南中五/八秒内重复点击的说明。

### GrimAC Security 与语言

六行 Grim 菜单在 R1 C5 显示状态；开关位于 R2 C2 **GrimAC Master**、C4 **Movement**、C6 **Combat**、C8 **Packets**；R4 C2 **Velocity / AntiKB**、C4 **World / Scaffold**、C6 **Anti X-Ray**、C8 **Admin Alerts**；以及 R5 C5 **Monitor mode**。Back 位于 R6 C1，Close 位于 R6 C9。Monitor mode 控制提醒/证据与执行模式之间的切换。Paper Anti-Xray 独立运行，更改后需要重启。这些是 GrimAC 控制；旧版 VexAC/AutoClick 菜单说明不适用于本版本。

Global Language 对所有人有效，并刷新菜单/物品。点击带名称的语言；Back 位于 R3 C5。`/mhlang` 打开同一选择器，`/mhhelp` 提供本地化玩家/管理员指南。

### 当前默认值、重连与管理处罚

`plugins/VexLandManhunt/config.yml` 中新配置的后备默认值为：

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` 表示自动移动出生点已关闭。Reset Settings 和 Classic 则会选择 15 分钟。在 Runner 的重连窗口内，其名额会保留；及时返回可获得十秒保护。已保存的服务器停机时间不计入。超时可能使 Runner 变为 Hunter，或结束比赛并判定 Hunter 获胜。Pause/Resume 冻结游戏系统并调整有效比赛计时。恢复文件由插件管理。

Grim 桥接设置保存在 `plugins/VexLandManhunt/grim-settings.yml`。新配置默认 Master ON、五个组全部 ON、Admin Alerts ON，以及 **Monitor mode OFF：已启用执行模式**。监控模式将证据/提醒加入队列，并取消符合条件的标记。在执行模式下，桥接层可将 Grim 踢出命令转换为允许重连的本地化断开连接；这并不建立永久封禁策略。实际阈值也取决于 Grim 配置。证据排队写入 `plugins/VexLandManhunt/anticheat/grim-evidence.log`；有上限的队列在高负载下可能丢弃条目。桥接层豁免观察者、暂停/冻结的游戏状态及某些载具场景，并在加入、传送和重生后给予三秒宽限期。不宣称任何反作弊准确率或性能基准。

## 公开命令参考 — 1.13.1

管理员权限指 OP 或 `vexland.admin`（默认 OP）。`/mspectator <player>` 处理器即使没有描述文件权限行，也会检查该权限。直接角色命令立即生效；在 RUNNING 状态下更改最后一名 Runner 的角色可能结束比赛。GUI 会为该情况提供确认。

| 命令 | 用途 | 权限 |
|---|---|---|
| `/mhgui` | 打开分类控制中心 | 管理员 |
| `/mhstart` | 开始完整比赛流程 | 管理员 |
| `/mhreset` | 完全重置比赛 | 管理员 |
| `/mhrelease` | 放行等待中的 Hunter | 管理员 |
| `/mrunner <player>` | 分配 Runner | 管理员 |
| `/mhunter <player>` | 分配 Hunter | 管理员 |
| `/mspectator <player>` | 分配 Spectator | 管理员；新增 |
| `/mhspectate` | 打开参赛者传送菜单 | 当前为 Spectator；新增 |
| `/teammsg <message>` | 发送给相同角色/队伍 | 玩家 |
| `/trash` | 一次性 54 格垃圾物品栏；别名 `/mhtrash`、`/vextrash` | 玩家 |
| `/nv` | 切换个人夜视 | 玩家 |
| `/mhlang` | 打开全局语言选择器 | 管理员 |
| `/mhkit <on\|off\|toggle\|status>` | 配置自适应 Hunter 装备包 | 管理员 |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | 配置出生点移动 | 管理员 |
| `/mhhelp` | 获取本地化角色/管理员指南 | 玩家 / 管理员 |
| `/mhpause` | 暂停进行中的比赛 | 管理员 |
| `/mhresume` | 继续暂停的比赛 | 管理员 |
| `/mhdebug` | 内部诊断 | 管理员 |

本版本未注册 `/mhnone`；请使用 GUI 的 No Team 角色。Hunter 右键点击追踪指南针来选择 Runner；这与观察者传送及管理员目标选择器各自独立。Runner 通过击败末影龙获胜；没有 Runner 剩余时 Hunter 获胜。若仍有其他 Runner，死亡的 Runner 会变为 Hunter。

## 语言、历史与第三方鸣谢

原插件提供 **10 种游戏内语言**：英语、波斯语、阿拉伯语、西班牙语、法语、德语、俄语、简体中文、印地语和葡萄牙语。`/mhlang` 为整个服务器选择一种语言，并保存到 `language.txt`。GitHub 手册有 **18 种语言**，不包含阿拉伯语文档版本。日语及其他额外 README 语言不会为未修改的 JAR 增加游戏内翻译。

[版本历史](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) 记录每个提供的构建版本。完整的旧版 1.9.11 / 1.6.4 手册保留在[版本化归档](../1.9.11/README.zh-CN.md)中。专门支持观察者的构建现已提供，并作为 1.13.1 发布；这些功能不应归属于旧版下载。

**GrimAC 是 GrimAC 贡献者开发的独立项目，以 GPL-3.0 分发。** Bardiya 和 Ali 创建了 Vexland_Manhunt 及其集成；他们不是 GrimAC 的作者。提供的 Grim JAR 与官方 Modrinth 2.3.73 Bukkit 文件的 SHA-512 和 SHA-1 一致。其内嵌源码提交与[上游 v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73)一致。发布内容包括未修改的二进制文件、校验和、上游源码快照、许可证及[第三方声明](../../../THIRD_PARTY_NOTICES.md)。这些组件声明不会为独立的 Manhunt 项目指定许可证。

## 给 Dream 的玩笑挑战

来自 Bardiya 的一点 Minecraft 玩笑 😄

> “唉……Ali 和我做了一个比 Dream 的好一百倍的 Manhunt 插件，可 Dream 害怕了，不肯来玩我们的！”

## 创建者与项目范围

**由 [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) 与 [Ali · Alivexor](https://github.com/Alivexor) 共同开发。** 两个账号也作为作者记录在原始插件描述文件中。

本仓库将原始编译版本、文档和版本说明作为共同作品集项目展示。功能描述基于对提供的 JAR 的静态检查。在此次发布工作流程中，尚未测试真实服务器兼容性、恢复性能、平衡性或反作弊准确性。

[Bardiya 的 GitHub 作品集](https://github.com/FarlandGame) · [Ali 的 GitHub](https://github.com/Alivexor) · [所有发布版本](https://github.com/FarlandGame/Vexland_Manhunt/releases)
