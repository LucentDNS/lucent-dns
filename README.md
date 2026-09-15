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
- **专注 AdGuard 生态** — 经官方 `hostlist-compiler` 编译，输出标准 AdGuard 语法，完全兼容 AdGuard Home / AdGuard 客户端。
- **自动更新** — 每 6 小时同步上游最新规则，永不过时。
- **多平台可用** — 虽然只提供 AdGuard 格式，但可通过路由器、AdGuard Home、AdGuard 客户端覆盖您的所有设备。

<hr>

## 📦 规则构成

| 数据源 | 定位 | 说明 |
|--------|------|------|
| [HaGeZi Normal](https://github.com/hagezi/dns-blocklists) | 全球广告/追踪 | 社区顶级平衡列表，家庭首选 |
| [OISD Blocklist Big](https://oisd.nl/) | 全球广告/追踪 | 极低误杀的经典大列表，与 HaGeZi 互补 |

> 合并去重压缩后，实际总规则量稳定在 **35 万条左右**，文件大小约 **8–10 MB**。足以满足绝大多数家庭与个人的日常防护需求。

<hr>

## 🚀 快速开始

### 订阅地址

在 AdGuard Home、AdGuard 客户端或其他支持 AdGuard 语法的软件中，添加以下 URL：

`https://github.com/LucentDNS/lucent-dns/releases/latest/download/dns-filter.txt`

### 手动编译

如果您需要在本地自行编译：

```bash
# 安装官方编译器
npm install -g @adguard/hostlist-compiler

# 创建输出目录并执行编译
mkdir -p dist
hostlist-compiler -c configuration.json -o dist/dns-filter.txt

<hr>
⏰ 自动更新

GitHub Actions 每 6 小时自动拉取上游最新规则并重新编译发布。
<hr>
🙏 致谢

    HaGeZi DNS Blocklists — 广告、追踪、威胁情报

    OISD — 经典广告拦截列表

    AdGuard Hostlist Compiler — 编译工具

<hr>
📄 许可证

MIT License © 2026 LucentDNS
