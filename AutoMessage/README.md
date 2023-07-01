AutoMessage
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
任意のメッセージを定期的に送信することができる**Bukkitプラグイン**です。

コマンド
-----------
<details>
<summary>automessage / am</summary>

| 名称 | 短縮 |
|:---|:---|
| automessage | am |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| message &lt;message&gt; | automessage.message | OP | メッセージを追加します。 |
| timer &lt;second&gt; | automessage.timer | OP | タイマーの秒数を設定します。 |
| reload | automessage.reload | OP | コンフィグの再読み込みを行います。 |
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

**現在`UpdateChecker`は動作しません。**
```yaml
# AutoMessage v1.7 Config
# ColorCodeList http://ess.khhq.net/mc/

## === 自動アップデートの設定 === ##
# [true で有効 | false で無効]
# 初期: true
# このプラグインが最新バージョンかチェックします。
# メッセージはOPにしか表示されません。
UpdateChecker: true
AutoDownload: true

## === オートメッセージの設定 === ##
# 設定したメッセージがランダムで表示されます。
# & でカラーコードを使用できます。
# %tellraw でtellrawコマンドを実行します。
# %line で改行することができます。(tellraw コマンドでは使用できません。)
Message:
  - '&aテスト1'
  - '&eテスト2'
  - '&cテスト3'
  - '%tellraw {"text":"tellraw テストメッセージです"}'

## === ログの設定 === ##
# ログの表示設定です。
Log: true

## === タイマーの設定 === ##
# メッセージが表示されるまでの時間の設定です。
Seconds: 60
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**AutoMessage v1.7**](https://github.com/yuttyann/FileArchive/raw/main/AutoMessage/jar/1.7/AutoMessage%20v1.7.jar) | `1.7.2-1.12.x` | `Java8` |

<details>
<summary>過去のバージョン</summary>

| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [AutoMessage v1.6](https://github.com/yuttyann/FileArchive/raw/main/AutoMessage/jar/1.6/AutoMessage%20v1.6.jar) | `1.7.2-1.12.x` | `Java8` |
| [AutoMessage v1.5](https://github.com/yuttyann/FileArchive/raw/main/AutoMessage/jar/1.5/AutoMessage%20v1.5.jar) | `1.7.2-1.12.x` | `Java8` |
| [AutoMessage v1.4](https://github.com/yuttyann/FileArchive/raw/main/AutoMessage/jar/1.4/AutoMessage%20v1.4.jar) | `1.7.2-1.12.x` | `Java8` |
| [AutoMessage v1.3](https://github.com/yuttyann/FileArchive/raw/main/AutoMessage/jar/1.3/AutoMessage%20v1.3.jar) | `1.7.2-1.9.x` | `Java8` |
| [AutoMessage v1.2](https://github.com/yuttyann/FileArchive/raw/main/AutoMessage/jar/1.2/AutoMessage%20v1.2.jar) | `1.7.2-1.8.x` | `Java8` |
| [AutoMessage v1.1](https://github.com/yuttyann/FileArchive/raw/main/AutoMessage/jar/1.1/AutoMessage%20v1.1.jar) | `1.7.2-1.8.x` | `Java8` |
| ~~AutoMessage v1.0~~ | `1.7.2-1.8.x` | `Java8` |
</details>