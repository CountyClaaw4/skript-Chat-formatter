# skript-Chat-formatter
### English version is available below.

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
| `!prefix`  | Vault経由のLuckPerms Prefix |
| `!suffix`  | Vault経由のLuckPerms Suffix |
| `!player`  | プレイヤーの表示名（display name）  |
| `!message` | チャットで発言したメッセージ（チャット用のみ）  |

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

1. `skript-chat-formatter.sk` を `plugins/Skript/scripts/` に配置
2. ファイル内の `設定` を必要に応じて編集
3. サーバーを起動

## ライセンス

このプロジェクトは [MITライセンス](LICENSE.txt) のもとで公開されています。

## お問い合わせ

何か問題があれば、DiscordやGitHub Issuesなどでご連絡ください。

---

# skript-Chat-formatter (English)

This Skript file is a prefix/suffix display management tool for chat and TAB list, compatible with Vault and LuckPerms environments.

## Features

* Retrieves LuckPerms prefix/suffix via Vault
* Separate display formatting for chat and TAB list
* Automatic updates on join or regular intervals
* Admin commands for manual update and format check
* Toggleable chat feature to prevent conflicts with other plugins

## Supported Environment

* Minecraft Versions: Any (as long as required plugins support it)
* Server Types: Paper / Spigot / Purpur, etc.
* Required Plugins:

  * Skript
  * Vault
  * LuckPerms

## Configuration (`options`)

### Chat Settings

| Option Name    | Description                         |
| -------------- | ----------------------------------- |
| `chat-enabled` | Enable chat formatting (true/false) |
| `chat-format`  | Chat display format string          |

### TAB List Settings

| Option Name   | Description                             |
| ------------- | --------------------------------------- |
| `tab-enabled` | Enable TAB list formatting (true/false) |
| `tab-format`  | TAB list display format string          |

### Join/Quit Messages

| Option Name    | Description                    |
| -------------- | ------------------------------ |
| `join-enabled` | Show join message              |
| `quit-enabled` | Show quit message              |
| `join-message` | Format string for join message |
| `quit-message` | Format string for quit message |

### Update Settings

| Option Name           | Description                              |
| --------------------- | ---------------------------------------- |
| `tab-update-interval` | Interval for updating TAB list (seconds) |

## Available Placeholders

| Placeholder | Description                         |
| ----------- | ----------------------------------- |
| `%prefix%`  | Prefix from LuckPerms via Vault     |
| `%suffix%`  | Suffix from LuckPerms via Vault     |
| `%player%`  | Player display name                 |
| `%message%` | Chat message (chat formatting only) |

## Admin Commands

| Command                | Permission | Description                               |
| ---------------------- | ---------- | ----------------------------------------- |
| `/updatetab`           | OP         | Manually update TAB list for all players  |
| `/checkconfig`         | OP         | Check current configuration               |
| `/testformat [player]` | OP         | Preview prefix/suffix format for a player |
| `/reloadformat`        | OP         | Reload configuration (updates TAB list)   |

## Notes

* Enabling the chat feature may conflict with other chat plugins like LunaChat.
* Set `chat-enabled: false` to avoid conflicts.
* You can use only the TAB list feature if preferred.

## Installation

1. Place `skript-chat-formatter.sk` into `plugins/Skript/scripts/`
2. Edit the `options` section in the file as needed
3. Start your server

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.txt) file for details.

## Contact

If you encounter any issues, please contact us via Discord or GitHub Issues.
