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

- **双源融合** — AdGuard DNS Filter + AdRules DNS List，全球基础拦截与国内广告专项增强
- **国内优化** — AdRules 针对百度、腾讯、字节跳动等国内广告联盟深度拦截，弥补通用规则的不足
- **自动更新** — 每 6 小时同步上游最新规则，永不过时

<hr>

## 📦 规则构成

| 数据源 | 格式 | 说明 |
|--------|------|------|
| [AdGuard DNS Filter](https://github.com/AdguardTeam/AdguardSDNSFilter) | Adblock | AdGuard 官方 DNS 优化规则，覆盖广告、追踪、恶意软件 |
| [AdRules DNS List](https://github.com/Cats-Team/AdRules) | Adblock | 国内广告联盟专项拦截，覆盖百度、腾讯、字节跳动、阿里等 |

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

    AdGuard DNS Filter — 官方核心数据源

    AdRules — 国内广告专项拦截列表

    Hostlist Compiler — 官方编译工具

<hr>
📄 许可证

MIT License © 2026 LucentDNS
