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

- **纯净防护** — 基于 HaGeZi Pro + TIF Mini 编译，过滤广告、追踪器、恶意域名
- **性能优先** — 合并去重后约 28-30 万条规则，适合 128MB+ 内存设备
- **智能威胁** — 内置威胁情报精简版，拦截钓鱼、勒索、C2 服务器
- **自动更新** — 每 6 小时同步上游最新规则，永不过时

<hr>

## 📦 规则构成

| 规则源 | 说明 | 规则量 |
| :--- | :--- | :--- |
| HaGeZi Pro | 社区标杆 DNS 过滤列表，低误杀，覆盖广告/追踪/恶意域名 | 225,134 条 |
| HaGeZi TIF Mini | 威胁情报精简版，专为家用设备优化 | 176,168 条 |
| **合并去重后** | 双源交叉去重，兼顾性能与安全 | **360,508 条**（含元数据） |

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

    HaGeZi's DNS Blocklists — 核心数据源，感谢 HaGeZi 的卓越贡献！❤️

<hr>
📄 许可证

MIT License © 2026 LucentDNS
