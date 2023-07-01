MetaandBlockChanger
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
ブロックのメタデータを変更やコピー・ペーストが可能になる**Bukkitプラグイン**です。  
利用方法は各ツールの説明文に記述されています。  

権限
-----------
<details>
<summary>一覧</summary>

| 権限 | 説明 |
|:---|:---|
| metaandblockchanger.command.gettool | [コマンド](#コマンド) |
| metaandblockchanger.metadatachanger | MetaDataChangerを利用するために必要です。 |
| metaandblockchanger.replacetool | ReplaceToolを利用するために必要です。 |
</details>

コマンド
-----------
<details>
<summary>gettool</summary>

| 名称 | 短縮 |
|:---|:---|
| gettool |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
|  | metaandblockchanger.command.gettool | OP | MetaDataChangerとReplaceToolを入手します。 |
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

```yaml
Enable_MetaDataChanger: true
Enable_ReplaceTool: true
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**MetaandBlockChanger v1.1**](https://github.com/yuttyann/FileArchive/raw/main/MetaandBlockChanger/jar/1.1/MetaandBlockChanger%20v1.1.jar) | `1.7.2-1.8.x` | `Java8` |
| ~~MetaandBlockChanger v1.0~~ | `1.7.2-1.8.x` | `Java8` |