---
title: Kimi
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Kimi", "Kimi K2", "Kimi K2.5", "Kimi K2.6", "Kimi K3", "Kimi K3.1 Pro", "Kimi Code"]
org: "[[entities/moonshot-ai]]"
released: "2023-10"
open_weights: true
competitors: ["[[entities/glm]]", "[[entities/minimax-m]]", "[[entities/qwen]]", "[[entities/deepseek-r1]]", "[[entities/doubao]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/moonshot-ai-survey-2026-11]]"]
---

# Kimi

## 描述

[[entities/moonshot-ai|月之暗面]]的模型与产品品牌：既指 2023-10 上线的 Kimi 助手，也指 2025-07 起开放权重的 Kimi K 系列模型。K2 到 K2.7 Code 都是 1T 总参数、32B 激活的 [[concepts/mixture-of-experts|MoE]]（384 个专家，每 token 选 8 个），许可证是 Modified MIT。K2.5 起原生多模态，并引入 Agent Swarm：把任务拆给动态生成的多个子 Agent 并行执行。K3 换成 Kimi Delta Attention（KDA）加 Attention Residuals 的新架构，2.8T 总参数、104B 激活、1M 上下文，许可证改为自定义的 Kimi K3 License。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/glm|GLM]]、[[entities/minimax-m|MiniMax-M]]、[[entities/qwen|Qwen]]、[[entities/deepseek-r1|DeepSeek-R1]]、[[entities/doubao|豆包]]（闭源）

## 主要版本

- **K2 / K2-Instruct-0905**：1T / 32B，15.5T token 预训练；0905 版上下文 256K
- **K2 Thinking**：边推理边调用工具的[[concepts/reasoning-model|推理模型]]，可连续 200–300 次工具调用，原生 INT4 [[concepts/quantization|量化]]
- **K2.5**：在 K2-Base 上用约 15T 图文 token 继续预训练，MoonViT 视觉编码器，Agent Swarm
- **K2.6**：Agent Swarm 扩到 300 个子 Agent、4000 步协同；主打长程编码和 24/7 后台 Agent
- **K2.7 Code**：基于 K2.6 的编码专用版，减少思考 token
- **K3**：2.8T / 104B，Stable LatentMoE（896 个专家选 16 个），KDA + AttnRes，1M 上下文，原生视觉；官方称整体仍落后于最强闭源模型
- **K3.1 Pro**：K3 经数百个领域联合强化学习后训练
- **小模型（MIT）**：Moonlight-16B-A3B、Kimi-VL-A3B、Kimi-Audio-7B、Kimi-Dev-72B、Kimi Linear 48B-A3B

## 许可证

- **K2 至 K2.7 Code（Modified MIT）**：只加一条：月活超 1 亿或月收入超 2000 万美元的商业产品要在界面显著标注 “Kimi K2”
- **K3 / K3.1 Pro（Kimi K3 License）**：保留标注条款，并新增 MaaS 条款：12 个月收入超 2000 万美元的模型服务商，商用前要和月之暗面另签协议；内部使用、经官方产品或认证推理伙伴使用不受限

## 开发者接入

- 官方 API（platform.moonshot.ai）；Kimi Code 命令行编码 Agent
- 提供 [[concepts/anthropic-messages-api|Anthropic Messages API]] 兼容端点，可驱动 [[entities/claude-code|Claude Code]]
- 阿里云百炼（2026-05 起上架 K2.6）；[[entities/agentscope|AgentScope]] 内置 Moonshot 提供方
- 被第三方用作基座：[[entities/cursor|Cursor]] Composer 2（报道基于 K2.5），Fireworks、Cognition 等基于 K3 的后训练模型

## 时间线

- 2023-10 Kimi 助手上线
- 2025-01-20 k1.5（闭源推理模型）
- 2025-02 Moonlight（MIT）
- 2025-07-11 K2 开放权重
- 2025-09 K2-Instruct-0905（256K 上下文）
- 2025-10-30 Kimi Linear
- 2025-11-06 K2 Thinking
- 2026-01-27 K2.5、Kimi Code
- 2026-04-20 K2.6
- 2026-06-12 K2.7 Code
- 2026-07-16 K3；权重 07-27 前放出
- 2026-10-23 K3.1 Pro

## 相关实体

- [[entities/moonshot-ai|月之暗面（Moonshot AI）]]
- [[entities/glm|GLM]]
- [[entities/minimax-m|MiniMax-M]]
- [[entities/qwen|Qwen]]
- [[entities/claude-code|Claude Code]]
- [[entities/hugging-face|Hugging Face]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/quantization|量化]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "It is a 2.8T-parameter model built on Kimi Delta Attention (KDA) and Attention Residuals (AttnRes), with native vision capabilities and a 1-million-token context window." — [[sources/moonshot-ai-survey-2026-11|月之暗面与 Kimi 调研]]（Kimi K3 模型卡）
- "Scaling horizontally to 300 sub-agents executing 4,000 coordinated steps" — [[sources/moonshot-ai-survey-2026-11|月之暗面与 Kimi 调研]]（Kimi K2.6 模型卡）
- "While its overall performance still trails the most powerful proprietary models" — [[sources/moonshot-ai-survey-2026-11|月之暗面与 Kimi 调研]]（Kimi K3 博客）
