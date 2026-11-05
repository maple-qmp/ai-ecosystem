---
title: Cursor
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["Cursor", "Cursor 编辑器", "Anysphere", "Composer"]
org: "[[entities/xai|xAI（SpaceX Super Intelligence）]]"
released: "2023"
competitors: ["[[entities/claude-code]]", "[[entities/github-copilot]]", "[[entities/windsurf]]", "[[entities/devin]]"]
depends_on: ["[[entities/claude]]", "[[entities/grok]]", "[[entities/gpt]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/frontier-closed-models-survey-2026-11]]", "[[sources/ai-applications-survey-2026-11]]"]
---

# Cursor

## 描述

Anysphere 公司基于 VS Code 打造的 AI 代码编辑器，提供补全、多文件编辑和 Agent 模式，可接入 [[entities/claude|Claude]] 等多家模型。2025 年底起训练自研代码模型 Composer（2026-03 出 Composer 2），减少对外部模型的依赖。它是增长最快的编程工具之一：年化收入 2026-04 底约 30 亿美元，06 月初超过 40 亿美元。2026 年它被卷入 [[entities/xai|xAI]] 体系：04 月与 SpaceX 签收购期权，07 月首发与 xAI 共同开发的 [[entities/grok|Grok 4.5]]，08 月 OpenAI 停止向它提供模型，08-14 SpaceX 以 600 亿美元全股票完成收购。它也集成了 [[concepts/agent-skills|Agent Skills]] 标准。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 编程 Agent / AI 编辑器
- **上游依赖**：[[entities/claude|Claude]]、[[entities/grok|Grok]]、自研 Composer；[[entities/gpt|GPT]] 至 2026-08 停供
- **竞争 / 替代**：[[entities/claude-code|Claude Code]]、[[entities/github-copilot|GitHub Copilot]]、[[entities/windsurf|Windsurf（Devin Desktop）]]、[[entities/devin|Devin]]

## 时间线

- 2023 发布
- 2025-10 / 11 首个自研代码模型 Composer（日期说法不一）
- 2026-03 Composer 2
- 2026-04-21 与 SpaceX（xAI）签期权，可在 2026 年底前以 600 亿美元收购 Anysphere
- 2026-04 底 年化收入约 30 亿美元（Bloomberg 来源）
- 2026-06 初 年化收入超过 40 亿美元
- 2026-06-16 SpaceX 宣布全股票收购
- 2026-07-08 与 xAI 共同开发的 [[entities/grok|Grok 4.5]] 首发于 Cursor
- 2026-08 OpenAI 停止向 Cursor 提供模型
- 2026-08-14 收购完成，归入 [[entities/xai|xAI（SpaceX Super Intelligence）]]

## 相关实体

- [[entities/claude-code|Claude Code]]
- [[entities/github-copilot|GitHub Copilot]]
- [[entities/windsurf|Windsurf（Devin Desktop）]]
- [[entities/claude|Claude]]
- [[entities/gpt|GPT]]
- [[entities/xai|xAI（SpaceX Super Intelligence）]]
- [[entities/grok|Grok]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-skills|Agent Skills]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "More than 70 agent platforms, including ChatGPT, Cursor, GitHub Copilot, and VS Code, have integrated Agent Skills since we published the standard in December 2025." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Anthropic 2026-10-22）
- "Starting with Grok 4.5, the models are co-developed with incoming SpaceXSI subsidiary Cursor." — [[sources/frontier-closed-models-survey-2026-11|前沿闭源模型时间线调研]]（Wikipedia）
