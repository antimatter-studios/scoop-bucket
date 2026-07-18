# antimatter-studios Scoop bucket

A [Scoop](https://scoop.sh) bucket for [trove](https://github.com/antimatter-studios/trove) — a KeePassXC-compatible secrets CLI for developer machines.

## Install

```powershell
scoop bucket add antimatter-studios https://github.com/antimatter-studios/scoop-bucket
scoop install trove
```

This puts two native Windows binaries on your PATH:

- `trove` — CLI client
- `troved` — background daemon (brokers your kdbx secrets to ssh / git / gpg)

## Quickstart

```powershell
troved
trove unlock C:\path\to\your.kdbx
```

`trove` and `troved` talk over a Windows named pipe, so this is fully native — no WSL required. If you work inside WSL instead, install the Linux build there (tarball or Linuxbrew) like on any Linux box; the two are independent.

For the GUI, install **Trove Desktop** from the [releases page](https://github.com/antimatter-studios/trove/releases).

## Updates

The [`trove`](bucket/trove.json) manifest carries `checkver`/`autoupdate`, and the [Excavator workflow](.github/workflows/excavator.yml) bumps it automatically when a new `trove` release ships.
