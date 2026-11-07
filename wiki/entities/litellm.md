---
title: LiteLLM
type: entity
tags: [project]
kind: infra
layer: L4
aliases: ["LiteLLM", "litellm", "LiteLLM Proxy", "LiteLLM AI Gateway", "BerriAI"]
org: "BerriAI"
released: "2023-07"
competitors: []
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/lowcode-agent-platforms-survey-2026-11]]"]
---

# LiteLLM

## 描述

BerriAI 开源的 LLM 网关（MIT，GitHub 约 6.29 万星），用 OpenAI 的请求格式统一调用 100 多家模型提供商。它有两种用法：Python SDK 直接嵌入应用；Proxy Server（LLM Gateway）由平台团队自托管，为整个组织提供虚拟密钥、按密钥 / 团队 / 用户的成本追踪与预算、限流、负载均衡和自动回退。很多 Agent 框架用它接入非 OpenAI 模型，如 [[entities/openai-agents-sdk|OpenAI Agents SDK]]（best-effort beta 支持）和 [[entities/dspy|DSPy]]（2026-04 起开始解耦）。2026-03-24 它遭遇供应链攻击：攻击者取得维护者的 PyPI 账号，发布了窃取凭据的恶意版本 1.82.7 和 1.82.8，[[entities/crewai|CrewAI]]、DSPy 等下游受波及，[[entities/mercor|Mercor]] 随后确认数据泄露源于此事件。2026 年下半年仓库简介改为“Rust core with Python SDK”，把性能敏感的路径迁到 Rust。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · LLM 网关
- **上游依赖**：—（各模型厂商 API）
- **下游**：[[entities/openai-agents-sdk|OpenAI Agents SDK]]、[[entities/dspy|DSPy]]、[[entities/crewai|CrewAI]] 等框架
- **竞争 / 替代**：各云厂商与框架自带的模型路由（如 [[entities/vercel-ai-sdk|AI SDK]] 的多提供商接口）

## 时间线

- 2023-07-27 litellm 0.1.0 上传 PyPI
- 2026-03-24 PyPI 恶意版本 1.82.7（导入 litellm.proxy 时触发）与 1.82.8（加入 .pth 文件，任何 Python 启动时触发）；官方 issue #24518 披露；根因被认为是 CI 中被入侵的 Trivy 扫描器泄露发布令牌（二手报道）
- 2026-03-31 Mercor 确认因 LiteLLM 被入侵而泄露数据
- 2026-04 DSPy 3.2.0 开始与 LiteLLM 解耦
- 2026 下半年 引入 Rust 核心；另有独立的 LiteLLM-Rust 极简网关（面向编码 Agent）
- 2026-11-06 PyPI 最新版 1.108.2

## 相关实体

- [[entities/openai-agents-sdk|OpenAI Agents SDK]]
- [[entities/dspy|DSPy]]
- [[entities/crewai|CrewAI]]
- [[entities/mercor|Mercor]]
- [[entities/dify|Dify]]

## 相关概念

- [[concepts/llm-observability|LLM 可观测性]]
- [[concepts/python-agent-development|Python Agent 开发]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "LiteLLM is an open source AI Gateway that gives you a single, unified interface to call 100+ LLM providers" — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
- "Self-hosted gateway for platform teams managing LLM access across an organization." — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
- "Track costs per key, team, and user across all providers." — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
- "The litellm PyPI package was compromised by an attacker who gained access to the maintainer's PyPI account." — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
