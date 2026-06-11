# Install Guide

> 🚧 **Pre-release.** The full step-by-step (with the exact download links and tools)
> is finalized when **v1.0** ships. This page lays out the shape of it so you know
> what to expect. Want to play *now* instead of hosting? Use the
> [demo realm](../README.md#-try-it-right-now-no-download).

## The two editions

- **Community Edition (free, this repo):** you assemble it yourself — download the release,
  extract your client data, set up the database, configure, and launch. More hands-on, fully yours.
- **The App (supporter):** one click installs, configures, updates and manages everything.
  If you'd rather skip the manual steps, that's what it's for — see [wow-legends.eu](https://wow-legends.eu).

## What you'll need

- A machine meeting the [requirements](REQUIREMENTS.md)
- A **WoW 3.3.5a (build 12340)** client (your own copy — the repack ships **no** Blizzard data)
- MySQL 8.x and the VC++ 2015–2022 x64 redistributable

## The manual flow (high level)

1. **Download** the latest Community Edition release from the [Releases page](https://github.com/WOWLegendsHQ/wow-legends-community/releases).
2. **Set up the database** — create the WL databases and import the bundled, pre-populated data.
3. **Extract client data** — generate `maps` / `vmaps` / `mmaps` / `dbc` from your own 3.3.5a client using the bundled extractor tools, and point the server's `DataDir` at them.
4. **Configure** — set your realm name/address, rates, bot count, hardcore rules and (optionally) AI chat, in the `.conf` files.
5. **Launch** — start MySQL, the auth server, then the world server. Create your GM account and log in.

> Detailed, copy-paste steps for each stage — with screenshots — land here at the v1.0 release.
> Hosting publicly also involves port-forwarding and securing your database; that guide ships alongside.

## Getting help

- 💬 Community support: [wow-legends.eu](https://wow-legends.eu)
- 🐛 Found a bug or a gap in these docs? Open an [issue](https://github.com/WOWLegendsHQ/wow-legends-community/issues).
