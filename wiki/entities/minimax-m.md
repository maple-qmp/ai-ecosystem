---
title: MiniMax-M
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["MiniMax-M", "MiniMax-M1", "MiniMax-M2", "MiniMax-M2.5", "MiniMax-M3", "MiniMax-01", "MiniMax Code"]
org: "[[entities/minimax]]"
released: "2025-01"
open_weights: true
competitors: ["[[entities/kimi]]", "[[entities/glm]]", "[[entities/qwen]]", "[[entities/deepseek-r1]]", "[[entities/doubao]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/minimax-survey-2026-11]]"]
---

# MiniMax-M

## 描述

[[entities/minimax|MiniMax]] 的开放权重语言模型系列，包括 2025-01 的 MiniMax-01 和之后的 M1、M2、M3。这条线经历了三次路线变化。MiniMax-01 和 M1 是 456B 总参数、45.9B 激活的 [[concepts/mixture-of-experts|MoE]]，把 Lightning Attention（线性注意力）和 Softmax 注意力混合，原生支持 1M 上下文。M2 系列改为 230B 总参数、10B 激活的小激活模型，主打编码与 Agent 的低延迟和低成本。M3 是约 428B / 23B 的原生多模态模型，用自研 MiniMax Sparse Attention（MSA）支撑 1M 上下文，许可证也从 Modified MIT 收紧为社区许可。系列之外，MiniMax 还有海螺视频、Speech、Music 和 H3 等生成模型。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/kimi|Kimi]]、[[entities/glm|GLM]]、[[entities/qwen|Qwen]]、[[entities/deepseek-r1|DeepSeek-R1]]、[[entities/doubao|豆包]]（闭源）

## 主要版本

- **MiniMax-01**（2025-01）：Text-01 与 VL-01，456B / 45.9B，Lightning Attention 混合架构
- **M1**（2025-06）：官方称是首个开放权重的大规模混合注意力[[concepts/reasoning-model|推理模型]]，40K / 80K 思考预算两个版本，Apache-2.0
- **M2**（2025-10）：230B / 10B，面向编码与 Agent 工具链
- **M2.1**（2025-12）：加强编码、工具调用、长程规划；同时推出基于它的 Agent 产品 MiniMax Code
- **M2.5**（2026-02）：SWE-Bench Verified 80.2%；官方称按每秒 100 token 连续跑一小时只要 1 美元；另有 Lightning 版本
- **M2.7**（2026-03 / 04）：官方称开启“模型自我进化”，内部版本自主迭代编程脚手架 100 多轮；SWE-Pro 56.22%
- **M3**（2026-06-01）：约 428B / 23B，文本、图像、视频输入，1M 上下文；在 1M 上下文下，预填充比 M2 快 9 倍、解码快 15 倍
- **M3.1-Flash**（2026-10）：同规模，全模型稀疏注意力、量化感知训练、DSpark [[concepts/speculative-decoding|推测解码]]，面向编码、计算机操作与网络安全

## 许可证

- M1：Apache-2.0
- M2 至 M2.7：Modified MIT
- M3 / M3.1-Flash：MiniMax 社区许可证。免费授权只限非商用；商用要先给 MiniMax 发一次性通知，产品年收入超 2000 万美元的须事先获得书面授权。这是 Kimi、GLM、MiniMax 三家里对商用限制最严的一份

## 开发者接入

- 开放平台 API（platform.minimax.io）；MiniMax Code（agent.minimax.io）
- 阿里云百炼（2026-05 起上架 M2.7）
- [[entities/agentscope|AgentScope]] 内置 `MiniMaxChatModel`
- 提供 [[concepts/anthropic-messages-api|Anthropic Messages API]] 兼容端点，可驱动 [[entities/claude-code|Claude Code]]

## 时间线

- 2025-01 MiniMax-01
- 2025-06 M1
- 2025-10 M2
- 2025-12 M2.1、MiniMax Code
- 2026-02 M2.5
- 2026-03 / 04 M2.7
- 2026-06-01 M3
- 2026-10 M3.1-Flash

## 相关实体

- [[entities/minimax|MiniMax]]
- [[entities/kimi|Kimi]]
- [[entities/glm|GLM]]
- [[entities/agentscope|AgentScope]]
- [[entities/claude-code|Claude Code]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "MiniMax-M3 is a native multimodal model with 1M context. It has ~428B parameters and ~23B activated parameters." — [[sources/minimax-survey-2026-11|MiniMax 调研]]（MiniMax-M3 模型卡）
- "We introduce MiniMax-M1, the world's first open-weight, large-scale hybrid-attention reasoning model." — [[sources/minimax-survey-2026-11|MiniMax 调研]]（MiniMax-M1 模型卡）
- "It costs just $1 to run the model continuously for an hour at a rate of 100 tokens per second." — [[sources/minimax-survey-2026-11|MiniMax 调研]]（MiniMax-M2.5 模型卡）
