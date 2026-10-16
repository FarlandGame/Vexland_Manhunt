# Vexland_Manhunt

[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**[Bardiya Alizadeh（Kabir）· Farland_game](https://github.com/FarlandGame) と [Ali · Alivexor](https://github.com/Alivexor) が共同制作した、Minecraftのランナー対ハンターを一通り楽しめるプラグインです。**

Vexland_Manhuntは、試合の準備、チームの役割、追跡の開始、トラッキング、進行状況、報酬、結果表示、管理機能を1つのPaperサーバープラグインにまとめています。ランナーはエンダードラゴンの討伐を目指し、ハンターは最後のランナーを倒そうとします。複数のランナーに対応し、死亡、リスポーン、ディメンション間の移動、再接続があっても追跡を続けられるようにしています。管理者は`/mhgui`のコントロールセンターからメニューで試合を操作でき、プレイヤー向けのメッセージやガイドブックも選択した言語で表示されます。

## ダウンロードと互換性

| ファイル / バージョン | ダウンロード | 用途 |
|---|---|---|
| **1.13.1 — 現行版** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Bardiya と Ali が制作した Manhunt プラグイン |
| **GrimAC 2.3.73 — 必須** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | 別途必要なサードパーティ製アンチチート |
| 1.9.11 — アーカイブ版 | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | 以前の Manhunt ビルド |
| 1.6.4 — アーカイブ版 | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | さらに古い Manhunt ビルド |

**対象環境：Paper 1.21.11、Java 21。** 1.6.4、1.9.11、1.13.1 はプラグインのリリース番号であり、対応する Minecraft のバージョン番号ではありません。1.13.1 では GrimAC が必須依存関係となり、連携ブリッジには 2.3.73 API が必要です。**現行版の JAR を両方**ダウンロードしてください。サーバープラグインのため、プレイヤーがクライアントの mods フォルダーに入れる必要はありません。

これらは個人サーバー向けのオリジナルビルドで、制作者固有の高度な管理権限を含め、提供された状態のまま保存されています。本マニュアルでは公開 Manhunt 操作を説明します。

## Manhuntの体験

- **ランナーとハンターのチーム：** オンラインプレイヤーをどちらかのチームに割り当てます。試合には最低1人のランナーと、1人のハンターまたは役割未割り当てのオンラインプレイヤーが必要です。味方が死亡しても生存中のランナーは続行し、死亡したランナーは、その死亡で試合が終了する場合を除いてハンターになります。
- **演出付きの試合開始：** インベントリとゲームモードを準備し、チームを紹介してから、ルーレットでランナーの先行時間を決めます。そのカウントダウン中、ハンターは動けず、画面のタイトルと音で状況が通知されます。先行時間はランダムで、管理者はハンターを早めに解放することもできます。
- **追跡対象を選べるコンパス：** ハンターには専用コンパスが渡されます。右クリックで対象メニューからランナーを選び、追跡中に対象を変更できます。別のディメンションにいる場合は、直接追跡できるようになるまで関連するポータル経路を案内します。リスポーンしたハンターには追跡用コンパスが再び渡されます。
- **進行状況の表示：** ボスバーと試合情報に、ランナーの装備、ネザーの資源、ブレイズロッド、エンダーパール、エンダーアイ、要塞、ジ・エンドへの進行を反映します。新しいビルドでは、より細かな段階とドラゴンの体力を反映した進行表示が加わります。
- **ランナーのキル報酬：** 試合中にランナーがハンターを倒すと、進行度を考慮した50項目の重み付き報酬プールが使われます。アニメーション付きの抽選、ダブル／トリプル報酬、連続キルの通知、レアアイテム獲得時の演出が含まれます。
- **勝利と結果：** 最後のランナーが死亡するとハンターの勝利、エンダードラゴンを倒すとランナーの勝利です。試合終了のタイトル、祝勝演出、キル／死亡情報、一時的なアイテムの片付けも含まれます。新しいビルドでは、MVP、ダメージ、移動距離の結果も表示します。
- **チーム連絡と便利な機能：** `/teammsg`で味方だけにメッセージを送り、`/trash`で54スロットの廃棄用インベントリを開き、`/nv`で自分の暗視を切り替えられます。
- **メニューによる管理：** コントロールセンターには、役割、開始／リセット、ハンターの早期解放、フレンドリーファイア、サーバーロック、全員のテレポート、回復／食料補充、言語、防護設定、状態、ガイドブックがあります。フリーズと完全リセットは、次の試合の準備にも使えます。
- **多言語ガイド：** ランナー、ハンター、管理者向けの本で、目標、追跡用コンパスの使い方、死亡、準備、コマンドを説明します。1.9.11では、`/mhhelp`でプレイヤーの役割に応じたガイドが渡されます。
- **Paper Anti-Xrayとの連携：** メニューからPaperのワールド単位の保護を設定します。変更を反映するにはサーバーの再起動が必要です。

## 1.13.1 の新機能

提供された 1.9.11 ビルドからの変更点：

- **ゴースト観戦者：** 管理者が割り当てる独立した役割。保護された飛行、他プレイヤーからの非表示、状態の保存と復元、ページ分けされた参加者へのテレポートメニューを備えます。
- **刷新されたコントロールセンター：** カテゴリー別メニュー、明示的な四種類の役割選択、名前付きの対象選択、再接続猶予時間の選択、Classic/Fast/Hardcore/Custom プリセット、専用の 30 秒確認画面。
- **GrimAC 連携：** 必須の GrimAC 2.3.73 が、従来有効だった VexAC の起動経路を置き換えます。GUI から全体、五つの検査グループ、通知、監視/適用モードを操作できます。Paper Anti-Xray は独立しています。
- **新しい Smart Hunter Kit プランナー：** Runner の装備とエンチャント、最寄りの Runner、チーム人数、距離、ディメンション、地形に応じて装備と補給を調整します。既存のより強い装備を保持し、道具の重複を避け、30 秒間の履歴で消耗品の補充量を制限します。固定の装備差や実測されたバランスを保証するものではありません。
- **検証付き復旧：** SHA-256 で封印したスナップショット、スキーマ/状態チェック、有効なバックアップへのフォールバックを使用します。無効または新しい形式のスナップショットは上書きせず保持します。観戦者の状態は別途永続化します。
- **メッセージの拡充：** 各同梱翻訳のキー数は 683 から 762 に増えました。ゲーム内の言語は従来と同じ十言語です。新たに二つの公開コマンド `/mspectator <player>` と `/mhspectate` が登録されています。
- **リセット時の代替動作：** オーバーワールドのスポーン地点付近に安全な地面が見つからない場合、無理にテレポートせず、その処理を省略できます。

## `/mhgui` によるセットアップと操作の全手順

サーバーを停止し、ワールドとプラグインデータをバックアップしてください。現行版の JAR を両方 `plugins/` に配置し、Manhunt JAR と GrimAC JAR はそれぞれ一つだけ残します。アップグレード時は既存の `plugins/VexLandManhunt/` の設定とデータを保持してください。Paper 1.21.11 / Java 21 サーバーを完全に起動します。ビルドを交換した場合は完全再起動を行ってください。GrimAC が正常に読み込まれる必要があります。プラグインの内部名は引き続き `VexLandManhunt` です。

本ガイドはプラグイン **1.13.1** を英語ラベルで説明します。実際のラベルはサーバー全体の言語設定に従います。位置は上から行、左から列を数えます。特別な操作の記載がなければ、通常の左クリックを使ってください。静的検査に基づくガイドであり、Minecraft サーバーは実行していません。

### 試合を設定する

1. `vexland.admin` 権限（既定：OP）で `/mhgui` を実行します。
2. **Player Roles** を開き、名前の付いたプレイヤータイルをクリックして、**Runner**、**Hunter**、**Spectator**、**No Team** のいずれかを選びます。指定した役割を選ぶ画面が開きます。プレイヤーのクリックで役割が順番に切り替わる仕組みではありません。
3. 少なくとも Runner 一人と Hunter 一人を割り当てます。試合開始時、未割り当てのオンラインプレイヤーは Hunter になる場合があります。観戦者はどちらのチームの必要人数にも含まれません。
4. **Match Settings**、**GrimAC Security**、**Global Language** を確認します。開始前に Server Freeze をオフにしてください。
5. **Match Controls → Start Match** を開きます。参加者のインベントリが準備/消去され、イントロが再生され、ルーレットで Hunter の待機時間が決まります。

### ホーム：`/mhgui`（五行）

| 位置 | ボタン | 動作 |
|---|---|---|
| R2 C2 | Match Controls | 開始、一時停止/再開、解放、リセット。 |
| R2 C4 | Player Roles | オンラインプレイヤーの役割一覧を開きます。 |
| R2 C6 | Match Settings | 味方へのダメージ、キット、スポーン、再接続、プリセット。 |
| R2 C8 | Player Management | 対象を選び、プレイヤー/ワールドのツールを使います。 |
| R4 C2 | GrimAC Security | 保護設定を開きます。 |
| R4 C4 | Global Language | 全員が使う言語を選びます。 |
| R4 C6 | Administrator Guide | 翻訳済み管理者ガイドブックをインベントリに追加します。 |
| R5 C5 | Close | メニューを閉じます。 |

R1 C5 のビーコンに試合状態と Runner/Hunter の人数が表示されます。

### Match Controls（五行）

| 位置 | ボタン | 動作 |
|---|---|---|
| R2 C2 | Start Match | 一連の開始処理を実行します。 |
| R2 C4 | Pause Match / Resume Match | ゲームプレイと試合タイマーを一時停止/再開します。RUNNING の試合で使用できます。 |
| R2 C6 | Release Hunters | 現在の Hunter 待機時間を早期終了します。 |
| R2 C8 | Reset Match | 確認画面を開き、試合を完全リセットします。 |
| R4 C2 | Server Freeze | 全体の非 OP プレイヤー凍結を切り替えます。 |
| R4 C4 | Teleport Everyone | 確認後、オンラインプレイヤー全員を自分の場所に集めます。 |
| R4 C6 | Match Info | 試合とチームのレポートを送ります。 |

**Back** は R5 C1、**Close** は R5 C9 です。Server Freeze と Pause Match は別機能です。時計とゲームシステムを一緒に止める必要がある場合は Pause を使ってください。

### Player Roles

六行のプレイヤー一覧は、最初の五行に最大 45 個の名前付き役割タイルをプレイヤー名順で表示します。Runner は黄緑色のコンクリート、Hunter は赤色のコンクリート、Spectator はエンダーアイ、No Team は灰色のコンクリートです。最下行の C1 に **Previous Page**、C3 にページ/オンライン情報、C5 に **Back to Control Center**、C9 に **Next Page** があります。

プレイヤーをクリックすると **Choose Player Role**（三行）が開きます。

| 位置 | 指定する役割 |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

R1 C5 にプレイヤー名/現在の役割が表示され、**Back** は R3 C1、**Close** は R3 C9 です。試合中も役割を変更できます。RUNNING 中に最後の割り当て済み Runner を別の役割にすると、**Last Runner: the match will end** 確認画面が開きます。適用すると Hunter の勝利になる場合があります。役割コマンドは即時適用されるため、意図を確認して使用してください。ここでは No Team も選べます。進行中の試合では、通常の開始/参加同期により未割り当てプレイヤーが Hunter になる場合があります。

### 観戦者

管理者が `/mspectator <player>` を実行するか、Player Roles で **Spectator** を選んで割り当てます。コマンド定義に権限の行はありませんが、処理側で管理者権限を確認します。プレイヤーが `/mhspectate` を実行しても、自分を観戦者に登録することはできません。

観戦者はホットバーの最初のスロットに **Spectator teleport** コンパスを受け取ります。メインハンドで持って右クリックするか、`/mhspectate` を使うと六行のテレポートメニューが開きます。Spectator の役割がある間だけ使用できます。最初の五行には、生存中のオンライン Runner/Hunter が名前順に最大 45 人表示されます。名前付き役割タイルをクリックすると、別ワールドも含め、そのプレイヤーの現在地へテレポートします。最下行の C1 は **Previous Page**、C5 は **Close**、C9 は **Next Page** です。適切な参加者がいない場合、R3 C5 に **No players available** と表示されます。メニューを閉じても観戦者のままです。

観戦者は飛行でき、他プレイヤーから非表示となり、衝突せず、ダメージから保護されます。実装は飛行付きアドベンチャーモードです。バニラのスペクテイターモードのカメラ機能やブロック通過は付与されません。攻撃、ブロックの破壊/設置、通常のブロック/エンティティ操作、アイテムの取得/投棄、オフハンド交換、インベントリのクリック/ドラッグ、防具立て操作、経験値の取得/増加は阻止されます。Mob は観戦者を標的にできず、空腹度の変化もキャンセルされます。`/teammsg <message>` は同じ Spectator の他プレイヤーに届きます。参加者の位置やその他の外部支援を競技者へ伝えないでください。

観戦をやめるには、管理者が **Runner**、**Hunter**、**No Team** を割り当てるか、`/mrunner <player>` または `/mhunter <player>` を使用します。自分で退出する専用コマンド/ボタンはありません。退出時は保存済みのインベントリ/カーソル、位置、ゲームモード、飛行、衝突、無敵状態を復元し、その後、新しい役割の試合動作を適用します。再参加に備えて観戦者状態は保存されます。完全な Match Reset は観戦者状態を復元し、役割を消去し、安全なオーバーワールドのスポーン地点があればオンラインプレイヤーをそこへ移動します。通常の試合終了時の片付けでは、観戦者は参加者向けのアイテム/飛行処理の対象外です。

### Match Settings（五行）

| 位置 | ボタン | 動作 |
|---|---|---|
| R2 C2 | Friendly Fire | チームメイトへのダメージを切り替えます。 |
| R2 C4 | Smart Hunter Kit | 適応型 Hunter リスポーンキットを切り替えます。 |
| R2 C6 | Auto World Spawn | 間隔の選択画面を開きます。 |
| R2 C8 | Reconnect Grace | Runner の再接続猶予時間を選びます。 |
| R4 C2 | Match Preset | Classic、Fast、Hardcore、Custom を選びます。 |
| R4 C4 | Reset Settings | バランス設定を確認します：Kit ON、Spawn 15m、Reconnect 15m。 |
| R4 C6 | Random Head Start | 情報タイルです。待機時間は引き続きルーレットで決まります。 |

**Back** は R5 C1、**Close** は R5 C9 です。

三行の **Reconnect Grace** 選択画面は R2 C2–C7 に **1、5、10、15、20、30 分**をこの順に表示します。クリックすると値が保存され、選択画面は開いたままになります。Back は R3 C1、Close は R3 C9 です。

三行の **Match Preset** 選択画面では R2 C2、C4、C6、C8 に **Classic**、**Fast**、**Hardcore**、**Custom** があります。Classic：Kit ON、Spawn 15m、Reconnect 15m。Fast：ON、5m、10m。Hardcore：OFF、OFF、5m。Custom は現在の手動設定を維持します。プリセットでもランダムな待機時間は維持されます。選択後もメニューは開いたままです。Back は R3 C1、Close は R3 C9 です。

**Auto World Spawn** は R2 C2、C3、C4 に OFF、5m、10m、R2 C6、C7、C8 に 15m、20m、30m を表示します。Back は R3 C5 です。間隔を選ぶか、`/mhspawn <off|5|10|15|20|30|status>` を使用してください。適切なオーバーワールドの Runner 付近へスポーン地点を移します。適切な対象がいなければ省略できます。`/mhkit <on|off|toggle|status>` はキットを直接操作します。

### Player Management（六行）

| 位置 | ボタン | 対象 |
|---|---|---|
| R1 C5 | Target Player | 名前付きのプレイヤー選択画面を開きます。 |
| R2 C2 | Full Heal | オンラインプレイヤー全員。 |
| R2 C4 | Full Hunger | オンラインプレイヤー全員。 |
| R2 C6 | Clear Effects | オンラインプレイヤー全員。 |
| R2 C8 | Freeze Target | 選択したプレイヤー。 |
| R4 C2 | Clear Target Inventory | 選択したプレイヤー。確認が必要です。 |
| R4 C4 | Kill Target | 選択したプレイヤー。確認が必要で、通常の試合結果が適用されます。 |
| R4 C6 | Set Day | 現在いるワールド。 |
| R4 C8 | Clear Weather | 現在いるワールド。 |
| R5 C2 | Clear Dropped Items | 現在いるワールド。確認が必要です。 |
| R5 C4 | Emergency Sync | オンラインプレイヤーの役割/実行時システムを更新します。 |
| R5 C6 | Freeze Team | 左：Runner、右：Hunter、Shift クリック：このツールのチーム/個別凍結を解除。 |

Back は R6 C1、Close は R6 C9 です。対象の選択は役割を変更しません。選択画面には自分以外のオンラインプレイヤーを一ページ 28 人、2–5 行目の 2–8 列に表示します。名前をクリックして選択し、戻ります。Previous/Back/Next は R6 C1/C5/C9 です。操作を適用する直前に表示対象を再確認してください。

### 確認画面

Reset Match、Teleport Everyone、Reset Settings、Clear Target Inventory、Kill Target、Clear Dropped Items、GUI での最後の Runner の役割変更は、独立した三行の **Confirm Action** 画面を使います。R1 C5 の操作/対象を読み、R2 C3 の緑色の **Confirm** または R2 C7 の赤色の **Cancel** をクリックします。確認は **30 秒**で期限切れになります。対象の変更/オフライン化や役割の変更があれば、再選択が必要です。これら新メニューの操作では、旧ガイドの五/八秒以内の連続クリック手順は置き換えられています。

### GrimAC Security と言語

六行の Grim メニューは R1 C5 に状態を表示します。切り替えは R2 C2 **GrimAC Master**、C4 **Movement**、C6 **Combat**、C8 **Packets**、R4 C2 **Velocity / AntiKB**、C4 **World / Scaffold**、C6 **Anti X-Ray**、C8 **Admin Alerts**、R5 C5 **Monitor mode** です。Back は R6 C1、Close は R6 C9 です。Monitor mode で通知/証拠収集と制裁適用を切り替えます。Paper Anti-Xray は独立しており、変更後に再起動が必要です。これは GrimAC の操作であり、古い VexAC/AutoClick メニューの説明は本リリースには当てはまりません。

Global Language は全員に適用され、メニュー/アイテムを更新します。言語名をクリックしてください。Back は R3 C5 です。`/mhlang` は同じ選択画面を開き、`/mhhelp` は翻訳済みのプレイヤー/管理者ガイドを提供します。

### 現在の既定値、再接続、違反への対応

`plugins/VexLandManhunt/config.yml` の新規設定で使われるフォールバック値：

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` は自動スポーン移動がオフであることを示します。Reset Settings と Classic は代わりに 15 分を選びます。Runner の再接続猶予中は枠が保持され、時間内の復帰には十秒間の保護が付きます。保存されたサーバー停止時間は除外されます。期限切れで Runner が Hunter に変わるか、Hunter 勝利で試合が終了する場合があります。Pause/Resume はゲームシステムを凍結し、有効な試合時間を調整します。復旧ファイルはプラグインが管理します。

Grim ブリッジ設定は `plugins/VexLandManhunt/grim-settings.yml` に保存されます。新規設定の既定値は Master ON、五グループすべて ON、Admin Alerts ON、**Monitor mode OFF：制裁適用が有効**です。監視モードは証拠/通知をキューに入れ、該当するフラグをキャンセルします。適用モードでは、ブリッジが Grim のキックコマンドを、再接続可能な翻訳済み切断メッセージへ変換する場合があります。永久 BAN 方針を定めるものではありません。実際のしきい値は Grim の設定にも依存します。証拠は `plugins/VexLandManhunt/anticheat/grim-evidence.log` への書き込みキューに入り、上限付きキューでは高負荷時に項目が失われる場合があります。ブリッジは観戦者、一時停止/凍結中のプレイ、一部の乗り物状況を除外し、参加、テレポート、リスポーン後に三秒の猶予を設けます。アンチチートの精度や性能のベンチマークは主張していません。

## 公開コマンド一覧 — 1.13.1

管理者権限は OP または `vexland.admin`（既定 OP）を意味します。`/mspectator <player>` はコマンド定義に権限行がなくても、処理側でこれを確認します。役割コマンドは即時適用されます。RUNNING 中に最後の Runner を変更すると、試合が終わる場合があります。GUI はこの状況で確認を表示します。

| コマンド | 用途 | 権限 |
|---|---|---|
| `/mhgui` | カテゴリー別コントロールセンターを開く | 管理者 |
| `/mhstart` | 試合の開始処理をすべて実行 | 管理者 |
| `/mhreset` | 試合を完全リセット | 管理者 |
| `/mhrelease` | 待機中の Hunter を解放 | 管理者 |
| `/mrunner <player>` | Runner を割り当て | 管理者 |
| `/mhunter <player>` | Hunter を割り当て | 管理者 |
| `/mspectator <player>` | Spectator を割り当て | 管理者、新規 |
| `/mhspectate` | 参加者へのテレポートメニューを開く | 現在の Spectator、新規 |
| `/teammsg <message>` | 自分と同じ役割/チームへ送信 | プレイヤー |
| `/trash` | 廃棄用の 54 スロットのインベントリ。別名 `/mhtrash`、`/vextrash` | プレイヤー |
| `/nv` | 個人の暗視を切り替え | プレイヤー |
| `/mhlang` | 全体の言語選択を開く | 管理者 |
| `/mhkit <on\|off\|toggle\|status>` | 適応型 Hunter キットを設定 | 管理者 |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | スポーン移動を設定 | 管理者 |
| `/mhhelp` | 翻訳済み役割/管理者ガイドを受け取る | プレイヤー / 管理者 |
| `/mhpause` | 進行中の試合を一時停止 | 管理者 |
| `/mhresume` | 一時停止した試合を再開 | 管理者 |
| `/mhdebug` | 内部診断 | 管理者 |

本リリースに `/mhnone` は登録されていません。GUI の No Team を使ってください。Hunter は追跡コンパスを右クリックして Runner を選びます。観戦者テレポートや管理者の対象選択とは別です。Runner はエンダードラゴンを倒すと勝利し、Runner が一人も残らないと Hunter が勝利します。他の Runner が残っていれば、死亡した Runner は Hunter に変わります。

## 言語、履歴、サードパーティへの謝辞

元のプラグインは **10 のゲーム内言語**に対応します：英語、ペルシャ語、アラビア語、スペイン語、フランス語、ドイツ語、ロシア語、簡体字中国語、ヒンディー語、ポルトガル語。`/mhlang` でサーバー全体の言語を選び、`language.txt` に保存します。GitHub マニュアルはアラビア語版を除く **18 言語**です。日本語などの追加 README 言語が、変更されていない JAR にゲーム内翻訳を追加するわけではありません。

[バージョン履歴](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) に各提供ビルドを記録しています。旧 1.9.11 / 1.6.4 の完全なマニュアルは[バージョン別アーカイブ](archive/1.9.11/README.ja.md)に残されています。専用の観戦者対応ビルドは提供済みで、1.13.1 として公開されました。この機能を古いダウンロードのものとして説明しないでください。

**GrimAC は GrimAC の貢献者による独立したプロジェクトで、GPL-3.0 で配布されています。** Bardiya と Ali は Vexland_Manhunt とその連携を制作しました。GrimAC の作者として記載されるものではありません。提供された Grim JAR の SHA-512 と SHA-1 は、公式 Modrinth 2.3.73 Bukkit アーティファクトと一致します。埋め込まれたソースコミットは[上流 v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73)と一致します。リリースには変更されていないバイナリ、チェックサム、上流ソースのスナップショット、ライセンス、[サードパーティ通知](../THIRD_PARTY_NOTICES.md)を含みます。これらのコンポーネント通知は、別プロジェクトである Manhunt にライセンスを付与するものではありません。

## Dreamへの冗談まじりの挑戦

Bardiyaから、ちょっとしたMinecraftの軽口です 😄

> 「はぁ……僕とAliのManhuntプラグインはDreamの100倍よくなったのに、Dreamは怖がって僕らのプラグインを遊んでくれないんだ！」

## 制作者とプロジェクトの範囲

**[Bardiya Alizadeh（Kabir）· Farland_game](https://github.com/FarlandGame) と [Ali · Alivexor](https://github.com/Alivexor) の共同制作です。** オリジナルのプラグイン定義にも、両ハンドルが作者として記載されています。

このリポジトリは、オリジナルのコンパイル済みリリース、ドキュメント、バージョン説明を、共同制作のポートフォリオとして紹介しています。機能説明は、受け取ったJARの静的検査に基づきます。この公開作業では、実際のサーバーでの互換性、復元性能、ゲームバランス、アンチチートの精度をテストしていません。

[BardiyaのGitHubポートフォリオ](https://github.com/FarlandGame) · [AliのGitHub](https://github.com/Alivexor) · [すべてのリリース](https://github.com/FarlandGame/Vexland_Manhunt/releases)
