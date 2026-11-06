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
depends_on: ["[[entities/kimi]]", "[[entities/grok]]", "[[entities/claude]]", "[[entities/gpt]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-06
sources: ["[[sources/frontier-closed-models-survey-2026-11]]", "[[sources/ai-applications-survey-2026-11]]"]
---

# Cursor

## 描述

Anysphere 公司基于 VS Code 打造的 AI 代码编辑器，提供补全、多文件编辑和 Agent 模式，可接入 [[entities/claude|Claude]] 等多家模型。2023-10 获 OpenAI Startup Fund 领投的 800 万美元种子轮，此后成为增长最快的编程工具之一：年化收入 2025-01 超过 1 亿美元、2025-06 超过 5 亿，2026 年初超过 30 亿（估值 293 亿美元）。2025-10 起训练自研 Agent 模型 Composer（MoE，用强化学习专门训练）；2026-03 的 Composer 2 基于月之暗面的 [[entities/kimi|Kimi]] K2.5，美国众议院国土安全委员会因此就使用中国模型向 Anysphere 施压。2026 年它并入 [[entities/xai|xAI]] 体系：04 月与 SpaceX 签收购期权，07 月首发与 xAI 共同开发的 [[entities/grok|Grok 4.5]]，08 月 OpenAI 停止向它提供模型，08-14 SpaceX 以 600 亿美元全股票完成收购，此后 Cursor 自己发布 Grok 4.6、4.7。它也集成了 [[concepts/agent-skills|Agent Skills]] 标准。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 编程 Agent / AI 编辑器
- **上游依赖**：自研 Composer（Composer 2 基于 [[entities/kimi|Kimi]] K2.5）、[[entities/grok|Grok]]、[[entities/claude|Claude]]；[[entities/gpt|GPT]] 至 2026-08 停供
- **竞争 / 替代**：[[entities/claude-code|Claude Code]]、[[entities/github-copilot|GitHub Copilot]]、[[entities/windsurf|Windsurf（Devin Desktop）]]、[[entities/devin|Devin]]

## 时间线

- 2023 发布；2023-10 种子轮 800 万美元（OpenAI Startup Fund 领投）
- 2024-11 收购代码补全公司 Supermaven
- 2025-01 年化收入超过 1 亿美元；2025-06 超过 5 亿
- 2025-10-29 首个自研 Agent 模型 Composer（MoE）
- 2026 年初 年化收入超过 30 亿美元，估值 293 亿美元
- 2026-03-19 Composer 2（基于 Kimi K2.5），每百万输入 / 输出 token 0.50 / 2.50 美元
- 2026-04 美国众议院国土安全委员会就使用 Kimi 模型向 Anysphere 施压
- 2026-04-21 SpaceX 获得在年内以 600 亿美元收购 Cursor 的权利（或改付 100 亿美元用于合作）
- 2026-06 初 年化收入超过 40 亿美元（二手报道）
- 2026-06-16 SpaceX 宣布全股票收购
- 2026-07-08 与 xAI 共同开发的 [[entities/grok|Grok 4.5]] 首发于 Cursor
- 2026-08 OpenAI 停止向 Cursor 提供模型
- 2026-08-12 发布 Grok 4.6
- 2026-08-14 收购完成，成为 SpaceX 全资子公司，并入 [[entities/xai|xAI（SpaceX Super Intelligence）]]
- 2026-09-21 Cursor 发布 Grok 4.7，称是其最强的长任务编程模型

## 相关实体

- [[entities/claude-code|Claude Code]]
- [[entities/github-copilot|GitHub Copilot]]
- [[entities/windsurf|Windsurf（Devin Desktop）]]
- [[entities/claude|Claude]]
- [[entities/gpt|GPT]]
- [[entities/xai|xAI（SpaceX Super Intelligence）]]
- [[entities/grok|Grok]]
- [[entities/kimi|Kimi]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-skills|Agent Skills]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Cursor has officially been acquired by SpaceX. This completes the acquisition process that started in April, when we announced our partnership with SpaceXAI to accelerate our model training efforts." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Cursor，2026-08-14）
- "Composer is a mixture-of-experts (MoE) language model supporting long-context generation and understanding." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Cursor，2025-10-29）
- "More than 70 agent platforms, including ChatGPT, Cursor, GitHub Copilot, and VS Code, have integrated Agent Skills since we published the standard in December 2025." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Anthropic 2026-10-22）
- "Starting with Grok 4.5, the models are co-developed with incoming SpaceXSI subsidiary Cursor." — [[sources/frontier-closed-models-survey-2026-11|前沿闭源模型时间线调研]]（Wikipedia）
