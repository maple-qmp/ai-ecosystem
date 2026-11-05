---
title: GitHub Copilot
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["GitHub Copilot", "Copilot", "Copilot CLI", "Copilot cloud agent", "Agent HQ"]
org: "[[entities/microsoft|Microsoft]]"
released: "2021"
competitors: ["[[entities/cursor]]", "[[entities/claude-code]]", "[[entities/windsurf]]", "[[entities/devin]]", "[[entities/codex-cli]]"]
depends_on: ["[[entities/gpt]]", "[[entities/claude]]", "[[entities/gemini]]", "[[entities/grok]]", "[[entities/kimi]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/ai-applications-survey-2026-11]]"]
---

# GitHub Copilot

## 描述

GitHub（[[entities/microsoft|Microsoft]]）的 AI 编程助手，2021-06 技术预览、2022-06 正式发布，是第一个大规模普及的 AI 编程产品。官方文档现在把它定义为“帮助你编写、理解和交付软件的 AI 助手”，能力分四类：辅助（补全、问答）、Agent（研究仓库、提计划、改文件、审 PR）、定制（指令、技能、自定义 Agent）和外部 Agent / 模型 / 工具（第三方编程 Agent 与 MCP 服务器）。它早已不只用 OpenAI 模型：2026-11 的模型表同时列出 [[entities/gpt|GPT]]、[[entities/claude|Claude]]、[[entities/gemini|Gemini]]、[[entities/grok|Grok]]、[[entities/kimi|Kimi K3]] 和微软自家的 MAI-Code。计费改为按 AI 积分（每积分 0.01 美元）计量，套餐从 Free 到 Max、Business、Enterprise，所有套餐都含 Copilot CLI 和 GitHub Copilot app。用户数 2025-07 超过 2000 万，但 2026 年在开发者工作场景的采用率被 [[entities/claude-code|Claude Code]] 超过。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 编程 Agent
- **上游依赖**：[[entities/gpt|GPT]]、[[entities/claude|Claude]]、[[entities/gemini|Gemini]]、[[entities/grok|Grok]]、[[entities/kimi|Kimi]]、Microsoft MAI-Code
- **竞争 / 替代**：[[entities/cursor|Cursor]]、[[entities/claude-code|Claude Code]]、[[entities/windsurf|Windsurf（Devin Desktop）]]、[[entities/devin|Devin]]、[[entities/codex-cli|Codex]]；Agent HQ 同时也把 Anthropic、OpenAI、Google、Cognition、xAI 的编程 Agent 接进 GitHub

## 套餐与模型（2026-11）

- **套餐**：Free、Student（认证学生免费）、Pro、Pro+、Max（个人最高积分额度）、Business、Enterprise；另有面向合格企业的 Copilot access（GitHub Enterprise Cloud 用户 0 美元席位费，否则每用户每月 10 美元，用量另计）
- **入口**：IDE、github.com、Copilot CLI、GitHub Copilot app、Copilot cloud agent
- **模型**：OpenAI GPT-5.3-Codex 至 GPT-6.1；Anthropic Claude Haiku / Sonnet / Opus 4.5–5.5 与 Fable 5 / 5.1；Google Gemini 3.8 Flash、Gemini 4 Argon；Microsoft MAI-Code-1.1-Flash；Moonshot AI Kimi K3；xAI Grok 4.5–4.7。自动模型选择在无其他模型可用时回退到长期支持模型 GPT-5.3-Codex

## 时间线

- 2021-06 技术预览
- 2022-06 正式发布
- 2025-04 用户超过 1500 万（二手报道）
- 2025-07 用户超过 2000 万，季度增加 500 多万（二手报道）
- 2025-10 用户超过 2600 万（二手报道）
- 2026-01 宣布 Agent HQ，统一接入第三方编程 Agent（二手报道，上线日期另有 2026-04-27 的说法）
- 2026-02 Copilot coding agent 正式可用（二手报道）
- 2026-05 至 07 JetBrains 开发者调查：工作场景采用率 21%，低于 Claude Code 的 39%（二手报道）
- 2026-07 Nadella 在财报电话会上称用户达 5000 万（二手报道，未核实）
- 2026-10-22 Anthropic 称 GitHub Copilot 已集成 Agent Skills

## 相关实体

- [[entities/microsoft|Microsoft]]
- [[entities/openai|OpenAI]]
- [[entities/cursor|Cursor]]
- [[entities/claude-code|Claude Code]]
- [[entities/devin|Devin]]
- [[entities/gpt|GPT]]
- [[entities/claude|Claude]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "GitHub Copilot is an AI assistant that helps you write, understand, and ship software. It suggests code as you type, answers questions about a codebase, reviews your changes, and works on tasks you assign it." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（GitHub Docs）
- "Third-party coding agents work asynchronously on development tasks and can make changes and open or update pull requests for your review." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（GitHub Docs）
- "All plans include Copilot CLI and the Copilot app." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（GitHub Docs）
