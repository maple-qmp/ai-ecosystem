---
title: Claude Code
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["Claude Code"]
org: "[[entities/anthropic|Anthropic]]"
released: "2025-02"
competitors: ["[[entities/cursor]]", "[[entities/github-copilot]]"]
depends_on: ["[[entities/claude]]", "[[entities/bun]]"]
status: active
as_of: 2026-06
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/bun-survey-2026-11]]"]
---

# Claude Code

## 描述

[[entities/anthropic|Anthropic]] 的 Agent 式编程工具，可在终端、IDE、桌面与网页中读写代码、运行命令，并通过 [[concepts/model-context-protocol|MCP]] 接入外部工具。CLI 以 [[entities/bun|Bun]] 单文件可执行分发，Anthropic 因此在 2025-12 收购了 Bun。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 应用产品
- **上游依赖**：[[entities/claude|Claude]]、[[entities/bun|Bun]]（运行时）
- **竞争 / 替代**：[[entities/cursor|Cursor]]、[[entities/github-copilot|GitHub Copilot]]

## 时间线

- 2025-02 研究预览
- 2025-05 正式发布
- 2025-11 年化收入达 10 亿美元（公开发布约 6 个月）
- 2025-12 [[entities/anthropic|Anthropic]] 收购 [[entities/bun|Bun]]；Bun 此前已参与 Claude Code 原生安装器
- 2026-07 Bun 用 Claude Code 跑约 50 个工作流完成 Zig → Rust 重写，见 [[concepts/agent-driven-code-migration|Agent 驱动的代码迁移]]
- 2026-08 Bun 1.4 发布，Claude Code 的 p99 CPU 从 24% 降到 10%（Bun 自报）

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/claude|Claude]]
- [[entities/bun|Bun]]
- [[entities/cursor|Cursor]]
- [[entities/github-copilot|GitHub Copilot]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/agent-driven-code-migration|Agent 驱动的代码迁移]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Claude Code ships as a Bun executable to millions of users." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "If Bun breaks, Claude Code breaks." — [[sources/bun-survey-2026-11|Bun 深度调研]]

