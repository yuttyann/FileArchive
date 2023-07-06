GunScopeandRecoil
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
銃に上下リコイルとスコープ時の画像を追加する**Bukkitプラグイン**です。  
スコープの仕組みとしては**プレイヤーにかぼちゃを装備**させています。

コマンド
-----------
<details>
<summary>gunscopeandrecoil / gsr</summary>

| 名称 | 短縮 |
|:---|:---|
| gunscopeandrecoil | gsr |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| reload | gunscopeandrecoil.command.reload | OP | ファイルの再読み込みを行います。 |
</details>

<details>
<summary>setscope</summary>

| 名称 | 短縮 |
|:---|:---|
| setscope |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| &lt;weaponname&gt; | gunscopeandrecoil.command.setscope | OP | 指定した銃にスコープ時の画像を実装します。 |
</details>

<details>
<summary>setrecoil</summary>

| 名称 | 短縮 |
|:---|:---|
| setrecoil |  |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| &lt;weaponname&gt; &lt;height&gt; &lt;width&gt; | gunscopeandrecoil.command.setrecoil | OP | 指定した銃のリコイルを設定します。 |
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

**現在`UpdateChecker`は動作しません。**
```yaml
#GunScopeandRecoil v1.3 Config
#CompliantVersion 1.7.2～1.10

#バージョンチェック、ダウンロード
#このプラグインが最新バージョンかチェックします。
#メッセージはOPにしか表示されません。
# trueで有効 falseで無効
UpdateChecker: true
AutoDownload: true

#リコイルの設定
#AK-47 と書いてある場所に武器のタイトルを入力してください。
#height は縦反動です。
#width は横反動です。
Recoil:
  AK-47:
    height: 3.0
    width: 1.0

#スコープの設定
#AK-47 と書いてある場所に武器のタイトルを入力してください。
# - (武器のタイトル)
Scope:
- AK-47
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**GunScopeandRecoil v1.3**](https://github.com/yuttyann/FileArchive/raw/main/GunScopeandRecoil/1.3/GunScopeandRecoil%20v1.3.jar) | `1.7.2-1.10.2` | [CrackShot](https://dev.bukkit.org/projects/crackshot), `Java8` |
| [GunScopeandRecoil v1.2](https://github.com/yuttyann/FileArchive/raw/main/GunScopeandRecoil/1.2/GunScopeandRecoil%20v1.2.jar) | `1.7.2-1.8.9` | [CrackShot](https://dev.bukkit.org/projects/crackshot), `Java8` |
| [GunScopeandRecoil v1.1](https://github.com/yuttyann/FileArchive/raw/main/GunScopeandRecoil/1.1/GunScopeandRecoil%20v1.1.jar) | `1.7.2-1.8.9` | [CrackShot](https://dev.bukkit.org/projects/crackshot), `Java8` |
| ~~GunScopeandRecoil v1.0~~ | `1.7.2-1.8.9` | [CrackShot](https://dev.bukkit.org/projects/crackshot), `Java8` |