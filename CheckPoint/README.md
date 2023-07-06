CheckPoint
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
チェックポイントの保存と移動が可能になる**Bukkitプラグイン**です。  

コマンド
-----------
<details>
<summary>checkpoint / cp</summary>

| 名称 | 短縮 |
|:---|:---|
| checkpoint | cp |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| reload | checkpoint.command.reload | OP | ファイルの再読み込みを行います。 |
| set [player] | checkpoint.command.set | OP | チェックポイントを保存します。 |
| clear [player] | checkpoint.command.clear | OP | チェックポイントを削除します。 |
| tp [player] | checkpoint.command.tp | OP | チェックポイントにテレポートします。 |
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

**現在`UpdateChecker`は動作しません。**
```yaml
#CheckPoint v1.0 Config
#CompliantVersion 1.7.2～1.10
#ColorCodeList http://ess.khhq.net/mc/

#バージョンチェック、ダウンロード
#このプラグインが最新バージョンかチェックします。
#メッセージはOPにしか表示されません。
# trueで有効 falseで無効
UpdateChecker: true
AutoDownload: true

#チェックポイントの保存設定
#PlayerAir プレイヤーが空中にいる場合にチェックポイントを設定できるか。
# trueで有効 falseで無効
SaveCheckPoint:
  PlayerAir: false

#チェックポイントメッセージの設定
#&で色を指定できます。ColorCodeListのURL参照
#%playerでプレイヤーを取得します。
CheckPointMessage:
  NoneCheckPoint: '&cチェックポイントがありません。'
  PlayerAir: '&c空中に居る為設定に失敗しました。'
  Set: '&6チェックポイントを設定しました。'
  Clear: '&cチェックポイントを削除しました。'
  Tp: '&bチェックポイントに移動しました。'
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**CheckPoint v1.0**](https://github.com/yuttyann/FileArchive/raw/main/CheckPoint/jar/1.0/CheckPoint%20v1.0.jar) | `1.7.2-1.10.2` | `Java8` |