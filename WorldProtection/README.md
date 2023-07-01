WorldProtection
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
簡単な設定でワールドを保護することができる**Bukkitプラグイン**です。  

コマンド
-----------
<details>
<summary>wp</summary>

| 名称 | 短縮 |
|:---|:---|
| wp |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| reload | wp.reload | OP | ファイルの再読み込みを行います。 |
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

```yaml
#WorldProtection Config v1.1
#BukkitVersion 1.7.2～1.8.x

#TNTの爆発を無効化
# trueで有効 falseで無効
TNTExplosionCancel: false

#TNTの地形破壊を無効化
# trueで有効 falseで無効
TNTExplosionGuard: false

#ブロック設置をできなくするGameModeを設定できます。
# trueで有効 falseで無効
BlockSetCreative: false
BlockSetSurvival: true
BlockSetAdventure: true

#ブロック破壊をできなくするGameModeを設定できます。
# trueで有効 falseで無効
BlockBreakCreative: false
BlockBreakSurvival: true
BlockBreakAdventure: true

#絵画と額縁を破壊できなくするGameModeを設定できます。
# trueで有効 falseで無効
PaintingCreative: false
PaintingSurvival: true
PaintingAdventure: true

#額縁のアイテムを外せなくするGameModeを設定できます。
# trueで有効 falseで無効
PictureFrameItemCreative: false
PictureFrameItemSurvival: true
PictureFrameItemAdventure: true

#額縁のアイテムのアイテムを操作できなくするGameModeを設定できます。
# trueで有効 falseで無効
ItemFrameClickCreative: false
ItemFrameClickSurvival: true
ItemFrameClickAdventure: true
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**WorldProtection v1.1**](https://github.com/yuttyann/FileArchive/raw/main/WorldProtection/jar/1.1/WorldProtection%20v1.1.jar) | `1.7.2-1.8.x` | `Java8` |

<details>
<summary>過去のバージョン</summary>

| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| ~~WorldProtection v1.0~~ | `1.7.2-1.8.x` | `Java8` |
</details>