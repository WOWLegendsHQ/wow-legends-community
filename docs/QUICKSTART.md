# WOW Legends — Quick Start (manual install)

**WOW Legends is a repack** — a ready-to-run *Wrath of the Lich King (3.3.5a)* server you host
yourself, with hundreds of smart playerbots, AI companion chat, hardcore mode, per-character XP and
a built-in auction economy. You run the world; anyone you invite plays in it.

> **Prefer zero hassle?** The **[WOW Legends App](https://wow-legends.eu)** sets all of this up in one
> click — guided install, one-click updates, and a server that starts and *restarts itself* — no
> command line, no babysitting. This guide is the **manual** route: you install, run and maintain
> everything yourself, in this one `wow_legends_repack` folder.

---

## What's in this folder
```
wow_legends_repack\
├─ start.bat   ← double-click to run the server (after setup)
├─ worldserver.exe, authserver.exe, dbimport.exe (+ runtime DLLs)
├─ configs\                ← settings (worldserver.conf, modules\…)
├─ modules\                ← server modules (playerbots, wowlegends, ahbot, xp) — REQUIRED, don't delete
├─ dump\                   ← the ready-made databases (imported once, in setup)
├─ data\
│   ├─ sql\create\         ← create_mysql.sql (makes the empty DBs + user)
│   └─ (extract dbc/maps/vmaps/mmaps/Cameras game data here)
└─ mysql\                  ← the bundled portable MySQL (from mysql_portable zip), or use your own
```

## 1. What you need
- **Windows** (64-bit)
- **MySQL 8.x** — bundled in `mysql\` (recommended), or your own service
- A **WoW 3.3.5a (build 12340)** client
- **Game data** — `dbc / maps / vmaps / mmaps / Cameras` (download separately, ~3.2 GB)
- **Microsoft Visual C++ runtime** — run `vc_redist.x64.exe` once

## 2. First-time setup (once)
1. **Game data:** extract the five game-data zips into `data\` → `data\dbc`, `data\maps`, `data\vmaps`, `data\mmaps`, `data\Cameras`.
2. **Databases** — pick one:
   - **Bundled MySQL (easiest):** extract `mysql_portable_8.4.9.zip` into this folder (it adds `mysql\`), then run **`mysql\init_mysql.bat` once**. It creates the `wowlegends` user + the four databases **and imports the ready-made dumps** from `dump\`. Takes a few minutes — let it finish.
   - **Your own MySQL service:** create the DBs + user, then import the dumps:
     ```
     mysql -u root -p < data\sql\create\create_mysql.sql
     mysql -u root wl_auth        < dump\wl_auth.sql
     mysql -u root wl_characters  < dump\wl_characters.sql
     mysql -u root wl_world       < dump\wl_world.sql
     mysql -u root wl_playerbots  < dump\wl_playerbots.sql
     ```
   The default DB login is `wowlegends` / `wowlegends` (the server uses it — no need to touch root).

## 3. Start it
**Double-click `start.bat`.** It launches MySQL (if bundled), the auth server, and the world
server — each in its own window. The databases were already populated in step 2. Close a server
window to stop it. (No window auto-restarts after a crash — that's the App's job; here you relaunch
`start.bat` yourself.)

## 4. Connect & accounts
1. Point your client's **realmlist** at the server — local play: `set realmlist 127.0.0.1` (in `realmlist.wtf`).
2. **Built-in accounts** — manage them in the **WorldServer** window. All three ship with the **same
   default password `wowlegends`** — **change every one before your realm is reachable** with:
   `account set password <name> <new-password> <new-password>` (type the new password twice).

   | Account | Purpose | Notes |
   |---|---|---|
   | `admin` | your GM account (level 3) | change this password first |
   | `ahbot` | drives the auction-house economy (server-side) | safe to change — nothing logs in with it |
   | `wlshop` | the register-portal **web shop** signs in as this to deliver items (GM 3) | change it too — and if you run the website, set the new password in the portal's `config.php` |

   > ⚠️ Don't **delete or rename** `ahbot` / `wlshop` — the auction house and web shop need these
   > accounts to exist. Just change their passwords.
3. To make a player or an extra GM account:
   ```
   account create <name> <password>
   account set gmlevel <name> 3 -1     # full GM (optional)
   ```
4. Log in, make a character, play.

---

## 5. Tuning (optional) — `configs\`
| Want to change… | File | Setting |
|---|---|---|
| Bots in the world | `configs\modules\playerbots.conf` | `AiPlayerbot.MaxRandomBots` (default **500**) |
| AI chat on/off + provider | `configs\modules\mod_wowlegends.conf` | `WowLegends.AiChat.Enabled`, `…Provider`, `…ApiKey` |
| Hardcore mode | `configs\modules\mod_wowlegends.conf` | `WowLegends.Hardcore.*` |
| Auction-house bots | `configs\modules\mod_ahbot.conf` | `AuctionHouseBot.EnableSeller / EnableBuyer` (on) |
| XP / drop / gold rates | `configs\worldserver.conf` | `Rate.XP.*`, etc. |
| Remote DB / different password | the `*.conf` DB lines | `…DatabaseInfo` connection strings |

**AI companion chat** is **on by default** and uses WOW Legends' **hosted AI** — register at
**wow-legends.eu**, create an API key (`wlk_…`) and paste it into `WowLegends.AiChat.ApiKey`. Prefer
fully local & free? Set `WowLegends.AiChat.Provider = ollama` and run a local model
(`ollama pull qwen2.5:1.5b`). With no key and no local model, the bots simply stay quiet.

## 6. Features & commands
Full how-to (bots, AI chat, XP, hardcore, Mak'gora, gear) + the searchable command list are on the
website — see the **Guide** and **Commands** pages.

> Tired of the manual upkeep — updates, restarts, tuning? The **[WOW Legends App](https://wow-legends.eu)**
> installs, runs and updates your whole server for you, one click.

---
*Built on [AzerothCore](https://www.azerothcore.org) (GPL). Not affiliated with Blizzard Entertainment. Private, non-commercial use.*
