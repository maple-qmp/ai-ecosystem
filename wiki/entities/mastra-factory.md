---
title: Mastra Factory
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["Mastra Factory"]
org: "[[entities/mastra-inc]]"
released: "2026-07"
competitors: []
depends_on: ["[[entities/mastra]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/mastra-ecosystem-survey-2026-11]]"]
---

# Mastra Factory

## 描述

[[entities/mastra-inc|Mastra 公司]]的开源、Agent 驱动的软件交付环境，在用户自己控制的 Web 应用里运行持久编程 Agent，用 [[entities/mastra|Mastra]] 框架构建。工作项依次经过 Intake、Triage、Planning、Building、Review、Done 六个阶段：Planning 产出的实现计划要人工批准，Building 在该工作项独立的 workspace 中进行并产出 PR，合并仍由人按仓库原有流程决定。每个阶段可单独设为手动或自动，协作者可用 Signals 在 Agent 运行中途引导。集成 GitHub、Linear、Slack，可用托管的 [[entities/mastra-platform|Mastra Platform]] 或自托管。Mastra 自报：自 2026-07 起，Factory 在自家仓库写了 25–35% 的 PR、关闭了 50–60% 的 issue（该仓库每周 100+ 新 issue、200–250 个合并 PR）。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 编程 Agent（团队级、异步）
- **上游依赖**：[[entities/mastra|Mastra]]（Agent Controller、Workspaces、Signals）
- **竞争 / 替代**：[[entities/github-copilot|GitHub Copilot]] 编程 Agent、Devin、Open SWE 等异步编程 Agent

## 时间线

- 2026-07-27 公布
- 2026-09-08 公开测试；09-09 Product Hunt 当日第一
- 2026-10-06 其所用会话运行时以 Agent Controller 名义在框架中 GA

## 相关实体

- [[entities/mastra|Mastra]]
- [[entities/mastra-code|Mastra Code]]
- [[entities/mastra-platform|Mastra Platform]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "AgentController keeps this conversation open and lets you watch it, interrupt and steer." — [[sources/mastra-ecosystem-survey-2026-11|Mastra 生态深度调研]]
