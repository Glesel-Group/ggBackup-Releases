# ggBackup

Professional backup solution for Spigot / Paper servers, by [Glesel-Group](https://glesel-group.de).

**Free.** Closed source – this repository only hosts downloads and the changelog.

## Features

- Backup profiles for worlds, plugins and extra folders (`worlds: all`, `plugins: all`, or pick names)
- Exclude patterns per profile (`*.log`, `cache`, `dynmap/tiles`)
- Scheduled backups: daily, weekdays, weekend or chosen days, with time zone support
- Backups run in the background, so players can keep playing
- Performance protection: waits for enough TPS, optional player limit, automatic retries
- Safe backups: written to a temporary file first, worlds are always switched back to autosave
- Disk space check before a backup starts
- Restore from in-game or console, with a confirmation step; the replaced data is kept as `<name>.old`
- Optional backup on server shutdown
- Chat announcements before scheduled backups, messages for admins
- Fully commented config that converts old configs automatically
- Languages: English and German
- Made for Minecraft 26.x (Spigot API 26.3)

## Commands

`/backup` (aliases `/bkup`, `/bu`)

| Subcommand | Description |
|---|---|
| `start [profile]` | Start a backup manually (default profile: `default`) |
| `profiles` | List backup profiles |
| `list [profile]` | List existing backups |
| `status` | Show backup status |
| `next` | Show next scheduled backup |
| `restore <file> [folder\|all] confirm` | Restore a backup (`confirm` is required) |
| `reload` | Reload the configuration |
| `help` | Show help |

Permissions: `ggbackup.use`, `ggbackup.start`, `ggbackup.list`, `ggbackup.status`, `ggbackup.next`, `ggbackup.restore`, `ggbackup.reload`, `ggbackup.notify` (all of them: `ggbackup.*`, default: op).

## Quick start

The config (`plugins/ggBackup/config.yml`) explains every option. Most servers only need two sections:

```yaml
profiles:
  default:
    worlds: all          # every world
    plugins: []          # or: all, or [Essentials, LuckPerms]
    folders: []          # extra folders/files, e.g. [config]
    exclude: ["*.log"]
    compress: true
    keep: 10             # how many backups to keep

schedules:
  - profile: default
    days: daily          # or weekdays, weekend, [MONDAY, THURSDAY]
    time: "02:00"
```

Run `/backup reload` after changes.

## Installation

1. Download the latest JAR from [Releases](../../releases/latest).
2. Put it into your server's `plugins` folder.
3. Restart the server and edit `plugins/ggBackup/config.yml`.

## Links

- Website: https://glesel-group.de
