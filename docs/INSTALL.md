# Install Guide

The full, step-by-step setup lives in **[QUICKSTART.md](QUICKSTART.md)** — download the release,
extract it, set up the database, and launch (about ten minutes). **Start there.**

This page is the bigger picture and notes on going public.

## The two editions

- **Community Edition (free, this repo):** you download the release, extract it, and run it
  yourself — fully yours, more hands-on.
- **The App (supporter):** one click installs, configures, updates and manages everything. If you'd
  rather skip the manual steps, that's what it's for — see [wow-legends.eu](https://wow-legends.eu).

## What you need

- A machine meeting the [requirements](REQUIREMENTS.md)
- A **WoW 3.3.5a (build 12340)** client to log in and play
- Windows (64-bit). The bundled MySQL 8.x and the VC++ 2015–2022 x64 redistributable come with the release.

## What's in the download

The release is a handful of files: the server (`WOW_Legends_Repack.zip`, with a ready-made database
inside), the game world data (`gamedata_*.zip`), a portable MySQL, and the VC++ runtime. You extract
them into one folder and run `start.bat` — see [QUICKSTART.md](QUICKSTART.md) for the exact steps.

## Hosting it publicly

Running a realm others can reach adds a few steps beyond the quick start:

- **Port-forward** the auth (3724) and world (8085) ports on your router, and set your realm's
  external address in the database `realmlist` so players can find it.
- **Change every default account password** — `admin`, `ahbot` and `wlshop` all ship with the same
  default; see the accounts section of [QUICKSTART.md](QUICKSTART.md).
- **Lock down remote access** — keep the RA and SOAP ports bound to localhost (the defaults), or
  firewall them.

## Getting help

- 💬 Community: [wow-legends.eu](https://wow-legends.eu)
- 🐛 Found a bug or a gap in these docs? Open an [issue](https://github.com/WOWLegendsHQ/wow-legends-community/issues).
