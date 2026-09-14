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

- **官方基线** — 以 AdGuard DNS filter 为底座，覆盖广告、追踪、中文区域、加密挖矿，自带官方白名单保护。
- **深度增强** — 叠加 HaGeZi Pro Mini，补齐更广的广告、追踪、遥测覆盖。
- **安全加固** — 叠加 HaGeZi TIF，拦截恶意软件、钓鱼、C2 通信。
- **自动更新** — 每 6 小时同步上游最新规则。
- **格式标准** — 经 hostlist-compiler 官方工具编译，完全兼容 AdGuard Home / AdGuard DNS。

<hr>

## 📦 规则构成

| 数据源 | 定位 | 说明 |
|--------|------|------|
| [AdGuard DNS filter](https://github.com/AdguardTeam/AdGuardSDNSFilter) | 全球基线 | 广告、追踪、中文区域、加密挖矿 |
| [HaGeZi COMBO: PRO-TIF-MINI](https://github.com/cbuijs/hagezi) | 增强层 | HaGeZi Pro Mini + TIF 组合，广告/追踪/威胁情报 |

> 合并去重后，总规则量约 30–35 万条，文件大小约 10–12 MB。

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

- [AdGuard DNS Filter](https://github.com/AdguardTeam/AdGuardSDNSFilter) — 全球基线与中文区域
- [HaGeZi DNS Blocklists](https://github.com/hagezi/dns-blocklists) — 广告、追踪、威胁情报
- [cbuijs/hagezi](https://github.com/cbuijs/hagezi) — 预编译 COMBO 组合包
- [AdGuard Hostlist Compiler](https://github.com/AdguardTeam/HostlistCompiler) — 编译工具

<hr>

## 📄 许可证

MIT License © 2026 LucentDNS
