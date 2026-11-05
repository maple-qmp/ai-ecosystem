---
title: Claude 应用
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["Claude 应用", "Claude App", "Claude.ai", "Claude Cowork", "Cowork", "Claude Design"]
org: "[[entities/anthropic|Anthropic]]"
released: "2023-07"
competitors: ["[[entities/chatgpt]]", "[[entities/gemini-app]]", "[[entities/doubao-app]]", "[[entities/kimi-app]]"]
depends_on: ["[[entities/claude]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-applications-survey-2026-11]]"]
---

# Claude 应用

## 描述

[[entities/anthropic|Anthropic]] 面向个人和团队的 Claude 应用，包括网页版 claude.ai、桌面端和 iOS / Android 移动端，底层是 [[entities/claude|Claude]] 模型。claude.ai 于 2023-07-11 随 Claude 2 以公开 beta 上线，先开放美国和英国。2026 年的重点是从聊天转向替用户做事：Cowork 在 2026-01 以研究预览形式进入桌面应用，把 [[entities/claude-code|Claude Code]] 的 Agent 能力带给非开发者，04 月在桌面端正式可用，07 月扩展到网页和移动端；到 2026-11 官网写明「Cowork 现在就是 Claude」，不再作为独立产品名。同年陆续推出 Claude Design（设计与原型）、Claude Tag（在 Slack 中 @Claude 委派任务）、Claude Science（科研工作台）等。套餐分 Free、Pro（20 美元 / 月）、Max（100 美元）、Ultra（200 美元），Pro 及以上包含 Claude Code。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 对话助手
- **上游依赖**：[[entities/claude|Claude]]
- **竞争 / 替代**：[[entities/chatgpt|ChatGPT]]、[[entities/gemini-app|Gemini App]]、[[entities/doubao-app|豆包 App]]、[[entities/kimi-app|Kimi App]]

## 产品构成（2026-11）

- **Claude**：网页、桌面、移动端聊天，含联网搜索、文件创建与代码执行、跨对话记忆、连接器、Artifacts、Claude Design / Slides / Docs；Cowork 已并入
- **Claude Code**：Agent 式编程工具，见 [[entities/claude-code|Claude Code]]
- **Claude Tag**：Slack 中的团队 Agent，Team / Enterprise beta
- **Claude Duet**：研究预览，候补名单
- **专项**：Claude Security、Claude Science
- **套餐**：Free；Pro（月付 20 美元，含 Claude Code、Claude Science、Projects、Claude in Chrome 与 Microsoft 365）；Max（Pro 的 5 倍用量，含 100 美元 API 积分）；Ultra（无五小时限制，Pro 的 10 倍周用量，含 200 美元 API 积分）

## 时间线

- 2023-07-11 随 Claude 2 推出 claude.ai 公开 beta（美、英），单次输入 10 万 token
- 2026-01-12 Cowork 研究预览，进入桌面应用（二手报道，另有来源称 01-30）
- 2026-04-09 Cowork 在 macOS / Windows 桌面应用正式可用（二手报道）
- 2026-04-17 Claude Design（Anthropic Labs，Claude Opus 4.7 驱动）研究预览
- 2026-05-06 与 SpaceX 签约使用 Colossus 1 全部算力，用于改善 Pro / Max 容量
- 2026-06-23 Claude Tag（Slack）beta
- 2026-06-30 Claude Science 可用
- 2026-07-07 Cowork 扩展到 claude.ai 网页和 iOS / Android，先给 Max 用户（二手报道）
- 2026-07-14 Claude for Teachers（美国 K-12 教师免费使用高级功能）
- 2026-11 官网称「Claude Cowork is now just Claude」，向 Pro、Max、Ultra 推送

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/claude|Claude]]
- [[entities/claude-code|Claude Code]]
- [[entities/chatgpt|ChatGPT]]
- [[entities/gemini-app|Gemini App]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Claude 2 has improved performance, longer responses, and can be accessed via API as well as a new public-facing beta website, claude.ai." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]
- "Today, we’re launching Claude Design, a new Anthropic Labs product that lets you collaborate with Claude to create polished visual work like designs, prototypes, slides, one-pagers, and more." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]
- "Claude Cowork is now just Claude." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（claude.com 产品页，2026-11-05）
