---
title: ChatGPT
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["ChatGPT", "ChatGPT Go", "ChatGPT Atlas", "ChatGPT Work"]
org: "[[entities/openai|OpenAI]]"
released: "2022-11"
competitors: ["[[entities/claude-app]]", "[[entities/gemini-app]]", "[[entities/doubao-app]]", "[[entities/kimi-app]]", "[[entities/perplexity]]"]
depends_on: ["[[entities/gpt]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-07
sources: ["[[sources/ai-applications-survey-2026-11]]", "[[sources/ai-applications-expansion-survey-2026-11]]"]
---

# ChatGPT

## 描述

[[entities/openai|OpenAI]] 的对话助手，2022-11-30 上线，最初基于 GPT-3.5，引爆了生成式 AI 浪潮，至今是用户最多的 AI 助手：2026-02 每周约 9 亿活跃用户、约 5000 万付费订阅（媒体援引 OpenAI 说法，另有报道称超过 8 亿）。底层始终是 [[entities/gpt|GPT]] 系列，GPT-5（2025-08）起在应用内自动路由快速与推理模型，2026-05 起默认模型为 GPT-5.5 Instant。2026 年开始做广告：01 月宣布在美国对免费用户测试广告，03 月起用户开始看到，08 月广告收入达到 10 亿美元，更高档的付费套餐不含广告。同年它也在向 Agent 扩展，07 月推出可基于已连接应用和文件生成文档的 ChatGPT Work。2025-10 推出的 AI 浏览器 ChatGPT Atlas 不到一年就关停：2026-03 OpenAI 宣布把 Atlas、ChatGPT 桌面应用和 Codex 合并成一个桌面应用，Atlas 于 08-09 停止服务。ChatGPT 也集成了 [[concepts/agent-skills|Agent Skills]] 标准。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 对话助手
- **上游依赖**：[[entities/gpt|GPT]]
- **竞争 / 替代**：[[entities/claude-app|Claude 应用]]、[[entities/gemini-app|Gemini App]]、[[entities/doubao-app|豆包 App]]、[[entities/kimi-app|Kimi App]]、[[entities/perplexity|Perplexity]]

## 时间线

- 2022-11-30 上线（GPT-3.5），两个月月活达 1 亿
- 2025-02 每周 4 亿活跃用户（二手报道）
- 2025-08-07 GPT-5 上线，统一路由快速与推理模型
- 2025-10-21 发布 AI 浏览器 ChatGPT Atlas（先上 macOS）
- 2026-01-07 推出 ChatGPT Health
- 2026-01-17 宣布在美国对已登录成年免费用户测试广告（二手报道记为美国时间 01-16，同时推出 8 美元 / 月的 ChatGPT Go）
- 2026-02 每周 9 亿活跃用户；付费订阅约 5000 万（二手报道）
- 2026-03 用户开始看到广告；OpenAI 宣布把 Atlas、ChatGPT 桌面应用与 Codex 合并为一个桌面应用
- 2026-05-05 GPT-5.5 Instant 成为默认模型（二手报道）
- 2026-05 / 06 App 月活约 10 亿（Sensor Tower 估算，日期说法不一）
- 2026-07 推出 Agent ChatGPT Work；ChatGPT 中的 apps 改名 plugins
- 2026-08 广告收入达 10 亿美元；StatCounter 估计占 AI 聊天机器人市场约 79%
- 2026-08-09 ChatGPT Atlas 正式关停

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
- [[concepts/ai-browser|AI 浏览器]]（Atlas）

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "More than 70 agent platforms, including ChatGPT, Cursor, GitHub Copilot, and VS Code, have integrated Agent Skills since we published the standard in December 2025." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Anthropic 2026-10-22）
