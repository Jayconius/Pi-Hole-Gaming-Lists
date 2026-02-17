# Pi-Hole-Gaming-Lists

# Gaming Network Filters

A collection of domain lists designed for network-level filtering (Pi-hole, AdGuard Home) to improve the gaming experience by removing advertisements while maintaining core functionality.

## 📋 Features
- **Ad Blocking:** Targets ad-servers in mod managers, game launchers, and software dashboards.
- **Achievement Protection:** Specifically avoids blocking domains required for "Achievement Unlocked" notifications, cloud saves, and login authentication.
- **Broad Compatibility:** Designed to work across all major gaming platforms and desktop clients.

---

## 🚀 How to Use (Pi-hole)

To use these lists, copy the **Raw URL** below and add it to your Pi-hole "Adlists" or "Whitelist" settings.

### 1. Gaming Ads Blocklist
This list blocks banner ads and trackers in mod managers and launchers.
- **URL:** `https://raw.githubusercontent.com/Jayconius/Pi-Hole-Gaming-Lists/refs/heads/main/Gaming%20Ads%20Blocklist.txt`

### 2. Gaming Whitelist
This list contains essential domains that should be **allowed** to ensure achievements and cloud saves work.
- **URL:** `https://raw.githubusercontent.com/Jayconius/Pi-Hole-Gaming-Lists/refs/heads/main/Gaming%20Whitelist.txt`

---

## 🛠 Setup Instructions
1. Navigate to your **Pi-hole Dashboard**.
2. Go to **Group Management** > **Adlists**.
3. Paste the **Raw URL** from above into the Address field.
4. Click **Add**.
5. Run `pihole -g` in your terminal or go to **Tools** > **Update Gravity** to apply changes.

## ⚖️ Maintenance
This repository is updated as new ad-servers are identified or when platforms change their telemetry endpoints. Feel free to monitor the commit history for changes.
