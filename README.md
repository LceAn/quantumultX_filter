# Quantumult X 分流规则

[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)
[![Quantumult X](https://img.shields.io/badge/Quantumult%20X-Supported-007AFF?style=flat-square&logo=apple)](https://apps.apple.com/app/id1443988620)
[![Updates](https://img.shields.io/badge/Updates-Daily-green?style=flat-square)](https://github.com/LceAn/quantumultX_filter/commits/main)
[![Stars](https://img.shields.io/github/stars/LceAn/quantumultX_filter?style=flat-square)](https://github.com/LceAn/quantumultX_filter/stargazers)
[![Issues](https://img.shields.io/github/issues/LceAn/quantumultX_filter?style=flat-square)](https://github.com/LceAn/quantumultX_filter/issues)

> 📦 2024 年新收集的网站分流规则，适用于 Quantumult X 代理工具

---

## 📖 简介

本仓库收集了 **2024 年新出现或较少被收录的网站分流规则**，适用于 Quantumult X 代理工具。规则经过整理和分类，能够帮助你更精准地控制网络流量，提升上网体验。

**特点：**
- ✅ **精准分流** - 针对特定网站和服务的精细规则
- ✅ **持续更新** - 每日更新，保持规则最新
- ✅ **易于使用** - 一键订阅，自动更新
- ✅ **开源免费** - MIT 许可，完全免费使用

**适用场景：**
- 🤖 **AI 服务** - ChatGPT、Gemini、Claude 等 AI 工具
- 💼 **企业微信** - 微信国际版、企业微信专用规则
- 🏢 **工作本地** - 本地工作网络分流规则
- 🎬 **视频流媒体** - Netflix、Disney+、HBO 等
- 📺 **国内视频** - 爱奇艺、腾讯、优酷、B 站等
- 🛒 **购物网站** - Amazon、eBay、淘宝等
- 💬 **社交媒体** - Twitter、Facebook、Instagram 等
- 🎮 **游戏平台** - Steam、Epic、PSN 等
- ☁️ **云服务** - AWS、Azure、Google Cloud 等

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

### 3️⃣ 验证规则

添加后检查规则是否生效：
1. 打开 Quantumult X → **分流**
2. 查看规则列表是否包含本仓库的规则
3. 访问测试网站验证分流效果

---

## 📁 规则文件说明

### 核心规则文件

| 文件 | 说明 | 规则数 | 推荐使用 |
|------|------|--------|---------|
| **AI.list** | AI 服务分流规则 | 50+ | ✅ 推荐 |
| **WeChat.list** | 微信国际版规则 | 60+ | ✅ 推荐 |
| **Work_local_filter.list** | 工作本地分流 | 3+ | 按需使用 |

### 规则分类说明

#### 🤖 AI.list - AI 服务规则

**包含服务：**
- ChatGPT (chat.openai.com, chatgpt.com)
- Google Gemini (gemini.google.com)
- Claude (claude.ai)
- OpenAI API (api.openai.com)
- 相关服务 (statsig, launchdarkly, intercom 等)

**规则示例：**
```ini
HOST-SUFFIX,openai.com,AI
HOST-SUFFIX,chatgpt.com,AI
HOST-SUFFIX,ai.com,AI
HOST-KEYWORD,openai,AI
```

#### 💼 WeChat.list - 微信国际版规则

**包含服务：**
- 微信国际版 (wechat.com)
- 企业微信
- 微信支付 (tenpay.com)
- 腾讯地图 (map.qq.com)
- 相关 CDN 和 API 服务

**规则示例：**
```ini
HOST-SUFFIX,wechat.com,WeChat
HOST-SUFFIX,weixin.qq.com,WeChat
HOST-SUFFIX,tenpay.com,WeChat
USER-AGENT,MicroMessenger*,WeChat
```

#### 🏢 Work_local_filter.list - 工作本地分流

**用途：** 本地工作网络专用分流规则
**说明：** 根据实际工作网络环境自定义配置

---

## ⚙️ 配置指南

### 在 Quantumult X 中使用

#### 方法一：远程订阅（推荐）

1. 打开 Quantumult X 配置文件
2. 在 `[filter_remote]` 部分添加：
```ini
[filter_remote]
https://raw.githubusercontent.com/LceAn/quantumultX_filter/main/AI.list, tag=AI 服务，enabled=true
https://raw.githubusercontent.com/LceAn/quantumultX_filter/main/WeChat.list, tag=微信国际版，enabled=true
```

#### 方法二：本地引用

1. 下载规则文件到本地
2. 在配置文件中引用：
```ini
[filter_local]
include-filter=AI.list
include-filter=WeChat.list
```

### 自定义策略组

编辑规则文件，将策略组名称修改为你配置中的策略组：
- `AI` → 你的 AI 节点策略组名称
- `WeChat` → 你的微信策略组名称
- `Work` → 你的工作节点策略组名称
- `DIRECT` → 直连
- `REJECT` → 广告拦截

### 添加白名单

在配置文件的 `[filter_local]` 部分添加：
```ini
HOST-SUFFIX,your-domain.com,DIRECT
```

---

## 🔧 常见问题

### Q1: 规则不生效怎么办？

**A:** 请检查以下步骤：
1. ✅ 确认规则 URL 正确
2. ✅ 执行"刷新所有资源"
3. ✅ 重启 Quantumult X
4. ✅ 检查策略组名称是否匹配
5. ✅ 查看 Quantumult X 日志

### Q2: 如何更新规则？

**A:** 
- **自动更新**：Quantumult X 会自动更新远程规则
- **手动更新**：点击"刷新所有资源"

### Q3: 可以修改规则吗？

**A:** 
- ✅ 欢迎提交 Issue 或 Pull Request
- ✅ 可以 Fork 后自定义修改
- ⚠️ 修改后请测试验证

### Q4: 规则会影响网速吗？

**A:** 
- ❌ 不会，分流规则只是决定流量走向
- ✅ 正确的分流反而能提升访问速度
- ⚠️ 建议定期更新规则保持最优

### Q5: 支持其他代理工具吗？

**A:** 
- ✅ 规则格式通用，可用于 Surge、Shadowrocket 等
- ⚠️ 部分工具可能需要调整格式
- ✅ 欢迎提交其他工具的适配版本

---

## 📊 规则统计

### 总体统计

| 指标 | 数值 |
|------|------|
| **规则文件** | 3 个 |
| **总规则数** | 110+ 条 |
| **最后更新** | 2024 年 |
| **更新频率** | 每日更新 |

### 分类统计

| 分类 | 规则数 | 类型 |
|------|--------|------|
| 🤖 AI 服务 | 50+ | HOST/HOST-SUFFIX/IP-CIDR |
| 💼 微信国际版 | 60+ | HOST/HOST-SUFFIX/USER-AGENT |
| 🏢 工作本地 | 3+ | HOST/IP-CIDR |

### 更新历史

| 日期 | 更新内容 |
|------|---------|
| 2024-XX-XX | 初始版本发布 |
| 2024-XX-XX | 添加 AI.list |
| 2024-XX-XX | 更新 WeChat.list |
| 2024-XX-XX | 添加 Work_local_filter.list |

---

## 🤝 贡献指南

欢迎提交新的分流规则或改进建议！

### 提交方式

1. **Issue** - 提交网站域名或问题反馈
   - 访问：https://github.com/LceAn/quantumultX_filter/issues

2. **Pull Request** - 直接修改规则文件
   - Fork 仓库 → 修改 → 提交 PR

3. **邮件** - rule@lcean.com

### 规则格式要求

```ini
# 标准格式
HOST-SUFFIX,domain.com,策略组名称
HOST-KEYWORD,keyword,策略组名称
IP-CIDR,192.168.1.0/24,策略组名称
USER-AGENT,AppName*,策略组名称
```

### 提交前检查

- ✅ 测试规则是否生效
- ✅ 确认域名拼写正确
- ✅ 选择合适的策略组
- ✅ 避免重复规则

---

## 📄 许可证

本项目采用 [MIT License](LICENSE)

**权限：**
- ✅ 商业使用
- ✅ 修改
- ✅ 分发
- ✅ 私有使用

**限制：**
- ⚠️ 需保留许可证和版权声明
- ⚠️ 不提供任何担保

---

## 🔗 相关链接

- **Quantumult X 官方** - [App Store](https://apps.apple.com/app/id1443988620)
- **本项目 Issues** - [问题反馈](https://github.com/LceAn/quantumultX_filter/issues)
- **更新日志** - [Commits](https://github.com/LceAn/quantumultX_filter/commits/main)
- **Star 支持** - [GitHub Stars](https://github.com/LceAn/quantumultX_filter/stargazers)

---

## 📮 联系方式

- **GitHub**: [@LceAn](https://github.com/LceAn)
- **Email**: rule@lcean.com
- **Issues**: [提交问题](https://github.com/LceAn/quantumultX_filter/issues)

---

<div align="center">

**🛡️ 持续更新中 · 欢迎 Star 支持**

Made with ❤️ by LceAn

[返回顶部](#quantumult-x-分流规则)

</div>
