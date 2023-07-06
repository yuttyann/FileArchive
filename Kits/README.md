Kits
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
任意の組み合わせのアイテムの保存と呼び出しが可能になる**Bukkitプラグイン**です。  
<details>
<summary>使い方</summary>

### kits.yml の記述方法
```yaml
KitNames: /kits で表示されるメッセージ
Kits:
  # キットの名前です。コマンド等で呼び出す際に利用されます。
  Test:
    # キットの値段です。経済系プラグインを導入している際に利用できます。
    Cost: 1000
    # アイテムの一覧です。構文の"Items"は固定です。
    Items:
      # アイテムの設定 構文"item1"は任意の文字列でも構いません。
      item1:
        # アイテムの名称です。"MaterialId"とすることでアイテムのIDで指定することも可能です。
        Material: IRON_SWORD
        # メタデータです。
        Meta: 0
        # アイテムの個数です。
        Amount: 1
        # アイテムフラグです。各パラメータの表示/非表示を行うことが可能です。
        ItemFrag:
        - HIDE_ENCHANTS
        # アイテムのエンチャントです。"(エンチャントID)-(レベル)"で指定することが可能です。
        Enchant:
        - KNOCKBACK-1 
        # アイテムの名前です。頭文字"&"のカラーコードが使用可能です。
        DisplayName: '&a鉄の剣'
        # アイテムの説明文です。頭文字"&"のカラーコードが使用可能です。
        Lore:
        - '&c鉄の剣です。'
        # 本の内容の設定です。
        Book:
          # 本の作者
          Author: 作者
          # 本のタイトル
          Title: タイトル
          # 本の各ページの内容
          Pages:
          - "1"
          - "2"
          - "3"
        # 耐久値を持つアイテムを消耗させない場合は"true"を記述してください。
        Unbreakable: true
        # ポーションのエフェクトのデータタグです。giveコマンドのデータタグと同等です。
　　　 　CustomPotionEffects:
        - '{"Amplifier":値,"Ambient":値,"Duration":値,"Id":値,"ShowParticles":値}'
        # 属性値のデータタグです。giveコマンドのデータタグと同等です。
        AttributeModifiers:
        - '{"Name":値,"Amount":値,"Operation":値,"UUIDLeast":値,"UUIDMost":値,"AttributeName":値}'
    # 防具の一覧です。構文の"Armors"は固定です。
    Armors:
      # ヘルメットです。構文の"Helmet"は固定です。
      Helmet:
        Material: LEATHER_HELMET
        Amount: 1
        # RGBを利用することで、皮防具等の色を変更することができます。
        Color:
          Red: 0
          Green: 0
          Blue: 255
      # チェストプレートです。構文の"ChestPlate"は固定です。
      ChestPlate:
        MaterialId: 307
        Amount: 1
      # レギンスです。構文の"Leggings"は固定です。
      Leggings:
        MaterialId: 308
        Amount: 1
      # ブーツです。構文の"Boots"は固定です。
      Boots:
        MaterialId: 309
        Amount: 1
```

### 看板 の記述方法
**通常**
```
1     [Kits]
2       
3     <name>
```

**装備を保存する**
```
1     [Kits]
2
3     KitSave
```

**装備を呼び出す**
```
1     [Kits]
2
3     KitLoad
```

**経済系プラグイン導入時のみ**
```
1     [Kits]
2
3     <name>
4     <価格を非表示にする場合"true"を記述してください ※1>
```
`※1 価格を非表示にした場合はコスト無しで購入することが可能です。`

