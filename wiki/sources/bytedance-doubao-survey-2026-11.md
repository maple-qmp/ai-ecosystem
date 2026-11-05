---
title: 字节跳动与豆包时间线调研（2026-11）
type: source
tags: [notes]
source_note: "[[字节-豆包调研-2026-11]]"
url: https://seed.bytedance.com/en/blog/seed-2-0-official-launch
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[entities/bytedance]]"
  - "[[entities/doubao]]"
  - "[[entities/agentscope]]"
---

# 字节跳动与豆包时间线调研（2026-11）

## Summary

整理 [[entities/bytedance|字节跳动]]大模型业务从 2023 年到 2026-11 的时间线，内容包括豆包 App、Seed 团队的 [[entities/doubao|豆包大模型（Doubao-Seed）]]、火山引擎的模型服务与定价、Seed 的开放权重项目，以及 Coze、TRAE 等开发者产品。另外三家的旗舰模型都开放权重，字节没有：豆包主力模型只通过火山引擎 API 和自有产品提供，开放的是 Seed-OSS-36B、UI-TARS 等中小模型。字节和阿里之间没有股权往来，是正面竞争：火山引擎对阿里云百炼，豆包对千问。

## Key Points

- **豆包 App**：2023-08 上线；2024-11 月活约 6000 万，国内第一；2026-05 用户约 3.3 亿，推出付费订阅
- **价格战起点**：2024-05-15 豆包大模型商用，Pro 32K 输入 0.0008 元 / 千 token
- **版本节奏**：1.5 Pro（2025-01）→ 1.6（2025-06）→ 1.8（2025-12）→ Seed 2.0（2026-02-14，Pro / Lite / Mini + Code）→ Seed 2.1（2026-06-23，Pro / Turbo）
- **价格回调**：Seed 2.1 Pro 输入 6 元、输出 30 元 / 百万 token，被报道为“告别价格战”
- **规模**：日均 token 2026-04 约 120 万亿、2026-06 超 180 万亿；IDC 称火山引擎在中国公有云 MaaS 市场份额 49.5%，排名第一
- **开放权重（中小模型）**：UI-TARS（2025-01）、Seed-Coder-8B（2025-04）、Seed-OSS-36B（2025-08，Apache-2.0）
- **开发者产品**：Coze Studio / Coze Loop 2025-07 开源（Apache-2.0）；TRAE IDE 是 Seed 2.0 Pro 与 Code 模型的首发入口之一
- **监管**：2026-07-15 为符合新的 AI Agent 规定，豆包 App 下线 Agent 功能
- **与阿里生态**：直接竞争；[[entities/agentscope|AgentScope]]（Python）把 Volcengine 列为内置模型提供方

## Mentioned Pages

- [[entities/bytedance|字节跳动]]
- [[entities/doubao|豆包]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/agentscope|AgentScope]]
- [[entities/qwen|Qwen]]
- [[entities/gpt|GPT]]
- [[entities/gemini|Gemini]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/reasoning-model|推理模型]]
