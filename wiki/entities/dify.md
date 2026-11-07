---
title: Dify
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Dify", "Dify.AI", "LangGenius", "difyctl"]
org: "LangGenius"
released: "2023"
competitors: ["[[entities/coze]]", "[[entities/n8n]]", "[[entities/langgraph]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/lowcode-agent-platforms-survey-2026-11]]"]
---

# Dify

## 描述

LangGenius 开源的 LLM 应用开发平台（GitHub 约 16.1 万星），用可视化画布编排 AI 工作流、[[concepts/rag|RAG]] 管道和 Agent，并内置模型管理与可观测性，可在云端、VPC 或自托管部署。协议是 Dify Open Source License，即附加条件的 Apache 2.0，并非标准开源协议。2025-02 的 v1.0 引入插件体系（模型、工具、数据源都以插件接入，配套 Marketplace），2025-07 的 v1.6 内置双向 [[concepts/model-context-protocol|MCP]]：既能调用 MCP 服务器，也能把 Dify 应用发布成 MCP 服务器。2026 年的版本加入人工输入节点（工作流可暂停等人审批）、摘要索引和团队共享工作流，并发布官方 CLI difyctl，让其他 Agent 能一条命令调用 Dify 应用。2026-03 公司完成 3000 万美元 Pre-A 轮，称 Dify 运行在全球 140 多万台机器上，280 家企业使用商业版。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 低代码 Agent 平台
- **上游依赖**：—（通过插件接入各模型厂商 API 与本地模型）
- **竞争 / 替代**：[[entities/coze|Coze / 扣子]]、[[entities/n8n|n8n]]；代码优先的 [[entities/langgraph|LangGraph]] 等框架

## 时间线

- 2023 首次开源（训练知识，待核实）
- 2025-01-09 推出插件系统；2025-02-17 v1.0.0
- 2025-06 GitHub 超过 10 万星
- 2025-07-10 v1.6.0 内置双向 MCP
- 2025-09 Knowledge Pipeline
- 2026-02-05 v1.12.0 摘要索引；2026-03-03 v1.13.0 人工输入节点
- 2026-03-09 Pre-A 轮 3000 万美元，HSG 领投（估值约 1.8 亿美元为二手报道）
- 2026-05-13 v1.14.1 工作流成为团队资产
- 2026-07-09 官方 CLI difyctl

## 相关实体

- [[entities/coze|Coze / 扣子]]
- [[entities/n8n|n8n]]
- [[entities/langgraph|LangGraph]]
- [[entities/litellm|LiteLLM]]

## 相关概念

- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Dify is an open-source LLM app development platform." — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
- "Build Agentic workflows, RAG pipelines, with rich AI model and tool support." — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
- "Dify introduces CLI access, making it easy for Agents to call Dify apps with a single command." — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
