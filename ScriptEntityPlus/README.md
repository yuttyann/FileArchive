[ScriptEntityPlus](https://github.com/yuttyann/ScriptEntityPlus)
==========

概要
-----------
このプラグインは[`ScriptBlockPlus`](#連携プラグイン)の拡張プラグインです。  
エンティティにスクリプトを設定することができる**Bukkitプラグイン**です。  
<details>
<summary>使い方</summary>

### ツールのモード
ツールをメインハンドに所持した状態で左クリック行うことでモードを切り替えることができます。  

**`NORMAL MODE`**  
エンティティをクリックした際に実行されるスクリプトを設定することができます。  

**`DEATH MODE`**  
エンティティが死亡した際に実行されるスクリプトを設定することができます。 

### チャットのイベント
色付きのテキストにカーソルを合わせる、クリックを行うことで情報の表示や実行をすることができます。  
  
**スクリプトの選択 `[MAINHAND+SHIFT+LEFT_CLICK]`**  
緑色のテキストをクリックすることで、エンティティに設定したいスクリプトを選択することができます。  
![ScriptTypes](https://github.com/yuttyann/FileArchive/blob/main/ScriptEntityPlus/image/ScriptTypes.png?raw=true)  

**設定されているスクリプトの表示 `[OFFHAND+RIGHT_CLICK]`**  
緑色のテキストをクリックすることで、スクリプトを実行するコマンドがチャットに設定されます。  
![Scripts](https://github.com/yuttyann/FileArchive/blob/main/ScriptEntityPlus/image/Scripts.png?raw=true)  

**エンティティの設定 `[OFFHAND+SHIFT+RIGHT_CLICK]`**  
橙色の`[...]`で囲まれたテキストをクリックすることで、設定の`有効`、`無効`、`表示`を行うことができます。  
また、水色のテキストにカーソルを合わせることで設定の説明が表示されます。  
![EntitySettings](https://github.com/yuttyann/FileArchive/blob/main/ScriptEntityPlus/image/EntitySettings.png?raw=true)  

### 設定の削除
ScriptBlockPlusのスクリプトの種類と座標をエンティティのUUIDを元に保存しているため、  
UUIDの変更(例: 額縁のアイテムを変更等)があった場合設定ファイルが残存し続けてしまうので注意してください。  
また、エンティティのスクリプトを削除しても設定元のスクリプトには影響はありません。  
**ファイルのパス：** 設定の保存先は`plugins/ScriptBlockPlus/json/entityscript/....`です。  
**ファイルの削除：** ツールでの削除またはプレイヤー以外が死亡した場合に設定ファイルが削除されます。  
</details>

解説
-----------
| ページ | 説明 |
|:---|:---|
| [MCPoteton](https://mcpoteton.com/mcpl-scriptentityplus) | あらゆる機能の解説をしています。 |

権限
-----------
<details>
<summary>一覧</summary>

| 権限 | 説明 |
|:---|:---|
| scriptentityplus.tool.scriptconnection | `Script Connection`を利用するために必要です。 |
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

```yaml
# ScriptEntityPlus v1.2.3 Config #


## ===== 開発者向け ===== ##
# 基本的に開発者以外は設定を変更しないでください。
# オプションの正確なクラスパスを指定してください。
# オプション内で取得する座標をエンティティの座標へ書き換える機能です。
FilterOptions:
- 'com.github.yuttyann.scriptblockplus.script.option.chat.Command'
- 'com.github.yuttyann.scriptblockplus.script.option.chat.Console'
- 'com.github.yuttyann.scriptblockplus.script.option.chat.BypassOP'
- 'com.github.yuttyann.scriptblockplus.script.option.vault.BypassPerm'
- 'com.github.yuttyann.scriptblockplus.script.option.vault.BypassGroup'
- 'com.github.yuttyann.scriptblockplus.script.option.other.PlaySound'
```
</details>

<details>
<summary>message.yml</summary>

```yaml
# ScriptEntityPlus v1.2.3 Message #
# Author: yuttyann44581


# &(code) : カラーコード(以降の項目全て対象)

## ===== ScriptConnection ===== ##
# プレースホルダはありません
ScriptConnection:
- '&aこのツールは、エンティティに対するスクリプトの操作をサポートします。'
- '&d---------- [ メインハンド ] ----------'
- '&6左クリック: &eツールのモードを変更します。'
- '&6右クリック: &eエンティティにスクリプトを設定します。'
- '&6シフト+左クリック: &e指定したスクリプトを選択します。'
- '&6シフト+右クリック: &eエンティティのスクリプトを削除します。'
- '&d---------- [ オフハンド ] ----------'
- '&6右クリック: &eエンティティに設定されているスクリプトを表示します。'
- '&6シフト+右クリック: &eエンティティの設定を表示します。'

# |~, \n : 改行(以降の項目全て対象)

## ===== Messages ===== ##
# プレースホルダはありません
InvincibleTextMessage: '&bエンティティへのダメージを無効化する設定'
ProjectileTextMessage: '&b発射物によってスクリプトを実行する設定'

# %name%  : 設定の名前
# %value% : 設定の値
SettingValueMessage: '&a設定"&b&l%name%&r&a"の値は"&e%value%&a"に変更されました。'
SettingViewMessage: '&d設定"&b&l%name%&r&d"の値は"&e%value%&d"です。'

# %scriptkey% : スクリプトキー
ScriptSelectMessage: '&aスクリプト"%scriptkey%"を指定しました。'

# %toolmode%   : ツールのモード
# %entitytype% : エンティティの種類
ScriptSettingEntityMessage: '&aエンティティ"%entitytype%"に"%toolmode%"のスクリプトを設定しました。'
ScriptRemoveEntityMessage: '&cエンティティ"%entitytype%"のスクリプトを削除しました。'
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**ScriptEntityPlus v1.2.3**](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.2.3/ScriptEntityPlus%20v1.2.3.jar) | `1.9-1.20.1` | [`ScriptBlockPlus v2.2.6`](#連携プラグイン), `Java8` |

<details>
<summary>過去のバージョン</summary>

| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [ScriptEntityPlus v1.2.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.2.2/ScriptEntityPlus%20v1.2.2.jar) | `1.9-1.19.2` | [`ScriptBlockPlus v2.2.1`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.2.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.2.1/ScriptEntityPlus%20v1.2.1.jar) | `1.9-1.18` | [`ScriptBlockPlus v2.2.1`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.2.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.2.0/ScriptEntityPlus%20v1.2.0.jar) | `1.9-1.18` | [`ScriptBlockPlus v2.2.0`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.1.9](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.1.9/ScriptEntityPlus%20v1.1.9.jar) | `1.9-1.17.1` | [`ScriptBlockPlus v2.1.8`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.1.8](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.1.8/ScriptEntityPlus%20v1.1.8.jar) | `1.9-1.17.1` | [`ScriptBlockPlus v2.1.7`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.1.7](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.1.7/ScriptEntityPlus%20v1.1.7.jar) | `1.9-1.17.1` | [`ScriptBlockPlus v2.1.6`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.1.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.1.6/ScriptEntityPlus%20v1.1.6.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.1.4`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.1.5](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.1.5/ScriptEntityPlus%20v1.1.5.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.1.3`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.1.4](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.1.4/ScriptEntityPlus%20v1.1.4.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.1.2`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.1.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.1.3/ScriptEntityPlus%20v1.1.3.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.1.0`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.1.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.1.2/ScriptEntityPlus%20v1.1.2.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.0.9`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.1.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.1.1/ScriptEntityPlus%20v1.1.1.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.0.8`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.1.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.1.0/ScriptEntityPlus%20v1.1.0.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.0.7`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.0.9](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.0.9/ScriptEntityPlus%20v1.0.9.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.0.5`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.0.8](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.0.8/ScriptEntityPlus%20v1.0.8.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.0.4`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.0.7](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.0.7/ScriptEntityPlus%20v1.0.7.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.0.3`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.0.6](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.0.6/ScriptEntityPlus%20v1.0.6.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.0.2`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.0.5](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.0.5/ScriptEntityPlus%20v1.0.5.jar) | `1.9-1.16.5` | [`ScriptBlockPlus v2.0.1`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.0.4](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.0.4/ScriptEntityPlus%20v1.0.4.jar) | `1.9-1.16.2` | [`ScriptBlockPlus v2.0.0`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.0.3](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.0.3/ScriptEntityPlus%20v1.0.3.jar) | `1.9-1.15.2` | [`ScriptBlockPlus v1.9.3`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.0.2](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.0.2/ScriptEntityPlus%20v1.0.2.jar) | `1.9-1.15.2` | [`ScriptBlockPlus v1.9.3`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.0.1](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.0.1/ScriptEntityPlus%20v1.0.1.jar) | `1.9-1.15.2` | [`ScriptBlockPlus v1.9.3`](#連携プラグイン), `Java8` |
| [ScriptEntityPlus v1.0.0](https://github.com/yuttyann/FileArchive/raw/main/ScriptEntityPlus/jar/1.0.0/ScriptEntityPlus%20v1.0.0.jar) | `1.9-1.15.2` | [`ScriptBlockPlus v1.9.3`](#連携プラグイン), `Java8` |
</details>

連携プラグイン
-----------
| プラグイン | 実装 | 説明 |
|:---|:---|:---|
| [ScriptBlockPlus](https://github.com/yuttyann/FileArchive/tree/main/ScriptBlockPlus) | `1.0.0-1.2.3` | プラグインを動作させるために必要です。 |