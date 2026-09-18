# scoop-bucket

Scoop bucket for my Windows tools.

## Add the bucket

```powershell
scoop bucket add yannick https://github.com/YannickHerrero/scoop-bucket
```

## Install

```powershell
scoop install yannick/wmenu
scoop install yannick/wbar
scoop install yannick/explorer
scoop install yannick/nekodachi
scoop install yannick/winarchy
scoop install yannick/proton-pass-cli
```

## Apps

| App | Repo | Description |
| --- | --- | --- |
| `wmenu` | [YannickHerrero/wmenu](https://github.com/YannickHerrero/wmenu) | Keyboard-driven launcher and hotkey daemon |
| `wbar` | [YannickHerrero/wbar](https://github.com/YannickHerrero/wbar) | Minimal status bar (pairs with GlazeWM) |
| `explorer` | [YannickHerrero/Explorer](https://github.com/YannickHerrero/Explorer) | Tauri-based file explorer |
| `nekodachi` | [YannickHerrero/nekodachi](https://github.com/YannickHerrero/nekodachi) | Tiny native desktop pet |
| `winarchy` | [YannickHerrero/winarchy](https://github.com/YannickHerrero/winarchy) | Keyboard-first tiling window manager and experimental shell |
| `proton-pass-cli` | [protonpass/pass-cli](https://github.com/protonpass/pass-cli) | Official Proton Pass command-line client (separate from the desktop app) |

## Proton Pass CLI

`proton-pass-cli` exposes the `pass-cli` command through Scoop's shims. The package
includes the DLL shipped in Proton's official Windows archive and verifies the
archive against Proton's published SHA-256. Version checks and autoupdate hashes
use Proton's official stable manifest.

Connect with `pass-cli login` and complete the browser flow. This session is
independent of the desktop app installed by `scoop install extras/proton-pass`.
Installing the CLI does not authenticate you or change an existing CLI session.
For a locked CLI session, use `pass-cli session unlock`.

Update through Scoop (`scoop update proton-pass-cli`), not the CLI's built-in
updater, so Scoop retains control of the installed version.
