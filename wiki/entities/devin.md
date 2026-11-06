---
title: Devin
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["Devin", "Devin AI", "Cognition", "Cognition AI", "SWE-1.7", "SWE-2"]
org: "Cognition AI"
released: "2024-03"
competitors: ["[[entities/claude-code]]", "[[entities/cursor]]", "[[entities/github-copilot]]", "[[entities/codex-cli]]"]
depends_on: ["[[entities/kimi]]", "[[entities/claude]]", "[[entities/gpt]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/ai-applications-survey-2026-11]]"]
---

# Devin

## 描述

Cognition AI 的自主编程 Agent，2024-03-12 发布时自称「第一个 AI 软件工程师」：在沙箱里拥有自己的 shell、代码编辑器和浏览器，可以端到端完成开发任务；2024-12 正式可用，2025-04 的 Devin 2.0 改为云端 IDE 并把入门价降到每月 20 美元。2025-07 Cognition 收购 [[entities/windsurf|Windsurf]]，2026-06 把它改造成 Devin Desktop，形成「云端 Agent + 桌面 Agent 管理器」两件套。Devin 不绑定单一模型：Cognition 自研 SWE 系列，其中 SWE-1.7 以 [[entities/kimi|Kimi]] K2.7 为基座，同时为 [[entities/claude|Claude]] Opus / Fable 和 [[entities/gpt|GPT]] Astra 等第三方模型做了专门的 Fusion harness。增长很快：年化收入从 2026-05 的 4.92 亿美元涨到 09-25 的 10 亿美元以上，估值在 2026-09 的 E 轮达到 480 亿美元。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 编程 Agent
- **上游依赖**：自研 SWE 系列（SWE-1.7 基于 [[entities/kimi|Kimi]] K2.7，SWE-2 Flash 基于 Thinking Machines 的 Inkling-Small）；第三方 [[entities/claude|Claude]]、[[entities/gpt|GPT]]
- **竞争 / 替代**：[[entities/claude-code|Claude Code]]、[[entities/cursor|Cursor]]、[[entities/github-copilot|GitHub Copilot]]（其 Agent HQ 也接入 Cognition 的 Agent）、[[entities/codex-cli|Codex]]

## 时间线

- 2023-08 Cognition 成立（Wikipedia；Cognition 自述为 2024-01）
- 2024-03-12 发布 Devin，早期访问
- 2024-04 估值 20 亿美元（Founders Fund 领投 1.75 亿美元）
- 2024-12-10 正式可用，团队版每月 500 美元起
- 2025-03 估值 40 亿美元
- 2025-04-03 Devin 2.0：云端 IDE、多个 Devin 并行，20 美元起
- 2025-07-14 签约收购 [[entities/windsurf|Windsurf]]
- 2025-09 估值约 100 亿美元
- 2025-10-29 自研 SWE-1.5（Cerebras 推理最高 950 token/s）
- 2026-05-27 D 轮超过 10 亿美元，估值 260 亿；年化收入 4.92 亿美元
- 2026-06-02 Windsurf 升级为 Devin Desktop
- 2026-07-08 SWE-1.7（基于 Kimi K2.7）
- 2026-09-08 E 轮超过 20 亿美元，估值 480 亿（a16z、Accel 领投）；年化收入近 9 亿美元
- 2026-09-10 SWE-2；09-11 Fusion harness 上线 Devin Desktop 与 CLI
- 2026-09-25 年化收入超过 10 亿美元
- 2026-10-26 Devin Security；10-28 收购 Corridor
- 2026-11-04 SWE-2 Flash

## 相关实体

- [[entities/windsurf|Windsurf（Devin Desktop）]]
- [[entities/kimi|Kimi]]
- [[entities/claude-code|Claude Code]]
- [[entities/cursor|Cursor]]
- [[entities/github-copilot|GitHub Copilot]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "We've also equipped Devin with common developer tools including the shell, code editor, and browser within a sandboxed compute environment—everything a human would need to do their work." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Cognition，2024-03-12）
- "Since SWE-1.7 was trained from a Kimi K2.7 base, which had already undergone extensive RL post-training, the large additional gains from our own training challenge the idea of a ‘post-training ceiling’" — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Cognition，2026-07-08）
- "Since our last round in May, Cognition’s run-rate revenue has grown from $492M to almost $900M." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Cognition，2026-09-08）
