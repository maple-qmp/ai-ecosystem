---
title: LangSmith
type: entity
tags: [product]
kind: infra
layer: L4
aliases: ["LangSmith", "LangSmith Deployment", "LangSmith Fleet", "LangGraph Platform"]
org: "[[entities/langchain-inc]]"
released: "2024-02"
competitors: []
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/langchain-ecosystem-survey-2026-11]]"]
---

# LangSmith

## 描述

[[entities/langchain-inc|LangChain 公司]]的闭源商业平台，也是公司的主要收入来源。2024-02 以 LLM 应用的可观测性（追踪）与评测工具发布，框架无关，不使用 [[entities/langchain|LangChain]] 也能接入。2025–2026 年扩展为“Agent 工程平台”：吸收了 [[entities/langgraph|LangGraph]] 的托管部署服务，加入无代码 Agent、托管 [[entities/deep-agents|Deep Agents]]、代码沙箱、LLM 网关和微调。提供 LangSmith Cloud、自托管和 AWS 上的 BYOC（部署在客户 VPC）。

## 产品模块

- **Observability / Evaluation**：追踪、评测；2026 年加入 AI Search（语义搜索追踪）、Trajectories（主 Agent 与子 Agent 的会话时间线）、Messages View
- **Deployment**（原 LangGraph Platform）与 **Studio**（原 LangGraph Studio，Agent 调试 IDE）
- **Fleet**（原 Agent Builder）：无代码 Agent 工作区，带权限、Agent 身份与凭证、人工审批收件箱、Slack 机器人、预置 Agent
- **Engine**：自动聚类线上失败、诊断根因并提出修复和评测；v2 加入红队测试
- **Managed Deep Agents**：Deep Agents 的托管运行时
- **Sandboxes**：在硬件虚拟化 microVM 中运行 Agent 生成的代码
- **LLM Gateway**：位于 Agent 与模型之间，做花费上限、限流、模型回退、PII 与密钥脱敏
- **Context Hub**：管理 AGENTS.md、技能、策略等文件的版本与评论
- **Fine-Tuning**：用线上轨迹作训练数据，经 Baseten 或 Fireworks 微调并部署
- **SmithDB**：自研的可观测性数据库，支撑 LangSmith 核心负载

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 基础设施（可观测性、评测、部署）
- **竞争 / 替代**：Langfuse、Arize Phoenix、Weights & Biases Weave、Braintrust（观测与评测）、[[entities/mastra-platform|Mastra Platform]]；托管运行时方向有 [[entities/vercel|Vercel]] 等

## 时间线

- 2024-02 发布
- 2025-05-14 LangGraph Platform GA
- 2025-07 上架 AWS Marketplace
- 2025-10 LangGraph Platform 更名 LangSmith Deployment；推出 Agent Builder
- 2026-03-19 Agent Builder 更名并扩展为 LangSmith Fleet
- 2026-05-14 Interrupt 2026：Engine（公开测试）、SmithDB、Managed Deep Agents、Sandboxes GA、Context Hub、LLM Gateway（私测）；Fleet 推出五个预置 Agent，Developer / Plus 套餐含免费模型额度（Fireworks 推理）
- 2026-08 Managed Deep Agents 公开测试（08-07，仅美国区 Cloud）；LLM Gateway 公开测试；AWS BYOC GA
- 2026-09 Managed Deep Agents v0.8（内置 Parallel 网页搜索）；Engine v2
- 2026-10 Managed Deep Agents v0.9（Slack 集成、用户级记忆、定时任务）、AI Search、Trajectories、Custom Apps、Fine-Tuning

## 相关实体

- [[entities/langchain-inc|LangChain 公司]]
- [[entities/langchain|LangChain]]
- [[entities/langgraph|LangGraph]]
- [[entities/deep-agents|Deep Agents]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/benchmark-contamination|基准污染与饱和]]
- [[concepts/terminal-bench|Terminal-Bench]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Each sandbox runs in a hardware-virtualized microVM, isolated from your services and from other sandboxes." — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
- "LLM Gateway sits between your agents and the models they call." — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
