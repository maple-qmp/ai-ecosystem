---
title: 豆包
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["豆包", "Doubao", "豆包大模型", "Doubao-Seed", "Seed 2.0", "Seed 2.1", "Seed-OSS"]
org: "[[entities/bytedance]]"
released: "2024-05"
open_weights: false
competitors: ["[[entities/qwen]]", "[[entities/kimi]]", "[[entities/glm]]", "[[entities/minimax-m]]", "[[entities/gpt]]", "[[entities/gemini]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/bytedance-doubao-survey-2026-11]]"]
---

# 豆包

## 描述

[[entities/bytedance|字节跳动]] Seed 团队的大模型家族，2024-05 起通过火山引擎商用，2026 年的 2.x 版本以 Doubao-Seed 命名。主力模型不开放权重，只通过火山引擎 API 和豆包 App、TRAE、Coze 等自有产品提供。“豆包”同时也是字节的 AI 助手 App 名称，它是国内用户最多的 AI 助手。版本节奏大约每半年一代，常在火山引擎 FORCE 大会上发布：1.5 Pro、1.6、1.8、Seed 2.0、Seed 2.1。定价先是 2024 年以极低价格引发国内价格战，到 2026 年 Seed 2.1 时明显上调。字节另外以 Apache-2.0 / MIT 开放了 Seed-OSS-36B、UI-TARS、Seed-Coder 等中小模型，本页一并记录。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源为主）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/qwen|Qwen]]（国内云与 C 端的主要对手）、[[entities/kimi|Kimi]]、[[entities/glm|GLM]]、[[entities/minimax-m|MiniMax-M]]、[[entities/gpt|GPT]]、[[entities/gemini|Gemini]]

## 主要版本

- **豆包大模型**（2024-05-15）：首批商用，Pro 32K 输入 0.0008 元 / 千 token
- **豆包 1.5 Pro**（2025-01）：输入 0.8 元 / 百万 token，命中缓存 0.16 元
- **豆包 1.6**（2025-06-11）：按输入长度分段统一定价，0–32K 区间输入 0.8 元、输出 8 元 / 百万 token
- **豆包 1.8**（2025-12-18）
- **Seed 2.0**（2026-02-14）：Pro、Lite、Mini 三个通用 Agent 模型加一个 Code 模型；官方称 Pro 在 SuperGPQA 上超过 GPT-5.2，在 ICPC、IMO、CMO 测试中达到金牌水平，价格约为同级模型的 1/10，但也承认部分高难基准仍落后于全球顶尖模型
- **Seed 2.1**（2026-06-23）：Pro 与 Turbo；Pro 输入 6 元、输出 30 元 / 百万 token，缓存命中输入 1.2 元
- **Doubao-Seed-Code**（2025-11）：编码模型，配合低价编码订阅

## 开放权重的 Seed 模型

- **UI-TARS**（2025-01，2B / 7B / 72B，Apache-2.0）：GUI Agent 模型；2025-04 出 1.5 版
- **Seed-Coder-8B**（2025-04，MIT）
- **Seed-OSS-36B**（2025-08-20，Apache-2.0）：Base 与 Instruct，12T token 训练，面向长上下文、推理和 Agent
- 另有 BAGEL-7B、SeedVR、Seed-X 翻译模型等研究模型

## 开发者接入

- 火山引擎 / 火山方舟 API
- [[entities/agentscope|AgentScope]]（Python）内置 Volcengine 提供方
- 自有产品：豆包 App、TRAE、Coze

## 时间线

- 2024-05-15 豆包大模型商用，引发价格战
- 2025-01 豆包 1.5 Pro；UI-TARS 开源
- 2025-06-11 豆包 1.6
- 2025-08-20 Seed-OSS-36B 开源
- 2025-11 Doubao-Seed-Code
- 2025-12-18 豆包 1.8
- 2026-02-14 Seed 2.0
- 2026-06-23 Seed 2.1（Pro、Turbo）

## 相关实体

- [[entities/bytedance|字节跳动]]
- [[entities/qwen|Qwen]]
- [[entities/kimi|Kimi]]
- [[entities/glm|GLM]]
- [[entities/agentscope|AgentScope]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/reasoning-model|推理模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Seed2.0 Pro has scored higher than GPT-5.2 on SuperGPQA." — [[sources/bytedance-doubao-survey-2026-11|字节跳动与豆包调研]]（Seed 2.0 官方博客）
- "there is still room for improvement in some challenging and difficult benchmarks compared to top global models." — [[sources/bytedance-doubao-survey-2026-11|字节跳动与豆包调研]]（Seed 2.0 官方博客）
