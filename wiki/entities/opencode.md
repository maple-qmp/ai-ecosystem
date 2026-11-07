---
title: OpenCode
type: entity
tags: [product]
kind: app
layer: L4
aliases: ["OpenCode", "opencode", "opencode-ai", "anomalyco/opencode", "sst/opencode"]
org: "Anomaly"
released: "2025-06"
competitors: ["[[entities/claude-code]]", "[[entities/codex-cli]]", "[[entities/pi-agent]]", "[[entities/deepseek-harness]]", "[[entities/cursor]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/agent-frameworks-comparison-survey-2026-11]]"]
---

# OpenCode

## 描述

开源、模型无关的 AI 编码 Agent，MIT 协议，由 SST 团队（Jay V、Frank Wang、Dax Raad、Adam Elmore）成立的公司 Anomaly 开发，仓库从 `sst/opencode` 迁到 `anomalyco/opencode`。提供终端、桌面（macOS、Windows、Linux）和 Web 三种界面。架构是客户端 / 服务端：运行 `opencode` 会同时启动 TUI 和 HTTP 服务器，TUI 只是客户端；`opencode serve` 可单独起无界面服务器，暴露 OpenAPI 3.1 接口，官方 SDK（`@opencode-ai/sdk`）和 IDE 插件都基于它，因此可以在本地跑 Agent、远程或从手机控制。内置 build（默认，完全权限）、plan（只读规划）两个主 Agent 和 general、explore 子 Agent，可用 Markdown 或 JSONC 定义自定义 Agent；权限是有序的 allow / ask / deny 规则。通过 Models.dev 支持 75 家以上提供方，也能接本地模型，是开源编码 Agent 中被当作 [[entities/claude-code|Claude Code]] 主要替代品的一个。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 编码 Agent
- **上游依赖**：Node / Bun 运行时；模型无关，经 [[entities/ollama|Ollama]] 等可接本地模型
- **竞争 / 替代**：[[entities/claude-code|Claude Code]]、[[entities/codex-cli|Codex CLI]]、[[entities/pi-agent|Pi]]、[[entities/deepseek-harness|DeepSeek Harness]]、[[entities/cursor|Cursor]]
- 横向比较见 [[concepts/agent-framework-selection|AI Agent 框架选型]]

## 商业化

- 免费 / 自带 key：用自己的 API key 或本地模型
- OpenCode Go：每月 10 美元的托管开放权重模型订阅
- Zen：按 token 付费的托管模型；另有企业版团队工作区
- 二手资料称 Anomaly 在发布后数月内完成未披露金额的融资，Zen 年化收入数百万美元，月活开发者 750 万（未核实）

## 时间线

- 2025-05-31 npm 包 `opencode-ai` 首发；2025-06 正式发布
- 2025-10-31 1.0.0
- 2026-01 加入 ChatGPT Plus / Pro 的 Codex OAuth 登录
- 2026-01-09 [[entities/anthropic|Anthropic]] 在服务端阻止第三方工具使用 Claude 订阅 OAuth，OpenCode 同日移除 Claude Pro / Max 支持；2026-02-19 Anthropic 条款明确禁止，OpenCode 删除全部 Claude OAuth 代码（二手资料）
- 2026-06-10 v1.17.3：桌面版多服务器、会话草稿
- 2026-10-11 1.19.0；2026-10-28 1.19.5
- 2026-11 GitHub 约 22.5 万星；CLI 周下载约 360 万，SDK 周下载约 3657 万

## 相关实体

- [[entities/claude-code|Claude Code]]
- [[entities/pi-agent|Pi]]
- [[entities/deepseek-harness|DeepSeek Harness]]
- [[entities/ollama|Ollama]]
- [[entities/unsloth|Unsloth]]（`unsloth start` 可把 OpenCode 接到本地模型）

## 相关概念

- [[concepts/agent-harness|Agent Harness]]
- [[concepts/agent-framework-selection|AI Agent 框架选型]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/agents-md|AGENTS.md]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The open source AI coding agent." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
- "The `opencode serve` command runs a headless HTTP server that exposes an OpenAPI endpoint that an opencode client can use." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
- "When you run `opencode` it starts a TUI and a server. Where the TUI is the client that talks to the server." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
