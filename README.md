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

- **无冗余聚合** — 拒绝简单的堆砌，以 HaGeZi 为唯一底座，直接整合 TIF 与国内优质规则，避免重复拦截。
- **家庭级稳定** — 采用 `Normal` 版本，主动规避错误追踪器误杀，真正做到“设置后忘记”。
- **国内精准补全** — 内嵌 AWAvenue Ads Rule，精准拦截国内 App 开屏、摇一摇等顽固广告。
- **自动更新** — 每 6 小时同步上游最新规则，永不过时。
- **格式标准** — 经 hostlist-compiler 官方工具编译，完全兼容 AdGuard Home / AdGuard DNS。

<hr>

## 📦 规则构成

| 数据源 | 定位 | 说明 |
|--------|------|------|
| [HaGeZi's Normal Blocklist](https://github.com/hagezi/dns-blocklists) | 核心防护 | 平衡防护，拦截广告、追踪、遥测、钓鱼、恶意软件。家庭环境首选，极低误杀。 |
| [HaGeZi's TIF Mini](https://github.com/hagezi/dns-blocklists) | 安全加固 | 核心威胁情报防护，拦截恶意软件、钓鱼及 C2 通信。 |
| [AWAvenue Ads Rule](https://github.com/TG-Twilight/AWAvenue-Ads-Rule) | 中文补全 | 专注拦截国内 App 广告 SDK（开屏、摇一摇、信息流）。 |

> 合并去重压缩后，总规则量约 35 万条。

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

- [HaGeZi DNS Blocklists](https://github.com/hagezi/dns-blocklists) — 核心防护与威胁情报
- [AWAvenue Ads Rule](https://github.com/TG-Twilight/AWAvenue-Ads-Rule) — 国内 App 广告拦截
- [AdGuard Hostlist Compiler](https://github.com/AdguardTeam/HostlistCompiler) — 编译工具

<hr>

## 📄 许可证

MIT License © 2026 LucentDNS
