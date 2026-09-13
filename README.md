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

- **从原始源构建** — 不依赖任何二次聚合列表，直接使用 AdGuard、EasyList、EasyPrivacy 等维护团队的原始输出，与官方 AdGuard DNS filter 同级。
- **全球覆盖** — 广告、追踪、加密挖矿、恶意软件、钓鱼，全维度覆盖，面向全球用户。
- **中文区域补充** — 内置 AdGuard Chinese filter，精准补充中文广告生态。
- **官方误报保护** — 应用 AdGuard 官方 exclusions 排除规则，过滤已知会导致网站损坏的域名。
- **自动更新** — 每 6 小时同步上游最新规则，永不过时。
- **格式标准** — 经 hostlist-compiler 官方工具编译，完全兼容 AdGuard Home / AdGuard DNS。

<hr>

## 📦 规则构成

| 数据源 | 定位 | 说明 |
|--------|------|------|
| [AdGuard Base filter](https://github.com/AdguardTeam/AdguardFilters) | 全球广告 | 广告服务器、第一方、外国服务器 |
| [EasyList](https://github.com/easylist/easylist) | 广告补充 | 经典广告列表，生态最广 |
| [AdGuard Tracking Protection](https://github.com/AdguardTeam/AdguardFilters) | 追踪防护 | 第三方、第一方追踪器 |
| [EasyPrivacy](https://github.com/easylist/easylist) | 追踪补充 | 覆盖面广的隐私追踪域名库 |
| [HaGeZi's TIF Mini](https://github.com/hagezi/dns-blocklists) | 安全加固 | 威胁情报，拦截恶意软件、钓鱼、C2 |
| [URLHaus](https://malware-filter.gitlab.io/malware-filter/) | 恶意软件 | 专业恶意 URL 库 |
| [AdGuard Base cryptominers](https://github.com/AdguardTeam/AdguardFilters) | 加密挖矿 | 官方维护的挖矿脚本拦截 |
| [AdGuard Chinese filter](https://github.com/AdguardTeam/AdguardFilters) | 中文区域 | 中文广告服务器及第一方补充 |

> 合并去重压缩后，总规则量约 20–25 万条。

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

    AdGuard Filters — 广告、追踪、挖矿、中文区域规则

    EasyList — 广告与追踪域名库

    HaGeZi DNS Blocklists — 威胁情报

    URLHaus Malware Filter — 恶意 URL 库

    AdGuard Hostlist Compiler — 编译工具

<hr>

## 📄 许可证

MIT License © 2026 LucentDNS
