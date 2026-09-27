<div align="center">

# ⚔️ WOW Legends — Community Edition

**A free WotLK 3.3.5a private-server repack you download and run yourself —
with a world full of AI playerbots you can talk to, an AI companion that remembers you,
Warband Camps and hardcore mode. Complete server source included.**

[🌐 Website](https://wow-legends.eu) · [🗺️ Roadmap](https://wow-legends.eu/roadmap) · [📜 Changelog](https://wow-legends.eu/changelog) · [🎮 Try the live demo](https://play.wow-legends.eu) · [💬 Discord](https://discord.gg/j8nN2rz42A)

</div>

---

> ### 🌍 v1.6.0 "Talk to your bots" is the free release — for everyone, with the complete server source
> Say **"lfg"** in a city and bots who fit your group answer; drive **Dungeon Clear** by talking; hire **Warband Camp staff** (banker, merchant, barkeep, guards) — on top of everything from v1.4 and v1.5: bots that walk real roads, a **Guide** that escorts you anywhere, the **Sage**, plain-language **party orders**, **Warband Camps**, **transmog** and **AoE loot**. **[Grab it from Releases](https://github.com/WOWLegendsHQ/wow-legends-community/releases/latest)**, or try the **permanent demo realm** below first, no download needed.
>
> *Supporters run the same builds early: **v1.7.0, the community release** — cross-faction bots, account-bound professions, `$lfg` building your whole group, a full PvP set with `.gear pvp` and more, every item from a community suggestion — is live in [the App](https://wow-legends.eu/app) today. Every release becomes the free community release later, full server source included. Nothing is permanently paywalled.*

---

## ✨ What makes it different

This isn't a bare repack. It's an AzerothCore-based WotLK 3.3.5a server with a living world built in:

- **🤖 Hundreds of AI playerbots** — questing, fighting, trading and roaming across Azeroth at every level, so the world feels alive at any hour. You set how many (100 out of the box; the engine has been run into the thousands).
- **🧠 AI bot chat** — whisper a bot (or speak near one) and it answers in character, in your language, each with its own personality. Runs on WOW Legends' **hosted AI** (credits) *or* your own: a free **local model** via Ollama, or your own API key.
- **🗣️ Talk-and-command** — with AI chat on, bots don't just talk, **they obey**: "follow me", "attack that warlock", "everyone wait here" — plain language, any language, for one bot or the whole party.
- **🧭 The Guide & the Sage** — ask a bot to *"take me to Booty Bay"* and it walks you there on real roads; ask *"who sells Refreshing Spring Water?"* and the answer comes from your server's actual data.
- **🏰 Dungeon Clear** — order a tank bot to clear a whole dungeon for your party.
- **🔥 Warband Camps** *(optional)* — claim a camp anywhere in the open world, furnish it, and your alts gather there on their own. Friends just walk in.
- **❤️ Personal AI Companion** — one permanent battle buddy that fights at your side, levels with you and **remembers your conversations** across sessions.
- **🏅 Paths of Legends** — opt-in challenge oaths sworn at the **Herald of the Fallen**, each ending in a trophy with your name on it.
- **💀 Hardcore mode + Mak'gora** — one life, permanent death, and consensual duels to the death between hardcore players.
- **⚔️ A living, dangerous world** *(optional)* — all-zones **World PvP** and **faction Battlefronts** in random zones.
- **👕 Transmog & AoE loot** — on a clean 3.3.5a client, fully server-side.
- **🛡️ Stability-first** — deep, ongoing core-level crash hardening, built for long uptime.
- **⚙️ Yours to tune** — bot counts, rates, hardcore rules and every WOW Legends feature are config switches. World-changing features ship **off**.

**→ [See everything it can do](https://wow-legends.eu/features)**

## 🎮 Try it right now (no download)

A **permanent demo realm** is online so you can try everything before you host your own:

1. Get a clean **WoW 3.3.5a (build 12340)** client.
2. Set your `realmlist.wtf` (in `Data\enUS\`, or your client's language folder) to:
   ```
   set realmlist ptr.wow-legends.eu
   ```
3. Create an account at **https://play.wow-legends.eu** and log in.

It's a test realm: its database can be reset at any time.

## 📥 Download & run your own

Two ways to run WOW Legends:

| | **Community Edition** (this repo) | [**The App**](https://wow-legends.eu/app) |
|---|---|---|
| Cost | **Free, forever** | **€25**, a one-time supporter donation — no subscription |
| Version | the free release (**v1.6.0** today) | the same builds, **early** (**v1.7.0** today) |
| Setup | Manual — you extract & configure it | One-click install, update & manage |
| Web portal | Bring your own | **Included** — sign-up, shop, armory, leaderboards & admin panel, the same site as [play.wow-legends.eu](https://play.wow-legends.eu) |
| Best for | Tinkerers, server admins, the curious | Anyone who just wants it running fast |

**Community Edition — grab the [latest release](https://github.com/WOWLegendsHQ/wow-legends-community/releases/latest).** You need every file below except the source (the server, the game data, MySQL and the C++ runtime):

| File | What it is |
|---|---|
| `WOW_Legends_Repack.zip` | the server — executables, configs, **modules**, road data and the ready-made database |
| `gamedata_dbc.zip` · `gamedata_maps.zip` · `gamedata_vmaps.zip` · `gamedata_mmaps.zip` · `gamedata_Cameras.zip` | the game world data (~1.2 GB zipped) |
| `mysql_portable_8.4.9.zip` | a bundled portable MySQL 8.4 LTS (or point the server at your own) |
| `vc_redist.x64.exe` | Microsoft Visual C++ runtime (run once) |
| `WOW_Legends_Server_Source.zip` | *optional* — the complete server source of this exact build |
| `SHA256SUMS.txt` · `manifest.json` | checksums to verify your downloads · the release manifest |

➡️ **Then follow [QUICKSTART.md](docs/QUICKSTART.md)** — it walks you through the whole setup. (It's bundled inside `WOW_Legends_Repack.zip` too.)

> Verify a download before trusting it: `Get-FileHash <file> -Algorithm SHA256` and compare it against `SHA256SUMS.txt`.

> **Become a supporter — €25, once.** You get [**The App**](https://wow-legends.eu/app) (one-click install, dashboard, one-click backups), **early access** to new builds, your own **player portal** (sign-up, shop, armory, leaderboards & admin panel), **hosted-AI credits** included, **12 months of App updates** (the App stays yours forever) and priority support. The Community Edition stays **free forever**. Free users can run the AI chat on a local Ollama model or their own API key, or buy hosted-AI credits on their own (1 € = 100+ bot replies).

## 📚 Documentation

- [**Quick Start**](docs/QUICKSTART.md) — download, set up and run your own server, step by step
- [**Install notes**](docs/INSTALL.md) — the bigger picture, upgrading, and going public
- [**Requirements**](docs/REQUIREMENTS.md) — hardware profiles, from a small box to a busy world
- [**Guide**](https://wow-legends.eu/guide) & [**Commands**](https://wow-legends.eu/commands) — in-depth how-to: bots, AI chat, Warband Camps, hardcore, Mak'gora, and the searchable command list

## 🧩 Related projects

- [Player addon](https://github.com/WOWLegendsHQ/wow-legends-player-addon) — command your bots without typing, XP rate, hardcore opt-in & QoL
- [GM addon](https://github.com/WOWLegendsHQ/wow-legends-gm-addon) — the whole command set as one-click buttons

## 🙏 Credits & license

Built on the excellent work of [**AzerothCore**](https://github.com/azerothcore/azerothcore-wotlk) (GPLv2) and [**mod-playerbots**](https://github.com/mod-playerbots/mod-playerbots) (AGPLv3); WOW Legends' own modules are AGPLv3. Every release ships its complete server source as `WOW_Legends_Server_Source.zip`, and the source for any build you run is available on request. World of Warcraft is a trademark of Blizzard Entertainment — this is a **non-commercial fan project**, not affiliated with or endorsed by Blizzard. You'll need your own WoW 3.3.5a (build 12340) game client to play.

<div align="center">

*See you in Azeroth.* 🐉

</div>
