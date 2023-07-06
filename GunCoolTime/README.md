GunCoolTime
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
銃を持ち替えた際のクールタイムを追加する**Bukkitプラグイン**です。  

コマンド
-----------
<details>
<summary>settime</summary>

| 名称 | 短縮 |
|:---|:---|
| settime |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| &lt;tick&gt; | gct.settime | OP | クールタイムを設定します。 |
</details>

<details>
<summary>setweapon</summary>

| 名称 | 短縮 |
|:---|:---|
| setweapon |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| &lt;weponname&gt; &lt;enable&gt; | gct.setweapon | OP | 指定した銃のクールタイムの有無を設定します。 |
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

サウンドの設定方法は"**(サウンド:ID)-(ボリューム:0-2)-(ピッチ0-2)-(ディレイ:Tick)**"です。
```yaml
Time: 20
Sounds:
  Slot0: FIRE_IGNITE-1-1-17,HURT_FLESH-1-0-18,DOOR_CLOSE-1-2-19
  Slot1: FIRE_IGNITE-1-1-17,HURT_FLESH-1-0-18,DOOR_CLOSE-1-2-19
  Slot2: FIRE_IGNITE-1-1-17,HURT_FLESH-1-0-18,DOOR_CLOSE-1-2-19
  Slot3: FIRE_IGNITE-1-1-17,HURT_FLESH-1-0-18,DOOR_CLOSE-1-2-19
  Slot4: FIRE_IGNITE-1-1-17,HURT_FLESH-1-0-18,DOOR_CLOSE-1-2-19
  Slot5: FIRE_IGNITE-1-1-17,HURT_FLESH-1-0-18,DOOR_CLOSE-1-2-19
  Slot6: FIRE_IGNITE-1-1-17,HURT_FLESH-1-0-18,DOOR_CLOSE-1-2-19
  Slot7: FIRE_IGNITE-1-1-17,HURT_FLESH-1-0-18,DOOR_CLOSE-1-2-19
  Slot8: FIRE_IGNITE-1-1-17,HURT_FLESH-1-0-18,DOOR_CLOSE-1-2-19
Weapons:
  AK-47:
    CoolTime: true
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**GunCoolTime v1.2**](https://github.com/yuttyann/FileArchive/raw/main/GunCoolTime/jar/1.2/GunCoolTime%20v1.2.jar) | `1.7.2-1.8.9` | [CrackShot](https://dev.bukkit.org/projects/crackshot), `Java8` |

<details>
<summary>過去のバージョン</summary>

| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| ~~GunCoolTime v1.1~~ | `1.7.2-1.8.9` | [CrackShot](https://dev.bukkit.org/projects/crackshot), `Java8` |
| ~~GunCoolTime v1.0~~ | `1.7.2-1.8.9` | [CrackShot](https://dev.bukkit.org/projects/crackshot), `Java8` |
</details>