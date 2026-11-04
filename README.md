# 🎮 Pi-Hole Gaming Lists

> **DNS whitelists and blocklists for gamers** — keeps achievements, cloud saves, gacha pulls, storefronts, and multiplayer working while blocking ads and trackers across every major gaming platform.

[![Last Updated](https://img.shields.io/badge/Last%20Updated-November%202026-brightgreen?style=flat-square)](https://github.com/Jayconius/Pi-Hole-Gaming-Lists/commits/main)
[![Platforms](https://img.shields.io/badge/Platforms-20%2B-blue?style=flat-square)](#-platform-coverage)
[![Compatible](https://img.shields.io/badge/Compatible-Pi--hole%20%7C%20AdGuard%20Home-orange?style=flat-square)](#-how-to-use)
[![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)](LICENSE)

---

## 📋 What's in this repo

| File | Type | Description |
|------|------|-------------|
| [`Gaming-Whitelist.txt`](Gaming-Whitelist.txt) | ✅ Whitelist | Allows essential domains for 20+ gaming platforms — login, achievements, cloud saves, store, CDN |
| [`Gaming-Gacha-Whitelist.txt`](Gaming-Gacha-Whitelist.txt) | ✅ Whitelist | Allows domains for 33 F2P gacha games — login, gacha pulls, events, patch downloads |
| [`Gaming-Ads-Blocklist.txt`](Gaming-Ads-Blocklist.txt) | 🚫 Blocklist | Blocks ad servers and trackers in game launchers and mod managers |

---

## 🚀 How to Use

### Pi-hole v6

1. Go to your **Pi-hole Admin Dashboard**
2. Navigate to **Group Management → Lists**
3. Paste the **Raw URL** from the table below
4. Add it as a **blocklist** or an **allowlist**, matching the list type
5. Run **Tools → Update Gravity** or run:

```bash
pihole -g
```

### Pi-hole v5

Pi-hole v5 can subscribe to blocklists but not allowlists, so the whitelists can't be added by URL.

- **Blocklist:** add the Raw URL under **Group Management → Adlists**, then update gravity
- **Whitelists:** add the domains you need one at a time under **Whitelist**, or upgrade to v6

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

Each platform has domains for login, achievements, cloud saves, multiplayer, store/CDN, and friend lists. Checkmarks show intended coverage, not results from testing every platform, so please report anything that breaks.

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
| Square Enix / Final Fantasy XIV | ✅ | N/A | N/A | ✅ (Patches) | ✅ |
| GeForce NOW | ✅ | N/A | N/A | N/A | ✅ (Streaming) |
| Twitch & Prime Gaming | ✅ | N/A | N/A | ✅ (Drops / Loot) | N/A |

Also includes **anti-cheat** domains (Easy Anti-Cheat, BattlEye) — games using them will refuse to launch if these are blocked.

### Gaming-Gacha-Whitelist.txt

Domains for login, gacha/banner pulls, events, friend lists, and patch delivery, where known. Every domain exists in public DNS, but the list hasn't been tested in the games. Coverage is thinner for titles where only site and login domains are known, such as Dragon Ball Legends, Pokémon TCG Pocket, Neverness to Everness, Path to Nowhere, and most recent additions.

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
| Infinity Nikki | Infold Games | PC, Mobile |
| Uma Musume: Pretty Derby | Cygames | PC, Mobile |
| Dragon Ball Legends | Bandai Namco | Mobile |
| Dragon Ball Z: Dokkan Battle | Bandai Namco | Mobile |
| Pokémon TCG Pocket | DeNA / The Pokémon Company | Mobile |
| Neverness to Everness | Hotta Studio / Perfect World | PC, Mobile |
| Blue Archive | Nexon | PC, Mobile |
| Epic Seven | Smilegate | PC, Mobile |
| Girls' Frontline 2: Exilium | Sunborn | PC, Mobile |
| Azur Lane | Manjuu / Yostar | Mobile |
| Mahjong Soul | Cat Food Studio / Yostar | PC, Mobile |
| Stella Sora | Yostar | PC, Mobile |
| Snowbreak: Containment Zone | Seasun Games | PC, Mobile |
| Love and Deepspace | Infold Games | Mobile |
| Cookie Run: Kingdom | Devsisters | Mobile |
| Persona 5: The Phantom X | Sega / Perfect World | PC, Mobile |
| Duet Night Abyss | Pan Studio / Hero Games | PC, Mobile |
| Brown Dust 2 | Neowiz | PC, Mobile |

---

## 🛡️ What the Blocklist Targets

`Gaming-Ads-Blocklist.txt` specifically targets:

- Banner and video ads in **mod managers and mod sites** (CurseForge, Thunderstore Mod Manager, Modrinth App, Nexus Mods website)
- Usage tracking and telemetry in **game launchers** (Epic, EA App)
- Tracking pixels and telemetry in **software dashboards**
- Aggressive ad-injection in **free-to-play game UIs**

Most entries come from real ad traffic captured in Thunderstore Mod Manager, Modrinth App, and CurseForge with blocking turned off. Vortex is not included because it reportedly shows no ads.

> ⚠️ **Achievement and login domains are intentionally excluded from the blocklist.** The whitelist files exist precisely to ensure blocking never interferes with core game functionality.

---

## ⚠️ Known Quirks

**Exact Matches** — In Pi-hole, list entries match the exact domain only. `doubleclick.net` doesn't cover `securepubads.g.doubleclick.net`, so subdomains are listed separately. When troubleshooting, whitelist the exact domain shown in your query log.

**CurseForge** — If the launcher shows a blank page after applying the blocklist, delete `%AppData%\CurseForge\cache` and restart.

**Amazon App** — If your Amazon shopping app or Amazon ads-related pages break, whitelist `aax.amazon-adsystem.com`, `aax-eu.amazon-adsystem.com`, or `c.amazon-adsystem.com`. These are on the blocklist because they serve ads inside mod managers.

**Google Shopping** — If product links or images break in Google Shopping, whitelist `googleads.g.doubleclick.net`. Note this will also re-enable ad-incentive rewards in some mobile apps (watch an ad for a reward).

**Rewarded Video Ads** — `imasdk.googleapis.com` is on the blocklist, so "watch an ad for a reward" videos may stop working in some mobile games. Whitelist it if you rely on them.

**Modrinth App** — When its ads are blocked, the app can send a very large number of repeat DNS lookups (see [modrinth/code#5367](https://github.com/modrinth/code/issues/5367)). If your Pi-hole starts rate-limiting that device, raise the rate limit in Pi-hole's settings.

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
