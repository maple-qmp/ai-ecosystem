---
title: ChatGPT
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["ChatGPT", "ChatGPT Go", "ChatGPT Atlas"]
org: "[[entities/openai|OpenAI]]"
released: "2022-11"
competitors: ["[[entities/claude-app]]", "[[entities/gemini-app]]", "[[entities/doubao-app]]", "[[entities/kimi-app]]", "[[entities/perplexity]]"]
depends_on: ["[[entities/gpt]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-applications-survey-2026-11]]"]
---

# ChatGPT

## 描述

[[entities/openai|OpenAI]] 的对话助手，2022-11-30 上线，最初基于 GPT-3.5，引爆了生成式 AI 浪潮，至今是用户最多的 AI 助手：2026-02 每周约 9 亿活跃用户、约 5000 万付费订阅（媒体援引 OpenAI 说法，另有报道称超过 8 亿）。底层始终是 [[entities/gpt|GPT]] 系列，GPT-5（2025-08）起在应用内自动路由快速与推理模型，2026-05 起默认模型为 GPT-5.5 Instant。2026 年商业化上有两步：01-16 推出每月 8 美元的 ChatGPT Go 套餐，02-09 起在美国对 Free / Go 用户测试广告，付费更高的套餐不含广告。2025-10 推出的 AI 浏览器 ChatGPT Atlas 不到一年就关停，功能并入桌面应用。ChatGPT 也集成了 [[concepts/agent-skills|Agent Skills]] 标准。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 对话助手
- **上游依赖**：[[entities/gpt|GPT]]
- **竞争 / 替代**：[[entities/claude-app|Claude 应用]]、[[entities/gemini-app|Gemini App]]、[[entities/doubao-app|豆包 App]]、[[entities/kimi-app|Kimi App]]、[[entities/perplexity|Perplexity]]

## 时间线

- 2022-11-30 上线（GPT-3.5）
- 2025-02 每周 4 亿活跃用户
- 2025-08-07 GPT-5 上线，统一路由快速与推理模型
- 2025-10-21 发布 AI 浏览器 ChatGPT Atlas（先上 macOS）
- 2026-01-16 宣布测试广告；ChatGPT Go（8 美元 / 月）全球上线
- 2026-02-09 在美国对已登录成年 Free / Go 用户测试广告
- 2026-02 每周约 9 亿活跃用户、约 5000 万付费订阅（二手报道）
- 2026-05-05 GPT-5.5 Instant 成为默认模型（二手报道）
- 2026-05 / 06 App 月活约 10 亿（Sensor Tower 估算，日期说法不一）
- 2026-08-09 ChatGPT Atlas 停止服务，功能并入新的桌面应用（二手报道）

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/gpt|GPT]]
- [[entities/claude-app|Claude 应用]]
- [[entities/gemini-app|Gemini App]]
- [[entities/perplexity|Perplexity]]
- [[entities/codex-cli|Codex CLI]]

## 相关概念

- [[concepts/agent-skills|Agent Skills]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "More than 70 agent platforms, including ChatGPT, Cursor, GitHub Copilot, and VS Code, have integrated Agent Skills since we published the standard in December 2025." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Anthropic 2026-10-22）
