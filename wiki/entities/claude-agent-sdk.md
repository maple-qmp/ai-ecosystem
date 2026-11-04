---
title: Claude Agent SDK
type: entity
tags: [product]
kind: framework
layer: L4
aliases: ["Claude Agent SDK", "Claude Code SDK", "claude-agent-sdk", "@anthropic-ai/claude-agent-sdk"]
org: "[[entities/anthropic]]"
released: "2025-06"
competitors: ["[[entities/openai-agents-sdk]]", "[[entities/codex-app-server]]", "[[entities/langgraph]]", "[[entities/mastra]]"]
depends_on: ["[[entities/claude-code]]", "[[entities/claude]]", "[[entities/bun]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/claude-independent-modules-survey-2026-11]]"]
---

# Claude Agent SDK

## 描述

[[entities/anthropic|Anthropic]] 把 [[entities/claude-code|Claude Code]] 的 Agent 循环做成库，供开发者嵌进自己的程序，原名 Claude Code SDK，有 Python（`claude-agent-sdk`）和 TypeScript（`@anthropic-ai/claude-agent-sdk`）两个版本。它不是从零实现 Agent，而是**启动一个 Claude Code CLI 子进程**，通过流式 JSON 与之通信：Python 包自带一份 CLI，也可以用 `cli_path` 指定别的版本。所以 Claude Code 有的能力它都有：文件读写和命令执行工具、会话（continue / resume / fork，可存到外部存储）、子 Agent、[[concepts/agent-skills|技能]]、插件、权限与 Hooks、文件检查点、结构化输出、进程内 [[concepts/model-context-protocol|MCP]] 自定义工具、OpenTelemetry。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · Agent 框架
- **上游依赖**：[[entities/claude-code|Claude Code]] CLI（运行时为 [[entities/bun|Bun]]）、[[entities/claude|Claude]] 模型
- **竞争 / 替代**：[[entities/openai-agents-sdk|OpenAI Agents SDK]]、[[entities/codex-app-server|Codex SDK / App Server]]（同样是“把编码 Agent 内核当库用”）、[[entities/langgraph|LangGraph]]、[[entities/mastra|Mastra]]

## 脱离 Anthropic 使用

部分可以。分两层看：

- **不经 Anthropic 服务、仍用 Claude**：和 Claude Code 一样，设 `CLAUDE_CODE_USE_BEDROCK`、`CLAUDE_CODE_USE_VERTEX`、`CLAUDE_CODE_USE_FOUNDRY` 等变量走云厂商，或指向企业自己的 LLM 网关。这是官方支持的路径
- **换非 Claude 模型**：把 `ANTHROPIC_BASE_URL` 指向提供 [[concepts/anthropic-messages-api|Anthropic Messages API]] 兼容端点的服务（Ollama、DeepSeek 等）技术上可行，但官方不支持，Claude 专有的特性（提示缓存、服务端工具等）会失效
- **协议限制**：TypeScript 版受 Anthropic 商业服务条款约束，“包括用它给你自己的客户提供产品和服务”；Python 版仓库是 MIT，但自带的 CLI 仍是专有软件
- **登录限制**：未经批准，第三方产品不得提供 claude.ai 登录或使用订阅额度，只能用 API key 等方式；产品也不能看起来像 Claude Code 或 Anthropic 的产品

和 [[entities/openai-agents-sdk|OpenAI Agents SDK]] 比：后者本身就是模型无关的开源框架，换模型只是换一个 provider；Agent SDK 换模型要绕过官方支持范围。

## 时间线

- 2025-06 Python 版仓库创建（当时叫 Claude Code SDK）
- 2025-09 改名 Claude Agent SDK，TypeScript 版独立成仓库
- 2026-11-04 npm 版本 0.3.318，与 Claude Code 2.1.318 同步发布；PyPI 版本 0.2.178

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/claude-code|Claude Code]]
- [[entities/claude|Claude]]
- [[entities/sandbox-runtime|Sandbox Runtime（srt）]]
- [[entities/openai-agents-sdk|OpenAI Agents SDK]]
- [[entities/codex-app-server|Codex App Server]]

## 相关概念

- [[concepts/agent-harness|Agent Harness]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The Claude Code CLI is automatically bundled with the package - no separate installation required!" — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]（Python README）
- "Unless previously approved, Anthropic does not allow third party developers to offer claude.ai login or rate limits for their products, including agents built on the Claude Agent SDK." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
- "Your product should maintain its own branding and not appear to be Claude Code or any Anthropic product." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
