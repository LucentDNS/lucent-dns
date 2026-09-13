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

- **顶级拦截** — 以社区第一梯队的 HaGeZi Multi PRO 为核心，提供广覆盖的广告、追踪、遥测和恶意软件拦截。
- **安全加固** — 叠加 HaGeZi TIF Mini，额外拦截钓鱼、C2 和恶意域名。
- **中文补充** — 内置 AdGuard Chinese filter，精准补齐中文广告。
- **官方误报保护** — 编译时应用 AdGuard 官方 exclusions 排除列表，过滤已知会导致网站损坏的域名。
- **自动更新** — 每 6 小时同步上游最新规则，永不过时。
- **格式标准** — 经 hostlist-compiler 官方工具编译，完全兼容 AdGuard Home / AdGuard DNS。

<hr>

## 📦 规则构成

| 数据源 | 定位 | 说明 |
|--------|------|------|
| [HaGeZi's Multi PRO](https://github.com/hagezi/dns-blocklists) | 全球广告/追踪 | 社区顶级平衡列表 |
| [HaGeZi's TIF Mini](https://github.com/hagezi/dns-blocklists) | 安全加固 | 威胁情报，恶意软件、钓鱼、C2 |
| [AdGuard Chinese filter](https://github.com/AdguardTeam/AdguardFilters) | 中文区域 | 中文广告服务器及第一方补充 |

> 合并去重并应用官方排除后，总规则量约 30-40 万条，文件大小约 10-15 MB。

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

- [HaGeZi DNS Blocklists](https://github.com/hagezi/dns-blocklists) — 广告、追踪、威胁情报
- [AdGuard Filters](https://github.com/AdguardTeam/AdguardFilters) — 中文广告、官方排除列表
- [AdGuard Hostlist Compiler](https://github.com/AdguardTeam/HostlistCompiler) — 编译工具

<hr>

## 📄 许可证

MIT License © 2026 LucentDNS
