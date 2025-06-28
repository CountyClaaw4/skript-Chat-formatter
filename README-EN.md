# skript-Chat-formatter

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

## Contact

If you encounter any issues, please contact us via Discord or GitHub Issues.
