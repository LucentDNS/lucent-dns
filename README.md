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

- **成熟底子** — 以 AdGuard DNS filter 为核心，官方持续维护，覆盖广告、追踪、中文区域、加密挖矿。
- **厂商遥测补充** — 叠加 HaGeZi Windows/Office 和 Vivo 追踪列表，补上官方 DNS filter 不覆盖的系统级遥测。
- **安全加固** — 叠加 HaGeZi TIF Mini 纯威胁情报，拦截恶意软件、钓鱼和 C2 通信。
- **无冗余集成** — 四个源各管一个维度，彼此无上下游关系，不存在重复聚合。
- **自动更新** — 每 6 小时同步上游最新规则，永不过时。
- **格式标准** — 经 hostlist-compiler 官方工具编译，完全兼容 AdGuard Home / AdGuard DNS。

<hr>

## 📦 规则构成

| 数据源 | 定位 | 说明 |
|--------|------|------|
| [AdGuard DNS filter](https://github.com/AdguardTeam/AdGuardSDNSFilter) | 广告/追踪/中文/挖矿 | 官方成熟聚合底子 |
| [HaGeZi's Windows/Office Tracker](https://github.com/hagezi/dns-blocklists) | 桌面遥测 | Windows 和 Office 遥测域名 |
| [HaGeZi's Vivo Tracker](https://github.com/hagezi/dns-blocklists) | 手机遥测 | Vivo 系统与内置应用遥测 |
| [HaGeZi's TIF Mini](https://github.com/hagezi/dns-blocklists) | 安全加固 | 威胁情报，恶意软件、钓鱼、C2 |

> 合并去重压缩后，总规则量约 28–32 万条。

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

## ⏰ 自动更新

GitHub Actions 每 6 小时自动拉取上游最新规则并重新编译发布。

<hr>

## 🙏 致谢

- [AdGuard Filters](https://github.com/AdguardTeam/AdguardFilters) — 广告、追踪、挖矿、中文区域规则
- [HaGeZi DNS Blocklists](https://github.com/hagezi/dns-blocklists) — 威胁情报
- [AdGuard Hostlist Compiler](https://github.com/AdguardTeam/HostlistCompiler) — 编译工具

<hr>

## 📄 许可证

MIT License © 2026 LucentDNS
