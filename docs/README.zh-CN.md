# Vexland_Manhunt


[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**完整的 Minecraft 逃亡者对抗猎人体验，由 [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) 与 [Ali · Alivexor](https://github.com/Alivexor) 共同开发。**

Vexland_Manhunt 将比赛设置、队伍角色、开场追逐、追踪、进度、奖励、结果与管理功能整合进一个 Paper 服务器插件。逃亡者试图击败末影龙，猎人则试图消灭最后一名逃亡者。插件支持多名逃亡者，并在死亡、重生、切换维度和重新连接后继续维持追逐。管理员可以通过 `/mhgui` 控制中心的菜单管理比赛，玩家则可以使用本地化消息与指南书。

## 下载与兼容性

| 提供的版本 | 下载 | 安装 |
|---|---|---|
| **2.0.0 — 合并包** | [VexLandManhunt-2.0.0.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0.jar) | **一个 JAR**，内含集成的 GrimAC 2.3.73 |
| **1.13.1 — 旁观者分支** | [版本及两个 JAR](https://github.com/FarlandGame/Vexland_Manhunt/releases/tag/v1.13.1) | Manhunt 加独立的 GrimAC 2.3.73 |
| 1.9.11 / 1.6.4 — 较旧版本 | [所有版本](https://github.com/FarlandGame/Vexland_Manhunt/releases) | 历史独立构建 |

**Paper 1.21.11 / Java 21。** 这些是服务端插件，不是客户端模组。提供的文件名和公开发布版本是 **2.0.0**，但未修改的描述文件报告版本为 **`1.9.11-grim.1`**，并将玩法基础标明为 1.9.11。此合并包**不包含**专用 Spectator 角色、`/mspectator <player>`、`/mhspectate`、分类菜单或其他 1.13.1 新增功能。如果需要这些功能，请继续使用单独列出的 1.13.1 分支。

这些个人服务器的原始构建按提供时的状态保留，其中包含创作者专属的提升管理权限。本指南介绍公开控制项。

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

## 提供的 2.0.0 包有哪些变化？

- **一个集成 JAR：** Manhunt、修改后的 GrimAC 2.3.73 和随包提供的 PacketEvents 共享同一个 Bukkit 插件实例。此包无需单独安装 GrimAC 或 PacketEvents。描述文件声明提供 `GrimAC`；归档内容已扁平化合并，并非在内部嵌套一个未修改的 Grim JAR。
- **模块状态：** 管理员命令 `/vexintegration` 报告 Grim 的 ACTIVE/INACTIVE、Bukkit 所有者、VexAC 状态、PacketEvents 状态和跟踪中的玩家数量。原生 `/grim` 和 `/grimac` 命令由集成模块注册。
- **受控启动：** 加载器要求 Paper 配置 API，且 Minecraft 版本必须恰好为 1.21.11。它会拒绝在有在线玩家时热加载，也拒绝存在独立 GrimAC 实例的情况。如果集成启动失败，插件将被禁用，并在日志中说明 Grim 保护未启用；服务器本身仍可继续运行。开始比赛前请核实状态。
- **现有数据迁移：** 首次集成加载时，迁移过程会备份原有两个插件的数据目录树，并且只在集成目标不存在时复制旧 GrimAC 数据。如果两者都存在，则优先使用现有集成数据，不进行合并或覆盖。原始数据会保留。
- **移动纠正归属：** `plugins/VexLandManhunt/integration.properties` 的默认值为 `movement-correction-owner=legacy`。支持的另一选项是 `grim`；其他值会中止启动。选择 grim 会抑制 VexAC 的 setback/传送纠正路径，同时保留 VexAC 检查、警报和证据记录。这不会禁用所有旧式处罚。
- **玩法基础：** 平面式 `/mhgui`、Runner/Hunter 角色循环、VexAC 控制项、Smart Hunter Kit V3、暂停/恢复、恢复机制和 683 个翻译键均沿用 1.9.11。这是一次合并打包与集成发布，并非具备旁观者功能的 1.13.1 功能集。

## 从 1.9.11 基础保留的玩法

以下系统加入于 1.9.11 基础版本，并由此合并包保留。它们是继承的玩法功能，而非 2.0.0 新增的旁观者功能。

| 新增或更改 | 1.9.11 中的行为 |
| --- | --- |
| **Smart Hunter Kit V3** | 自适应重生装备包考虑逃亡者装备、队伍与比赛情况。系统旨在将猎人的装备包保持在逃亡者平均装备水平以下，可通过 `/mhkit` 或 GUI 开关。 |
| **自动主世界出生点** | 按所选间隔，将世界出生点移动到符合条件的主世界逃亡者附近：关闭、5、10、15、20 或 30 分钟。系统会选择安全的地表候选位置，并跳过不适合的情况。 |
| **暂停与恢复** | `/mhpause` 冻结游戏，以及与比赛相关的计时器、追踪和出生点移动；`/mhresume` 恢复这些功能。暂停时间会从有效比赛时间中扣除。 |
| **重启／崩溃恢复** | 恢复层利用主／备份快照、定期保存和关服保存，恢复比赛状态、角色、追踪目标、进度、奖励／死亡计时器与重新连接状态。 |
| **逃亡者重新连接设置** | 可配置的重新连接时限取代了之前固定的 60 分钟时限。全新配置默认值为 15 分钟，并提供 10 秒的重新加入保护。服务器停机时间不计入时限；超时可能使逃亡者变为猎人或结束比赛。 |
| **扩展管理功能** | 在进行中的比赛里更改角色，同时保留最后一名逃亡者；选定玩家操作、队伍传送／冻结、运行时重新同步和快捷功能改善了比赛管理。 |
| **需要确认的设置重置** | 在八秒内点击两次，会应用 Smart Kit 开启、每 15 分钟自动移动出生点，以及 15 分钟重新连接时限。这与全新安装的自动出生点关闭默认值不同。 |
| **VexAC 3.0** | 移动、战斗、AutoClick、速度／击退和世界建筑检查；分组／总开关、证据日志、管理员提醒以及环境／延迟豁免。 |
| **Ultra Deep Debug v4** | `/mhdebug` 提供状态机、GUI、合成装备包／压力、语言占位符、恢复往返和完整性诊断。 |
| **扩展显示** | 更详细的进度、末影龙生命值显示、MVP／伤害／移动距离结果，以及 TAB 延迟信息。 |
| **命令变化** | 新增 `/mhkit`、`/mhspawn`、`/mhpause`、`/mhresume` 和 `/mhdebug`；移除 `/mhnone`；让 `/mhhelp` 区分玩家／管理员，并新增 `/trash` 别名。 |
| **更多本地化消息** | 每种语言的翻译资源从 446 个消息键扩展至 683 个。 |

VexAC 内置的检查涵盖 Fly、Speed、Timer、Phase、Step、NoSlow、GroundSpoof、Reach、KillAura、AimAssist、穿墙攻击、BadPackets、AutoClick 点击时间模式、修改击退、Scaffold、Tower、FastPlace、Nuker 和方块交互距离。界面使用“仅监测”的标签，但已编译代码也包含踢出玩家的路径；在依赖该标签之前，应先在测试服务器上确认实际管理行为。较早的构建则包含旧版 Anti AutoClick 和 Anti Fly 控制。

## 使用 `/mhgui` 的完整设置与操作指南

### 1. 安装合并构建

1. 完全停止 **Paper 1.21.11 / Java 21** 服务器，并备份世界和插件数据。
2. 只将本次发布的 `VexLandManhunt-2.0.0.jar` 放入 `plugins/`。把旧 Manhunt 和独立 GrimAC JAR 移出启用中的插件目录。保留它们的数据文件夹，不要删除。玩家无需在客户端安装此 JAR。
3. 正常启动，不要使用 `/reload`。集成加载器负责管理 Grim 和 PacketEvents 的生命周期。
4. 以 OP 身份或拥有 `vexland.admin` 权限运行 `/vexintegration`。确认 `Grim=ACTIVE` 和 `PacketEvents=true` 后，再进入 `/mhgui`。保护未启用意味着启动有问题，并不代表集成安装成功。

Grim 配置位于 `plugins/VexLandManhunt/grim/`（`config.yml`、`messages.yml`、`punishments.yml`、`discord.yml`），可选历史记录使用 `violations.sqlite`。首次迁移的备份存放在 `plugins/VexLandManhunt-integration-backups/`；`plugins/VexLandManhunt/integration-migration-v1.txt` 标记迁移完成。如果旧 Grim 数据和集成 Grim 数据同时存在，则保留集成目标并记录警告。迁移拒绝符号链接。

在 `plugins/VexLandManhunt/integration.properties` 中检查移动纠正归属，保留其他设置。全新安装的默认值：

```properties
movement-correction-owner=legacy
```

下方完整的公开菜单指南遵循此包的 1.9.11 玩法基础。旁观者分支有独立的归档指南。

### 2. 打开控制中心

使用拥有 **OP** 或 **`vexland.admin`** 权限的管理员身份进入服务器，并输入：

```text
/mhgui
```

以下说明涵盖插件版本 **2.0.0** 的公开界面，并使用其英文按钮名称。按钮标签会随所选服务器语言变化。要使用全部 GUI 功能，请使用可信的 **OP** 账号：描述文件中的权限允许执行打开菜单的命令，但部分提供的 GUI 处理程序会实施更严格的 OP 检查。主物品栏共有五行，每行九格。将鼠标悬停在按钮上，可以阅读说明和当前设置。大多数按钮使用普通点击；特殊鼠标操作和确认步骤在下文说明。较小的 1.6.4 菜单在本节末尾介绍。

#### 设置你的第一场比赛

1. 打开 **Player Roles（玩家角色）**。点击每位参赛者的玩家头像，直到显示的角色正确。2.0.0 中角色在 **Runner（逃亡者）** 与 **Hunter（猎人）** 之间循环；尚未分配角色的参赛者第一次点击后会成为逃亡者。左键／右键／Shift 点击并不是分别选择角色的快捷操作。需要时使用 **Previous Page（上一页）**、**Next Page（下一页）** 和 **Back to Control Center（返回控制中心）**。
2. 至少分配一名逃亡者和一名猎人。开始流程可以把其余尚未分配角色的在线玩家转为猎人，因此明确分配每位参赛者有助于清楚划分队伍。
3. 点击 **Friendly Fire（友军伤害）**，选择队友是否可以互相造成伤害。点击后检查 ON/OFF 指示。
4. 点击 **Language（语言）**，选择全服务器使用的语言。此设置影响所有人的消息、界面、通知和指南书，而不仅是你自己的玩家。
5. 检查 **Smart Hunter Kit（智能猎人装备包）**、**Auto World Spawn（自动世界出生点）** 和 **Anti-Cheat（反作弊）**。需要游戏内说明时，可通过书本按钮阅读管理员指南。
6. 确认 **Server Freeze（服务器冻结）** 已关闭，然后点击 **Start Match（开始比赛）**。开始流程会准备玩家和物品栏，播放介绍与随机的猎人等待轮盘，然后开始追逐。开始前，请将需要保留的物品放在参赛者物品栏之外。

#### 控制中心主按钮

下方位置按从上到下的行、从左到右的列计算，描述的是 2.0.0 完成装饰后的布局。

| 位置 | 英文按钮 | 功能 |
|---|---|---|
| 第 2 行，第 2 列 | Player Roles | 打开分页的逃亡者／猎人玩家头像菜单。 |
| 第 2 行，第 3 列 | Target Player | 循环选择其他在线玩家，供针对所选目标的管理操作使用。请检查当前目标名称。 |
| 第 2 行，第 4 列 | Friendly Fire | 切换队友之间是否可造成伤害。 |
| 第 2 行，第 5 列 | Match Info | 发送比赛状态、队伍、友军伤害和所选目标的简要报告。 |
| 第 2 行，第 6 列 | Start Match | 执行正常的比赛开始和随机领先时间流程。 |
| 第 2 行，第 7 列 | Full Heal | 为所有在线玩家恢复生命值。 |
| 第 2 行，第 8 列 | Reset Match | 执行完整比赛重置。与 Reset Settings 不同。 |
| 第 3 行，第 2 列 | Full Hunger | 为所有在线玩家恢复饥饿值和饱和度。 |
| 第 3 行，第 3 列 | Release Hunters | 在领先时间结束前释放等待中的猎人。 |
| 第 3 行，第 4 列 | Clear Effects | 移除所有在线玩家的药水效果。 |
| 第 3 行，第 5 列 | Server Freeze | 切换全局服务器冻结；普通非 OP 玩家会被冻结。 |
| 第 3 行，第 6 列 | Clear Target Inventory | 确认后清空所选玩家的物品栏、盔甲和副手。 |
| 第 3 行，第 7 列 | Teleport Everyone | 将所有在线玩家传送到你当前的位置。 |
| 第 3 行，第 8 列 | Kill Target | 确认后杀死所选玩家；正常死亡规则可能影响比赛。 |
| 第 4 行，第 2 列 | Anti-Cheat | 打开 VexAC Security 控制。 |
| 第 4 行，第 3 列 | Freeze Target | 切换所选玩家的单独冻结。 |
| 第 4 行，第 4 列 | Emergency Restore | 为所有在线玩家恢复生命、饥饿值和饱和度。 |
| 第 4 行，第 5 列 | Freeze Team | 左键切换逃亡者；右键切换猎人；Shift 点击解除单独／队伍冻结。 |
| 第 4 行，第 6 列 | Set Day | 将你当前世界的时间设为白天。 |
| 第 4 行，第 7 列 | Clear Weather | 停止你当前世界的降雨与雷暴。 |
| 第 4 行，第 8 列 | Language | 打开全局语言选择器。 |
| 第 5 行，第 2 列 | Smart Hunter Kit | 切换自适应猎人重生装备包；显示 ON/OFF。 |
| 第 5 行，第 3 列 | Clear Dropped Items | 移除你当前世界中的掉落物实体。 |
| 第 5 行，第 4 列 | Pause Match / Resume Match | 停止或恢复正在进行的游戏与比赛计时器。 |
| 第 5 行，第 5 列 | Emergency Sync | 重新同步玩家角色、追踪器和相关运行时状态。 |
| 第 5 行，第 6 列 | Reset Settings | 经两次点击确认后恢复平衡设置。 |
| 第 5 行，第 7 列 | Close | 关闭控制中心。 |
| 第 5 行，第 8 列 | Auto World Spawn | 打开自动主世界出生点间隔选择器。 |
| 第 5 行，第 9 列 | Manhunt Administrator Guide | 提供本地化的管理员指南书。 |

装饰玻璃以及标题／状态物品不是游戏操作按钮。

#### 角色与所选目标

**Player Roles（玩家角色）** 更改参赛者实际所属的 Manhunt 队伍。点击玩家头像，并查看更新后的角色。在 STARTING/RUNNING 期间，界面允许更改逃亡者／猎人角色，但拒绝将最后一名逃亡者转为猎人。这样可以保留当前比赛的逃亡者阵营。请有意识地更改角色，因为更改后会同步队伍运行时状态与追踪器。

**Target Player（目标玩家）** 是独立功能：选择某位玩家，用于 Freeze Target、Clear Target Inventory 或 Kill Target 等操作，而不更改其队伍。循环选择，直到显示想要操作的在线玩家名称。若保存的目标变得不可用，代码可能回退到第一位其他在线玩家，因此每次执行目标操作前，都要立即确认名称。如果没有其他玩家在线，会报告没有可用目标。

**Clear Target Inventory（清空目标物品栏）** 和 **Kill Target（杀死目标）** 要求在**五秒**内，对同一目标点击同一操作两次。第一次点击启动确认并指明目标；第二次点击执行操作。更换目标或等待太久都需要重新确认。清空物品栏会删除其中的内容；杀死逃亡者可能按照正常死亡规则结束或改变比赛。

**Freeze Team（冻结队伍）** 是此菜单中唯一具有队伍专属鼠标快捷操作的功能：普通左键选择逃亡者队伍，普通右键选择猎人队伍，Shift 点击则解除该工具管理的全部单独／队伍冻结。全局 Server Freeze 开关是另一个独立控制；若玩家仍被冻结，应单独将其关闭。

#### Smart Hunter Kit（智能猎人装备包）

点击 **Smart Hunter Kit** 开启或关闭自适应猎人重生装备包。按钮显示当前状态。开启时，重生的猎人可以获得根据逃亡者装备和比赛情况调整的装备包；内置玩家指南将其描述为弱于逃亡者平均装备水平。关闭时，猎人死亡后不会自动获得装备包。这不会关闭追踪指南针。

若要直接设置而不是切换状态，可以使用 `/mhkit on`、`/mhkit off` 或 `/mhkit status`。检查到的全新配置回退值为开启。

#### Auto World Spawn（自动世界出生点）

点击 **Auto World Spawn**，然后选择 **OFF（关闭）**、**5 minutes（5 分钟）**、**10 minutes（10 分钟）**、**15 minutes（15 分钟）**、**20 minutes（20 分钟）** 或 **30 minutes（30 分钟）**。选择一个选项后会保存并返回 `/mhgui`；**Back（返回）** 则不选择新间隔，直接返回。

启用后，系统定期在活动的主世界逃亡者附近寻找安全的主世界地表，并将世界出生点移到那里。若没有逃亡者位于主世界，或找不到安全候选位置，就会跳过移动。全新配置的回退值为关闭。使用命令进行相同控制时，可输入 `/mhspawn off`、`/mhspawn 15` 或 `/mhspawn status`，并用任何支持的间隔替代 15。

#### 暂停、重新连接与恢复

比赛处于 RUNNING 时可使用 **Pause Match（暂停比赛）**。它会冻结游戏系统、移动／交互、比赛计时器、追踪和出生点移动。**Resume Match（恢复比赛）** 恢复这些系统，并补偿暂停时间。Server Freeze 只冻结玩家；需要暂停比赛计时器时，不应把它当作替代功能。

逃亡者重新连接时限可以配置，全新配置的回退值为 **15 分钟**。及时重新加入会恢复逃亡者状态，并提供十秒的重新加入保护。服务器停机不会消耗已保存的重新连接时间。超时的逃亡者位置会转为猎人；最后一名逃亡者超时可能使猎人获胜。

**提供的 2.0.0 GUI 中没有独立的重新连接时长选择器。** 若要自定义，请停止服务器，编辑 `plugins/VexLandManhunt/config.yml`，保留其他设置，并设置：

```yaml
features:
  custom-reconnect-minutes: 15
```

编辑后重启。小于一分钟的值会被限制为一分钟。**Reset Settings（重置设置）** 会将此值恢复为 15 分钟。已编译构建还会保存比赛／重新连接状态与备份快照，以便在服务器重启／崩溃后恢复；请让插件管理这些文件，而不要在游戏期间编辑它们。

#### Reset Settings（重置设置）与 Reset Match（重置比赛）

**Reset Settings** 要求在**八秒**内点击按钮两次。第一次点击启动确认；第二次恢复 **Smart Kit 开启**、**每 15 分钟自动移动出生点**、**15 分钟重新连接时限** 和**随机领先时间**。这与全新安装不同，后者的 Auto World Spawn 回退值为关闭。此操作更改配置，并不代替完整比赛重置。

**Reset Match** 执行已有的比赛重置，清除临时比赛状态／物品，并将玩家送回主世界出生点，准备下一轮。其主按钮不使用 Reset Settings 的两次点击确认。**Start Match** 可能会准备／清空参赛者物品栏。点击前，请确认你打算使用哪个重置／开始控制。

#### 语言与反作弊控制

**Language（语言）** 打开全局选择器。点击你想要的语言名称。两个提供的构建都包含英语、波斯语、阿拉伯语、西班牙语、法语、德语、俄语、简体中文、印地语和葡萄牙语。所选语言由全服务器共享，并会持久保存。日语 README 文档不会向插件的游戏内选择器添加日语。

**Anti-Cheat（反作弊）** 打开 **VexAC Security**。点击 **VexAC Master** 启用／禁用内部引擎，或点击 **Movement**、**Combat**、**AutoClick**、**Velocity / AntiKB** 或 **World / Scaffold** 切换对应分组。**Anti X-Ray** 切换 Paper 已配置的 Anti-Xray；重启服务器后才能应用此更改。状态、证据日志和检测模型方块会说明当前系统。**Back to Control Center（返回控制中心）** 返回主菜单。

构建的界面将管理行为描述为仅监测，但静态检查发现仍保留了基于阈值的踢出路径。请将菜单中“不踢出玩家”的表述视为实现与文档之间的差异，并在受控服务器上确认管理行为后再依赖它。

#### 集成 GrimAC 与旧 VexAC

现有 **VexAC Security** GUI 控制旧 VexAC 引擎，其 Master/分组按钮并非新的 Grim 控制面板。集成 GrimAC 与它并行运行。使用 `/vexintegration` 查看模块状态，使用原生 `/grim` 或 `/grimac` 访问 Grim 自身的命令和受权限控制的工具。Grim 设置和处罚规则位于 `plugins/VexLandManhunt/grim/`。

1.13.1 的 GrimBridge monitor/分组菜单和 `grim-settings.yml` 不适用于此包。不要假设关闭 VexAC 也会禁用集成 GrimAC，也不要把 monitor 标签视为不踢出玩家的政策保证。Paper Anti-Xray 仍是独立设置，修改后需要重启。

#### 游戏内指南与故障排查

点击 **Manhunt Administrator Guide（Manhunt 管理员指南）**，或使用 `/mhhelp` 获取本地化指南书。2.0.0 中，玩家可以用 `/mhhelp` 获取与其角色对应的指南。猎人右键点击指南针来选择逃亡者；此追踪器界面与管理员的 Target Player 选择器是独立的。

若角色或追踪器似乎不同步，**Emergency Sync（紧急同步）** 会刷新相关运行时状态。**Match Info（比赛信息）** 有助于检查当前队伍与状态。如果请求开始比赛失败，请检查比赛是否准备就绪、服务器冻结是否关闭，以及逃亡者／猎人队伍是否存在。更换 JAR 后，应完整重启服务器，而不是使用 `/reload`。`/mhdebug` 是 2.0.0 包含的管理员诊断命令；它的存在并不表示这些版本已通过真实服务器测试。

#### 使用较早的 1.6.4 控制中心

1.6.4 保留了 **Player Roles**、**Friendly Fire**、**Start Match**、**Reset Match**、**Release Hunters Now**、**Server Lock**、**Teleport Everyone To Me**、**Heal & Feed Everyone**、**Match Status**、语言选择、**Anti Cheat** 以及管理员指南。角色按 **None → Runner → Hunter** 循环，比赛正在开始／进行时禁止更改角色。

其反作弊菜单包含旧版 **Anti AutoClick**（30-CPS 规则，并提供警告／踢出处理）、**Anti Fly** 和 Paper **Anti X-Ray**。逃亡者重新连接时限固定为 **60 分钟**。上文介绍的新 Smart Hunter Kit V3 开关、Auto World Spawn 选择器、暂停／恢复、Reset Settings 确认，以及扩展的所选目标／世界工具都属于 2.0.0，不应期待它们出现在旧菜单里。

本指南根据提供的 JAR 元数据、内置语言／帮助文本和静态反汇编得出。本次检查没有在真实 Minecraft 服务器上运行界面。

### 3. 开始追逐

逃亡者在随机领先时间内逃离，并朝击败末影龙的目标推进。猎人等待释放，然后右键点击追踪指南针来选择一名逃亡者。游戏中可以更换目标，包括追逐跨越维度时。使用 `/teammsg <message>` 仅向自己的队伍发言，并在 2.0.0 中使用 `/mhhelp` 获取本地化角色指南。

若一名逃亡者死亡，其余逃亡者继续游戏，死亡玩家则成为猎人。猎人可以重生并继续追踪。最后一名逃亡者死亡，或逃亡者断线时限到期，可能使比赛以猎人获胜结束；击败末影龙则让逃亡者获胜。

### 4. 暂停、结束并准备下一场比赛

2.0.0 中，通过 `/mhpause` 暂停，并用 `/mhresume` 继续。若要在领先时间倒计时结束前释放猎人，请使用 `/mhrelease`。开始新比赛时，使用控制中心的完整重置或 `/mhreset`；重置会清除临时比赛状态和物品，并把玩家送回主世界出生点。更改 Paper Anti-Xray 设置需要重启。

## 合并 2.0.0 包的默认设置

检查到的全新配置回退值如下：

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` 表示关闭自动出生点移动。GUI 中经确认的设置重置操作则会将出生点间隔设为 15 分钟。使用 GUI，或 `/mhkit` 和 `/mhspawn` 管理相应设置。

## 公开命令参考 — 合并 2.0.0

管理员命令要求 OP 或 `vexland.admin`（默认为 OP）。团队聊天、垃圾箱和夜视是玩家实用工具；`/mhhelp` 提供与角色相符的指南。表中列出 17 个 Manhunt/集成命令；原生 Grim 命令具有各自的权限。此处未注册 `/mhnone`。

| 命令 | 用途 |
| --- | --- |
| `/vexintegration` | 报告集成 Grim、VexAC、PacketEvents 和共享 Bukkit 所有者的状态 |
| `/mhgui` | 打开控制中心 |
| `/mhstart` | 执行完整的比赛开始流程 |
| `/mhreset` | 完整重置当前比赛 |
| `/mhrelease` | 提前释放猎人 |
| `/mrunner <player>` | 分配逃亡者 |
| `/mhunter <player>` | 分配猎人 |
| `/teammsg <message>` | 向队友发送私密消息 |
| `/trash` | 打开 54 格临时垃圾物品栏 |
| `/nv` | 切换个人夜视 |
| `/mhlang` | 打开全局语言选择器 |
| `/mhhelp` | 获取本地化指南书 |
| `/mhkit <on\|off\|toggle\|status>` | 配置智能猎人装备包 |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | 配置自动出生点移动 |
| `/mhpause` | 暂停进行中的比赛 |
| `/mhresume` | 恢复已暂停的比赛 |
| `/mhdebug` | 运行内部诊断 |

## 游戏内语言与文档

此包保留 **10 种游戏语言**：英语、波斯语、阿拉伯语、西班牙语、法语、德语、俄语、简体中文、印地语和葡萄牙语。每份随包翻译均沿用 1.9.11，包含 **683 个键**。`/mhlang` 设置整个服务器共用的一种语言，保存于 `language.txt`。

项目文档提供 **18 种语言**，不包含阿拉伯语文档版。这些翻译不会为未修改的二进制文件添加日语或其他额外的游戏内语言。

## 版本历史、源码与致谢

[CHANGELOG.md](../CHANGELOG.md) 记录每个提供的版本。完整的 [1.13.1 旁观者指南](archive/1.13.1/README.zh-CN.md) 和[较旧的 1.9.11 / 1.6.4 指南](archive/1.9.11/README.zh-CN.md) 仍然可用。每个提供的版本保留各自的下载和校验和。

**Manhunt 由 Bardiya / Farland_game 和 Ali / Alivexor 共同创作。GrimAC 是 GrimAC / DefineOutside 及贡献者开发的独立项目。** 此集成产物修改了三个 Grim 类，并非较早双文件版本中未经修改的官方 Grim 二进制文件。随附的[源码包](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0-source.zip) 保留提供的源码、构建脚本、依赖输入和声明，省略测试/运行时证据，源码保持不变。发布内容还包括 GPLv3 文本、校验和及[第三方声明](../THIRD_PARTY_NOTICES.md)。此次发布过程中未进行实机服务器测试或可复现构建测试。

## 给 Dream 的玩笑挑战

来自 Bardiya 的一点 Minecraft 玩笑 😄

> “唉……Ali 和我做了一个比 Dream 的好一百倍的 Manhunt 插件，可 Dream 害怕了，不肯来玩我们的！”

## 创建者与项目范围

**由 [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) 与 [Ali · Alivexor](https://github.com/Alivexor) 共同开发。** 两个账号也作为作者记录在原始插件描述文件中。

本仓库将原始编译版本、文档和版本说明作为共同作品集项目展示。功能描述基于对提供的 JAR 的静态检查。在此次发布工作流程中，尚未测试真实服务器兼容性、恢复性能、平衡性或反作弊准确性。

[Bardiya 的 GitHub 作品集](https://github.com/FarlandGame) · [Ali 的 GitHub](https://github.com/Alivexor) · [所有发布版本](https://github.com/FarlandGame/Vexland_Manhunt/releases)
