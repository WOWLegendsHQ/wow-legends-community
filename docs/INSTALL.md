# Install Guide

The full, step-by-step setup lives in **[QUICKSTART.md](QUICKSTART.md)** — download the release,
extract it, set up the database, and launch (about ten minutes). **Start there.**

This page is the bigger picture: the two editions, upgrading, and going public.

## The two editions

- **Community Edition (free, this repo):** you download the release, extract it, and run it
  yourself — fully yours, more hands-on. Every release ships the complete server source
  (`WOW_Legends_Server_Source.zip`); building it yourself is optional.
- **The App (supporter, €25 once):** one click installs, configures, updates and manages everything,
  and supporters run the same builds **early** — each one becomes the free community release later.
  See [wow-legends.eu/app](https://wow-legends.eu/app).

## What you need

- A machine meeting the [requirements](REQUIREMENTS.md)
- A **WoW 3.3.5a (build 12340)** client to log in and play
- Windows (64-bit). The bundled MySQL 8.4 LTS and the VC++ 2015–2022 x64 redistributable come with
  the release.

## What's in the download

The release is a handful of files: the server (`WOW_Legends_Repack.zip`, with a ready-made database
inside), the game world data (`gamedata_*.zip`), a portable MySQL, the VC++ runtime, and the optional
server source. You extract them into one folder and run `start.bat` — see
[QUICKSTART.md](QUICKSTART.md) for the exact steps.

## Upgrading

Upgrading keeps your characters: replace the executables, bring your configs up to date, and apply
the SQL files in `dump\extras\` — never re-import `dump\`. The steps are in
[QUICKSTART.md → Upgrading an older install](QUICKSTART.md#6-upgrading-an-older-install). The App
does it with one click.

## Hosting it publicly

Running a realm others can reach adds a few steps beyond the quick start (the website's
[Play with friends](https://wow-legends.eu/play-with-friends) guide walks through them):

- **Port-forward** the auth (3724) and world (8085) ports on your router, and set your realm's
  external address in the `realmlist` table of the auth database so players can find it.
- **Change every default account password** — `admin`, `ahbot` and `wlshop` all ship with the same
  default; see the accounts section of [QUICKSTART.md](QUICKSTART.md).
- **Keep remote administration closed.** RA and SOAP both ship **disabled**. SOAP listens on
  localhost only; RA, if you turn it on, listens on **all** addresses (port 3443). Either set
  `Ra.IP = "127.0.0.1"` in `worldserver.conf` or firewall that port.

## Getting help

- 💬 Community & support: the [WOW Legends Discord](https://discord.gg/j8nN2rz42A)
- 🐛 Found a bug or a gap in these docs? Open an [issue](https://github.com/WOWLegendsHQ/wow-legends-community/issues).
