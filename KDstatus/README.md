KDstatus
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
キル/デス数を保存するシステムを追加する**Bukkitプラグイン**です。  

コマンド
-----------
<details>
<summary>mystatus</summary>

| 名称 | 短縮 |
|:---|:---|
| mystatus |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
|  | kdstatus.command.status | OP | ステータスを表示します。 |
</details>

<details>
<summary>kdranking</summary>

| 名称 | 短縮 |
|:---|:---|
| kdranking |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| &lt;top&gt; | kdstatus.command.status | OP | ランキングを表示します。 |
</details>

<details>
<summary>kdstatus</summary>

| 名称 | 短縮 |
|:---|:---|
| kdstatus |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| reload | kdstatus.command.status | OP | ファイルの再読み込みを行います。 |
| &lt;player&gt; setkills &lt;amount&gt; | kdstatus.command.status | OP | PVP-Killsを設定します。 |
| &lt;player&gt; setdeaths &lt;amount&gt; | kdstatus.command.status | OP | PVP-Deathsを設定します。 |
| &lt;player&gt; setalldeaths &lt;amount&gt; | kdstatus.command.status | OP | All-Deathsを設定します。 |
| &lt;player&gt; setkdr &lt;amount&gt; | kdstatus.command.status | OP | PVP-KDRを設定します。 |
| &lt;player&gt; setallkdr &lt;amount&gt; | kdstatus.command.status | OP | All-KDRを設定します。 |
</details>

ファイル
-----------
<details>
<summary>items.yml</summary>

```yaml
ItemDrop: true
items:
  gold_apple:
    MaterialId: 322
    Meta: 0
    Amount: 1
```

### 記述方法
```yaml
# trueの場合はアイテムがその場にドロップし、falseの場合は直接インベントリに付与されます。
ItemDrop: true

# アイテムの一覧です。複数追加可能です。
items:
  # 任意のIDを記述してください。
  gold_apple:
    # アイテムID
    MaterialId: 322
    # アイテムのメタデータ
    Meta: 0
    # アイテムの個数
    Amount: 1
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**KDstatus v1.2**](https://github.com/yuttyann/FileArchive/raw/main/KDstatus/jar/1.2/KDstatus%20v1.2.jar) | `1.8-1.9.x` | `Java8` |

<details>
<summary>過去のバージョン</summary>

| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [KDstatus v1.1](https://github.com/yuttyann/FileArchive/raw/main/KDstatus/jar/1.1/KDstatus%20v1.1.jar) | `1.8-1.8.x` | `Java8` |
| ~~KDstatus v1.0~~ | `1.8-1.8.x` | `Java8` |
</details>