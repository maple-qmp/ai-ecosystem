---
title: Coze / 扣子
type: entity
tags: [product]
kind: framework
layer: L4
aliases: ["Coze", "扣子", "Coze Studio", "Coze Loop", "扣子编程"]
org: "[[entities/bytedance]]"
released: "2024-02"
competitors: ["[[entities/dify]]", "[[entities/n8n]]", "[[entities/agentscope]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/lowcode-agent-platforms-survey-2026-11]]"]
---

# Coze / 扣子

## 描述

[[entities/bytedance|字节跳动]]的 AI Agent 开发平台，国内版叫“扣子”（coze.cn），海外版叫 Coze（coze.com），用户可通过可视化界面搭建 Bot、工作流和 Agent 并发布到各渠道。2025-07-29 字节开源了两部分：Coze Studio（可视化 Agent 开发工具，Go 后端 + React/TypeScript 前端，GitHub 约 2.18 万星）和 Coze Loop（Agent 调试、评测与观测），协议均为 Apache-2.0；README 称核心引擎完全开放，但部分功能（如音色定制）仅商业版提供。更早开源的 Go 语言框架 Eino 是其底层之一。商业版 2026 年快速迭代：扣子 2.0（2026-01）加入 Agent Skills、可持续执行数日的 Agent Plan、处理 Office 文档的 Agent Office，开发平台升级为“扣子编程”；扣子 3.0（2026-05 或 06）转向多人多 Agent 协作，可一键接入 Claude Code、Codex CLI 等外部 Agent。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 低代码 Agent 平台
- **上游依赖**：—（商业版接入 [[entities/doubao|豆包大模型]] 等，素材未列明全部模型）
- **竞争 / 替代**：[[entities/dify|Dify]]、[[entities/n8n|n8n]]；阿里的百炼应用与 [[entities/agentscope|AgentScope]]

## 时间线

- 2024-02 扣子上线（训练知识，待核实）
- 2025-02 开源 Go 语言 LLM 应用框架 Eino（二手报道）
- 2025-07-29 开源 Coze Studio 与 Coze Loop（Apache-2.0），48 小时合计约 9000 星（二手报道）
- 2026-01-19 扣子 2.0：Agent Skills、Agent Plan、Agent Office、Agent Coding（二手报道）
- 2026-05-27 或 06-01 扣子 3.0：多人多 Agent 协作、行业技能包、接入外部编码 Agent（二手报道，日期两说）

## 相关实体

- [[entities/bytedance|字节跳动]]
- [[entities/doubao|豆包大模型]]
- [[entities/dify|Dify]]
- [[entities/agentscope|AgentScope]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/llm-observability|LLM 可观测性]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Coze Studio is an all-in-one AI agent development tool." — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
- "An AI agent development platform with all-in-one visual tools, simplifying agent creation, debugging, and deployment like never before." — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
