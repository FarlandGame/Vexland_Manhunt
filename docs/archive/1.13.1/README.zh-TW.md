# Vexland_Manhunt — 1.13.1

> 舊版本封存指南 · [2.0.0 →](../../README.zh-TW.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**完整的 Minecraft 逃亡者對抗獵人體驗，由 [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) 與 [Ali · Alivexor](https://github.com/Alivexor) 共同開發。**

Vexland_Manhunt 將比賽設定、隊伍角色、開場追逐、追蹤、進度、獎勵、結果與管理功能整合進一個 Paper 伺服器外掛。逃亡者試圖擊敗終界龍，獵人則試圖消滅最後一名逃亡者。外掛支援多名逃亡者，並在死亡、重生、切換維度和重新連線後繼續維持追逐。管理員可以透過 `/mhgui` 控制中心的選單管理比賽，玩家則可以使用本地化訊息與指南書。

## 下載與相容性

| 檔案 / 版本 | 下載 | 用途 |
|---|---|---|
| **1.13.1 — 目前版本** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Bardiya 和 Ali 開發的 Manhunt 外掛 |
| **GrimAC 2.3.73 — 必需** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | 獨立的第三方反作弊依賴 |
| 1.9.11 — 已封存 | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | 上一個 Manhunt 建置版本 |
| 1.6.4 — 已封存 | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | 更早的 Manhunt 建置版本 |

**目標環境：Paper 1.21.11、Java 21。** 1.6.4、1.9.11 和 1.13.1 是外掛的發佈版本號，不是支援的 Minecraft 版本號。在 1.13.1 中，GrimAC 是強制依賴，橋接層需要 2.3.73 API。請下載**兩個目前版本的 JAR**。它們是伺服器外掛，玩家無需將其安裝到用戶端的 mods 資料夾。

這些是原始的個人伺服器建置，保留了創作者專屬的進階管理權限，內容與提供時完全一致。本手冊介紹公開的 Manhunt 控制功能。

## Manhunt 體驗

- **逃亡者與獵人隊伍：**將線上玩家分配到任一陣營。比賽至少需要一名逃亡者，以及一名獵人或一名尚未分配角色的線上玩家。隊友死亡後，存活的逃亡者仍會繼續比賽；死亡的逃亡者會成為獵人，除非這次死亡使比賽結束。
- **電影式比賽開場：**準備物品欄和遊戲模式，介紹隊伍，並透過輪盤隨機決定逃亡者的領先時間。獵人在倒計時期間被凍結，並收到標題與聲音提示。領先時間是隨機的；管理員可以提前釋放獵人。
- **可選擇目標的追蹤指南針：**獵人獲得一枚特殊指南針。右鍵點擊它，在目標選單中選擇一名逃亡者，並在追逐期間更換目標。跨維度時，追蹤會沿相關傳送門路線進行，直到可以直接追蹤目標。獵人重生後會再次獲得追蹤器。
- **進度顯示：**Boss 欄和比賽資訊根據逃亡者裝備，以及地獄資源、烈焰桿、終界珍珠、終界之眼、要塞和終界等進程更新。新建置版本增加了更細緻的階段，以及隨終界龍生命值變化的進度顯示。
- **逃亡者擊殺獎勵：**在進行中的比賽裡，逃亡者擊殺獵人時，系統會使用一個隨進度變化、包含 50 個條目的加權獎勵池。包含抽獎動畫、雙重／三重獎勵、連殺公告和稀有物品慶祝效果。
- **勝利與結果：**最後一名逃亡者死亡，獵人獲勝；擊敗終界龍，逃亡者獲勝。包含比賽結束標題、慶祝效果、擊殺／死亡資訊以及臨時物品清理。新建置版本還報告 MVP、傷害和移動距離結果。
- **隊伍交流與實用功能：**透過 `/teammsg` 私下向隊友發訊息，使用 `/trash` 打開 54 格臨時垃圾物品欄，以及透過 `/nv` 切換個人夜視。
- **透過選單管理：**控制中心提供角色分配、開始／重置、提前釋放獵人、友軍傷害、伺服器鎖定、全員傳送、治療／補充飢餓、語言、保護設定、狀態和指南書。凍結和完整重置有助於準備下一場比賽。
- **本地化指南：**逃亡者、獵人和管理員指南書解釋目標、追蹤器用法、死亡、設定與命令。1.9.11 版本透過 `/mhhelp` 向玩家提供與其角色對應的指南。
- **Paper Anti-Xray 整合：**選單控制 Paper 的世界級保護；更改需要重啟伺服器才會生效。

## 1.13.1 有哪些新內容？

與提供的 1.9.11 建置相比：

- **幽靈旁觀者：** 獨立角色，由管理員分配；提供受保護的飛行、對其他玩家隱藏、狀態保存與恢復，以及分頁的參賽者傳送選單。
- **重新設計的控制中心：** 分類選單、明確的四種角色選擇、按名稱選擇目標、重新連線時長選擇器、Classic/Fast/Hardcore/Custom 預設，以及獨立的 30 秒確認介面。
- **GrimAC 整合：** 必需的 GrimAC 2.3.73 替代了原先啟用的 VexAC 啟動路徑。GUI 提供總開關、五個檢測組、提醒及監控/執行模式控制。Paper Anti-Xray 仍然獨立執行。
- **新的 Smart Hunter Kit 規劃器：** 根據 Runner 的裝備和附魔、最近的 Runner、隊伍人數、距離、維度及地形調整裝備與補給。保留已有的更強裝備，避免重複工具，並透過 30 秒歷史記錄限制消耗品補充。這不保證固定的裝備差距，也不代表經過實測的平衡性。
- **經校驗的恢復：** 使用 SHA-256 封存快照、檢查資料結構和狀態，並在需要時回退到有效備份；無效或格式更新的快照會保留，不會被覆蓋。旁觀者狀態單獨持久化保存。
- **更多訊息：** 每份內建翻譯的訊息鍵從 683 個增加到 762 個，遊戲內語言仍為相同的十種。新增兩個公開註冊命令：`/mspectator <player>` 和 `/mhspectate`。
- **重置後備行為：** 如果主世界出生點附近找不到安全地面，重置可以跳過該次傳送，而不強行傳送。

## 使用 `/mhgui` 完整設定與操作

停止伺服器，並備份世界及外掛資料。將兩個目前版本的 JAR 放入 `plugins/`，該目錄中只保留一個 Manhunt JAR 和一個 GrimAC JAR。升級時保留現有的 `plugins/VexLandManhunt/` 設定與資料。完整啟動 Paper 1.21.11 / Java 21 伺服器；替換建置版本後應完全重啟。GrimAC 必須成功載入。外掛的內部名稱仍為 `VexLandManhunt`。

本指南介紹外掛 **1.13.1**，並使用英文介面標簽。實際標簽遵循伺服器的全局語言。位置按從上到下數行、從左到右數列。除非另有說明，否則使用普通左鍵點擊。本指南基于靜態檢查，未執行 Minecraft 伺服器。

### 設定一場比賽

1. 使用具有 `vexland.admin` 權限的賬號執行 `/mhgui`（預設：OP）。
2. 打開 **Player Roles**，點擊帶玩家名稱的圖標，然後選擇 **Runner**、**Hunter**、**Spectator** 或 **No Team**。這會打開明確的角色選擇器；點擊玩家不會循環切換角色。
3. 至少分配一名 Runner 和一名 Hunter。比賽開始時，尚未分配角色的在線玩家可能變為 Hunter；旁觀者不能充當任一隊伍所需的成員。
4. 檢查 **Match Settings**、**GrimAC Security** 和 **Global Language**。開始前關閉 Server Freeze。
5. 打開 **Match Controls → Start Match**。系統準備/清空參賽者的物品欄，播放開場介紹，並由輪盤決定 Hunter 的延遲出發時間。

### 主頁：`/mhgui`（五行）

| 位置 | 按鈕 | 操作 |
|---|---|---|
| R2 C2 | Match Controls | 開始、暫停/繼續、放行及重置。 |
| R2 C4 | Player Roles | 打開在線玩家角色列表。 |
| R2 C6 | Match Settings | 友軍傷害、裝備包、出生點、重新連線及預設。 |
| R2 C8 | Player Management | 選擇目標並使用玩家/世界工具。 |
| R4 C2 | GrimAC Security | 打開保護設定。 |
| R4 C4 | Global Language | 選擇所有人使用的語言。 |
| R4 C6 | Administrator Guide | 將本地化管理員指南書加入物品欄。 |
| R5 C5 | Close | 關閉選單。 |

R1 C5 的信標顯示比賽狀態及 Runner/Hunter 人數。

### Match Controls（五行）

| 位置 | 按鈕 | 操作 |
|---|---|---|
| R2 C2 | Start Match | 開始完整流程。 |
| R2 C4 | Pause Match / Resume Match | 暫停或繼續遊戲及比賽計時；適用于 RUNNING 狀態的比賽。 |
| R2 C6 | Release Hunters | 提前結束目前 Hunter 等待時間。 |
| R2 C8 | Reset Match | 打開確認介面，然後完全重置比賽。 |
| R4 C2 | Server Freeze | 切換對全服非 OP 玩家的凍結。 |
| R4 C4 | Teleport Everyone | 打開確認介面，然後將所有在線玩家傳送到你身邊。 |
| R4 C6 | Match Info | 發送比賽和隊伍報告。 |

**Back** 位于 R5 C1；**Close** 位于 R5 C9。Server Freeze 與 Pause Match 相互獨立：需要同時停止計時和遊戲系統時，請使用 Pause。

### Player Roles

六行的玩家列表在前五行最多顯示 45 個帶名稱的角色圖標，按玩家名稱排序。Runner 使用淺綠色混凝土，Hunter 使用紅色混凝土，Spectator 使用終界之眼，No Team 使用灰色混凝土。底行 C1 是 **Previous Page**，C3 顯示頁碼/在線資訊，C5 是 **Back to Control Center**，C9 是 **Next Page**。

點擊玩家可打開 **Choose Player Role**（三行）：

| 位置 | 指定角色 |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

玩家名稱/目前角色顯示在 R1 C5；**Back** 位于 R3 C1，**Close** 位于 R3 C9。比賽期間可以更改角色。在 RUNNING 狀態下，將最後一名已分配的 Runner 改為其他角色，會打開 **Last Runner: the match will end** 確認介面。確認後可能判定 Hunter 獲勝。直接角色命令會立即生效，請謹慎使用。這里可以分配 No Team；在正在進行的比賽中，正常的開始/加入同步可能將未分配角色的玩家變為 Hunter。

### 旁觀者

管理員使用 `/mspectator <player>` 或在 Player Roles 中選擇 **Spectator** 來分配角色。雖然命令描述檔案沒有權限行，處理器仍檢查管理員權限。玩家執行 `/mhspectate` 不會自行加入旁觀者。

旁觀者會在快捷列第一格收到 **Spectator teleport** 指南針。主手持有它並右鍵點擊，或使用 `/mhspectate`，即可打開六行傳送選單。此選單僅在玩家具有 Spectator 角色時可用。前五行最多列出 45 名存活且在線的 Runner/Hunter，按名稱排序；點擊帶名稱的角色圖標可傳送到該玩家的目前位置，也支援其他世界。底行 C1 是 **Previous Page**，C5 是 **Close**，C9 是 **Next Page**。沒有合適參賽者時，R3 C5 顯示 **No players available**。關閉選單後仍保持旁觀者角色。

旁觀者可以飛行、對其他玩家隱藏、無碰撞，並受到傷害保護。實現采用帶飛行能力的冒險模式，不提供原版旁觀模式的攝像機功能或穿墻移動。系統阻止攻擊、破壞/放置方塊、普通方塊/實體交互、拾取/丟棄物品、副手交換、物品欄點擊/拖動、操作盔甲架及拾取/獲得經驗。生物無法將其設為目標，饑餓值變化也會被取消。`/teammsg <message>` 會發送給其他 Spectator 角色玩家。請勿向參賽者泄露參與者位置或提供其他場外協助。

退出時，管理員分配 **Runner**、**Hunter** 或 **No Team**，或使用 `/mrunner <player>`、`/mhunter <player>`。沒有專門的自行退出命令/按鈕。退出會恢復保存的物品欄/游標物品、位置、遊戲模式、飛行、碰撞及免傷狀態，再套用新角色的比賽行為。旁觀者狀態會保存以便重新加入。完整 Match Reset 會恢復旁觀者狀態、清除角色，並在存在安全主世界出生點時將在線玩家傳送過去。正常的比賽結束清理不會對旁觀者執行參賽者的物品/飛行處理。

### Match Settings（五行）

| 位置 | 按鈕 | 操作 |
|---|---|---|
| R2 C2 | Friendly Fire | 切換隊友傷害。 |
| R2 C4 | Smart Hunter Kit | 切換自適應 Hunter 重生裝備包。 |
| R2 C6 | Auto World Spawn | 打開間隔選擇器。 |
| R2 C8 | Reconnect Grace | 打開 Runner 重新連線時長選擇器。 |
| R4 C2 | Match Preset | 選擇 Classic、Fast、Hardcore 或 Custom。 |
| R4 C4 | Reset Settings | 確認平衡設定：Kit ON、Spawn 15m、Reconnect 15m。 |
| R4 C6 | Random Head Start | 資訊圖標；延遲仍由輪盤決定。 |

**Back** 位于 R5 C1；**Close** 位于 R5 C9。

三行的 **Reconnect Grace** 選擇器在 R2 C2–C7 依次提供 **1、5、10、15、20、30 分鐘**。點擊後保存數值，並保持選擇器打開。Back 位于 R3 C1；Close 位于 R3 C9。

三行的 **Match Preset** 選擇器在 R2 C2、C4、C6、C8 放置 **Classic**、**Fast**、**Hardcore**、**Custom**。Classic：Kit ON、Spawn 15m、Reconnect 15m。Fast：ON、5m、10m。Hardcore：OFF、OFF、5m。Custom 保留目前手動設定。預設保留隨機延遲出發。選擇後選單保持打開；Back 位于 R3 C1，Close 位于 R3 C9。

**Auto World Spawn** 在 R2 C2、C3、C4 提供 OFF、5m、10m，在 R2 C6、C7、C8 提供 15m、20m、30m。Back 位于 R3 C5。選擇間隔或使用 `/mhspawn <off|5|10|15|20|30|status>`。它會將主世界出生點移動到合適的主世界 Runner 附近；沒有合適目標時可以跳過。`/mhkit <on|off|toggle|status>` 可直接控制裝備包。

### Player Management（六行）

| 位置 | 按鈕 | 作用對象 |
|---|---|---|
| R1 C5 | Target Player | 打開按名稱選擇玩家的介面。 |
| R2 C2 | Full Heal | 所有在線玩家。 |
| R2 C4 | Full Hunger | 所有在線玩家。 |
| R2 C6 | Clear Effects | 所有在線玩家。 |
| R2 C8 | Freeze Target | 選中的玩家。 |
| R4 C2 | Clear Target Inventory | 選中的玩家；需要確認。 |
| R4 C4 | Kill Target | 選中的玩家；需要確認，並適用正常比賽結果規則。 |
| R4 C6 | Set Day | 你目前所在的世界。 |
| R4 C8 | Clear Weather | 你目前所在的世界。 |
| R5 C2 | Clear Dropped Items | 你目前所在的世界；需要確認。 |
| R5 C4 | Emergency Sync | 刷新在線玩家的角色/執行時系統。 |
| R5 C6 | Freeze Team | 左鍵：Runner；右鍵：Hunter；Shift 點擊：清除這些隊伍/個人凍結。 |

Back 位于 R6 C1；Close 位于 R6 C9。選擇目標不會更改角色。選擇器每頁顯示另外 28 名在線玩家，位于第 2–5 行、第 2–8 列；點擊名稱即可選擇並返回。Previous/Back/Next 分別位于 R6 C1/C5/C9。執行操作前再次核對顯示的目標。

### 確認介面

Reset Match、Teleport Everyone、Reset Settings、Clear Target Inventory、Kill Target、Clear Dropped Items，以及 GUI 中最後一名 Runner 的角色更改，均使用獨立的三行 **Confirm Action** 介面。查看 R1 C5 的操作/目標，然後點擊 R2 C3 的綠色 **Confirm** 或 R2 C7 的紅色 **Cancel**。確認在 **30 秒**後過期。目標發生變化/離線，或角色變化時，需要重新選擇。這些新選單路徑取代舊指南中五/八秒內重複點擊的說明。

### GrimAC Security 與語言

六行 Grim 選單在 R1 C5 顯示狀態；開關位于 R2 C2 **GrimAC Master**、C4 **Movement**、C6 **Combat**、C8 **Packets**；R4 C2 **Velocity / AntiKB**、C4 **World / Scaffold**、C6 **Anti X-Ray**、C8 **Admin Alerts**；以及 R5 C5 **Monitor mode**。Back 位于 R6 C1，Close 位于 R6 C9。Monitor mode 控制提醒/證據與執行模式之間的切換。Paper Anti-Xray 獨立執行，更改後需要重啟。這些是 GrimAC 控制；舊版 VexAC/AutoClick 選單說明不適用于本版本。

Global Language 對所有人有效，並刷新選單/物品。點擊帶名稱的語言；Back 位于 R3 C5。`/mhlang` 打開同一選擇器，`/mhhelp` 提供本地化玩家/管理員指南。

### 目前預設值、重新連線與管理處罰

`plugins/VexLandManhunt/config.yml` 中新配置的後備預設值為：

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` 表示自動移動出生點已關閉。Reset Settings 和 Classic 則會選擇 15 分鐘。在 Runner 的重新連線時限內，其名額會保留；及時返回可獲得十秒保護。已保存的伺服器停機時間不計入。超時可能使 Runner 變為 Hunter，或結束比賽並判定 Hunter 獲勝。Pause/Resume 凍結遊戲系統並調整有效比賽計時。恢復檔案由外掛管理。

Grim 橋接設定保存在 `plugins/VexLandManhunt/grim-settings.yml`。新配置預設 Master ON、五個組全部 ON、Admin Alerts ON，以及 **Monitor mode OFF：已啟用執行模式**。監控模式將證據/提醒加入佇列，並取消符合條件的標記。在執行模式下，橋接層可將 Grim 踢出命令轉換為允許重新連線的本地化中斷連線；這並不建立永久封禁策略。實際閾值也取決于 Grim 配置。證據排隊寫入 `plugins/VexLandManhunt/anticheat/grim-evidence.log`；有上限的佇列在高負載下可能丟棄項目。橋接層豁免旁觀者、暫停/凍結的遊戲狀態及某些載具場景，並在加入、傳送和重生後給予三秒寬限期。不宣稱任何反作弊準確率或性能基準。

## 公開命令參考 — 1.13.1

管理員權限指 OP 或 `vexland.admin`（預設 OP）。`/mspectator <player>` 處理器即使沒有描述檔案權限行，也會檢查該權限。直接角色命令立即生效；在 RUNNING 狀態下更改最後一名 Runner 的角色可能結束比賽。GUI 會為該情況提供確認。

| 命令 | 用途 | 權限 |
|---|---|---|
| `/mhgui` | 打開分類控制中心 | 管理員 |
| `/mhstart` | 開始完整比賽流程 | 管理員 |
| `/mhreset` | 完全重置比賽 | 管理員 |
| `/mhrelease` | 放行等待中的 Hunter | 管理員 |
| `/mrunner <player>` | 分配 Runner | 管理員 |
| `/mhunter <player>` | 分配 Hunter | 管理員 |
| `/mspectator <player>` | 分配 Spectator | 管理員；新增 |
| `/mhspectate` | 打開參賽者傳送選單 | 目前為 Spectator；新增 |
| `/teammsg <message>` | 發送給相同角色/隊伍 | 玩家 |
| `/trash` | 一次性 54 格垃圾物品欄；別名 `/mhtrash`、`/vextrash` | 玩家 |
| `/nv` | 切換個人夜視 | 玩家 |
| `/mhlang` | 打開全局語言選擇器 | 管理員 |
| `/mhkit <on\|off\|toggle\|status>` | 配置自適應 Hunter 裝備包 | 管理員 |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | 配置出生點移動 | 管理員 |
| `/mhhelp` | 獲取本地化角色/管理員指南 | 玩家 / 管理員 |
| `/mhpause` | 暫停進行中的比賽 | 管理員 |
| `/mhresume` | 繼續暫停的比賽 | 管理員 |
| `/mhdebug` | 內部診斷 | 管理員 |

本版本未註冊 `/mhnone`；請使用 GUI 的 No Team 角色。Hunter 右鍵點擊追蹤指南針來選擇 Runner；這與旁觀者傳送及管理員目標選擇器各自獨立。Runner 透過擊敗終界龍獲勝；沒有 Runner 剩余時 Hunter 獲勝。若仍有其他 Runner，死亡的 Runner 會變為 Hunter。

## 語言、歷史與第三方鳴謝

原外掛提供 **10 種遊戲內語言**：英語、波斯語、阿拉伯語、西班牙語、法語、德語、俄語、簡體中文、印地語和葡萄牙語。`/mhlang` 為整個伺服器選擇一種語言，並保存到 `language.txt`。GitHub 手冊有 **18 種語言**，不包含阿拉伯語文檔版本。日語及其他額外 README 語言不會為未修改的 JAR 增加遊戲內翻譯。

[版本歷史](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) 記錄每個提供的建置版本。完整的舊版 1.9.11 / 1.6.4 手冊保留在[版本化封存](../1.9.11/README.zh-TW.md)中。專門支援旁觀者的建置現已提供，並作為 1.13.1 發佈；這些功能不應歸屬于舊版下載。

**GrimAC 是 GrimAC 貢獻者開發的獨立項目，以 GPL-3.0 分發。** Bardiya 和 Ali 創建了 Vexland_Manhunt 及其整合；他們不是 GrimAC 的作者。提供的 Grim JAR 與官方 Modrinth 2.3.73 Bukkit 檔案的 SHA-512 和 SHA-1 一致。其內嵌原始碼提交與[上游 v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73)一致。發佈內容包括未修改的二進位檔案、校驗碼、上游原始碼快照、授權條款及[第三方聲明](../../../THIRD_PARTY_NOTICES.md)。這些組件聲明不會為獨立的 Manhunt 項目指定授權條款。

## 給 Dream 的玩笑挑戰

來自 Bardiya 的一點 Minecraft 玩笑 😄

> “唉……Ali 和我做了一個比 Dream 的好一百倍的 Manhunt 外掛，可 Dream 害怕了，不肯來玩我們的！”

## 建立者與專案範圍

**由 [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) 與 [Ali · Alivexor](https://github.com/Alivexor) 共同開發。** 兩個帳號也作為作者記錄在原始外掛描述檔案中。

本儲存庫將原始編譯版本、文件和版本說明作為共同作品集專案展示。功能描述基於對提供的 JAR 的靜態檢查。在此次發布工作流程中，尚未測試真實伺服器相容性、恢復效能、平衡性或反作弊準確性。

[Bardiya 的 GitHub 作品集](https://github.com/FarlandGame) · [Ali 的 GitHub](https://github.com/Alivexor) · [所有發布版本](https://github.com/FarlandGame/Vexland_Manhunt/releases)
