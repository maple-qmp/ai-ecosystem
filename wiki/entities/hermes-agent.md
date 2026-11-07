---
title: Hermes Agent
type: entity
tags: [project]
kind: app
layer: L4
aliases: ["Hermes Agent", "hermes-agent", "Nous Hermes Agent"]
org: "Nous Research"
released: "2026-02"
competitors: ["[[entities/openclaw]]", "[[entities/claude-code]]", "[[entities/opencode]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/agent-frameworks-comparison-survey-2026-11]]"]
---

# Hermes Agent

## 描述

开源模型实验室 Nous Research 发布的“自我改进”Agent，MIT 协议，用 Python 编写，2026-02-25 发布。卖点是内置学习循环：Agent 自己维护记忆并定期提醒自己整理，完成复杂任务后自动生成[[concepts/agent-skills|技能]]（兼容 agentskills.io 标准）并在使用中改进；用 SQLite + FTS5 全文检索和 LLM 摘要回忆过往会话，用 Honcho 做用户建模。形态上与 [[entities/openclaw|OpenClaw]] 相近：单个 gateway 进程接入 Telegram、Discord、Slack、WhatsApp、Signal 等 20 多个平台，内置自然语言描述的 cron 定时任务、并行子 Agent、60 多个工具和 [[concepts/model-context-protocol|MCP]]。执行环境有六种后端：本地、Docker、SSH、Modal、Daytona、Vercel Sandbox，因此常见用法是跑在便宜 VPS 或云沙箱上、用 Telegram 遥控。还提供批量轨迹生成与压缩，用于训练工具调用模型。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 常驻自主助理
- **上游依赖**：模型无关，支持 Nous Portal、OpenRouter、OpenAI 或任意端点（20 多家）
- **竞争 / 替代**：[[entities/openclaw|OpenClaw]]；编码场景也与 [[entities/claude-code|Claude Code]]、[[entities/opencode|OpenCode]] 重叠
- 横向比较见 [[concepts/agent-framework-selection|AI Agent 框架选型]]

## 关键特性

- **迁移**：`hermes import-agent openclaw` 可从 OpenClaw、Claude Code、Codex CLI、Cursor 导入设置、记忆和技能；API key 只在加 `--migrate-secrets` 时导入
- **安全**：命令审批与容器隔离，有单独的安全指南
- **学习循环的边界**：自我改进是生成可打开、可编辑的技能和记忆文件，不改写 Hermes 自身代码（第三方评论）
- **安装**：官方用安装脚本（Linux、macOS、WSL2、Windows PowerShell，另有 Android / Termux APT 源）

## 时间线

- 2026-02-25 在 GitHub 发布（Product Hunt 记为 02-26）
- 2026-03-23 v0.4.0，新增六个消息适配器
- 2026-04-03 [[entities/anthropic|Anthropic]] 阻止 OpenClaw 使用 Claude 订阅后，Nous 推广从 OpenClaw 迁移的命令，迁移流量激增（社区报告）
- 2026-04-08 v0.8.0；2026-04-11 约 5.7 万星（社区报告）
- 2026-08-03 v0.20.0 “Herald”（二手资料）
- 2026-11 GitHub 约 26.1 万星；npm 非官方桥接标注版本 0.23.0

## 相关实体

- [[entities/openclaw|OpenClaw]]
- [[entities/pi-agent|Pi]]
- [[entities/claude-code|Claude Code]]
- [[entities/codex-cli|Codex CLI]]

## 相关概念

- [[concepts/agent-memory|Agent 记忆]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/agent-framework-selection|AI Agent 框架选型]]
- [[concepts/synthetic-data|合成数据]]（轨迹生成）

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The self-improving AI agent built by Nous Research." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
- "Agent-curated memory with periodic nudges. Autonomous skill creation after complex tasks." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
- "Built-in cron scheduler with delivery to any platform." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
