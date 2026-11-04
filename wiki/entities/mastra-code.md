---
title: Mastra Code
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["Mastra Code", "mastracode"]
org: "[[entities/mastra-inc]]"
released: "2026-02"
competitors: ["[[entities/claude-code]]"]
depends_on: ["[[entities/mastra]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/mastra-ecosystem-survey-2026-11]]"]
---

# Mastra Code

## 描述

[[entities/mastra-inc|Mastra 公司]]的开源终端（TUI）编程 Agent，2026-02-24 发布，用 [[entities/mastra|Mastra]] 框架构建。主打卖点是“从不压缩”：用 [[concepts/observational-memory|Observational Memory]] 代替常见的上下文压缩（compaction），长会话里没有压缩停顿，也不丢细节。支持 plan / build 两种模式、LSP 与 ast-grep 的 AST 感知编辑、可用不同模型的子 Agent、skills、worktree，以及项目级的持久会话。可用 Claude Max、ChatGPT Plus 订阅登录，或用 API key 经 Mastra 模型路由接入约 1800 个模型；数据存在本地 LibSQL（SQLite）。框架的 Agent Controller 最初就是为它而建。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 编程 Agent
- **上游依赖**：[[entities/mastra|Mastra]]（Agent Controller、Observational Memory）
- **竞争 / 替代**：[[entities/claude-code|Claude Code]]、Codex CLI、[[entities/cursor|Cursor]]

## 时间线

- 2026-02-24 发布
- 2026-02-27 Product Hunt 上线
- 2026-10-06 其会话运行时以 Agent Controller 名义在框架中 GA

## 相关实体

- [[entities/mastra|Mastra]]
- [[entities/mastra-factory|Mastra Factory]]
- [[entities/claude-code|Claude Code]]

## 相关概念

- [[concepts/observational-memory|Observational Memory]]
- [[concepts/agent-harness|Agent Harness]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Mastra Code is a TUI coding agent that never forgets." — [[sources/mastra-ecosystem-survey-2026-11|Mastra 生态深度调研]]
- "There’s no compaction pause and no noticeable degradation, even with long-running sessions." — [[sources/mastra-ecosystem-survey-2026-11|Mastra 生态深度调研]]
