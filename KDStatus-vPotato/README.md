KDStatus-vPotato
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
**このプラグインはポテトさんの依頼により作成されています。**  
PVP/PVEのキル/デス数を保存するシステムを追加する**Bukkitプラグイン**です。  

コマンド
-----------
<details>
<summary>kdstatus / kds</summary>

| 名称 | 短縮 |
|:---|:---|
| kdstatus | kds |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| reload | kdstatus.command.reload | OP | ファイルの再読み込みをします。 |
| ranking &lt;pvp / pve&gt; [top] | kdstatus.command.ranking | OP | ランキングを表示します。 |
| status [player] | kdstatus.command.status | OP | ステータスを表示します。 |
| set pvpkills &lt;player&gt; &lt;amount&gt; | kdstatus.command.set | OP | PVP-Killsを設定します。 |
| set pvpdeaths &lt;player&gt; &lt;amount&gt; | kdstatus.command.set | OP | PVP-Deathsを設定します。 |
| set pvekills &lt;player&gt; &lt;amount&gt; | kdstatus.command.set | OP | PVE-Killsを設定します。 |
| set pvedeaths &lt;player&gt; &lt;amount&gt; | kdstatus.command.set | OP | PVE-Deathsを設定します。 |
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

```yaml
# KDStatus v1.0.1 Config #
Drop: true

Items:
  gold_apple:
    Material: GOLDEN_APPLE
    Damage: 0
    Amount: 1
```

### 記述方法
```yaml
# trueの場合はアイテムがその場にドロップし、falseの場合は直接インベントリに付与されます。
Drop: true

# アイテムの一覧です。複数追加可能です。
Items:
  # 任意のIDを記述してください。
  gold_apple:
    # アイテムID
    Material: GOLDEN_APPLE
    # アイテムのメタデータ
    Damage: 0
    # アイテムの個数
    Amount: 1
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**KDStatus-vPotato v1.0.1**](https://github.com/yuttyann/FileArchive/raw/main/KDStatus-vPotato/jar/1.0.1/KDStatus-vPotato%20v1.0.1.jar) | `1.8-1.14.4` | `Java8` |

<details>
<summary>過去のバージョン</summary>

| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [KDStatus-vPotato v1.0.0](https://github.com/yuttyann/FileArchive/raw/main/KDStatus-vPotato/jar/1.0.0/KDStatus-vPotato%20v1.0.0.jar) | `1.8-1.14.4` | `Java8` |
</details>