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

- **平衡拦截** — 以社区公认的黄金平衡列表 HaGeZi Normal 为核心，覆盖广告、追踪、遥测、分析。
- **安全加固** — 叠加 HaGeZi TIF Mini，额外拦截恶意软件、钓鱼、C2 通信。
- **同源维护** — 两个源均来自 HaGeZi，无规则冲突，去重后体积精简。
- **自动更新** — 每 6 小时同步上游最新规则，永不过时。
- **格式标准** — 经 hostlist-compiler 官方工具编译，完全兼容 AdGuard Home / AdGuard DNS。

<hr>

## 📦 规则构成

| 数据源 | 定位 | 说明 |
|--------|------|------|
| [HaGeZi Normal](https://github.com/hagezi/dns-blocklists) | 全球广告/追踪 | 社区顶级平衡列表，家庭首选 |
| [HaGeZi TIF Mini](https://github.com/hagezi/dns-blocklists) | 安全加固 | 威胁情报，恶意软件、钓鱼、C2 |

> 合并去重后，总规则量约 28–32 万条，文件大小约 8–10 MB。

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
- [AdGuard Hostlist Compiler](https://github.com/AdguardTeam/HostlistCompiler) — 编译工具

<hr>

## 📄 许可证

MIT License © 2026 LucentDNS
