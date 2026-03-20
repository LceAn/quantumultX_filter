# 规则文件索引 | Rules Index

> 本仓库所有规则文件的完整索引，包含原创规则和外部收集规则。  
> Complete index of all rule files in this repository, including original and external rules.

**最后更新：** 2026-03-20  
**规则文件总数：** 58 个  
**总规则数：** 2000+ 条

---

## 📁 目录结构 | Directory Structure

```
proxy-filter-rules/
├── original-rules/          # 原创规则
│   ├── AI.list             # AI 服务规则 (50+)
│   ├── WeChat.list         # 微信国际版规则 (60+)
│   ├── Work_local_filter.list  # 工作本地分流 (3+)
│   └── Surge_ZD2025.list   # Surge ZD2025 配置 (200+)
├── external-rules/          # 外部规则
│   ├── blackmatrix7/       # blackmatrix7 规则 (46 个)
│   └── skk.moe/            # skk.moe 规则 (6 个)
└── README.md               # 本索引文件
```

---

## 🎨 原创规则 | Original Rules

由本仓库作者原创整理的规则文件。

| 文件 | 说明 | 规则数 | 平台 | 状态 |
|------|------|--------|------|------|
| **AI.list** | AI 服务分流规则 | 50+ | Quantumult X | ✅ |
| **WeChat.list** | 微信国际版规则 | 60+ | Quantumult X | ✅ |
| **Work_local_filter.list** | 工作本地分流 | 3+ | Quantumult X | ✅ |
| **Surge_ZD2025.list** | ZD2025 完整配置规则 | 200+ | Surge | ✅ |

**总计：** 4 个原创规则文件  
**总规则数：** 310+ 条

### 规则详情

#### 🤖 AI.list

**平台：** Quantumult X  
**规则数：** 50+  
**包含服务：**
- ChatGPT (chat.openai.com, chatgpt.com)
- Google Gemini (gemini.google.com)
- Claude (claude.ai)
- OpenAI API (api.openai.com)
- 相关服务 (statsig, launchdarkly, intercom 等)

**使用示例：**
```ini
[filter_remote]
https://raw.githubusercontent.com/LceAn/proxy-filter-rules/main/original-rules/AI.list, tag=🤖 AI 服务，enabled=true
```

#### 💼 WeChat.list

**平台：** Quantumult X  
**规则数：** 60+  
**包含服务：**
- 微信国际版 (wechat.com)
- 企业微信
- 微信支付 (tenpay.com)
- 腾讯地图 (map.qq.com)
- 相关 CDN 和 API 服务

**使用示例：**
```ini
[filter_remote]
https://raw.githubusercontent.com/LceAn/proxy-filter-rules/main/original-rules/WeChat.list, tag=💼 微信国际版，enabled=true
```

#### 🏢 Work_local_filter.list

**平台：** Quantumult X  
**规则数：** 3+  
**用途：** 本地工作网络专用分流规则

**使用示例：**
```ini
[filter_local]
include-filter=Work_local_filter.list
```

#### 📦 Surge_ZD2025.list

**平台：** Surge  
**规则数：** 200+  
**说明：** 完整的 Surge 配置文件规则，包含 AI/微信/开发/流媒体等分流

**使用示例：**
```ini
[Rule]
RULE-SET,https://raw.githubusercontent.com/LceAn/proxy-filter-rules/main/original-rules/Surge_ZD2025.list,🚀 节点选择
```

---

## 🌐 外部规则 | External Rules

收集自其他开源项目的规则文件，已标注来源。

### 来源统计

| 来源 | 文件数 | 规则数 | 许可证 |
|------|--------|--------|--------|
| **blackmatrix7/ios_rule_script** | 46 | 1500+ | MIT |
| **skk.moe/ruleset** | 6 | 200+ | MIT |

### 分类统计

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

**外部规则总计：** 52 个文件  
**外部规则总数：** 1700+ 条

### 详细列表

查看 [external-rules/README.md](external-rules/README.md) 获取完整列表。

---

## 📊 总体统计 | Overall Statistics

### 文件统计

| 类型 | 文件数 | 占比 |
|------|--------|------|
| 原创规则 | 4 | 6.9% |
| 外部规则 | 52 | 89.7% |
| **总计** | **56** | **100%** |

### 规则数统计

| 类型 | 规则数 | 占比 |
|------|--------|------|
| 原创规则 | 310+ | 15.5% |
| 外部规则 | 1700+ | 84.5% |
| **总计** | **2000+** | **100%** |

### 平台支持

| 平台 | 文件数 | 说明 |
|------|--------|------|
| Quantumult X | 53 | 3 原创 + 50 外部 |
| Surge | 55 | 1 原创 + 54 外部 |

---

## 🔗 来源标注 | Sources

### 原创规则
- **作者：** LceAn
- **许可证：** MIT License

### 外部规则

#### blackmatrix7/ios_rule_script
- **仓库：** https://github.com/blackmatrix7/ios_rule_script
- **作者：** blackmatrix7
- **许可证：** MIT License
- **文件数：** 46 个

#### skk.moe/ruleset
- **仓库：** https://github.com/Loyalsoldier/clash-rules
- **作者：** Loyalsoldier
- **许可证：** MIT License
- **文件数：** 6 个

---

## 📄 许可证 | License

### 原创规则
采用 [MIT License](../LICENSE)

### 外部规则
遵循各自原作者的许可证：
- blackmatrix7 规则 - MIT License
- skk.moe 规则 - MIT License

---

## 🔗 相关链接 | Links

- **主 README** - [../README.md](../README.md)
- **外部规则详情** - [external-rules/README.md](external-rules/README.md)
- **失败文件列表** - [external-rules/FAILED_RULES.md](external-rules/FAILED_RULES.md)
- **GitHub 仓库** - https://github.com/LceAn/proxy-filter-rules

---

**最后更新：** 2026-03-20  
**维护者：** LceAn  
**联系方式：** rule@lcean.com
