# ggBackup

Professional backup solution for Spigot / Paper servers, by [Glesel-Group](https://glesel-group.de).

**Free.** Closed source – this repository only hosts downloads and the changelog.

## Features

- Backup profiles for worlds, plugins and custom folders
- Scheduled backups with timezone support
- Manual backups and restore from in-game or console
- Performance protection: waits for enough TPS, optional player limit, automatic retries
- Configurable compression (ZIP) and file naming
- Optional backup on server shutdown
- Notifications and broadcast announcements
- Languages: English and German

## Commands

`/backup` (aliases `/bkup`, `/bu`)

| Subcommand | Description |
|---|---|
| `start` | Start a backup manually |
| `profiles` | List backup profiles |
| `list` | List existing backups |
| `status` | Show backup status |
| `next` | Show next scheduled backup |
| `restore` | Restore a backup |
| `reload` | Reload the configuration |
| `help` | Show help |

Permissions: `ggbackup.use`, `ggbackup.start`, `ggbackup.list`, `ggbackup.status`, `ggbackup.next`, `ggbackup.restore`, `ggbackup.reload`, `ggbackup.notify` (all of them: `ggbackup.*`, default: op).

## Installation

1. Download the latest JAR from [Releases](../../releases/latest).
2. Put it into your server's `plugins` folder.
3. Restart the server and edit `plugins/ggBackup/config.yml`.

## Links

- Website: https://glesel-group.de
