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

## 📌 核心特性

- **极低误杀，设置后即忘** — 以社区公认的黄金平衡列表 `HaGeZi NORMAL` 和 `OISD` 为核心。
- **拒绝过度拦截** — 坚决不包含容易导致网站崩溃、App 功能异常的高误杀规则，保护您的日常冲浪体验。
- **多格式输出** — 自动编译并发布 AdGuard、Hosts、Domains 三种格式，覆盖全平台设备。
- **自动更新** — 每 6 小时同步上游最新规则，永不过时。
- **格式标准** — 经 `hostlist-compiler` 官方工具编译，完全兼容 AdGuard Home / AdGuard DNS。

<hr>

## 📦 规则构成

| 数据源 | 定位 | 说明 |
|--------|------|------|
| [HaGeZi Normal](https://github.com/hagezi/dns-blocklists) | 全球广告/追踪 | 社区顶级平衡列表，家庭首选 |
| [OISD Blocklist Big](https://oisd.nl/) | 全球广告/追踪 | 极低误杀的经典大列表，与 HaGeZi 互补 |

> 合并去重后，总规则量通常在 **18–22 万条**之间，文件大小约 **6–8 MB**。

<hr>

## 🚀 快速开始

### 订阅地址

根据您的设备，选择对应格式的 URL 进行订阅（所有链接都指向最新版本）：

- **AdGuard Home / AdGuard 客户端**：
`https://github.com/LucentDNS/lucent-dns/releases/latest/download/dns-filter.txt`

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
- [OISD](https://oisd.nl/) — 经典广告拦截列表
- [AdGuard Hostlist Compiler](https://github.com/AdguardTeam/HostlistCompiler) — 编译工具

<hr>

## 📄 许可证

MIT License © 2026 LucentDNS
