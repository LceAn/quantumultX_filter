# Proxy Filter Rules

[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)
[![Quantumult X](https://img.shields.io/badge/Quantumult%20X-Supported-007AFF?style=flat-square&logo=apple)](https://apps.apple.com/app/id1443988620)
[![Surge](https://img.shields.io/badge/Surge-Supported-FF6900?style=flat-square&logo=surge)](https://nssurge.com/)
[![Updates](https://img.shields.io/badge/Updates-Daily-green?style=flat-square)](https://github.com/LceAn/proxy-filter-rules/commits/main)
[![Stars](https://img.shields.io/github/stars/LceAn/proxy-filter-rules?style=flat-square)](https://github.com/LceAn/proxy-filter-rules/stargazers)
[![Issues](https://img.shields.io/github/issues/LceAn/proxy-filter-rules?style=flat-square)](https://github.com/LceAn/proxy-filter-rules/issues)

> 📦 适用于 Quantumult X / Surge 的分流规则集合 | Proxy Filter Rules for Quantumult X & Surge

---

## 📖 简介 | Introduction

本仓库收集了适用于 **Quantumult X** 和 **Surge** 的分流规则，帮助精准控制网络流量，提升上网体验。

This repository collects proxy filter rules for **Quantumult X** and **Surge**, helping to control network traffic precisely and improve browsing experience.

**特点 | Features:**
- ✅ **双平台支持** - Quantumult X & Surge
- ✅ **精准分流** - 针对特定网站和服务的精细规则
- ✅ **持续更新** - 每日更新，保持规则最新
- ✅ **易于使用** - 一键订阅，自动更新
- ✅ **开源免费** - MIT 许可，完全免费使用

---

## 🚀 快速开始 | Quick Start

### Quantumult X

#### 方法一：远程订阅

在配置文件的 `[filter_remote]` 部分添加：

```ini
[filter_remote]
https://raw.githubusercontent.com/LceAn/proxy-filter-rules/main/AI.list, tag=AI 服务，enabled=true
https://raw.githubusercontent.com/LceAn/proxy-filter-rules/main/WeChat.list, tag=微信国际版，enabled=true
```

#### 方法二：本地引用

```ini
[filter_local]
include-filter=AI.list
include-filter=WeChat.list
```

---

### Surge

#### 方法一：远程规则

在配置文件的 `[Rule]` 部分添加：

```ini
[Rule]
RULE-SET,https://raw.githubusercontent.com/LceAn/proxy-filter-rules/main/Surge_AI.list,AI 服务
RULE-SET,https://raw.githubusercontent.com/LceAn/proxy-filter-rules/main/Surge_WeChat.list,微信国际版
```

#### 方法二：本地引用

```ini
[Rule]
RULE-SET,Surge_AI.list,AI 服务
RULE-SET,Surge_WeChat.list,微信国际版
```

---

## 📁 规则文件 | Rule Files

### 原创规则 | Original Rules

| 文件 | 说明 | 规则数 | 平台 |
|------|------|--------|------|
| **AI.list** | AI 服务分流规则 | 50+ | QX |
| **WeChat.list** | 微信国际版规则 | 60+ | QX |
| **Work_local_filter.list** | 工作本地分流 | 3+ | QX |
| **Surge_ZD2025.list** | ZD2025 完整配置规则 | 200+ | Surge |

### 外部规则 | External Rules

收集自其他开源项目的规则文件，已标注来源。

| 分类 | 文件数 | 来源 |
|------|--------|------|
| 🤖 AI 服务 | 3 | blackmatrix7 |
| 💬 社交媒体 | 6 | blackmatrix7 |
| 🎬 流媒体 | 10 | blackmatrix7 |
| 🛒 购物支付 | 5 | blackmatrix7 |
| 💼 办公生产力 | 11 | blackmatrix7 |
| 🐱 开发技术 | 4 | blackmatrix7 |
| 🎮 游戏平台 | 5 | blackmatrix7 |
| 🌍 地区规则 | 3 | blackmatrix7 |
| 📥 下载测速 | 3 | skk.moe |
| 🌐 全局规则 | 3 | skk.moe |

**总计：** 52 个外部规则文件  
**来源：** [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script), [skk.moe/ruleset](https://github.com/Loyalsoldier/clash-rules)  
**详情：** 查看 [external-rules/README.md](external-rules/README.md)

---

## 📊 规则统计 | Statistics

### 总体统计

| 指标 | 数值 |
|------|------|
| **原创规则文件** | 4 个 |
| **外部规则文件** | 52 个 |
| **总规则文件** | 56 个 |
| **总规则数** | 2000+ 条 |
| **支持平台** | Quantumult X, Surge |
| **更新频率** | 每日更新 |

### 分类统计

| 分类 | 规则数 | 类型 |
|------|--------|------|
| 🤖 AI 服务 | 100+ | HOST/HOST-SUFFIX/RULE-SET |
| 💼 微信国际版 | 120+ | HOST/HOST-SUFFIX/USER-AGENT |
| 🏢 工作本地 | 3+ | HOST/IP-CIDR |
| 📦 ZD2025 配置 | 200+ | RULE-SET/DOMAIN-SUFFIX |

---

## ⚙️ 配置指南 | Configuration Guide

### Quantumult X 配置示例

```ini
[filter_remote]
https://raw.githubusercontent.com/LceAn/proxy-filter-rules/main/AI.list, tag=🤖 AI 服务，enabled=true
https://raw.githubusercontent.com/LceAn/proxy-filter-rules/main/WeChat.list, tag=💼 微信国际版，enabled=true

[filter_local]
HOST-SUFFIX,openai.com,🤖 AI 服务
HOST-SUFFIX,chatgpt.com,🤖 AI 服务
```

### Surge 配置示例

```ini
[Proxy Group]
🤖 AI 服务 = select, 美国节点，主力高速，节点选择

[Rule]
RULE-SET,https://raw.githubusercontent.com/LceAn/proxy-filter-rules/main/Surge_AI.list,🤖 AI 服务
DOMAIN-SUFFIX,openai.com,🤖 AI 服务
DOMAIN-SUFFIX,chatgpt.com,🤖 AI 服务
```

---

## 🔧 常见问题 | FAQ

### Q1: 规则不生效怎么办？

**A:** 请检查以下步骤：
1. ✅ 确认规则 URL 正确
2. ✅ 执行"刷新所有资源"
3. ✅ 重启代理工具
4. ✅ 检查策略组名称是否匹配
5. ✅ 查看日志

### Q2: 如何更新规则？

**A:** 
- **自动更新**：代理工具会自动更新远程规则
- **手动更新**：点击"刷新所有资源"

### Q3: 支持其他代理工具吗？

**A:** 
- ✅ **Clash** - 规则格式通用，可用于 Clash
- ✅ **Shadowrocket** - 部分规则兼容
- ✅ **Loon** - 部分规则兼容
- ⚠️ 部分工具可能需要调整格式

### Q4: Quantumult X 和 Surge 规则有什么区别？

**A:** 
- **Quantumult X** - 使用 `HOST-SUFFIX`, `HOST-KEYWORD` 等
- **Surge** - 使用 `RULE-SET`, `DOMAIN-SUFFIX` 等
- 本仓库提供两种格式，按需选择

### Q5: 可以自定义规则吗？

**A:** 
- ✅ 欢迎提交 Issue 或 Pull Request
- ✅ 可以 Fork 后自定义修改
- ⚠️ 修改后请测试验证

---

## 🤝 贡献 | Contributing

欢迎提交新的分流规则或改进建议！

### 提交方式

1. **Issue** - 提交网站域名或问题反馈
   - Visit: https://github.com/LceAn/proxy-filter-rules/issues

2. **Pull Request** - 直接修改规则文件
   - Fork repo → Modify → Submit PR

3. **邮件** - rule@lcean.com

### 规则格式要求

#### Quantumult X
```ini
HOST-SUFFIX,domain.com,策略组名称
HOST-KEYWORD,keyword,策略组名称
IP-CIDR,192.168.1.0/24,策略组名称
USER-AGENT,AppName*,策略组名称
```

#### Surge
```ini
RULE-SET,ruleset.list,策略组名称
DOMAIN-SUFFIX,domain.com,策略组名称
DOMAIN-KEYWORD,keyword,策略组名称
IP-CIDR,192.168.1.0/24,策略组名称
USER-AGENT,AppName*,策略组名称
```

### 提交前检查

- ✅ 测试规则是否生效
- ✅ 确认域名拼写正确
- ✅ 选择合适的策略组
- ✅ 避免重复规则
- ✅ 注明适用平台（QX/Surge/Both）

---

## 📄 许可证 | License

本项目采用 [MIT License](LICENSE)

**权限 | Permissions:**
- ✅ 商业使用 | Commercial use
- ✅ 修改 | Modification
- ✅ 分发 | Distribution
- ✅ 私有使用 | Private use

**限制 | Conditions:**
- ⚠️ 需保留许可证和版权声明
- ⚠️ 不提供任何担保

---

## 🔗 相关链接 | Links

- **Quantumult X** - [App Store](https://apps.apple.com/app/id1443988620)
- **Surge** - [Official Website](https://nssurge.com/)
- **Issues** - [问题反馈](https://github.com/LceAn/proxy-filter-rules/issues)
- **Commits** - [更新日志](https://github.com/LceAn/proxy-filter-rules/commits/main)
- **Stars** - [GitHub Stars](https://github.com/LceAn/proxy-filter-rules/stargazers)

---

## 📮 联系方式 | Contact

- **GitHub**: [@LceAn](https://github.com/LceAn)
- **Email**: rule@lcean.com
- **Issues**: [提交问题](https://github.com/LceAn/proxy-filter-rules/issues)

---

<div align="center">

**🛡️ 持续更新中 · 欢迎 Star 支持**

Made with ❤️ by LceAn

[返回顶部](#proxy-filter-rules)

</div>
