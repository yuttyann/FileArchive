CustomChat
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
プレイヤーのチャットをカスタムすることができる**Bukkitプラグイン**です。  

コマンド
-----------
<details>
<summary>customchat</summary>

| 名称 | 短縮 |
|:---|:---|
| customchat |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| reload | customchat.command.reload | OP | ファイルの再読み込みを行います。 |
| japanize &lt;on / off&gt; | customchat.command.japanize | OP | チャットの日本語化を設定します。 |
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

**現在`UpdateChecker`は動作しません。**
```yaml
# CustomChat v1.7 Config
# CompliantVersion 1.7.2～1.10
# ColorCodeList http://ess.khhq.net/mc/

## === 自動アップデートの設定 === ##
# [true で有効 | false で無効]
# 初期: true
# このプラグインが最新バージョンかチェックします。
# メッセージはOPにしか表示されません。
UpdateChecker: true
AutoDownload: true

## === カラーコードの設定 === ##
# [true で有効 | false で無効]
# 初期: true
# チャットに使用するカラーコードの設定です。
ChatColorCode:
  Enable: true
  ColorCode: '&'

## === 日本語化の設定 === ##
#DefaultJapanizeの設定
# [true で有効 | false で無効]
# 初期: true
# プレイヤーのデフォルト設定で日本語化を有効にするか。
# ログイン時に日本語化設定が無い場合にデフォルト設定が適用されます。
#JapanizeTypeの設定
# kana でローマ字変換
# kanzi でローマ字変換⇒漢字変換
#JapanizeFormatの設定
# & でカラーコードを使用できます。
# %japanize で日本語化チャットを取得できます。
DefaultJapanize: true
JapanizeType: kana
JapanizeFormat: '&7(%japanize)&r'

## === NGワードの設定 === ##
# [true で有効 | false で無効]
# 初期: true
#MessageTypeの設定
# broadcast サーバー全体にメッセージを送信します。
# send NGワードに引っかかったプレイヤーにメッセージを送信します。
#NGMessageの設定
# & でカラーコードを使用できます。
# %prefix でPrefixを取得します。
# %suffix でSuffixを取得します。
# %player でプレイヤーを取得します。
# %world でワールドを取得します。
# %message でプレイヤーのチャットを取得します。
NGword:
  Enable: true
  MessageType: send
  NGMessage: '&cNGワードが含まれています'

## === チャットグループの設定 === ##
#----------- 設定 -------------
# <グループ名>: <チャット>
#-----------------------------
# & でカラーコードを使用できます。
# %time で現在の時刻を取得します。
# %prefix でPrefixを取得します。
# %suffix でSuffixを取得します。
# %player でプレイヤーを取得します。
# %world でワールドを取得します。
# %message でプレイヤーのチャットを取得します。
# %addjapanize でJapanizeFormatの設定を取得します。
ChatGroups:
  Admin: '&4[Admin]&b%player: &f%message %addjapanize'
  Default: '<%player> %message'

## === プレイヤーの設定 === ##
#----------- 設定 -------------
# 通常プレイヤー:
# NormalPlayer: <チャットグループ>
# #指定したプレイヤー:
# Players:
#   <UUID>:
#     Groups: <チャットグループ>
#-----------------------------
NormalPlayers: Default
Players:
  6a0f004c-682f-4e35-9d89-faa21b4d2c29:
    Group: Admin
```
</details>

<details>
<summary>ngword.yml</summary>

```yaml
#NGワードに引っかからないワードの設定
Exception:
- 'だしね'
#NGワードの設定
NGword:
- 'しね'
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**CustomChat v1.7**](https://github.com/yuttyann/FileArchive/raw/main/CustomChat/jar/1.7/CustomChat%20v1.7.jar) | `1.7.2-1.10.2` | [`Vault`](https://www.spigotmc.org/resources/34315/), `Java8` |

<details>
<summary>過去のバージョン</summary>

| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [CustomChat v1.6](https://github.com/yuttyann/FileArchive/raw/main/CustomChat/jar/1.6/CustomChat%20v1.6.jar) | `1.7.2-1.10.2` | [`Vault`](https://www.spigotmc.org/resources/34315/), `Java8` |
| [CustomChat v1.5](https://github.com/yuttyann/FileArchive/raw/main/CustomChat/jar/1.5/CustomChat%20v1.5.jar) | `1.7.2-1.10.2` | [`Vault`](https://www.spigotmc.org/resources/34315/), `Java8` |
| [CustomChat v1.4](https://github.com/yuttyann/FileArchive/raw/main/CustomChat/jar/1.4/CustomChat%20v1.4.jar) | `1.7.2-1.10.2` | [`Vault`](https://www.spigotmc.org/resources/34315/), `Java8` |
| [CustomChat v1.3](https://github.com/yuttyann/FileArchive/raw/main/CustomChat/jar/1.3/CustomChat%20v1.3.jar) | `1.7.2-1.10.2` | [`Vault`](https://www.spigotmc.org/resources/34315/), `Java8` |
| [CustomChat v1.2](https://github.com/yuttyann/FileArchive/raw/main/CustomChat/jar/1.2/CustomChat%20v1.2.jar) | `1.7.2-1.10.2` | [`Vault`](https://www.spigotmc.org/resources/34315/), `Java8` |
| [CustomChat v1.1](https://github.com/yuttyann/FileArchive/raw/main/CustomChat/jar/1.1/CustomChat%20v1.1.jar) | `1.7.2-1.8.9` | [`Vault`](https://www.spigotmc.org/resources/34315/), `Java8` |
| ~~CustomChat v1.0~~ | `1.7.2-1.8.9` | [`Vault`](https://www.spigotmc.org/resources/34315/), `Java8` |
</details>