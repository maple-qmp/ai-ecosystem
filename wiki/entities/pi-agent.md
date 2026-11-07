---
title: Pi
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Pi", "Pi coding agent", "pi-coding-agent", "pi-mono", "pi.dev", "@earendil-works/pi-coding-agent"]
org: "Earendil"
released: "2025-11"
competitors: ["[[entities/opencode]]", "[[entities/claude-code]]", "[[entities/codex-cli]]", "[[entities/deepseek-harness]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/agent-frameworks-comparison-survey-2026-11]]"]
---

# Pi

## 描述

Mario Zechner（libGDX 作者）开发的极简、可扩展 [[concepts/agent-harness|Agent harness]] 与终端编码 Agent，MIT 协议，用 TypeScript 编写。核心主张是编码 Agent 只需要 read、write、edit、bash 四个工具和一千 token 以内的系统提示，其余一律由扩展实现：子 Agent、计划模式、权限弹窗、待办、后台 bash 都不内置。扩展是 TypeScript 模块，可注册工具、命令、快捷键、模型提供方和 TUI 组件，用户甚至可以让 Pi 修改自己再 `/reload`。仓库是分层的 monorepo：`pi-ai`（多厂商统一 LLM API）、`pi-agent-core`（Agent 循环）、`pi-tui`（差分渲染终端 UI）、`pi-coding-agent`（CLI），以及 1.0 时加入的 `pi-durable`。除交互模式外还有 print / JSON 模式、stdin/stdout 上的 RPC 协议和嵌入式 SDK，[[entities/openclaw|OpenClaw]] 就建立在 Pi 的组件上。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 编码 Agent / harness 内核
- **上游依赖**：Node.js；模型经 `pi-ai` 接入 30 多家提供方（Anthropic、OpenAI、Google、Azure、Bedrock、Mistral、[[entities/groq|Groq]]、[[entities/cerebras|Cerebras]]、xAI 等）
- **竞争 / 替代**：[[entities/opencode|OpenCode]]、[[entities/claude-code|Claude Code]]、[[entities/codex-cli|Codex CLI]]、[[entities/deepseek-harness|DeepSeek Harness]]
- **下游**：[[entities/openclaw|OpenClaw]]
- 横向比较见 [[concepts/agent-framework-selection|AI Agent 框架选型]]

## 关键特性

- **会话树**：会话以带 parent id 的 JSONL 保存，可用 `/tree` 跳到任意节点，`/fork` 分叉
- **上下文**：AGENTS.md、SYSTEM.md、自动压缩、按需加载的[[concepts/agent-skills|技能]]、动态上下文注入
- **运行中引导**：可向正在执行的 Agent 发送引导消息，或排队后续指令
- **包**：扩展、技能、提示模板、主题可打包，从 npm 或 git 安装
- **安全**：没有内置权限系统，以启动用户的权限运行，官方建议放进容器
- **MCP**：长期拒绝内置 [[concepts/model-context-protocol|MCP]]，0.99.0 起内置，并提供 Codemode（只让脚本输出进入模型上下文）

## 时间线

- 2025-08 仓库以 `badlogic/pi-mono` 创建
- 2025-11-12 npm 包 `@mariozechner/pi-coding-agent` 首发；2025-11-30 Zechner 发布设计文章
- 2025-12 Pi + Claude Opus 4.5 在 [[concepts/terminal-bench|Terminal-Bench]] 2.0 排第 7（二手资料）
- 2026-04-08 Earendil（Armin Ronacher 的公司）收购 Pi，Zechner 成为股东，同时发布云端 Agent 平台 Lefos（二手资料）
- 2026-04-30 v0.71.0 移除 Gemini CLI 与 Antigravity 登录
- 2026-05-07 npm 包迁到 `@earendil-works/pi-coding-agent`（0.74.0）
- 2026-09-29 v0.99.0 内置 MCP
- 2026-10-01 Pi 1.0，同时发布实验性的 Pi Durable
- 2026-11-02 v1.5.0；npm 新包周下载约 606 万，GitHub 约 12.1 万星

## 相关实体

- [[entities/openclaw|OpenClaw]]
- [[entities/opencode|OpenCode]]
- [[entities/claude-code|Claude Code]]
- [[entities/deepseek-harness|DeepSeek Harness]]
- [[entities/hermes-agent|Hermes Agent]]

## 相关概念

- [[concepts/agent-harness|Agent Harness]]
- [[concepts/agent-framework-selection|AI Agent 框架选型]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/context-compaction|上下文压缩]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Pi is a minimal, extensible agent harness that you can make your own." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
- "Pi is a minimal agent harness. Adapt Pi to your workflows, not the other way around." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
- "Extensions are TypeScript modules with access to tools, commands, keyboard shortcuts, events, and the full TUI." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
- "There does not appear to be a need for 10,000 tokens of system prompt" — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]（Zechner 设计文章，转引）
