# System Requirements

WOW Legends runs on modest hardware. **What you need depends mostly on how many AI
bots you want living in your world** — that's the main resource driver, and it's a
config setting you tune. Pick a profile below.

## Baseline (any setup)

- **OS:** Windows 10 / 11 or Windows Server (64-bit)
- **CPU:** a modern multi-core chip — **4 cores minimum**; more cores = more bots (the bot AI runs across the map-update threads)
- **Storage:** **SSD strongly recommended** (a spinning hard drive can stall the database under load). Roughly **25–40 GB** free for the server, game data and the pre-populated database.
- **A WoW 3.3.5a (build 12340) client** — to log in and play (the server's world data is included in the download)
- **Runtimes:** MySQL 8.x and the Microsoft Visual C++ 2015–2022 x64 Redistributable (both bundled in the release)

## Server profiles

RAM below is the **whole picture** — it already accounts for the worldserver, MySQL and the OS.

| Profile | AI bots | Grid preload | Total RAM | Good for |
|---|---|---|---|---|
| **Starter** | ~25–50 | Off | **8 GB** | Solo or a small group |
| **Community** | ~100–200 | Off | **16 GB** | Small active communities |
| **Living World** | 500+ | On | **24–32+ GB** | Busy, fully-populated worlds |

> Every figure is a config setting you can tune. The release **ships configured for a busy world (500 bots)** — on a Starter or Community box, just lower the bot count (below).

## The two settings that drive the profiles

- **Bot count** — `AiPlayerbot.MinRandomBots` / `AiPlayerbot.MaxRandomBots`. The biggest lever for both RAM and CPU. Ships at 500; drop it to ~25–50 for a small box.
- **Grid preload** — `PreloadAllNonInstancedMapGrids`. Off by default; turning it on adds ~3 GB RAM but preloads the whole world for maximum stability and zero load-hitches. Recommended for big servers with RAM to spare.

## AI features (optional)

The AI companion & bot chat need a language-model backend — either:

- a **cloud API** (WOW Legends' hosted AI, or a provider like DeepSeek directly) — *negligible* local resources, **or**
- a **local model via Ollama** — adds ~2 GB RAM; a GPU helps but isn't required (CPU-compatible).

The server runs perfectly fine with AI chat disabled or cloud-backed, so AI doesn't inflate the base requirements.
