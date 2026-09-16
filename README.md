# ✨ Lucent DNS

Luminous · Clear · Pure DNS Filtering Rules

[![GitHub Actions](https://github.com/LucentDNS/lucent-dns/actions/workflows/build.yml/badge.svg)](https://github.com/LucentDNS/lucent-dns/actions/workflows/build.yml)
[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.html)
[![Release](https://img.shields.io/github/v/release/LucentDNS/lucent-dns?include_prereleases&label=latest&style=flat)](https://github.com/LucentDNS/lucent-dns/releases/latest)

---

## 📌 Core Features

- **Ultra-lightweight, mobile-first** — Merges only HaGeZi's `Pro Mini` (core ad blocking) and `TIF Mini` (security).
- **Low false-positive rate** — Removes aggressive, high-breakage rules to ensure a seamless browsing experience.
- **AdGuard ecosystem optimized** — Compiled with official `hostlist-compiler`, ensuring full compatibility with AdGuard Home and AdGuard clients.
- **Auto-updated** — Syncs with upstream sources every 6 hours.
- **Universal compatibility** — Works seamlessly on desktop AdGuard Home and mobile AdGuard clients with the same subscription URL.

---

## 📦 Rule Composition

| Source | Purpose | Description |
|--------|---------|-------------|
| [HaGeZi Pro Mini](https://github.com/hagezi/dns-blocklists) | Global Ads & Tracking | Ultra-compact core domain list, saving battery and RAM |
| [HaGeZi TIF Mini](https://github.com/hagezi/dns-blocklists) | Security | Blocks phishing, malware, scams, and more with a friendly file size |

> After deduplication and compression, the total rule count is approximately **200,000 - 220,000 rules** (~4-6 MB). Perfect for mobile devices and lightweight hardware.

---

## 🚀 Quick Start

### Subscription URL (Recommended: jsDelivr CDN)

Add the following URL to AdGuard Home or AdGuard client:

`https://cdn.jsdelivr.net/gh/LucentDNS/lucent-dns@main/dist/dns-filter.txt`

*(Backup GitHub Release URL: `https://github.com/LucentDNS/lucent-dns/releases/latest/download/dns-filter.txt`)*

### Manual Compilation

```bash
# Install the official compiler
npm install -g @adguard/hostlist-compiler

# Create output directory and compile
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
