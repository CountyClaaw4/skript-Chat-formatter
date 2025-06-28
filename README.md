# skript-Chat-formatter

このSkriptファイルは、Vault + LuckPerms 環境に対応したチャット・TABリストへのPrefix/Suffix表示管理ツールです。

## 特徴

* Vaultを介してLuckPermsのprefix/suffixを取得
* チャットとTABリストの表示フォーマットを個別に設定可能
* 定期更新や参加時更新で自動反映
* 管理者向けコマンドで手動更新や確認も可能
* チャット機能は競合対策のためON/OFF切り替え可能

## 対応環境

* Minecraft バージョン: 任意（前提プラグインが対応していればOK）
* サーバー: Paper / Spigot / Purpur など
* 前提プラグイン:
  * Skript
  * Vault
  * LuckPerms

## 設定方法（`options`）

### チャット関連

| オプション名         | 説明                     |
| -------------- | ---------------------- |
| `chat-enabled` | チャット表示を有効化（true/false） |
| `chat-format`  | チャットの表示フォーマット文字列       |

### TABリスト関連

| オプション名        | 説明                       |
| ------------- | ------------------------ |
| `tab-enabled` | TABリスト表示を有効化（true/false） |
| `tab-format`  | TAB上の表示フォーマット文字列         |

### 入退出メッセージ

| オプション名         | 説明             |
| -------------- | -------------- |
| `join-enabled` | 参加メッセージを表示するか  |
| `quit-enabled` | 退出メッセージを表示するか  |
| `join-message` | 入室メッセージのフォーマット |
| `quit-message` | 退室メッセージのフォーマット |

### 更新設定

| オプション名                | 説明               |
| --------------------- | ---------------- |
| `tab-update-interval` | TABリストを更新する間隔（秒） |

## 利用可能なプレースホルダー

| プレースホルダー    | 内容                       |
| ----------- | ------------------------ |
| `%prefix%`  | Vault経由のLuckPerms Prefix |
| `%suffix%`  | Vault経由のLuckPerms Suffix |
| `%player%`  | プレイヤーの表示名（display name）  |
| `%message%` | チャットで発言したメッセージ（チャット用のみ）  |

## 管理コマンド一覧

| コマンド                   | 権限 | 説明                          |
| ---------------------- | -- | --------------------------- |
| `/updatetab`           | OP | 全プレイヤーのTABリストを手動で更新         |
| `/checkconfig`         | OP | 現在の設定を確認                    |
| `/testformat [player]` | OP | 指定プレイヤーのPrefix/Suffix表示例を確認 |
| `/reloadformat`        | OP | 設定の再適用（TABリスト更新）            |

## 注意点

* チャット機能を使用する場合、LunaChatなど他のチャットプラグインと競合する可能性があります。
* `chat-enabled: false` に設定することで競合を回避可能です。
* TABリスト機能のみ有効にして運用することも可能です。

## 導入手順

1. `skript-chat-fomatter.sk` を `plugins/Skript/scripts/` に配置
2. ファイル内の `設定` を必要に応じて編集
3. サーバーを起動

## 作者・ライセンス

* 作成者: あなたの名前（必要に応じて変更）
* ライセンス: MIT または自由に再配布可（記載がない場合は記載推奨）

## お問い合わせ

何か問題があれば、DiscordやGitHub Issuesなどでご連絡ください。
