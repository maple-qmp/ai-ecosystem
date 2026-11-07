---
title: Microsoft 365 Copilot
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["Microsoft 365 Copilot", "M365 Copilot", "Copilot Cowork", "Agent 365", "Microsoft 365 E7", "Frontier Suite"]
org: "[[entities/microsoft]]"
released: "2023-11"
competitors: ["[[entities/notion-ai]]", "[[entities/salesforce-agentforce]]", "[[entities/claude-app]]", "[[entities/chatgpt]]"]
depends_on: ["[[entities/gpt]]", "[[entities/claude]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/ai-applications-expansion-survey-2026-11]]"]
---

# Microsoft 365 Copilot

## 描述

[[entities/microsoft|Microsoft]] 内嵌在 Word、Excel、PowerPoint、Outlook、Teams 里的企业 AI 助手，另有 Copilot Chat 对话入口，单独购买时是每用户每月 30 美元的附加许可（二手报道）。2026 年它从助手转向 Agent：2026-02 起 Office 网页版推出 Agent Mode，2026-03-09 的「Wave 3」发布与 [[entities/anthropic|Anthropic]] 合作的 Copilot Cowork，把 [[entities/claude-app|Claude Cowork]] 的底层技术带进 Microsoft 365，用来执行长时间、多步的任务。模型上它主动走多模型路线，官方称“model-diverse by design”：[[entities/claude|Claude]] 经 Frontier 计划进入主线 Copilot Chat，与最新的 [[entities/gpt|GPT]] 模型并列。管理侧推出 Agent 365（管理和保护 AI Agent 的控制平面），并把 E5、Copilot、Agent 365 打包成 Microsoft 365 E7「Frontier Suite」，两者都在 2026-05-01 正式可用。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 办公与企业
- **上游依赖**：[[entities/gpt|GPT]]（OpenAI）、[[entities/claude|Claude]]（Anthropic，Copilot Cowork 与 Copilot Chat）；云端运行在 [[entities/azure|Azure]]
- **竞争 / 替代**：[[entities/notion-ai|Notion AI]]、[[entities/salesforce-agentforce|Salesforce Agentforce]]、[[entities/claude-app|Claude 应用]]（Cowork）、[[entities/chatgpt|ChatGPT]]（ChatGPT Work）

## 时间线

- 2023-11 Microsoft 365 Copilot 向企业客户正式提供（训练知识，待核实）
- 2026-02 Word、Excel、PowerPoint 网页版逐步推出 Agent Mode（二手报道）
- 2026-03-09 Wave 3：Copilot Cowork（与 Anthropic 合作，先经 Frontier 计划）；Claude 进入主线 Copilot Chat；Word / Excel / PowerPoint / Outlook / Copilot Chat 推出新一代 Agent 体验；宣布 Agent 365 与 E7
- 2026-05-01 Agent 365 与 Microsoft 365 E7「Frontier Suite」正式可用；E7 每用户每月 99 美元，Agent 365 单买 15 美元（价格为二手报道）

## 相关实体

- [[entities/microsoft|Microsoft]]
- [[entities/anthropic|Anthropic]]
- [[entities/claude-app|Claude 应用]]
- [[entities/github-copilot|GitHub Copilot]]
- [[entities/microsoft-agent-framework|Microsoft Agent Framework]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/computer-use|Computer Use]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Microsoft 365 Copilot is model-diverse by design." — [[sources/ai-applications-expansion-survey-2026-11|AI 应用扩容调研]]
- "Agent 365, the control plane for AI agents, will become generally available on May 1." — [[sources/ai-applications-expansion-survey-2026-11|AI 应用扩容调研]]