#### 記述例
![Sign](https://github.com/yuttyann/FileArchive/blob/main/Kits/image/sign.png?raw=true)
</details>

権限
-----------
<details>
<summary>一覧</summary>

| 権限 | 説明 |
|:---|:---|
| kits.command.view | [コマンド](#コマンド) |
| kits.command.reload | [コマンド](#コマンド) |
| kits.command.setcost | [コマンド](#コマンド) |
| kits.command.create | [コマンド](#コマンド) |
| kits.command.give.&lt;name&gt; | [コマンド](#コマンド) |
| kits.command.purchase.&lt;name&gt; | [コマンド](#コマンド) |
| kits.sign.create | 専用の看板を作成するために必要です。 |
| kits.sign.kitsave | 看板で装備を保存するために必要です。 |
| kits.sign.kitload | 看板で装備を呼び出すために必要です。 |
| kits.sign.purchase.&lt;name&gt; | 看板で指定したキットを呼び出すために必要です。 |
</details>

コマンド
-----------
<details>
<summary>kits</summary>

| 名称 | 短縮 |
|:---|:---|
| kits |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
|  | kits.command.view | OP | キットの一覧を表示します。 |
| reload | kits.command.reload | OP | ファイルの再読み込みを行います。 |
| setcost &lt;name&gt; &lt;cost&gt; | kits.command.setcost | OP | 指定したキットに購入額を設定します。 |
| create &lt;name&gt; [cost] | kits.command.create | OP | インベントリのアイテムでキットを作成します。 |
| give &lt;player&gt; &lt;name&gt; | kits.command.give.&lt;name&gt; | OP | 指定したプレイヤーにキットを与えます。 |
| purchase &lt;name&gt; | kits.command.purchase.&lt;name&gt; | OP | 指定したキットを購入します。 |
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

```yaml
# Kits v1.0 Config

## === キット購入時に表示される通貨名 === ##
Currency: '円'
## === キットを購入したら次回以降はお金を払わなくてもいいようにするか === ##
SavePurchasePlayers: false
## === インベントリのアイテムをキットで保存した際にアイテムのないスロットも保存するか === ##
InventoryAir: false
## === キットを受け取るたびにインベントリのアイテムを削除するか === ##
KitItemClear: false
## === セーブキットを読み込むたびにインベントリのアイテムを削除するか === ##
LoadItemClear: true
```
</details>

<details>
<summary>kits.yml</summary>

```yaml
KitNames: '&aキット一覧: &6Hunter, Warrior'
Kits:
  Hunter:
    Cost: 1200
    Items:
      bow:
        Material: BOW
        Amount: 1
        Enchant:
        - ARROW_KNOCKBACK-1
      sword:
        MaterialId: 272
        Amount: 1
      pork:
        MaterialId: 320
        Amount: 32
      arrow:
        MaterialId: 262
        Amount: 64
    Armors:
      Helmet:
        MaterialId: 306
        Amount: 1
        Enchant:
        - PROTECTION_ENVIRONMENTAL-1
        DisplayName: '&f鉄のヘルメット'
        Lore: 
        - '&e鉄のヘルメットです。'
      ChestPlate:
        MaterialId: 307
        Amount: 1
      Leggings:
        MaterialId: 308
        Amount: 1
      Boots:
        MaterialId: 309
        Amount: 1
  Warrior:
    Cost: 1500
    Items:
      sword:
        MaterialId: 267
        Amount: 1
        Enchant:
        - DAMAGE_ALL-1
      pork:
        MaterialId: 320
        Amount: 32
      potion:
        MaterialId: 373
        Amount: 1
        Meta: 8229
    Armors:
      Helmet:
        MaterialId: 306
        Amount: 1
        Enchant:
        - PROTECTION_ENVIRONMENTAL-1
      ChestPlate:
        MaterialId: 307
        Amount: 1
      Leggings:
        MaterialId: 308
        Amount: 1
      Boots:
        MaterialId: 309
        Amount: 1
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**Kits v1.0**](https://github.com/yuttyann/FileArchive/raw/main/Kits/jar/1.0/Kits%20v1.0.jar) | `1.7.2-1.12.2` | [`Vault`](https://www.spigotmc.org/resources/34315/), `Java8` |