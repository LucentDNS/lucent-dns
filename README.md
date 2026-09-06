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

- **双源融合** — 精选 AdGuard DNS filter + OISD Blocklist Big，覆盖广告、追踪器、恶意软件、钓鱼
- **性能优先** — 合并去重压缩后约 35 万条规则，运行轻快
- **官方品质** — 两个源均为业界公认精品，各自有专业团队持续维护
- **自动更新** — 每 6 小时同步上游最新规则，永不过时

<hr>

## 📦 规则构成

| 数据源 | 说明 |
|--------|------|
| AdGuard Base Filter | 官方核心广告域名库（adservers + first-party + foreign + cryptominers） |
| AdGuard Mobile Ads Filter | 移动端广告拦截 |
| AdGuard Tracking Protection Filter | 官方核心追踪域名库（third-party + first-party + mobile） |
| EasyList + EasyPrivacy | 社区经典广告/追踪列表 |
| AdGuard Chinese Filter | 中文地区广告拦截 |
| EasyList China | 中文地区补充 |
| OISD Blocklist Big | 社区高覆盖综合性列表 |
| **手动修正** | 用户反馈的误杀/遗漏通过 `custom_exclusions.txt` 快速响应 |

> 合并去重压缩后，总规则量约 **35~40 万条**

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

    AdGuard DNS filter — 官方核心源

    OISD Blocklist — 社区优秀综合列表

    Hostlist Compiler — 官方编译工具

<hr>
📄 许可证

MIT License © 2026 LucentDNS
