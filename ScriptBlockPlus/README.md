[ScriptBlockPlus](https://github.com/yuttyann/ScriptBlockPlus)
==========

概要
-----------
ブロックにスクリプトを設定することができる**Bukkitプラグイン**です。  

解説
-----------
| ページ | 説明 |
|:---|:---|
| [MCPoteton](https://mcpoteton.com/mcplugin-scriptblockplus) | あらゆる機能の解説をしています。 |
| [README.md](https://github.com/yuttyann/ScriptBlockPlus/blob/master/README.md) | ScriptBlockPlusのリポジトリの`README.md`です。 |
| [チュートリアル](https://github.com/yuttyann/ScriptBlockPlus/wiki/%5BJP%5D-Plugin-Tutorial) | 各機能の説明です。 |
| [コマンドの一覧](https://github.com/yuttyann/ScriptBlockPlus/wiki/%5BJP%5D-Command-and-Permission) | コマンドの引数等の説明です。 |
| [オプションの一覧](https://github.com/yuttyann/ScriptBlockPlus/wiki/%5BJP%5D-Option-Description) | オプションの利用方法の説明です。 |

権限
-----------
<details>
<summary>一覧</summary>

| 権限 | 説明 |
|:---|:---|
| scriptblockplus.command.tool | [コマンド](#コマンド) |
| scriptblockplus.command.reload | [コマンド](#コマンド) |
| scriptblockplus.command.backup | [コマンド](#コマンド) |
| scriptblockplus.command.checkver | [コマンド](#コマンド) |
| scriptblockplus.command.datamigr | [コマンド](#コマンド) |
| scriptblockplus.command.&lt;scriptkey&gt; | [コマンド](#コマンド) |
| scriptblockplus.command.selector | [コマンド](#コマンド) |
| scriptblockplus.&lt;scripttype&gt;.use | スクリプトを実行するために必要です。 |
| scriptblockplus.tool.scripteditor | `Script Editor`を利用するために必要です。 |
| scriptblockplus.tool.scriptviewer | `Script Viewer`を利用するために必要です。 |
| scriptblockplus.tool.scriptmanager | `Script Manager`を利用するために必要です。 |
| scriptblockplus.tool.blockselector | `Block Selector`を利用するために必要です。 |
| scriptblockplus.option.&lt;optionid&gt; | オプションを実行するために必要です。 |
</details>

コマンド
-----------
<details>
<summary>scriptblockplus / sbp</summary>

| 名称 | 短縮 |
|:---|:---|
| scriptblockplus | sbp |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| tool | scriptblockplus.command.tool | OP | 補助ツールの選択ウィンドウを表示します。 |
| reload | scriptblockplus.command.reload | OP | 全てのファイルの再読み込みを行います。 |
| backup | scriptblockplus.command.backup | OP | プラグインデータのバックアップを作成します。 |
| checkver | scriptblockplus.command.checkver | OP | 最新のプラグインが存在するかチェックします。 |
| datamigr | scriptblockplus.command.datamigr | OP | ScriptBlockのスクリプトをSBPlusへ移行します。 |
| &lt;scriptkey&gt; create &lt;options&gt; | scriptblockplus.command.&lt;scriptkey&gt; | OP | ブロックにスクリプトを設定します。 |
| &lt;scriptkey&gt; add &lt;options&gt; | scriptblockplus.command.&lt;scriptkey&gt; | OP | ブロックにスクリプトを追加します。 |
| &lt;scriptkey&gt; remove | scriptblockplus.command.&lt;scriptkey&gt; | OP | ブロックのスクリプトを削除します。 |
| &lt;scriptkey&gt; view | scriptblockplus.command.&lt;scriptkey&gt; | OP | ブロックのスクリプトを表示します。 |
| &lt;scriptkey&gt; nametag [nametag] | scriptblockplus.command.&lt;scriptkey&gt; | OP | ブロックにネームタグを設定します。 |
| &lt;scriptkey&gt; redstone [repeat] [filter] [selector] | scriptblockplus.command.&lt;scriptkey&gt; | OP | レッドストーンの動力で動作するか設定します。 |
| &lt;scriptkey&gt; run [player] &lt;world&gt; &lt;x&gt; &lt;y&gt; &lt;z&gt; | scriptblockplus.command.&lt;scriptkey&gt; | OP | 指定したスクリプトを実行します。 |
| selector paste [pasteonair] [overwrite] | scriptblockplus.command.selector | OP | 選択範囲にスクリプトをペーストします。 |
| selector remove | scriptblockplus.command.selector | OP | 選択範囲のスクリプトを削除します。 |
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

**現在`UpdateChecker`は動作しません。**
```yaml
# ScriptBlockPlus v2.2.5 Config #


## ===== 自動アップデート ===== ##
# [true -> 有効 | false -> 無効]
# 確認メッセージは"OP"にしか表示されません。
# 最新バージョンを確認するかどうか。
UpdateChecker: true

# 前提 "UpdateChecker: true"
# 最新のプラグインをダウンロードするかどうか。
AutoDownload: true

# 前提 "UpdateChecker: true"
# ダウンロードした更新内容を、メモ帳で開くかどうか。
OpenChangeLog: true

## ===== Json ===== ##
# [true -> 有効 | false -> 無効]
# リロード、サーバー起動時に全ファイルをキャッシュします。
# スムーズな動作が可能ですが、メモリを多く消費する可能性があります。
CacheAllJson: true

# JSONの整形を許可する要素数の上限を設定します。
# 上限を設定することで、容量の削減や処理速度の短縮が期待できます。
FormatLimit: 10000

## ===== スクリプトの並び替え ===== ##
# [true -> 有効 | false -> 無効]
# スクリプト実行時に推奨される順番通りにオプションを実行するかどうか。
# 設定されている優先順にオプションを並び替えて最適な順番で実行します。
SortScripts: true

## ===== コンソールログ ===== ##
# [true -> 有効 | false -> 無効]
# 言語ファイルの頭文字"console"が対象です。
# コンソールに操作メッセージ等を表示させることができます。
ConsoleLog: false

## ===== オプションヘルプ ===== ##
# [true -> 有効 | false -> 無効]
# タブ補完を行った際に、オプションのヘルプを表示するかどうか。
OptionHelp: true

## ===== オプション実行権限 ===== ##
# [true -> 有効 | false -> 無効]
# オプションを実行時に権限をチェックするかどうか。
OptionPermission: false

## ===== スクリプトの実行 ===== ##
# [true -> 有効 | false -> 無効]
# "左"または"右"クリックからのスクリプトの実行を無効化するかどうか。
Actions:
  # 左クリックの設定
  InteractLeft: true
  # 右クリックの設定
  InteractRight: true
```
</details>

<details>
<summary>message.yml</summary>

```yaml
# ScriptBlockPlus v2.2.5 Message #
# 作成者: yuttyann44581


## ===== Commands ===== ##
# プレースホルダはありません
ToolCommandMessage: 'tool - 補助ツールの選択ウィンドウを表示します。'
ReloadCommandMessage: 'reload - 全てのファイルの再読み込みを行います。'
BackupCommandMessage: 'backup - プラグインデータのバックアップを作成します。'
CheckVerCommandMessage: 'checkver - 最新のプラグインが存在するかチェックします。'
DataMigrCommandMessage: 'datamigr - ScriptBlockのスクリプトをSBPlusへ移行します。'
CreateCommandMessage: '<scriptkey> create <options> - ブロックにスクリプトを設定します。'
AddCommandMessage: '<scriptkey> add <options> - ブロックにスクリプトを追加します。'
RemoveCommandMessage: '<scriptkey> remove - ブロックのスクリプトを削除します。'
ViewCommandMessage: '<scriptkey> view - ブロックのスクリプトを表示します。'
NameTagCommandMessage: '<scriptkey> nametag <tag> - ブロックにネームタグを設定します。'
RedstoneCommandMessage: '<scriptkey> redstone [repeat] [filter] [selector] - レッドストーンの動力で動作するか設定します。'
RunCommandMessage: '<scriptkey> run [player] <world> <x> <y> <z> - 指定したスクリプトを実行します。'
SelectorPasteCommandMessage: 'selector paste [pasteonair] [overwrite] - 選択範囲にスクリプトをペーストします。'
SelectorRemoveCommandMessage: 'selector remove - 選択範囲のスクリプトを削除します。'

# &(code) : カラーコード(以降の項目全て対象)

## ===== GUI ===== ##
# プレースホルダはありません
CustomGUI:
  System:
    Input: '入力してください'
    Reset: '&cテキストをリセット'
    InPlayer: '&c他のプレイヤーが、スクリプトを編集中です。'
    Overflow: '&c文字数が、上限を越えているため正常な編集ができません。'
    SearchGUI: 'スクリプトの検索'
    SettingGUI: 'スクリプトの設定'
    ToolBoxGUI: 'ツールボックス'
  Item:
    SearchGUI:
      Next: '&d次のページ'
      Prev: '&d前のページ'
      Reset: '&dリセット'
      Setting: '&6スクリプト'
      Scriptkey: '&dスクリプトキー'
      Script: '&bスクリプトの指定'
      Time: '&b時間の指定'
      Coords: '&b座標の指定'
      NameTag: '&bネームタグの指定'
    SettingGUI:
      Delete: '&c設定の削除'
      Close: '&d検索ページへ戻る'
      Copy: '&dコピー'
      Paste: '&dペースト'
      Teleport: '&b移動'
      Execute: '&b実行'
      Info: '&b情報'
      Redstone: '&aターゲットセレクターの編集'
      Script: '&aスクリプトの編集'
      NameTag: '&aネームタグの編集'

## ===== ScriptEditor ===== ##
# プレースホルダはありません
ScriptEditor:
- '&aこのツールは、スクリプトの編集をサポートします。'
- '&6左クリック: &eツールの対象を切り替えます。'
- '&6右クリック: &eスクリプトのコピーを行います。'
- '&6シフト+左クリック: &eスクリプトの削除を行います。'
- '&6シフト+右クリック: &eスクリプトのペーストを行います。'

## ===== ScriptViewer ===== ##
# プレースホルダはありません
ScriptViewer:
- '&aこのツールは、スクリプトのチェックをサポートします。'
- '&6左クリック: &e周囲のスクリプトの検索を開始します。'
- '&6右クリック: &e周囲のスクリプトの検索を停止します。'

## ===== ScriptManager ===== ##
# プレースホルダはありません
ScriptManager:
- '&aこのツールは、スクリプトの管理をサポートします。'
- '&6右クリック: &e検索ウィンドウを開きます。'

## ===== BlockSelector ===== ##
# プレースホルダはありません
BlockSelector:
- '&aこのツールは、範囲選択をサポートします。'
- '&6左クリック: &eブロックを選択範囲の始点に指定します。'
- '&6右クリック: &eブロックを選択範囲の終点に指定します。'
- '&6シフト+左クリック: &e現在位置を選択範囲の始点に指定します。'
- '&6シフト+右クリック: &e現在位置を選択範囲の終点に指定します。'

# |~, \n : 改行(以降の項目全て対象)

## ===== Messages ===== ##
# プレースホルダはありません
SenderNoPlayerMessage: '&cコマンドはゲーム内から実行してください。'
NotPermissionMessage: '&cパーミッションが無いため、実行できません。'
GiveToolMessage: '&a補助ツールが配布されました。'
AllFileReloadMessage: '&a全てのファイルの再読み込みが完了しました。'
PluginBackupMessage: '&aプラグインデータのバックアップが完了しました。'
ErrorPluginBackupMessage: '&cプラグインデータのバックアップに失敗しました。'
NotLatestPluginMessage: '&b現在のバージョンが最新です。'
NotScriptBlockFileMessage: '&cScriptBlockのデータファイルが見つかりません。'
DataMigrStartMessage: '&7ScriptBlockのスクリプトを移行しています....'
DataMigrEndMessage: '&bスクリプトの移行が完了しました。'
UpdateDownloadStartMessage: '&6最新のプラグインをダウンロードしています...'

# %name% : ファイル名
# %path% : ファイルパス
# %size% : ファイルサイズ
UpdateDownloadEndMessage: '&6ダウンロードが終了しました。|~ファイル名: %name%|~ファイルサイズ: %size%|~ファイルパス: %path%'

# %name%    : プラグイン名
# %version% : 最新バージョン
# %details% : 更新内容
UpdateCheckMessage: '&b最新のバージョンを検出しました。|~v%version%にアップデートしてください。|~プラグイン名: %name%|~☆アップデート内容☆|~%details%'

# プレースホルダはありません
ErrorUpdateMessage: '&cアップデートに失敗しました。'

# %scriptkey% : スクリプトキー
ScriptCopyMessage: '&aブロック"%scriptkey%"のスクリプトをコピーしました。'
ScriptPasteMessage: '&aブロック"%scriptkey%"にスクリプトをペーストしました。'
ScriptCreateMessage: '&aブロック"%scriptkey%"でスクリプトを作成しました。'
ScriptAddMessage: '&aブロック"%scriptkey%"にスクリプトを追加しました。'
ScriptRemoveMessage: '&cブロック"%scriptkey%"のスクリプトを削除しました。'
ScriptNameTagMessage: '&aブロック"%scriptkey%"のネームタグを編集しました。'
ScriptRedstoneMessage: '&aブロック"%scriptkey%"のターゲットセレクターを編集しました。'

# プレースホルダはありません
NotSelectionMessage: '&cBlockSelectorで座標を選択してください。'

# プレースホルダはありません
ScriptViewerStartMessage: '&a周囲のスクリプトの検索を開始しました。'
ScriptViewerStopMessage: '&c周囲のスクリプトの検索を停止しました。'

# %world%  : ワールドの名前
# %coords% : 座標(x, y, z)
SelectorPos1Message: '&b始点"%coords%"を選択しました。'
SelectorPos2Message: '&b終点"%coords%"を選択しました。'

# %scriptkey%  : スクリプトキー
# %blockcount% : ブロック数
SelectorPasteMessage: '&aブロック(%blockcount%)"%scriptkey%"にスクリプトをペーストしました。'
SelectorRemoveMessage: '&cブロック(%blockcount%)"%scriptkey%"のスクリプトを削除しました。'

# %option% : オプション名
# %cause%  : 発生原因
OptionFailedToExecuteMessage: '&cオプション"%option%"の実行に失敗しました。|~&c発生原因: %cause%'

# プレースホルダはありません
ActiveDelayMessage: '&c遅延したスクリプトが実行されるまで、再度実行することはできません。'

# %hour%   : 時
# %minute% : 分
# %second% : 秒
ActiveCooldownMessage: '&cクールダウン終了まで、%hour%時間%minute%分%second%秒です。'

# %action% : アクション
SuccActionDataMessage: '&aアクション"%action%"を選択しました。'

# プレースホルダはありません
ErrorActionDataMessage: '&c既にアクションが選択されています。'
ErrorScriptCheckMessage: '&c入力されたスクリプトが正しくありません。'
ErrorScriptFileCheckMessage: '&cスクリプトが見つかりません。'

# %scriptkey% : スクリプトキー
ErrorScriptExecMessage: '&cブロック"%scriptkey%"のスクリプトの実行に失敗しました。'

# %group% : グループ名
ErrorGroupMessage: '&cグループ"%group%"のメンバーのみ、スクリプトを実行することが出来ます。'

# %material% : アイテムのID
# %amount%   : アイテムの個数
# %damage%   : アイテムのダメージ値
# %name%     : アイテムの名前
# %lore%     : アイテムの概要
ErrorHandMessage: '&cアイテム"&r%name%&r[%material%:%damage%] &e%amount%個&c"を持っていません。'
ErrorItemMessage: '&cアイテム"&r%name%&r[%material%:%damage%] &e%amount%個&c"を所持していません。'

# %cost%   : 必要な金額
# %result% : 足りない金額
ErrorCostMessage: '&cお金が"%result%円"足りません。スクリプトの実行には"%cost%円"必要です。'

# %scriptkey% : スクリプトキー
# %world%     : ワールドの名前
# %coords%    : 座標(x, y, z)
ConsoleScriptEditMessage: '&aスクリプトが編集されました。[キー"%scriptkey%"、座標"%world%, %coords%"]'
ConsoleScriptViewMessage: '&aスクリプトの設定が表示されました。[キー"%scriptkey%"、座標"%world%, %coords%"]'
ConsoleSuccScriptExecMessage: '&aスクリプトが実行されました。[キー"%scriptkey%"、座標"%world%, %coords%"]'
ConsoleErrorScriptExecMessage: '&cスクリプトの実行に失敗しました。[キー"%scriptkey%"、座標"%world%, %coords%"]'

# %scriptkey%  : スクリプトキー
# %blockcount% : ブロック数
# %world%      : ワールドの名前
# %mincoords%  : 最小座標(x, y, z)
# %maxcoords%  : 最大座標(x, y, z)
ConsoleSelectorPasteMessage: '&aスクリプトがペーストされました。[キー"%scriptkey%"、最小座標"%world%, %mincoords%"、最大座標"%world%, %maxcoords%"]'
ConsoleSelectorRemoveMessage: '&cスクリプトが削除されました。[キー"%scriptkey%"、最小座標"%world%, %mincoords%"、最大座標"%world%, %maxcoords%"]'
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**ScriptBlockPlus v2.2.5**](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.2.5/ScriptBlockPlus%20v2.2.5.jar) | `1.9-1.19.3` | `Java11` |

<details>
<summary>Java8対応</summary>

| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [ScriptBlockPlus v2.1.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar-8/2.1.1/ScriptBlockPlus%20v2.1.1-JV8.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v2.1.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar-8/2.1.0/ScriptBlockPlus%20v2.1.0-JV8.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v2.0.9](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar-8/2.0.9/ScriptBlockPlus%20v2.0.9-JV8.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v2.0.8](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar-8/2.0.8/ScriptBlockPlus%20v2.0.8-JV8.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v2.0.7](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar-8/2.0.7/ScriptBlockPlus%20v2.0.7-JV8.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v2.0.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar-8/2.0.6/ScriptBlockPlus%20v2.0.6-JV8.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
</details>

<details>
<summary>1.8-1.15.2対応</summary>

| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [ScriptBlockPlus v1.8.5-ex](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar-ex/1.8.5/ScriptBlockPlus%20v1.8.5-ex.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
</details>

<details>
<summary>過去のバージョン</summary>

| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [ScriptBlockPlus v2.2.4](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.2.4/ScriptBlockPlus%20v2.2.4.jar) | `1.9-1.19.2` | `Java11` |
| [ScriptBlockPlus v2.2.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.2.3/ScriptBlockPlus%20v2.2.3.jar) | `1.9-1.19.2` | `Java11` |
| [ScriptBlockPlus v2.2.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.2.2/ScriptBlockPlus%20v2.2.2.jar) | `1.9-1.18` | `Java11` |
| [ScriptBlockPlus v2.2.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.2.1/ScriptBlockPlus%20v2.2.1.jar) | `1.9-1.18` | `Java11` |
| [ScriptBlockPlus v2.2.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.2.0/ScriptBlockPlus%20v2.2.0.jar) | `1.9-1.18` | `Java11` |
| [ScriptBlockPlus v2.1.8](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.1.8/ScriptBlockPlus%20v2.1.8.jar) | `1.9-1.17.1` | `Java11` |
| [ScriptBlockPlus v2.1.7](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.1.7/ScriptBlockPlus%20v2.1.7.jar) | `1.9-1.17.1` | `Java11` |
| [ScriptBlockPlus v2.1.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.1.6/ScriptBlockPlus%20v2.1.6.jar) | `1.9-1.17.1` | `Java11` |
| [ScriptBlockPlus v2.1.5](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.1.5/ScriptBlockPlus%20v2.1.5.jar) | `1.9-1.17.1` | `Java11` |
| [ScriptBlockPlus v2.1.4](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.1.4/ScriptBlockPlus%20v2.1.4.jar) | `1.9-1.17` | `Java11` |
| [ScriptBlockPlus v2.1.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.1.3/ScriptBlockPlus%20v2.1.3.jar) | `1.9-1.17` | [`Vault`](#連携プラグイン), `Java11` |
| [ScriptBlockPlus v2.1.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.1.2/ScriptBlockPlus%20v2.1.2.jar) | `1.9-1.17` | [`Vault`](#連携プラグイン), `Java11` |
| [ScriptBlockPlus v2.1.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.1.1/ScriptBlockPlus%20v2.1.1.jar) | `1.9-1.17` | [`Vault`](#連携プラグイン), `Java11` |
| [ScriptBlockPlus v2.1.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.1.1/ScriptBlockPlus%20v2.1.1.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java11` |
| [ScriptBlockPlus v2.1.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.1.0/ScriptBlockPlus%20v2.1.0.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java11` |
| [ScriptBlockPlus v2.0.9](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.0.9/ScriptBlockPlus%20v2.0.9.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java11` |
| [ScriptBlockPlus v2.0.8](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.0.8/ScriptBlockPlus%20v2.0.8.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java11` |
| [ScriptBlockPlus v2.0.7](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.0.7/ScriptBlockPlus%20v2.0.7.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java11` |
| [ScriptBlockPlus v2.0.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.0.6/ScriptBlockPlus%20v2.0.6.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java11` |
| [ScriptBlockPlus v2.0.5](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.0.5/ScriptBlockPlus%20v2.0.5.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java11` |
| [ScriptBlockPlus v2.0.4](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.0.4/ScriptBlockPlus%20v2.0.4.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java11` |
| [ScriptBlockPlus v2.0.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.0.3/ScriptBlockPlus%20v2.0.3.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v2.0.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.0.2/ScriptBlockPlus%20v2.0.2.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v2.0.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.0.1/ScriptBlockPlus%20v2.0.1.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v2.0.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/2.0.0/ScriptBlockPlus%20v2.0.0.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.9.9](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.9.9/ScriptBlockPlus%20v1.9.9.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.9.8](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.9.8/ScriptBlockPlus%20v1.9.8.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.9.7](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.9.7/ScriptBlockPlus%20v1.9.7.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.9.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.9.6/ScriptBlockPlus%20v1.9.6.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.9.5](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.9.5/ScriptBlockPlus%20v1.9.5.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.9.4](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.9.4/ScriptBlockPlus%20v1.9.4.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.9.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.9.3/ScriptBlockPlus%20v1.9.3.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.9.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.9.2/ScriptBlockPlus%20v1.9.2.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.9.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.9.1/ScriptBlockPlus%20v1.9.1.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.9.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.9.0/ScriptBlockPlus%20v1.9.0.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.8.9](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.8.9/ScriptBlockPlus%20v1.8.9.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.8.8](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.8.8/ScriptBlockPlus%20v1.8.8.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.8.7](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.8.7/ScriptBlockPlus%20v1.8.7.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.8.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.8.6/ScriptBlockPlus%20v1.8.6.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.8.5](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.8.5/ScriptBlockPlus%20v1.8.5.jar) | `1.9-1.16.5` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.8.4](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.8.4/ScriptBlockPlus%20v1.8.4.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.8.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.8.3/ScriptBlockPlus%20v1.8.3.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.8.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.8.2/ScriptBlockPlus%20v1.8.2.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.8.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.8.1/ScriptBlockPlus%20v1.8.1.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.8.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.8.0/ScriptBlockPlus%20v1.8.0.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.7.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.7.6/ScriptBlockPlus%20v1.7.6.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.7.5](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.7.5/ScriptBlockPlus%20v1.7.5.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.7.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.7.3/ScriptBlockPlus%20v1.7.3.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.7.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.7.2/ScriptBlockPlus%20v1.7.2.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.7.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.7.1/ScriptBlockPlus%20v1.7.1.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.7.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.7.0/ScriptBlockPlus%20v1.7.0.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.6.7](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.6.7/ScriptBlockPlus%20v1.6.7.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.6.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.6.6/ScriptBlockPlus%20v1.6.6.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.6.5](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.6.5/ScriptBlockPlus%20v1.6.5.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.6.4](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.6.4/ScriptBlockPlus%20v1.6.4.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.6.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.6.3/ScriptBlockPlus%20v1.6.3.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.6.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.6.2/ScriptBlockPlus%20v1.6.2.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.6.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.6.1/ScriptBlockPlus%20v1.6.1.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.6.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.6.0/ScriptBlockPlus%20v1.6.0.jar) | `1.8-1.15.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.5.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.5.0/ScriptBlockPlus%20v1.5.0.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.4.9](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.4.9/ScriptBlockPlus%20v1.4.9.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.4.8](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.4.8/ScriptBlockPlus%20v1.4.8.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.4.7](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.4.7/ScriptBlockPlus%20v1.4.7.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.4.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.4.6/ScriptBlockPlus%20v1.4.6.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.4.5](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.4.5/ScriptBlockPlus%20v1.4.5.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.4.4](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.4.4/ScriptBlockPlus%20v1.4.4.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.4.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.4.3/ScriptBlockPlus%20v1.4.3.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.4.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.4.2/ScriptBlockPlus%20v1.4.2.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.4.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.4.1/ScriptBlockPlus%20v1.4.1.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.4.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.4.0/ScriptBlockPlus%20v1.4.0.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java8` |
| [ScriptBlockPlus v1.3.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.3.3/ScriptBlockPlus%20v1.3.3.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.3.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.3.2/ScriptBlockPlus%20v1.3.2.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.3.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.3.1/ScriptBlockPlus%20v1.3.1.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.3.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.3.0/ScriptBlockPlus%20v1.3.0.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.2.9](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.2.9/ScriptBlockPlus%20v1.2.9.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.2.8](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.2.8/ScriptBlockPlus%20v1.2.8.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.2.7](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.2.7/ScriptBlockPlus%20v1.2.7.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.2.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.2.6/ScriptBlockPlus%20v1.2.6.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.2.5](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.2.5/ScriptBlockPlus%20v1.2.5.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.2.4](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.2.4/ScriptBlockPlus%20v1.2.4.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.2.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.2.3/ScriptBlockPlus%20v1.2.3.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.2.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.2.2/ScriptBlockPlus%20v1.2.2.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.2.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.2.1/ScriptBlockPlus%20v1.2.1.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.2.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.2.0/ScriptBlockPlus%20v1.2.0.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.1.9](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.1.9/ScriptBlockPlus%20v1.1.9.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.1.8](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.1.8/ScriptBlockPlus%20v1.1.8.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.1.7](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.1.7/ScriptBlockPlus%20v1.1.7.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.1.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.1.6/ScriptBlockPlus%20v1.1.6.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.1.5](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.1.5/ScriptBlockPlus%20v1.1.5.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.1.4](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.1.4/ScriptBlockPlus%20v1.1.4.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.1.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.1.3/ScriptBlockPlus%20v1.1.3.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.1.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.1.2/ScriptBlockPlus%20v1.1.2.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| [ScriptBlockPlus v1.1.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptBlockPlus/jar/1.1.1/ScriptBlockPlus%20v1.1.1.jar) | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| ~~ScriptBlockPlus v1.1.0~~ | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| ~~ScriptBlockPlus v1.0.9~~ | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| ~~ScriptBlockPlus v1.0.8~~ | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| ~~ScriptBlockPlus v1.0.7~~ | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| ~~ScriptBlockPlus v1.0.6~~ | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| ~~ScriptBlockPlus v1.0.5~~ | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| ~~ScriptBlockPlus v1.0.4~~ | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| ~~ScriptBlockPlus v1.0.3~~ | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| ~~ScriptBlockPlus v1.0.2~~ | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| ~~ScriptBlockPlus v1.0.1~~ | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
| ~~ScriptBlockPlus v1.0.0~~ | `1.7.2-1.13.2` | [`Vault`](#連携プラグイン), `Java7` |
</details>

連携プラグイン
-----------
| プラグイン | 実装 | 説明 |
|:---|:---|:---|
| [Vault](https://www.spigotmc.org/resources/34315/) | `1.0.0-2.2.5` | 権限、経済系の機能を利用することができます。 |
| [DiscordSRV](https://www.spigotmc.org/resources/18494/) | `2.1.4-2.2.5` | ディスコ―ドと連携することができます。 |
| [PlaceholderAPI](https://www.spigotmc.org/resources/6245/) | `1.8.7-2.2.5` | プレースホルダを更に拡張することができます。 |
| [ScriptEntityPlus](https://github.com/yuttyann/FileArchive/tree/main/ScriptEntityPlus) | `1.9.3-2.2.5` | エンティティにスクリプトを紐付けすることができます。 |

<details>
<summary>過去の連携プラグイン</summary>

| プラグイン | 実装 | 説明 |
|:---|:---|:---|
| [ProtocolLib](https://www.spigotmc.org/resources/1997/) | `2.0.4-2.1.1` | 発光エンティティの管理に利用していました。 |
| [PsudoCommands](https://www.spigotmc.org/resources/56738/) | `2.0.0-2.0.4` | ターゲットセレクターの再現に利用していました。 |
</details>