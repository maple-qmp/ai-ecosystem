---
title: OpenAI
type: entity
tags: [organization]
kind: lab
layer: X
aliases: ["OpenAI", "Open AI"]
released: "2015"
competitors: ["[[entities/anthropic]]", "[[entities/google-deepmind]]"]
depends_on: ["[[entities/microsoft]]", "[[entities/nvidia]]"]
status: active
as_of: 2026-06
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/openai-developers-survey-2026-11]]", "[[sources/frontier-closed-models-survey-2026-11]]"]
---

# OpenAI

## 描述

2015 年成立的 AI 研究与产品公司。推出 [[entities/gpt|GPT]] 系列模型和 ChatGPT（2022-11），后者引爆了生成式 AI 浪潮；2024 年起推出以 o1 为首的推理模型系列。与 [[entities/microsoft|Microsoft]] 有深度资本与云合作。

## 开发者平台模块的服务依赖

开发者门户 developers.openai.com 的大部分内容是 API 与 ChatGPT 平台接入文档，离不开 OpenAI。能脱离 OpenAI 服务使用的部分（详见 [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]）：

- **完全独立**：[[entities/gpt-oss|gpt-oss]] 与 gpt-oss-safeguard（开放权重）、[[concepts/harmony-response-format|harmony]]、[[entities/tiktoken|tiktoken]]、[[concepts/agents-md|AGENTS.md]]、[[concepts/agent-skills|Agent Skills]]、MCP Apps（见 [[concepts/mcp-extensions|MCP 扩展]]）、[[concepts/agentic-commerce-protocol|Agentic Commerce Protocol]]、[[entities/promptfoo|Promptfoo]]
- **默认连 OpenAI、可改配置**：[[entities/openai-agents-sdk|Agents SDK]]、[[entities/codex-cli|Codex CLI]]、[[entities/codex-app-server|Codex SDK / App Server]]、官方 SDK（改 `base_url`）
- **部分独立**：[[entities/chatkit|ChatKit]]（后端自建，前端脚本走 OpenAI CDN）
- **离不开 OpenAI**：Responses / Realtime / Agents API、托管工具、微调、Codex cloud、Codex Security、插件上架、Sign in with ChatGPT、Ads、Workspace Agents

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · AI 实验室
- **上游依赖**：[[entities/microsoft|Microsoft]]、[[entities/nvidia|NVIDIA]]
- **竞争 / 替代**：[[entities/anthropic|Anthropic]]、[[entities/google-deepmind|Google DeepMind]]

## 时间线

- 2015 成立
- 2020 GPT-3
- 2022-11 ChatGPT
- 2024-09 o1 推理模型
- 2025-03 开源 [[entities/openai-agents-sdk|Agents SDK]]
- 2025-04 开源 [[entities/codex-cli|Codex CLI]]
- 2025-08 发布开放权重模型 [[entities/gpt-oss|gpt-oss]]
- 2025-08-07 发布 [[entities/gpt|GPT-5]]，o 系列推理模型并入主线
- 2025-09 与 Stripe 发布 [[concepts/agentic-commerce-protocol|Agentic Commerce Protocol]]
- 2025-10 DevDay：Apps SDK、[[entities/chatkit|ChatKit]]、Agent Builder；同月发布 gpt-oss-safeguard
- 2025-12 与 Anthropic、Block 共同发起 Linux Foundation 下的 Agentic AI Foundation，捐出 [[concepts/agents-md|AGENTS.md]]
- 2026-02-13 ChatGPT 下线 GPT-4o
- 2026-03 收购 [[entities/promptfoo|Promptfoo]]
- 2026-03-24 宣布停止 Sora 应用与 API
- 2026-08 以蒸馏等违约行为为由停止向 [[entities/cursor|Cursor]] 提供模型
- 2026-09-03 发布 GPT-6 Astra
- 2026-11-30 Evals 平台与 Agent Builder 计划关闭

## 相关实体

- [[entities/gpt|GPT]]
- [[entities/microsoft|Microsoft]]
- [[entities/anthropic|Anthropic]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/gpt-oss|gpt-oss]]
- [[entities/openai-agents-sdk|OpenAI Agents SDK]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/chatkit|ChatKit]]
- [[entities/promptfoo|Promptfoo]]

## 相关概念

- [[concepts/reasoning-model|推理模型]]
- [[concepts/scaling-laws|规模定律]]
- [[concepts/agents-md|AGENTS.md]]
- [[concepts/agentic-commerce-protocol|Agentic Commerce Protocol]]
- [[concepts/frontier-safety-frameworks|前沿模型安全框架]]（Preparedness Framework）
- [[concepts/swe-bench|SWE-bench]]（Verified 由 Preparedness 团队合作推出）

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

