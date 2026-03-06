# Quantumult X 分流规则

> 📦 2024 年新收集的网站分流规则，适用于 Quantumult X 代理工具

[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)
[![Quantumult X](https://img.shields.io/badge/Quantumult%20X-Supported-007AFF?style=flat-square&logo=apple)](https://apps.apple.com/app/id1443988620)
[![Updates](https://img.shields.io/badge/Updates-Daily-green?style=flat-square)](https://github.com/LceAn/quantumultX_filter/commits/main)
[![Stars](https://img.shields.io/github/stars/LceAn/quantumultX_filter?style=flat-square)](https://github.com/LceAn/quantumultX_filter/stargazers)

---

## 📖 简介

本仓库收集了 **2024 年新出现或较少被收录的网站分流规则**，适用于 Quantumult X 代理工具。规则经过整理和分类，能够帮助你更精准地控制网络流量，提升上网体验。

**适用场景：**
- ✅ 国内视频网站（爱奇艺、腾讯、优酷等）
- ✅ 国外流媒体（Netflix、Disney+、HBO 等）
- ✅ 购物网站（Amazon、eBay 等）
- ✅ 社交媒体（Twitter、Facebook、Instagram 等）
- ✅ 云服务与开发资源

---

## 🚀 快速开始

### 1️⃣ 添加订阅

在 Quantumult X 中打开 **配置文件** → **分流** → **添加远程规则**：

```
https://raw.githubusercontent.com/LceAn/quantumultX_filter/main/rules/main.conf
```

### 2️⃣ 更新规则

定期执行以下操作以获取最新规则：
1. 打开 Quantumult X
2. 点击 **刷新所有资源**
3. 重启 Quantumult X

---

## 📁 规则分类

| 分类 | 文件 | 说明 |
|------|------|------|
| 🎬 视频流媒体 | `streaming.conf` | Netflix、Disney+、HBO 等 |
| 📺 国内视频 | `china-video.conf` | 爱奇艺、腾讯、优酷、B 站等 |
| 🛒 购物网站 | `shopping.conf` | Amazon、eBay、淘宝等 |
| 💬 社交媒体 | `social.conf` | Twitter、Facebook、Instagram 等 |
| 🎮 游戏平台 | `gaming.conf` | Steam、Epic、PSN 等 |
| ☁️ 云服务 | `cloud.conf` | AWS、Azure、Google Cloud 等 |
| 🌐 通用规则 | `main.conf` | 综合规则（推荐直接使用） |

---

## 📋 规则示例

```ini
# 流媒体分流示例
HOST-SUFFIX,netflix.com,🚀 节点选择
HOST-SUFFIX,disneyplus.com,🚀 节点选择
HOST-KEYWORD,hbogo,🚀 节点选择

# 国内视频分流示例
HOST-SUFFIX,iqiyi.com,DIRECT
HOST-SUFFIX,v.qq.com,DIRECT
HOST-SUFFIX,bilibili.com,DIRECT

# 购物网站分流示例
HOST-SUFFIX,amazon.com,🚀 节点选择
HOST-SUFFIX,ebay.com,🚀 节点选择
```

---

## ⚙️ 自定义配置

### 添加白名单

在配置文件中的 `[filter_local]` 部分添加：

```ini
HOST-SUFFIX,your-domain.com,DIRECT
```

### 修改策略组

编辑规则文件，将节点组名称修改为你配置中的策略组名称：
- `🚀 节点选择` → 你的节点组名称
- `DIRECT` → 直连
- `REJECT` → 广告拦截

---

## 🔧 常见问题

### Q1: 规则不生效怎么办？
**A:** 请检查以下步骤：
1. 确认规则 URL 正确
2. 执行"刷新所有资源"
3. 重启 Quantumult X
4. 检查策略组名称是否匹配

### Q2: 如何更新规则？
**A:** 在 Quantumult X 中点击"刷新所有资源"即可

### Q3: 可以修改规则吗？
**A:** 欢迎提交 Issue 或 Pull Request！

---

## 📊 规则统计

| 分类 | 规则数量 | 最后更新 |
|------|---------|---------|
| 流媒体 | 150+ | 每日更新 |
| 国内视频 | 80+ | 每日更新 |
| 购物网站 | 60+ | 每日更新 |
| 社交媒体 | 100+ | 每日更新 |
| 游戏平台 | 40+ | 每日更新 |
| 云服务 | 50+ | 每日更新 |

---

## 🤝 贡献

欢迎提交新的分流规则！

### 提交方式
1. **Issue**: 提交网站域名
2. **Pull Request**: 直接修改规则文件
3. **邮件**: rule@lcean.com

### 格式要求
```ini
HOST-SUFFIX,domain.com,策略组名称
```

---

## 📄 许可证

本项目采用 [MIT License](LICENSE)

---

## 🔗 相关链接

- [Quantumult X 官方文档](https://www.quantumultx.com/)
- [本项目 Issues](https://github.com/LceAn/quantumultX_filter/issues)
- [更新日志](https://github.com/LceAn/quantumultX_filter/commits/main)

---

<div align="center">

**🛡️ 持续更新中 · 欢迎 Star 支持**

Made with ❤️ by LceAn

</div>
