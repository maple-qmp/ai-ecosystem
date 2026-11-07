---
title: Notion AI
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["Notion AI", "Notion Agent", "Notion Custom Agents", "Notion 3.0"]
org: "Notion Labs"
released: "2023-02"
competitors: ["[[entities/microsoft-365-copilot]]", "[[entities/claude-app]]", "[[entities/chatgpt]]"]
depends_on: ["[[entities/gpt]]", "[[entities/claude]]", "[[entities/kimi]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/ai-applications-expansion-survey-2026-11]]"]
---

# Notion AI

## 描述

笔记与协作工具 Notion 内置的 AI。2025-09-18 发布的 Notion 3.0 把它“从零重建为 Agents”：个人 Agent 能在工作区里做用户能做的任何事，例如把一个上线计划拆成任务并分派。之后推出可按计划或事件自动运行、可在团队共享的 Custom Agents，并接入 MCP 集成。Notion 不绑定单一模型：管理员可分别限定 Notion Agent 与 Custom Agents 可用的模型，2026 年的可选模型包括 [[entities/gpt|GPT]]（GPT-6.1-Sol、GPT-6 Luna）、[[entities/claude|Claude]]（Opus 5.5、Sonnet 5.5）和 [[entities/kimi|Kimi]] K3；2026-10 起还可用 ChatGPT 套餐额度或自带 AI。2026 下半年的迭代集中在 [[concepts/agent-skills|技能]]（团队技能库，可导出到 Claude Code、Codex、Cursor）、子 Agent 调用，以及 2026-10-19 重建的 Agent harness：Agent 自带计算机和浏览器，单个任务最长运行 24 小时。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 办公与企业
- **上游依赖**：[[entities/gpt|GPT]]、[[entities/claude|Claude]]、[[entities/kimi|Kimi]] 等第三方模型（用户可选，另有 Auto 路由）
- **竞争 / 替代**：[[entities/microsoft-365-copilot|Microsoft 365 Copilot]]、[[entities/claude-app|Claude 应用]]、[[entities/chatgpt|ChatGPT]]

## 时间线

- 2023-02 Notion AI 正式推出（训练知识，待核实）
- 2025-09-18 Notion 3.0：Notion AI 重建为 Agents
- 2026-02 前后 Custom Agents 推出（Notion 3.3）；2026-05-04 起消耗 Notion 积分（二手报道，日期说法不一）
- 2026-07-31 AI 会议纪要完成后可触发 Custom Agents
- 2026-08-14 模型选择器重做，按速度、智能、成本给出评分
- 2026-09-09 管理员可分别设定 Notion Agent 与 Custom Agents 的可用模型
- 2026-09-15 Notion 3.7：团队共享技能库，技能可导出到 Claude Code、Codex、Cursor；Agent SDK 公测
- 2026-10-13 Notion 3.8：Custom Agents 可调用其他 Custom Agents 作为子 Agent；Skills API；可用 ChatGPT 套餐额度
- 2026-10-19 Agent 重建：自带计算机和浏览器，任务最长 24 小时；Auto 模型路由、统一积分、自带 AI

## 相关实体

- [[entities/microsoft-365-copilot|Microsoft 365 Copilot]]
- [[entities/claude-code|Claude Code]]
- [[entities/cursor|Cursor]]
- [[entities/kimi|Kimi]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/computer-use|Computer Use]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Notion 3.0 is here! We’ve rebuilt Notion AI from the ground up as Agents." — [[sources/ai-applications-expansion-survey-2026-11|AI 应用扩容调研]]
- "Now, anything you can do in Notion, your Agent can do for you." — [[sources/ai-applications-expansion-survey-2026-11|AI 应用扩容调研]]
- "Custom Agents can now run right after an AI Meeting Note is finished." — [[sources/ai-applications-expansion-survey-2026-11|AI 应用扩容调研]]
