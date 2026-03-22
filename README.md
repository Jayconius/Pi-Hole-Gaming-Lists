# 🎮 Pi-Hole Gaming Lists

> **DNS whitelists and blocklists for gamers** — keeps achievements, cloud saves, gacha pulls, storefronts, and multiplayer working while blocking ads and trackers across every major gaming platform.

[![Last Updated](https://img.shields.io/badge/Last%20Updated-March%202026-brightgreen?style=flat-square)](https://github.com/Jayconius/Pi-Hole-Gaming-Lists/commits/main)
[![Platforms](https://img.shields.io/badge/Platforms-20%2B-blue?style=flat-square)](#-platform-coverage)
[![Compatible](https://img.shields.io/badge/Compatible-Pi--hole%20%7C%20AdGuard%20Home-orange?style=flat-square)](#-how-to-use)
[![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)](LICENSE)

---

## 📋 What's in this repo

| File | Type | Description |
|------|------|-------------|
| [`Gaming-Whitelist.txt`](Gaming-Whitelist.txt) | ✅ Whitelist | Allows essential domains for 20+ gaming platforms — login, achievements, cloud saves, store, CDN |
| [`Gaming-Gacha-Whitelist.txt`](Gaming-Gacha-Whitelist.txt) | ✅ Whitelist | Allows domains for the top 20 F2P gacha games — login, gacha pulls, events, patch downloads |
| [`Gaming-Ads-Blocklist.txt`](Gaming-Ads-Blocklist.txt) | 🚫 Blocklist | Blocks ad servers and trackers in game launchers and mod managers |

---

## 🚀 How to Use

### Pi-hole (v5 / v6)

1. Go to your **Pi-hole Admin Dashboard**
2. Navigate to **Group Management → Adlists** (for blocklists) or **Whitelist** (for whitelists)
3. Paste the **Raw URL** from the table below
4. Click **Add**, then run **Tools → Update Gravity** or run:

```bash
pihole -g
```

### AdGuard Home

1. Go to **Filters → DNS Blocklists** (or **DNS Allowlists**)
2. Click **Add blocklist → Add a custom list**
3. Paste the Raw URL and save

---

## 🔗 Raw URLs

| List | Raw URL |
|------|---------|
| Gaming Whitelist | `https://raw.githubusercontent.com/Jayconius/Pi-Hole-Gaming-Lists/main/Gaming-Whitelist.txt` |
| Gacha Whitelist | `https://raw.githubusercontent.com/Jayconius/Pi-Hole-Gaming-Lists/main/Gaming-Gacha-Whitelist.txt` |
| Gaming Ads Blocklist | `https://raw.githubusercontent.com/Jayconius/Pi-Hole-Gaming-Lists/main/Gaming-Ads-Blocklist.txt` |

---

## 🖥️ Platform Coverage

### Gaming-Whitelist.txt

Each platform is fully covered for login, achievements, cloud saves, multiplayer, store/CDN, and friend lists.

| Platform | Login | Achievements | Cloud Saves | Store / CDN | Multiplayer |
|----------|:-----:|:------------:|:-----------:|:-----------:|:-----------:|
| Steam (Valve) | ✅ | ✅ | ✅ | ✅ | ✅ |
| Epic Games Store | ✅ | ✅ | ✅ | ✅ | ✅ |
| Xbox / Game Pass (PC) | ✅ | ✅ | ✅ | ✅ | ✅ |
| PlayStation 4 / 5 (PSN) | ✅ | ✅ (Trophies) | ✅ | ✅ | ✅ |
| Nintendo Switch Online | ✅ | N/A | ✅ | ✅ (eShop) | ✅ |
| Minecraft (Java + Bedrock) | ✅ | ✅ | ✅ | ✅ (Marketplace) | ✅ (Realms) |
| EA App | ✅ | ✅ | ✅ | ✅ | ✅ |
| Ubisoft Connect | ✅ | ✅ | ✅ | ✅ | ✅ |
| Blizzard Battle.net | ✅ | ✅ | ✅ | ✅ | ✅ |
| Activision / Call of Duty | ✅ | ✅ | ✅ | ✅ | ✅ |
| Riot Games (Valorant / LoL) | ✅ | ✅ | ✅ | ✅ | ✅ |
| Rockstar / Social Club | ✅ | ✅ | ✅ | ✅ | ✅ |
| Bethesda / id Software | ✅ | ✅ | ✅ | ✅ (Mods) | ✅ |
| GOG Galaxy | ✅ | ✅ | ✅ | ✅ | ✅ |
| 2K Launcher | ✅ | ✅ | ✅ | ✅ | ✅ |
| Paradox Launcher | ✅ | ✅ | ✅ | ✅ (Mods) | ✅ |
| Roblox | ✅ | ✅ | ✅ | ✅ | ✅ |
| Discord | ✅ | N/A | N/A | N/A | ✅ |

### Gaming-Gacha-Whitelist.txt

Covers login, gacha/banner pulls, events, friend lists, and patch delivery for all titles.

| Game | Developer | Platforms |
|------|-----------|-----------|
| Genshin Impact | HoYoverse | PC, Mobile, PS4/5 |
| Honkai: Star Rail | HoYoverse | PC, Mobile, PS5 |
| Zenless Zone Zero | HoYoverse | PC, Mobile, PS5 |
| Honkai Impact 3rd | HoYoverse | PC, Mobile |
| Wuthering Waves | Kuro Games | PC, Mobile, Console |
| Arknights | Hypergryph / Yostar | Mobile |
| Arknights: Endfield | Hypergryph / Gryphline | PC, Mobile |
| NIKKE: Goddess of Victory | Shift Up / Level Infinite | PC, Mobile |
| Punishing: Gray Raven | Kuro Games | PC, Mobile |
| Fate/Grand Order | Aniplex | Mobile |
| Reverse: 1999 | Bluepoch | PC, Mobile |
| Limbus Company | Project Moon | PC, Mobile |
| Path to Nowhere | AISNO Games | Mobile |
| Tower of Fantasy | Hotta Studio / Level Infinite | PC, Mobile |
| Solo Leveling: Arise | Netmarble | PC, Mobile |
| Infinity Nikki | Infold Games / Level Infinite | PC, Mobile |
| Uma Musume: Pretty Derby | Cygames / DMM | PC, Mobile |
| Dragon Ball Legends | Bandai Namco | Mobile |
| Dragon Ball Z: Dokkan Battle | Bandai Namco | Mobile |
| Pokémon TCG Pocket | DeNA / The Pokémon Company | Mobile |
| Neverness to Everness | Seasun Games | PC, Mobile |

---

## 🛡️ What the Blocklist Targets

`Gaming-Ads-Blocklist.txt` specifically targets:

- Banner and video ads in **mod managers** (CurseForge, Nexus Mods)
- Ads and sponsored content in **game launchers** (Epic, EA App, GOG)
- Tracking pixels and telemetry in **software dashboards**
- Aggressive ad-injection in **free-to-play game UIs**

> ⚠️ **Achievement and login domains are intentionally excluded from the blocklist.** The whitelist files exist precisely to ensure blocking never interferes with core game functionality.

---

## ⚠️ Known Quirks

**CurseForge** — If the launcher shows a blank page after applying the blocklist, delete `%AppData%\CurseForge\cache` and restart.

**Amazon App** — If your Amazon shopping app breaks, whitelist `aax-eu.amazon-adsystem.com` or `aax-us.amazon-adsystem.com`. This domain is on the blocklist because it serves ads inside CurseForge.

**Google Shopping** — If product links or images break in Google Shopping, whitelist `googleads.g.doubleclick.net`. Note this will also re-enable ad-incentive rewards in some mobile apps (watch an ad for a reward).

**Minecraft Bedrock Marketplace** — If purchased content or skin packs are missing, make sure `api.minecraftservices.com` is whitelisted. This is the most common cause of Marketplace issues behind a Pi-hole.

**Xbox App / Game Pass** — If game downloads fail with error `0x00000001`, ensure `settings-win.data.microsoft.com` is whitelisted. This is a known Pi-hole interaction with the Xbox App installer.

**Nintendo Switch** — If your Switch shows a "Registration required" captive portal warning on your home network, whitelist `ctest.cdn.nintendo.net`. The Switch hits this domain immediately on connecting to any network.

---

## 🔄 Maintenance

Lists are reviewed and updated when:
- Platforms update their infrastructure or CDN endpoints
- New games or launchers are added
- Community reports a broken domain

Check the [commit history](https://github.com/Jayconius/Pi-Hole-Gaming-Lists/commits/main) to see what's changed recently.

---

## 🤝 Contributing

Found a domain that's missing or incorrectly blocked? Open an **Issue** or submit a **Pull Request**.

When reporting a broken game or platform, please include:
- The game or launcher affected
- What specifically stopped working (login, achievements, downloads, etc.)
- The domain you found in your Pi-hole query log (if known)

---

## 📣 Related Communities

If this list helped you, these are the communities where others are solving the same problems:

- [r/pihole](https://www.reddit.com/r/pihole/) — Pi-hole support and list sharing
- [Pi-hole Discourse Forum](https://discourse.pi-hole.net/) — official community forum
- [r/homelab](https://www.reddit.com/r/homelab/) — home networking and self-hosted tools
- [r/selfhosted](https://www.reddit.com/r/selfhosted/) — self-hosted software community

---

## ⚖️ Disclaimer

This project is not affiliated with Pi-hole, AdGuard, or any of the game developers or publishers listed. All game and platform names are trademarks of their respective owners. These lists are provided as-is with no warranty — always review domain lists before applying them to your network.

---

*If this list saved your achievements, give it a ⭐ — it helps others find it.*
