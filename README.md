<div align="center">

# ⚔️ WOW Legends — Community Edition

**A free WotLK 3.3.5a private-server repack you download and run yourself —
with a world full of AI playerbots, an AI battle companion that remembers you,
and hardcore mode.**

[🌐 Website](https://wow-legends.eu) · [🗺️ Roadmap](https://wow-legends.eu/roadmap) · [🎮 Try the live demo](https://play.wow-legends.eu) · [💬 Discord](https://discord.gg/j8nN2rz42A)

</div>

---

> ### 🌍 v1.2.0 "The Bots Come Alive" is out — free for everyone
> Bots that remember **you**, recognize familiar faces, hold grudges, and hold short AI-written conversations with each other; a rewritten in-world bot voice; and a little secret in Stranglethorn Vale — **[grab it from Releases](https://github.com/WOWLegendsHQ/wow-legends-community/releases/latest)** and host your own realm in about ten minutes. Want to look before you leap? Hop on the **permanent demo realm** below, no download needed.
>
> *Supporters ride one release ahead: **v1.3.0 "Paths of Legends"** — opt-in challenge Paths (the Iron Oath, the Pilgrim's Way, the Slow Burn and more) sworn at the Herald of the Fallen, plus bots that obey plain-language commands in any language — is live in [the App](https://wow-legends.eu/app) today. Every version lands here for free when the next one ships.*

---

## ✨ What makes it different

This isn't a bare repack. It's an AzerothCore-based WotLK 3.3.5a server with a living world built in:

- **🤖 Hundreds of AI playerbots** — questing, fighting, trading and roaming across Azeroth at every level, so the world feels alive at any hour. You set how many (100 out of the box; the engine has been run into the thousands).
- **⚔️ A living, dangerous world** *(optional)* — flip on all-zones **World PvP** (continuous, or scheduled PvP windows) and enemy players *and bots* become fair game everywhere; **faction Battlefront** events erupt in random zones with a real tug-of-war objective both factions fight over.
- **🧠 AI bot chat** — whisper a bot (or speak near one) and it answers in character, in your language. Runs on WOW Legends' **hosted AI** (credits-based — supporters get a welcome batch) *or* a free **local model** via Ollama — your choice.
- **❤️ Personal AI Companion** — claim one permanent battle buddy that fights at your side, levels with you, and **remembers your conversations and the milestones you live through together** across sessions.
- **💀 Hardcore mode + Mak'gora** — one life, permanent death, and consensual duels to the death between hardcore players.
- **🛡️ Stability-first** — deep, ongoing core-level crash hardening, built for long, stable uptime rather than a realm that falls over every few hours.
- **⚙️ Yours to tune** — bot counts, rates, hardcore rules and more are all config. Scales from a solo box to a fully-populated world.

**→ [See everything it can do](https://wow-legends.eu/features)**

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

| | **Community Edition** (this repo) | [**The App**](https://wow-legends.eu/app) |
|---|---|---|
| Cost | **Free, forever** | **€25** (supporter) |
| Setup | Manual — you extract & configure it | One-click install, update & manage |
| Web portal | Bring your own | **Included** — player sign-up, accounts & shop, the same site as [play.wow-legends.eu](https://play.wow-legends.eu) |
| Best for | Tinkerers, server admins, the curious | Anyone who just wants it running fast |

**Community Edition — grab the [latest release](https://github.com/WOWLegendsHQ/wow-legends-community/releases/latest).** You need every file below (the server, the game data, MySQL and the C++ runtime):

| File | What it is |
|---|---|
| `WOW_Legends_Repack.zip` | the server — executables, configs, **modules**, scripts and the ready-made database |
| `gamedata_dbc.zip` · `gamedata_maps.zip` · `gamedata_vmaps.zip` · `gamedata_mmaps.zip` · `gamedata_Cameras.zip` | the game world data (~1.2 GB zipped) |
| `mysql_portable_8.4.9.zip` | a bundled portable MySQL (or point the server at your own) |
| `vc_redist.x64.exe` | Microsoft Visual C++ runtime (run once) |
| `SHA256SUMS.txt` | checksums to verify your downloads |

➡️ **Then follow [QUICKSTART.md](docs/QUICKSTART.md)** — it walks you through the whole setup. (It's bundled inside `WOW_Legends_Repack.zip` too.)

> Verify a download before trusting it: `Get-FileHash <file> -Algorithm SHA256` and compare it against `SHA256SUMS.txt`.

> **Become a supporter — €25.** You get [**The App**](https://wow-legends.eu/app) (one-click install, update & manage), a ready-made **player website** (sign-up, accounts & shop — the same as [play.wow-legends.eu](https://play.wow-legends.eu)), **12 months of updates**, and **~2,500 welcome credits to power the AI chat** on the hosted AI. The Community Edition here stays **free forever** — and you can run the AI chat for free on a local Ollama model any time.

## 📚 Documentation

- [**Quick Start**](docs/QUICKSTART.md) — download, set up and run your own server, step by step
- [**Requirements**](docs/REQUIREMENTS.md) — hardware profiles, from a small box to a busy world
- [**Guide & Commands**](https://wow-legends.eu/guide) — in-depth how-to: bots, AI chat, hardcore, Mak'gora & the searchable command list

## 🧩 Related projects

- [Player addon](https://github.com/WOWLegendsHQ/wow-legends-player-addon) — bot control, XP rate, hardcore opt-in & QoL
- [GM addon](https://github.com/WOWLegendsHQ/wow-legends-gm-addon) — in-game admin tools

## 🙏 Credits & license

Built on the excellent work of [**AzerothCore**](https://github.com/azerothcore/azerothcore-wotlk) (GPLv2) and the [**mod-playerbots**](https://github.com/liyunfan1223/mod-playerbots) project (AGPLv3); WOW Legends' own additions follow their licensing. World of Warcraft is a trademark of Blizzard Entertainment — this is a **non-commercial fan project**, not affiliated with or endorsed by Blizzard. You'll need your own WoW 3.3.5a (build 12340) game client to play.

<div align="center">

*See you in Azeroth.* 🐉

</div>
