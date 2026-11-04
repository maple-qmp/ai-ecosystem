---
title: Codex CLI
type: entity
tags: [product]
kind: app
layer: L4
aliases: ["Codex CLI", "OpenAI Codex CLI", "@openai/codex"]
org: "[[entities/openai]]"
released: "2025-04"
competitors: ["[[entities/claude-code]]", "[[entities/mastra-code]]", "[[entities/cursor]]", "[[entities/github-copilot]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/openai-developers-survey-2026-11]]"]
---

# Codex CLI

## 描述

[[entities/openai|OpenAI]] 开源的终端编码 Agent，在本机读写代码、执行命令，Apache-2.0 协议，仓库 `openai/codex`（约 13 万星）。最初用 TypeScript 写，后改为 Rust（`codex-rs`）。能力包括沙箱与审批策略、[[concepts/agents-md|AGENTS.md]] 项目指令、[[concepts/agent-skills|Agent Skills]]、[[concepts/model-context-protocol|MCP]] 客户端、子 Agent、Hooks、非交互模式 `codex exec`（用于脚本和 CI）。同一套内核还驱动 IDE 扩展和 ChatGPT 桌面端里的 Codex；嵌入自家产品用 [[entities/codex-app-server|Codex SDK / App Server]]。仓库接受 issue，但不接受外部代码贡献。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 编码 Agent
- **上游依赖**：—（默认调 OpenAI 模型，可换）
- **竞争 / 替代**：[[entities/claude-code|Claude Code]]、[[entities/mastra-code|Mastra Code]]、[[entities/cursor|Cursor]]、[[entities/github-copilot|GitHub Copilot]]、Gemini CLI

## 脱离 OpenAI 使用

可以脱离。登录方式本来就有 ChatGPT 账号和 API key 两种，不登录也能用本地模型。

- **本地开源模型**：`codex --oss` 连本机的 Ollama 或 LM Studio；用 `--local-provider` 单次指定，或在 `config.toml` 设 `oss_provider`。都没设时交互模式会询问，`codex exec` 直接报错。常见搭配是 [[entities/gpt-oss|gpt-oss]]
- **自定义提供商**：在 `[model_providers.<id>]` 下写 `base_url`、`env_key`、可选 HTTP 头；`<id>` 不能用保留名 `openai`、`ollama`、`lmstudio`、`amazon-bedrock`、`amazon-bedrock-runtime`、`gcp`。注意 `wire_api` 现在只支持 `responses`，所以后端必须提供 Responses 兼容接口；只有 Chat Completions 的服务要在前面加转换代理（社区旧指南里的 `wire_api = "chat"` 已不适用）
- **云厂商**：内置 Amazon Bedrock 和 GCP 提供商；Azure OpenAI 用 `openai_base_url` 改地址
- **关掉回传**：`analytics.enabled = false` 关闭内置的 Statsig 指标；`feedback.enabled = false` 关闭 `/feedback`；OTel 日志导出器设 `none` 时只在本地记录
- **会丢的能力**：Codex cloud 任务、云端代码审查、ChatGPT 账号同步的插件与技能都依赖 OpenAI；IDE 扩展闭源

## 相关组件的独立性

- **Codex Security CLI / TypeScript SDK**（`openai/codex-security`，Apache-2.0）：代码开源，但扫描需要 ChatGPT 登录或 OpenAI API key，按用量计费，可用 `--max-cost` 设上限，属于离不开 OpenAI 的一类
- **Codex GitHub Action**：在 GitHub 事件上触发 Codex，用 OpenAI API key
- **codex-universal**：Codex cloud 的基础 Docker 镜像，可以单独拉下来当本地开发环境用（仓库未声明协议）

## 时间线

- 2025-04 开源发布（TypeScript 版）
- 2025 年内改写为 Rust
- 2025-08 AGENTS.md 作为跨工具的项目指令格式推出
- 2025-12 加入 Agent Skills 支持；同月 OpenAI 把 AGENTS.md 捐给 Agentic AI Foundation
- 2026-07 开源 Codex Security CLI 与 TypeScript SDK
- 2026 年移除 `codex mcp-server`，统一到 App Server
- 2026-10-29 发布 rust-v0.166.0

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/codex-app-server|Codex App Server]]
- [[entities/gpt-oss|gpt-oss]]
- [[entities/claude-code|Claude Code]]
- [[entities/openai-agents-sdk|OpenAI Agents SDK]]

## 相关概念

- [[concepts/agent-harness|Agent Harness]]
- [[concepts/agents-md|AGENTS.md]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Codex can run against a local "open source" provider such as Ollama or LM Studio when you pass `--oss`." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
- "`responses` is the only supported value, and it is the default when omitted." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]（`wire_api`）
- "Setting this to `false` disables the built-in Statsig metrics exporter." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]（`analytics.enabled`）
