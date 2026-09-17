# ✨ Lucent DNS

Luminous · Clear · Pure DNS Filtering Rules

[![GitHub Actions](https://github.com/LucentDNS/lucent-dns/actions/workflows/build.yml/badge.svg)](https://github.com/LucentDNS/lucent-dns/actions/workflows/build.yml)
[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.html)
[![Release](https://img.shields.io/github/v/release/LucentDNS/lucent-dns?include_prereleases&label=latest&style=flat)](https://github.com/LucentDNS/lucent-dns/releases/latest)

---

## 📌 Core Features

- **High-coverage filtering** — Merges HaGeZi's `Pro` (ads, tracking, malware), `TIF Mini` (threat intelligence), `DynDNS` (abused dynamic DNS) and `TikTok` (native tracker).
- **Controlled false positives** — All sources are validated and compressed, removing redundant subdomain rules.
- **AdGuard ecosystem optimized** — Compiled with official `hostlist-compiler`, fully compatible with AdGuard Home and AdGuard clients.
- **Auto-updated** — Syncs with upstream sources every 6 hours.
- **Self-maintained extension** — `local-rules.txt` allows project-specific supplementary rules.

---

## 📦 Rule Composition

| Source | Purpose | Description |
|--------|---------|-------------|
| [HaGeZi Pro](https://github.com/hagezi/dns-blocklists) | Ads & Tracking | Full-coverage core blocklist |
| [HaGeZi TIF Mini](https://github.com/hagezi/dns-blocklists) | Security | Phishing, malware, scam domains |
| [HaGeZi DynDNS](https://github.com/hagezi/dns-blocklists) | Security | Abused dynamic DNS domains |
| [HaGeZi TikTok](https://github.com/hagezi/dns-blocklists) | Tracking | TikTok native tracker domains |
| Local Rules | Supplementary | Project-specific extra rules |

> After deduplication and compression, the total rule count is approximately **360,000 - 370,000 rules** (~8-10 MB). Suitable for AdGuard Home, desktop AdGuard, and modern mobile devices.

---

## 🚀 Quick Start

### Subscription URL (Recommended: jsDelivr CDN)

Add the following URL to AdGuard Home or AdGuard client:

`https://cdn.jsdelivr.net/gh/LucentDNS/lucent-dns@main/dist/dns-filter.txt`

*(Backup GitHub Release URL: `https://github.com/LucentDNS/lucent-dns/releases/latest/download/dns-filter.txt`)*

### Manual Compilation

```bash
npm install -g @adguard/hostlist-compiler
mkdir -p dist
hostlist-compiler -c configuration.json -o dist/dns-filter.txt
```

---

## ⏰ Auto Update

GitHub Actions automatically pulls the latest upstream rules and recompiles every 6 hours.

---

## 🙏 Credits

- [HaGeZi DNS Blocklists](https://github.com/hagezi/dns-blocklists) — Ads, tracking, and threat intelligence
- [AdGuard Hostlist Compiler](https://github.com/AdguardTeam/HostlistCompiler) — Compilation tool

---

## 📄 License

GPL-3.0 License © 2026 LucentDNS
