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

- **官方核心** — 以 AdGuard DNS Filter 为基础，经过数亿用户验证，稳定性极高
- **多维补充** — 叠加 NoCoin（反挖矿）、CJX's Annoyance（反骚扰）、Steven Black（经典 hosts）三大成熟源
- **自动更新** — 每 6 小时同步上游最新规则，永不过时
- **格式标准** — 经 hostlist-compiler 编译，完全兼容 AdGuard Home / AdGuard DNS

<hr>

## 📦 规则构成

| 数据源 | 格式 | 说明 |
|--------|------|------|
| [AdGuard DNS Filter](https://github.com/AdguardTeam/AdGuardSDNSFilter) | Adblock | 官方精选组合，涵盖广告、追踪、移动广告等（约 8 万条） |
| [NoCoin Filter List](https://github.com/hoshsadiq/adblock-nocoin-list) | hosts | 拦截浏览器端加密货币挖矿脚本 |
| [CJX's Annoyance List](https://github.com/cjx82630/cjxlist) | Adblock | 拦截 Cookie 提示、订阅弹窗等烦人元素 |
| [Steven Black's Hosts](https://github.com/StevenBlack/hosts) | hosts | 经典 hosts 集合，覆盖 adware + malware |

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

    AdGuard DNS Filter — 官方核心规则

    NoCoin Filter List — 反挖矿拦截

    CJX's Annoyance List — 反骚扰拦截

    Steven Black's Hosts — 经典 hosts 集合

<hr>
📄 许可证

MIT License © 2026 LucentDNS
