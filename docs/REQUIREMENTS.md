# System Requirements

WOW Legends runs on modest hardware. **What you need depends mostly on how many AI
bots you want living in your world** — that's the main resource driver, and it's a
config setting you tune. Pick a profile below.

## Baseline (any setup)

- **OS:** Windows 10 / 11 or Windows Server (64-bit)
- **CPU:** modern multi-core (4 cores minimum; more cores = more bots — the bot AI runs across map-update threads)
- **Storage:** **SSD strongly recommended** (a hard drive can stall the database under load). ~25–40 GB free for the server, extracted client data and database.
- **A WoW 3.3.5a (build 12340) client** — needed once to extract world data (no Blizzard data is shipped)
- **Bundled/required runtime:** MySQL 8.x and the Microsoft VC++ 2015–2022 x64 Redistributable (the App installs these for you)

## Server profiles

RAM below is the **whole picture** — it already accounts for the worldserver, MySQL (~1–2 GB typical) and the OS.

| Profile | AI bots | Grid preload | Total RAM | Good for |
|---|---|---|---|---|
| **Starter** | ~25–50 | Off (default) | **8 GB** | Solo or a few friends, on a modest box |
| **Community** | ~100–200 | Off | **16 GB** | An active small community |
| **Living World** | 500+ | On | **16 GB** (24+ comfortable) | A busy, fully-populated world |

> These are starting points — every figure is a config setting you can tune. Fewer bots =
> less RAM and CPU. For reference: on the public demo realm, **500 bots + everything loaded
> uses ~7.5 GB across all server processes** at a 5–16 ms server tick on a 6-core CPU.

## The two settings that drive the profiles

- **Bot count** — `AiPlayerbot.MinRandomBots` / `MaxRandomBots`. The biggest lever for both RAM and CPU.
- **Grid preload** — `PreloadAllNonInstancedMapGrids`. Off by default; turning it on uses a few GB more RAM but preloads the whole world for maximum stability and zero load-hitches. Recommended for big servers with RAM to spare.

## AI features (optional)

The AI companion & bot chat need a language-model backend — either:

- a **cloud API key** (e.g. DeepSeek — extremely cheap, *negligible* local resources), **or**
- a **local model via Ollama** (adds ~2 GB RAM; a GPU helps but isn't required).

The server runs perfectly fine with AI chat disabled or cloud-backed, so AI doesn't inflate the base requirements.
