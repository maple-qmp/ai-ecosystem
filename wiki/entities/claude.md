---
title: Claude
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Claude", "Claude 模型", "Claude Opus", "Claude Sonnet", "Claude Haiku", "Claude Mythos", "Claude Fable"]
org: "[[entities/anthropic|Anthropic]]"
released: "2023-03"
open_weights: false
competitors: ["[[entities/gpt]]", "[[entities/gemini]]", "[[entities/grok]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-07
sources: ["[[sources/claude-independent-modules-survey-2026-11]]", "[[sources/frontier-closed-models-survey-2026-11]]"]
---

# Claude

## 描述

[[entities/anthropic|Anthropic]] 的闭源模型家族，2023-03 首发。Claude 3（2024-03）起每代分 Haiku / Sonnet / Opus 三档；2026 年在其上加了 Mythos 档，只开放给经过验证的组织（Project Glasswing、Cyber Verification Program），面向公众的同级版本叫 Fable，对网络安全、生物等高风险请求加了额外限制。当前阵容是 Fable 5.1、Opus 5.5（官方推荐的默认起点）、Sonnet 5.5 和 Haiku 5.5，全部 1M 上下文、128K 输出、自适应思考。除 Anthropic 自家 API 外，也通过 Amazon Bedrock、Google Cloud、Microsoft Foundry、Claude Platform on AWS 提供；接口格式 [[concepts/anthropic-messages-api|Anthropic Messages API]] 已被许多其他模型服务兼容。行为规范以 [[concepts/claude-constitution|Claude 宪法]] 公开（CC0）。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/gpt|GPT]]、[[entities/gemini|Gemini]]、[[entities/grok|Grok]]

## 当前阵容（2026-11，官方模型总览）

- **Fable 5.1**（`claude-fable-5-1`）：$10 / $50 每百万 token，用于高难度推理和长程 Agent 任务；Mythos 5.1 能力相同，只给经验证的组织
- **Opus 5.5**：$4 / $20，长时间运行的 Agent 编码与知识工作
- **Sonnet 5.5**：$2 / $10，速度与能力的平衡
- **Haiku 5.5**：从 $0.10 / $0.50 起，分类、抽取、路由等大批量任务
- 共同点：可靠知识截止 2026-06；4.6 代起模型 ID 不带日期、每个 ID 都是固定快照；API 版本 `2026-10-21` 删除了 `temperature` / `top_p` / `top_k`

## 生命周期

- 每个模型标注“最早不早于”某日退役，约为发布后一年；退役前至少提前 60 天通知
- 官方承诺长期保存已退役模型的权重
- 已退役：Claude 1 / Instant（2024-11）、Claude 2 系列（2025-07）、Sonnet 3.5（2025-10）、Opus 3（2026-01）、Sonnet 3.7 与 Haiku 3.5（2026-02）、Sonnet 4 / Opus 4（2026-06）、Opus 4.1（2026-08）；Sonnet 4.5 计划 2026-11-30

## 时间线

- 2023-03 Claude 1（仅限审批用户）
- 2023-07 Claude 2，第一个公开可用版本；2.1 上下文 200K
- 2024-03-04 Claude 3 家族
- 2024-06-20 Claude 3.5 Sonnet 与 Artifacts
- 2024-10-22 升级版 3.5 Sonnet、3.5 Haiku，computer use 公测
- 2025-02 Claude 3.7 Sonnet
- 2025-05-22 Claude Sonnet 4 / Opus 4，Opus 4 按 ASL-3 部署
- 2025-08 Opus 4.1
- 2025-09-29 Sonnet 4.5；10-15 Haiku 4.5；11-24 Opus 4.5
- 2026-02-05 Opus 4.6；02-17 Sonnet 4.6
- 2026-04-07 Project Glasswing：Mythos Preview 只给 11 家机构做漏洞挖掘
- 2026-04-16 Opus 4.7，换新分词器
- 2026-05-28 Opus 4.8
- 2026-06-09 Fable 5 公开发布，Mythos 5 走受信准入
- 2026-06-12 遵照美国商务部指令暂停 Mythos 级模型对外国人的访问；07-01 Fable 重新上线
- 2026-06-30 Sonnet 5；07-24 Opus 5
- 2026-09-01 Fable 5.1 与 Mythos 5.1
- 2026-09-22 Opus 5.5；09-28 Sonnet 5.5；10-07 Haiku 5.5

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/claude-code|Claude Code]]
- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[entities/gpt|GPT]]
- [[entities/gemini|Gemini]]
- [[entities/grok|Grok]]

## 相关概念

- [[concepts/reasoning-model|推理模型]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]
- [[concepts/claude-constitution|Claude 宪法]]
- [[concepts/computer-use|Computer Use]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "If you’re unsure which model to use, start with Claude Opus 5.5 for most workloads." — [[sources/frontier-closed-models-survey-2026-11|前沿闭源模型调研]]（Anthropic 模型总览）
- "Claude Mythos 5.1 offers the same capabilities only to organizations verified through Anthropic’s verification programs, such as the Cyber Verification Program." — [[sources/frontier-closed-models-survey-2026-11|前沿闭源模型调研]]（Claude Fable 5.1 模型页）
- "Anthropic has committed to long-term preservation of model weights and other measures to help mitigate these impacts." — [[sources/frontier-closed-models-survey-2026-11|前沿闭源模型调研]]（Anthropic 弃用页）
