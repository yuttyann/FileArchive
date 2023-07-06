SignEditor
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
再設置を行わずに看板を編集することができる**Bukkitプラグイン**です。  

コマンド
-----------
<details>
<summary>signeditor</summary>

| 名称 | 短縮 |
|:---|:---|
| signeditor |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| set &lt;0&gt; &lt;1&gt; &lt;2&gt; &lt;3&gt; | signeditor.command | OP | 実行後に看板をクリックすることで編集が完了します。 |
| remove | signeditor.command | OP | `/signeditor set ...`実行をキャンセルします。 |

`set <0> <1> <2> <3>`にはカラーコード(&)が使用可能な他、下記のプレースホルダを利用できます。  
**`%clear`** 既存の文字を削除することができます。  
**`%blank`** 空白` `に置換します。  
**`%null`** 既存の文字に置換します。  
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

**現在`UpdateChecker`は動作しません。**
```yaml
#SignEditor v1.2 Config
#BukkitVersion 1.7.2～1.9.2

#バージョンチェック、ダウンロード
#このプラグインが最新バージョンかチェックします。
#メッセージはOPにしか表示されません。
# trueで有効 falseで無効
UpdateChecker: true
AutoDownload: true
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**SignEditor v1.2**](https://github.com/yuttyann/FileArchive/raw/main/SignEditor/jar/1.2/SignEditor%20v1.2.jar) | `1.7.2-1.9.4` | `Java8` |

<details>
<summary>過去のバージョン</summary>

| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [SignEditor v1.1](https://github.com/yuttyann/FileArchive/raw/main/SignEditor/jar/1.1/SignEditor%20v1.1.jar) | `1.7.2-1.8.9` | `Java8` |
| ~~SignEditor v1.0~~ | `1.7.2-1.8.9` | `Java8` |
</details>