CustomMessage
==========

## 留意事項
古い仕様のプラグインであるため、基本的に修正や機能追加等のアップデートは行いません。  
また、最新のバージョンの情報を記載しています。

概要
-----------
ゲーム内の様々なメッセージを変更することができる**Bukkitプラグイン**です。  

権限
-----------
<details>
<summary>一覧</summary>

| 権限 | 説明 |
|:---|:---|
| custommessage.command.reload | [コマンド](#コマンド) |
| custommessage.command.rules | [コマンド](#コマンド) |
| custommessage.command.title | [コマンド](#コマンド) |
| custommessage.command.tabtitle | [コマンド](#コマンド) |
| custommessage.sound.kill | キル時のサウンドの再生権限です。 |
| custommessage.sound.death | デス時のサウンドの再生権限です。 |
| custommessage.sound.firstjoin | 初参加時のサウンドの再生権限です。 |
| custommessage.sound.join | 参加時のサウンドの再生権限です。 |
| custommessage.sound.quit | 退出時のサウンドの再生権限です。 |
| custommessage.sound.chat | チャット時のサウンドの再生権限です。 |
| custommessage.sound.command | コマンド時のサウンドの再生権限です。 |
| custommessage.sound.ban | BAN時のサウンドの再生権限です。 |
| custommessage.sound.kick | キック時のサウンドの再生権限です。 |
| custommessage.sound.afk | 放置キック時のサウンドの再生権限です。 |
</details>

コマンド
-----------
<details>
<summary>custommessage / cmg</summary>

| 名称 | 短縮 |
|:---|:---|
| custommessage | cmg |

| 引数 | 権限 | 初期 | 説明 |
|:---|:---|:---|:---|
| reload | custommessage.command.reload | OP | ファイルの再読み込みを行います。 |
| rules | custommessage.command.rules | OP | 設定したルールを表示します。 |
| title [player] [title] [subtitle] | custommessage.command.title | OP | 指定したプレイヤーにタイトルを表示します。 |
| tabtitle [player] [header] [footer] | custommessage.command.tabtitle | OP | 指定したプレイヤーにタブタイトルを表示します。 |

`[header]`、`[footer]`では`%blank`が利用可能であり空白に置換することができます。
</details>

ファイル
-----------
<details>
<summary>config.yml</summary>

```yaml
# CustomMessage Config #

## === SpigotProtocolHack1.7-1.8 === ##
# [true で有効 | false で無効]
# 初期: false
#SpigotProtocolHack1.7-1.8を使用している場合は有効にしてください。
UseSpigotProtocolHack: false

## === メッセージの設定 === ##
# [trueで有効 | falseで無効]
# 初期: true
# メッセージの左側にプラグイン名を表示します。
MessagePrefix: true

## === 曜日表記の設定 === ##
# ここに設定した曜日は%weekで使用されます。
Sunday: '日'
Monday: '月'
Tuesday: '火'
Wednesday: '水'
Thursday: '木'
Friday: '金'
Saturday: '土'

## === 時刻の設定 === ##
# & でカラーコードを使用できます。
# %year で現在の年を取得します。
# %month で現在の月を取得します。
# %day で現在の日にちを取得します。
# %hour で現在の時を取得します。
# %minute で現在の分を取得します。
# %second で現在の秒を取得します。
# %week で現在の曜日を取得します。
# %dayofyear で現在の年の何日目かを取得します。
TimesofDay: '&e%year年%month月%day日%week曜日 %hour時%minute分%second秒'

## === プレイヤーカウントメッセージの設定 === ##
# [true で有効 | false で無効]
# 初期: false
# & でカラーコードを使用できます。
# none でカーソルを合わせても接続中のプレイヤーIdが表示されなくなります。
# %players でサーバーに接続している人数を取得します。
# %maxplayers で最大接続人数を取得します。
# %servername でサーバー名を取得します。
# %version でサーバーのバージョンを取得します。
# %time でTimesofDayに設定した時刻を取得します。
PlayerCountMessage:
  Enable: false
  Message:
  - '&aMinecraft1'
  - '&cMinecraft2'
  - '&eMinecraft3'

## === 最大接続人数の設定 === ##
# [true で有効 | false で無効]
# 初期: true
# 最大接続人数の表示を変更しているだけなので、実際に入れる人数は変わりません。
FakeMaxPlayer:
  Enable: true
  MaxPlayer: 999

## === サウンドの設定 === ##
# 発生するイベント名は多少略しています。
# イベントが発生するタイミングの説明です。
# | PlayerKickEvent - プレイヤーがキックされた時発生
# | PlayerDeathEvent - プレイヤーが死亡した時発生
# | PlayerJoinEvent - プレイヤーがログインした時発生
# | PlayerQuitEvent - プレイヤーがログアウトした時発生
# | PlayerChatEvent - プレイヤーが発言した時発生
# | PlayerCommandEvent - プレイヤーがコマンドを実行した時発生
# 音を追加したいときは設定の最後に,を入れてください。
# 1.8以前と1.9以降で(音の種類)が変わります。
# 1.9以降の場合はSoundListを参照してください。
# 1.8以前の場合はOldSoundListを参照してください。
# 音設定 (音の種類)-(音量)-(音の高さ)-(音が鳴る時間)
# none で音を無効化できます。
Sounds:
  PlayerKickEvent_KickSound: none
  PlayerKickEvent_BanSound: none
  PlayerKickEvent_AFKSound: none
  PlayerDeathEvent_KillSound: none
  PlayerDeathEvent_DeathSound: none
  PlayerJoinEvent_FirstSound: none
  PlayerJoinEvent_JoinSound: none
  PlayerQuitEvent_QuitSound: none
  PlayerChatEvent_ChatSound: CHICKEN_EGG_POP-1-1-0
  PlayerCommandEvent_CommandSound: none

## === サウンドタイプの設定 === ##
# player でイベントを発生させたプレイヤーに音を再生します。
# allplayers で接続しているプレイヤー全員に音を再生します。
SoundTypes:
  PlayerKickEvent_KickSoundType: player
  PlayerKickEvent_BanSoundType: player
  PlayerKickEvent_AFKSoundType: player
  PlayerDeathEvent_KillSoundType: player
  PlayerDeathEvent_DeathSoundType: player
  PlayerJoinEvent_FirstSoundType: player
  PlayerJoinEvent_JoinSoundType: player
  PlayerQuitEvent_QuitSoundType: player
  PlayerChatEvent_ChatSoundType: allplayers
  PlayerCommandEvent_CommandSoundType: player

## === サウンド権限の設定 === ##
# none で全てのプレイヤーに音を再生できます。
# operator でオペレーター権限を持っている人のみ音を再生できます。
# permission でパーミッション権限を持っている人のみ音を再生できます。
SoundAuthoritys:
  PlayerKickEvent_KickSoundAuthority: none
  PlayerKickEvent_BanSoundAuthority: none
  PlayerKickEvent_AFKSoundAuthority: none
  PlayerDeathEvent_KillSoundAuthority: none
  PlayerDeathEvent_DeathSoundAuthority: none
  PlayerJoinEvent_FirstSoundAuthority: none
  PlayerJoinEvent_JoinSoundAuthority: none
  PlayerQuitEvent_QuitSoundAuthority: none
  PlayerChatEvent_ChatSoundAuthority: operator
  PlayerCommandEvent_CommandSoundAuthority: none

## === 死亡メッセージの設定 === ##
# [true で有効 | false で無効]
# 初期: false
# & でカラーコードを使用できます。
# %deader で殺害されたプレイヤーを取得します。
# %killer で殺害したプレイヤー、エンティティを取得します。(殺害メッセージのみ使用可能です。)
# %deadercoords で殺害されたプレイヤーの座標を取得します。
# %killercoords で殺害したプレイヤー、エンティティの座標を取得します。(殺害メッセージのみ使用可能です。)
# %world でワールド名を取得します。
# %weapon で殺害したプレイヤーの武器を取得します。(Playerのみ使用可能です。)
# %time でTimesofDayに設定した時刻を取得します。
DeathMessage:
  Enable: false
  Weapon:
    NullMessage: '素手'
  Messages:
    Drowning: '&c%deaderは死亡しました。死因: 水'
    Fire: '&c%deaderは死亡しました。死因: 炎'
    Fall: '&c%deaderは死亡しました。死因: 落下'
    Void: '&c%deaderは死亡しました。死因: 奈落'
    Lava: '&c%deaderは死亡しました。死因: 溶岩'
    Magic: '&c%deaderは死亡しました。死因: 魔法'
    Suffocation: '&c%deaderは死亡しました。死因: 窒息'
    Projectile: '&c%deaderは死亡しました。死因: 飛び道具'
    Starvation: '&c%deaderは死亡しました。死因: 飢餓'
    Withered: '&c%deaderは死亡しました。死因: ウィザー'
    Explosion: '&c%deaderは死亡しました。死因: 爆発'
    Player: '&c%deaderは%killerに%weaponで殺害されました。'
    ZombiePigman: '&c%deaderはゾンビピッグマンに殺害されました。'
    Zombie: '&c%deaderはゾンビに殺害されました。'
    Husk: '&c%deaderはハスクに殺害されました。'
    CaveSpider: '&c%deaderは洞窟グモに殺害されました。'
    Spider: '&c%deaderはクモに殺害されました。'
    SilverFish: '&c%deaderはシルバーフィッシュに殺害されました。'
    Slime: '&c%deaderはスライムに殺害されました。'
    MagmaCube: '&c%deaderはマグマキューブに殺害されました。'
    EnderMite: '&c%deaderはエンダーマイトに殺害されました。'
    Enderman: '&c%deaderはエンダーマンに殺害されました。'
    EnderDragon: '&c%deaderはエンダードラゴンに殺害されました。'
    IronGolem: '&c%deaderはアイアンゴーレムに殺害されました。'
    Wolf: '&c%deaderはオオカミに殺害されました。'
    PolarBear: '&c%deaderはシロクマに殺害されました。'
    Giant: '&c%deaderはジャイアントに殺害されました。'
    Guardian: '&c%deaderはガーディアンに殺害されました。'
    Wither: '&c%deaderはウィザーに殺害されました。'
    Witch: '&c%deaderはウィッチに殺害されました。'
    Blaze: '&c%deaderはブレイズに殺害されました。'
    Ghast: '&c%deaderはガストに殺害されました。'
    Stray: '&c%deaderはストレイに殺害されました。'
    Skeleton: '&c%deaderはスケルトンに殺害されました。'
    WitherSkeleton: '&c%deaderはウィザースケルトンに殺害されました。'

## === ログイン、ログアウトメッセージの設定 === ##
# [true で有効 | false で無効]
# 初期: true
# & でカラーコードを使用できます。
# %player でプレイヤーを取得します。
# %time でTimesofDayに設定した時刻を取得します。
PlayerJoinQuitMessage:
  Enable: true
  FirstJoinMessage: '&e%playerさんが初めてサーバーに参加しました。'
  JoinMessage: '&e%playerさんがサーバーに参加しました。'
  QuitMessage: '&e%playerさんがサーバーから退出しました。'

## === ログインメッセージの設定 === ##
# [true で有効 | false で無効]
# 初期: false
# & でカラーコードを使用できます。
# %player でプレイヤーを取得します。
# %time でTimesofDayに設定した時刻を取得します。
PlayerLoginMessage:
  Enable: false
  Message:
  - 'アップデート情報: テストです。'

## === アイテム配布の設定 === ##
# [true で有効 | false で無効]
# 初期: false
# Kits導入時のみ動作します。
# キット名を指定することで初ログイン時に配布されます。
FirstJoinItem:
  Enable: false
  KitName: Hunter

## === チャットの設定 === ##
# [true で有効 | false で無効]
# 初期: false
# & でカラーコードを使用できます。
# %player でプレイヤーを取得します。
# %message でプレイヤーのチャットを取得します。
# %time でTimesofDayに設定した時刻を取得します。
ChatMessageFormat:
  Enable: false
  Message: '<&e%player&f> %message'

## === キックメッセージの設定 === ##
# [true で有効 | false で無効]
# 初期: false
# BroadcastMessageはサーバー全体に流れるメッセージです。
# & でカラーコードを使用できます。
# none でメッセージの設定を無効化できます。
# %player でプレイヤーを取得します。
# %reason で理由を取得できます。
# %line で改行することができます。(BroadcastMessage以外で使用可能)
# %time でTimesofDayに設定した時刻を取得します。
PlayerKickMessage:
  Enable: false
  BanMessage: '&cあなたはBanされました。'
  KickMessage: '&eあなたはKickされました。'
  AFKMessage: '&c放置していたためKickされました！'
  BanBroadcastMessage: '&c%playerさんがBanされました！'
  KickBroadcastMessage: '&c%playerさんがKickされました！'
  AFKBroadcastMessage: '&c%playerさんが放置していたためKickされました！'

## === ログインキックメッセージの設定 === ##
# [true で有効 | false で無効]
# 初期: false
# & でカラーコードを使用できます。
# %player でプレイヤーを取得します。
# %line で改行することができます。
# %time でTimesofDayに設定した時刻を取得します。
PlayerLoginKickMessage:
  Enable: false
  BanMessage: '&cBANされているためログインできません。'
  WhiteListMessage: 'ホワイトリストが有効になっているためログインできません。'

## === サーバールールの設定 === ##
# [true で有効 | false で無効]
# 初期: false
# & でカラーコードを使用できます。
Rules:
  Enable: false
  Message:
  - '&b---------&aサーバールール&b---------'
  - '&e楽しんでください'
  - '&e挨拶をしてください'

## === タイトルの表示時間などの設定 === ##
# FadeIn 表示するまでの時間
# Stay 表示している時間
# FadeOut 消えるまでの時間
TitleTime:
  FadeIn: 10
  Stay: 40
  FadeOut: 10

## === タイトルメッセージの設定 === ##
# [true で有効 | false で無効]
# 初期: true
# & でカラーコードを使用できます。
# %player でプレイヤーを取得します。
# %time でTimesofDayに設定した時刻を取得します。
Title:
  Enable: true
  TitleMessage: '&aテスト1'
  SubTitleMessage: '&eテスト2'

## === タブタイトルの設定 === ##
# [true で有効 | false で無効]
# 初期: true
# タブタイトルに %time が含まれているとタイマーがスタートします。
# & でカラーコードを使用できます。
# %player でプレイヤーを取得します。
# %time でTimesofDayに設定した時刻を取得します。
TabTitle:
  Enable: true
  Header: '&dテスト1'
  Footer: '&bテスト2'

## === サーバーアイコンの設定 === ##
# [true で有効 | false で無効]
# 初期: false
# アイコンはServerIconに保存してください。
# ファイルに入れたアイコンをランダムで表示します。
ServerIcon:
  Enable: false

## === Motdの設定 === ##
# [true で有効 | false で無効]
# 初期: true
# 両方有効にしている場合はRandomMotdが優先されます。
# & でカラーコードを使用できます。
# %players でサーバーにログインしている人数を取得します。
# %maxplayers で最大接続人数を取得します。
# %servername でサーバー名を取得します。
# %version でサーバーのバージョンを取得します。
# %time でTimesofDayに設定した時刻を取得します。
RandomMotd:
  Enable: false
  Message:
    test1:
    - '&1ようこそマインクラフトサーバーへ'
    - '&2バージョン%version &3現在サーバーで%players人が遊んでます'
    test2:
    - '&4ようこそマインクラフトサーバーへ'
    - '&5バージョン%version &7現在サーバーで%players人が遊んでます'
Motd:
  Enable: true
  Message:
  - '&bようこそマインクラフトサーバーへ'
  - '&dバージョン%version &6現在サーバーで%players人が遊んでます'
```
</details>

ダウンロード
-----------
| プラグイン | サポート | 前提環境 |
|:---:|:---:|:---:|
| [**CustomMessage v1.0.0**](https://github.com/yuttyann/FileArchive/raw/main/CustomMessage/jar/1.0.0/CustomMessage%20v1.0.0.jar) | `1.7.2-1.11.x` | [`ProtocolLib`](https://www.spigotmc.org/resources/1997/), [`Kits`](https://github.com/yuttyann/FileArchive/tree/main/Kits), `Java8` |