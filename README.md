<h1 align="center">✨ Lucent DNS</h1>

<p align="center">发光的 · 清澈的 · 纯净的 DNS 过滤规则</p>

<p align="center">
  <a href="https://github.com/LucentDNS/lucent-dns/actions/workflows/build.yml">
    <img src="https://github.com/LucentDNS/lucent-dns/actions/workflows/build.yml/badge.svg" alt="GitHub Actions">
  </a>
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT">
  </a>
  <a href="https://github.com/LucentDNS/lucent-dns/releases/latest">
    <img src="https://img.shields.io/github/v/release/LucentDNS/lucent-dns?include_prereleases&label=latest&style=flat" alt="Release">
  </a>
</p>

<hr>

## 📌 特性

- **三重防护** — HaGeZi's Pro Blocklist 为基础，叠加威胁情报源（TIF）与恶意软件专项拦截，强化安全防护
- **安全增强** — 集成 HaGeZi Threat Intelligence Feeds 与 Dandelion Sprout's Anti-Malware List，提升对恶意软件、钓鱼、诈骗的拦截能力
- **自动更新** — 每 6 小时同步上游最新规则，永不过时

<hr>

## 📦 规则构成

| 数据源 | 格式 | 说明 |
|--------|------|------|
| [HaGeZi's Pro Blocklist](https://github.com/hagezi/dns-blocklists) | Adblock | 社区公认的高强度拦截规则，覆盖广告、追踪、恶意软件、诈骗等 |
| [HaGeZi's TIF mini](https://github.com/hagezi/dns-blocklists) | Adblock | 精简版威胁情报源，针对恶意软件、钓鱼、诈骗等实时威胁 |
| [Dandelion Sprout's Anti-Malware List](https://github.com/DandelionSprout/adfilt) | Adblock | 专门针对恶意软件、病毒、蠕虫等威胁的拦截列表 |

> 合并去重压缩后，总规则量以编译后实际数据为准。

<hr>

## 🚀 快速开始

### 订阅地址

在 AdGuard Home 或 AdGuard 客户端中添加以下 URL：

https://github.com/LucentDNS/lucent-dns/releases/latest/download/dns-filter.txt

### 手动编译

```bash
npm install -g @adguard/hostlist-compiler
hostlist-compiler -c configuration.json -o dns-filter.txt
```

<hr>
⏰ 自动更新

GitHub Actions 每 6 小时自动拉取上游最新规则并重新编译发布。
<hr>
🙏 致谢

    HaGeZi's Pro Blocklist — 社区公认的高强度拦截规则

    HaGeZi's Threat Intelligence Feeds — 实时威胁情报源

    Dandelion Sprout's Anti-Malware List — 恶意软件专项拦截列表

<hr>
📄 许可证

MIT License © 2026 LucentDNS
