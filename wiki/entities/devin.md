---
title: Devin
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["Devin", "Devin AI", "Cognition", "Cognition AI"]
org: "Cognition AI"
released: "2024-03"
competitors: ["[[entities/claude-code]]", "[[entities/cursor]]", "[[entities/github-copilot]]", "[[entities/codex-cli]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-applications-survey-2026-11]]"]
---

# Devin

## 描述

Cognition AI 的自主编程 Agent，2024-03-12 发布时自称「第一个 AI 软件工程师」：在沙箱里拥有自己的 shell、代码编辑器和浏览器，可以端到端完成开发任务。发布时公布的 SWE-bench 成绩是在 25% 随机子集上解决 13.86% 的问题，此前最好成绩是 1.96%。2025-07 Cognition 收购 [[entities/windsurf|Windsurf]]，2026-04 起把 Devin 嵌入 Windsurf 编辑器，2026-06 再把 Windsurf 改名 Devin Desktop，形成「云端 Agent + 桌面 IDE」两件套。公司估值从 2025-09 的 102 亿美元升到 2026-05 的 260 亿美元。Cognition 没有公开 Devin 用哪些底层模型；它自研了 SWE 系列模型，见 [[entities/windsurf|Windsurf]] 页。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 编程 Agent
- **上游依赖**：未公开；自研 SWE 系列模型
- **竞争 / 替代**：[[entities/claude-code|Claude Code]]、[[entities/cursor|Cursor]]、[[entities/github-copilot|GitHub Copilot]]（Copilot 的 Agent HQ 也接入了 Cognition 的 Agent）、[[entities/codex-cli|Codex]]

## 时间线

- 2024-03-12 发布 Devin，早期访问；同时公布 Founders Fund 领投的 2100 万美元 A 轮
- 2025-04 Devin 2.0，入门价降到每月 20 美元（日期有来源写 2026-04）
- 2025-07-14 收购 [[entities/windsurf|Windsurf]]，带来约 8200 万美元 ARR、350 多家企业客户
- 2025-09 融资 4 亿美元，估值 102 亿美元
- 2026-04-15 Windsurf 2.0 内嵌 Devin
- 2026-05-27 D 轮超过 10 亿美元，投后估值 260 亿美元
- 2026-06-02 Windsurf 改名 Devin Desktop
- 2026-08 报道称洽谈估值至少 400 亿美元（未确认）

## 相关实体

- [[entities/windsurf|Windsurf（Devin Desktop）]]
- [[entities/claude-code|Claude Code]]
- [[entities/cursor|Cursor]]
- [[entities/github-copilot|GitHub Copilot]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Devin correctly resolves 13.86%* of the issues end-to-end, far exceeding the previous state-of-the-art of 1.96%." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Cognition 博客 2024-03-12，经搜索摘要读取）
