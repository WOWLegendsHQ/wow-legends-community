<div align="center">

# ⚔️ WOW Legends — Community Edition

**A free WotLK 3.3.5a private-server repack you download and run yourself —
with a world full of AI playerbots, an AI battle companion that remembers you,
and hardcore mode.**

[🌐 Website](https://wow-legends.eu) · [🗺️ Roadmap](https://wow-legends.eu/roadmap) · [🎮 Try the live demo](#-try-it-right-now-no-download) · [💬 Discord](https://discord.gg/2RdZZ3pRZ)

</div>

---

> ### 🎉 v1.0 is here
> The first public release of the Community Edition is out — **[grab it from Releases](https://github.com/WOWLegendsHQ/wow-legends-community/releases/latest)** and host your own realm in about ten minutes. Want to look before you leap? Hop on the **permanent demo realm** below, no download needed.

---

## ✨ What makes it different

This isn't a bare repack. It's an AzerothCore-based WotLK 3.3.5a server with a living world built in:

- **🤖 Hundreds of AI playerbots** — questing, fighting, trading and roaming across Azeroth, so the world feels alive at any hour. You set how many (500 by default).
- **🧠 AI bot chat** — whisper a bot (or speak near one) and it answers in character, in your language. Backed by WOW Legends' hosted AI (your own API key from the site) *or* a local model — your choice.
- **❤️ Personal AI Companion** — claim one permanent battle buddy that fights at your side, levels with you, and **remembers your conversations** across sessions.
- **💀 Hardcore mode + Mak'gora** — one life, permanent death, and consensual duels to the death between hardcore players.
- **🛡️ Stability-first** — deep, ongoing core-level crash hardening, built for long, stable uptime rather than a realm that falls over every few hours.
- **⚙️ Yours to tune** — bot counts, rates, hardcore rules and more are all config. Scales from a solo box to a fully-populated world.

## 🎮 Try it right now (no download)

A **permanent demo realm** is online so you can experience everything before you host your own:

1. Get a clean **WoW 3.3.5a (build 12340)** client.
2. Set `Data\enUS\realmlist.wtf` to:
   ```
   set realmlist ptr.wow-legends.eu
   ```
3. Create an account at **https://play.wow-legends.eu** and log in.

## 📥 Download & run your own

Two ways to run WOW Legends:

| | **Community Edition** (this repo) | **The App** |
|---|---|---|
| Cost | **Free, forever** | Supporter |
| Setup | Manual — you extract & configure it | One-click install, update & manage |
| Best for | Tinkerers, server admins, the curious | Anyone who just wants it running fast |

**Community Edition — grab the [latest release](https://github.com/WOWLegendsHQ/wow-legends-community/releases/latest).** You need every file below (the server, the game data, MySQL and the C++ runtime):

| File | What it is |
|---|---|
| `WOW_Legends_Repack.zip` | the server — executables, configs, scripts and the ready-made database |
| `gamedata_dbc.zip` · `gamedata_maps.zip` · `gamedata_vmaps.zip` · `gamedata_mmaps.zip` · `gamedata_Cameras.zip` | the game world data (~1.2 GB zipped) |
| `mysql_portable_8.4.9.zip` | a bundled portable MySQL (or point the server at your own) |
| `vc_redist.x64.exe` | Microsoft Visual C++ runtime (run once) |
| `SHA256SUMS.txt` | checksums to verify your downloads |

➡️ **Then follow [QUICKSTART.md](docs/QUICKSTART.md)** — it walks you through the whole setup. (It's bundled inside `WOW_Legends_Repack.zip` too.)

> Verify a download before trusting it: `Get-FileHash <file> -Algorithm SHA256` and compare it against `SHA256SUMS.txt`.

> Every release also ships through **The App** as a one-click update, and supporters get **early access** to each new version before it rolls out free here.

## 📚 Documentation

- [**Quick Start**](docs/QUICKSTART.md) — download, set up and run your own server, step by step
- [**Requirements**](docs/REQUIREMENTS.md) — hardware profiles, from a small box to a busy world

## 🧩 Related projects

- [Player addon](https://github.com/WOWLegendsHQ/wow-legends-player-addon) — bot control, XP rate, hardcore opt-in & QoL
- [GM addon](https://github.com/WOWLegendsHQ/wow-legends-gm-addon) — in-game admin tools

## 🙏 Credits & license

Built on the excellent work of [**AzerothCore**](https://github.com/azerothcore/azerothcore-wotlk) (GPLv2) and the [**mod-playerbots**](https://github.com/liyunfan1223/mod-playerbots) project (AGPLv3); WOW Legends' own additions follow their licensing. World of Warcraft is a trademark of Blizzard Entertainment — this is a **non-commercial fan project**, not affiliated with or endorsed by Blizzard. You'll need your own WoW 3.3.5a (build 12340) game client to play.

<div align="center">

*See you in Azeroth.* 🐉

</div>
