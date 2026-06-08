# AgentVault 智研仓

> 用 Agent 搞出来的一切调研成果，统一归档在这里。

这是个人/团队的 **Agent 调研知识库**——市场、支付、竞品、技术选型、合规……凡是 Agent 帮你摸清楚、写下来的东西，都往这儿扔。不追求代码，追求 **可检索、可沉淀、可复用**。

## 和别的仓库怎么分工

| 仓库 | 角色 |
|------|------|
| **AgentVault**（本仓） | 调研**成果**归档：报告、结论、对比表、决策记录 |
| [PayAtlas](https://github.com/opc-x/PayAtlas) | 支付渠道**框架**：匹配引擎、接入蓝图、渠道数据 |
| [ZuiTi](https://github.com/opc-x/ZuiTi) | 嘴替 **Prompt** 与回复管线 |

流程一般是：**Agent 调研 → 结论写入 AgentVault → 需要落地的再反哺到 PayAtlas / ZuiTi 等工程仓**。

## 目录结构

```
AgentVault/
├── INDEX.md              # 总索引（新报告记得登记）
├── templates/            # 报告模板
├── market/               # 市场 & 行业
├── payments/             # 支付 & 金融科技
├── competitor/           # 竞品分析
├── tech/                 # 技术选型 & 架构
├── product/              # 产品 & 用户研究
├── legal-compliance/     # 法务 & 合规
├── operations/           # 运营 & 增长
└── misc/                 # 其它
```

## 怎么新增一份调研

1. 从 [`templates/research-report.md`](./templates/research-report.md) 复制模板
2. 存到对应分类目录，文件名建议：`YYYY-MM-DD-主题-简述.md`
3. 在 [`INDEX.md`](./INDEX.md) 加一行索引
4. commit，写清楚「调研了什么、结论是什么」

## 命名规范

```
YYYY-MM-DD-<主题>-<简述>.md

示例：
2026-06-08-sea-wallet-landscape.md
2026-06-10-stripe-vs-adyen-fees.md
```

## 报告元数据（YAML Frontmatter）

每份报告头部带上这些字段，方便以后检索：

```yaml
---
title: "报告标题"
date: 2026-06-08
category: payments        # market | payments | competitor | tech | product | legal-compliance | operations | misc
tags: [SEA, wallet, PSP]
status: draft             # draft | reviewed | archived
agent: cursor             # 用的什么 Agent / 模型
confidence: medium        # low | medium | high
related: []               # 关联报告文件名或外部链接
summary: "一句话结论"
---
```

## License

调研内容默认私有知识资产；仓库 MIT，内容版权归作者所有。
