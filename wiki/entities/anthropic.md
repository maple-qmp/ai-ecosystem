---
title: Anthropic
type: entity
tags: [organization]
kind: lab
layer: X
aliases: ["Anthropic PBC"]
released: "2021"
competitors: ["[[entities/openai]]", "[[entities/google-deepmind]]"]
depends_on: []
status: active
as_of: 2026-11
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/bun-survey-2026-11]]", "[[sources/claude-independent-modules-survey-2026-11]]", "[[sources/frontier-closed-models-survey-2026-11]]"]
---

# Anthropic

## 描述

AI 安全与研究公司，2021 年由 Dario Amodei、Daniela Amodei 等前 OpenAI 成员创立，总部位于旧金山。主力产品是 [[entities/claude|Claude]] 模型家族与 [[entities/claude-code|Claude Code]]，并提出了开放协议 [[concepts/model-context-protocol|MCP]]。2025-12 收购 JavaScript 运行时 [[entities/bun|Bun]]（开发公司 [[entities/oven|Oven]]），作为 Claude Code 和 Claude Agent SDK 的基础设施。以安全研究（如 Constitutional AI、可解释性）为核心定位。

## 开源与依赖分级

Anthropic 的核心产品是专有的，可独立使用的部分集中在标准、基础设施和研究工具（详见 [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]）：

- **完全独立**：[[concepts/model-context-protocol|MCP]]（已捐给 AAIF）、[[concepts/agent-skills|Agent Skills]] 格式、[[concepts/mcp-bundles|MCP Bundles]]、[[entities/sandbox-runtime|Sandbox Runtime]]、[[entities/bun|Bun]]、[[concepts/claude-constitution|Claude 宪法]]（CC0）、[[entities/circuit-tracer|circuit-tracer]] 与 jacobian-lens、[[entities/petri|Petri / Bloom]]（已交给 Meridian Labs）、hh-rlhf 等数据集
- **需要 Claude、可不经 Anthropic**：[[entities/claude-code|Claude Code]]、[[entities/claude-agent-sdk|Claude Agent SDK]]、claude-code-action 等，可走 Amazon Bedrock、Google Cloud、Microsoft Foundry、Claude Platform on AWS
- **可接非 Claude 模型但官方不支持**：通过 [[concepts/anthropic-messages-api|Anthropic Messages API]] 兼容端点（Ollama、DeepSeek、GLM 等）
- **离不开 Anthropic**：claude.ai 与桌面端、云端会话、Developer Platform 服务端功能、订阅登录、文档技能（docx / pdf / pptx / xlsx，source-available）

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · AI 实验室
- **上游依赖**：—
- **竞争 / 替代**：[[entities/openai|OpenAI]]、[[entities/google-deepmind|Google DeepMind]]

## 时间线

- 2021 成立
- 2023-03 发布 Claude
- 2024-11 发布 MCP
- 2025 推出 Claude Code
- 2025-05 开源 [[entities/circuit-tracer|circuit-tracer]]
- 2025-10 开源 [[entities/sandbox-runtime|Sandbox Runtime]] 与 [[entities/petri|Petri]]
- 2025-12 MCP 捐给 Linux Foundation 下新成立的 Agentic AI Foundation；[[concepts/agent-skills|Agent Skills]] 作为开放标准发布
- 2025-12-03 宣布收购 [[entities/bun|Bun]]（金额未披露），同时宣布 Claude Code 年化收入达 10 亿美元
- 2026-01 发布新版 [[concepts/claude-constitution|Claude 宪法]]，CC0 协议
- 2026-03-31 Claude Code npm 包误带 source map，源码外泄
- 2026-04-07 Project Glasswing：Mythos Preview 只给受信机构
- 2026-05-07 Petri 与 Bloom 交给非营利组织 Meridian Labs
- 2026-06-09 发布 Claude Fable 5 与 Mythos 5
- 2026-07-28 MCP 发布无状态版规范，见 [[concepts/mcp-request-flow|MCP 请求流程]]
- 2026-09-22 起发布 Claude 5.5 系列（Opus / Sonnet / Haiku），见 [[entities/claude|Claude]]

## 相关实体

- [[entities/claude|Claude]]
- [[entities/claude-code|Claude Code]]
- [[entities/bun|Bun]]
- [[entities/oven|Oven]]
- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[entities/sandbox-runtime|Sandbox Runtime（srt）]]
- [[entities/circuit-tracer|circuit-tracer]]
- [[entities/petri|Petri]]
- [[entities/openai|OpenAI]]
- [[entities/google-deepmind|Google DeepMind]]

## 相关概念

- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]
- [[concepts/claude-constitution|Claude 宪法]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Bun will remain open source and MIT-licensed, and we will continue to invest in making it the runtime" — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "Claude Code reached $1 billion in run-rate revenue in only 6 months" — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "Released under CC0 1.0." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]（Claude 宪法）
