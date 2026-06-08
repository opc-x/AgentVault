---
title: "东南亚电子钱包格局（示例）"
date: 2026-06-08
category: payments
tags: [SEA, wallet, e-wallet, PSP]
status: draft
agent: cursor
confidence: medium
related: [https://github.com/opc-x/PayAtlas]
summary: "示例报告：SEA 需全球 PSP + 本地 PSP 组合，钱包/VA 不可只用卡通道覆盖。"
---

# 东南亚电子钱包格局（示例）

> 这是一份**格式示例**，展示 AgentVault 里调研报告长什么样。内容仅供结构参考，数据请自行复核后替换。

## 调研背景

- **为什么要调研**：跨境电商进入东南亚，需确认本地支付方式覆盖
- **决策要回答的问题**：只用 Stripe 够不够？要不要上 Xendit？
- **调研范围**：印尼、菲律宾、新加坡、泰国主流电子钱包

## 方法与来源

- Agent / 模型：Cursor Agent
- 主要信息源：PSP 官网、行业公开资料
- 调研时间：2026-06-08

## 核心结论

1. 东南亚 **卡渗透率低于欧美**，钱包 + 银行转账是主流
2. 全球 PSP（Stripe/Adyen）可覆盖部分场景，但 **本地方式深度不足时需区域 PSP**
3. 推荐路径：**全球卡通道 + 本地 PSP（如 Xendit）** 双通道，按国家逐步开通

## 详细发现

### 各国主流钱包

| 国家 | 主流方式 |
|------|----------|
| 印尼 | GoPay、OVO、DANA、VA |
| 菲律宾 | GCash、Maya |
| 泰国 | PromptPay、TrueMoney |
| 新加坡 | PayNow、GrabPay |

### 接入建议

- 第一阶段：卡 + PayPal/Stripe 覆盖跨境买家
- 第二阶段：接 Xendit / 2C2P 补本地钱包与 VA
- 尽调清单见 [PayAtlas 尽调模板](https://github.com/opc-x/PayAtlas/blob/main/channels/surveys/due-diligence-checklist.md)

## 风险 & 未决问题

- 各国监管与 KYB 要求需逐国确认
- 费率与结算周期以商务谈判为准

## 建议下一步

- [ ] 按 PayAtlas 跑一遍 SEA 渠道匹配
- [ ] 针对主力市场（如印尼）做 PSP 尽调表
- [ ] 确认是否需要本地实体
