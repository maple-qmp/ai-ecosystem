---
title: Codex App Server
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Codex App Server", "codex app-server", "Codex SDK", "@openai/codex-sdk"]
org: "[[entities/openai]]"
released: "2025"
competitors: ["[[entities/claude-agent-sdk]]"]
depends_on: ["[[entities/codex-cli]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/openai-developers-survey-2026-11]]"]
---

# Codex App Server

## 描述

把 [[entities/codex-cli|Codex CLI]] 的 Agent 内核嵌入到其他程序的接口层，源码在 `openai/codex` 仓库的 `codex-rs/app-server`，Apache-2.0。Codex 的 VS Code 扩展就是通过它驱动的。协议和 [[concepts/model-context-protocol|MCP]] 一样是双向 JSON-RPC 2.0（线上省略 `"jsonrpc":"2.0"` 头），负责认证、会话历史、审批和流式事件。在它之上有两个 SDK：TypeScript 的 `@openai/codex-sdk`（Node 18+，启动、继续、恢复本地线程，适合 CI）和 Python SDK（3.10+，通过 JSON-RPC 控制本地 app-server，发布包自带固定版本的 CLI）。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 嵌入接口
- **上游依赖**：[[entities/codex-cli|Codex CLI]]
- **竞争 / 替代**：[[entities/claude-agent-sdk|Claude Agent SDK]]（[[entities/claude-code|Claude Code]] 的嵌入方式）

## 脱离 OpenAI 使用

能否脱离完全取决于底下的 Codex CLI 配置：SDK 和 App Server 只是控制本地进程，CLI 配好 `--oss` 或自定义提供商，它们就不连 OpenAI。SDK 可以用 `config` / `configOverrides` 传入提供商设置，不改用户的配置文件。

## 传输与部署

- **stdio**（默认）：换行分隔的 JSON（JSONL）
- **WebSocket**：`--listen ws://IP:PORT`，官方标为实验性、不受支持；同一端口提供 `/readyz`、`/healthz` 健康检查，带 `Origin` 头的请求一律 403
- **Unix socket**：`--listen unix://` 或指定路径
- **远程终端**：`codex app-server --listen ws://127.0.0.1:4500` 加 `codex --remote ws://…`，在另一台机器上连终端界面；非本地连接要配 bearer token 和 TLS
- **Code Mode 远程主机**：`--code-mode-host` 指向 HTTP/2 gRPC 端点，多个线程共享一个远程执行主机

## 时间线

- 2025 年作为 IDE 扩展的后端推出
- 2026 年 `codex mcp-server` 命令和独立的 `codex-mcp-server` 被移除，原有集成迁到 App Server

## 相关实体

- [[entities/codex-cli|Codex CLI]]
- [[entities/openai|OpenAI]]
- [[entities/openai-agents-sdk|OpenAI Agents SDK]]

## 相关概念

- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/agent-harness|Agent Harness]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Codex app-server is the interface Codex uses to power rich clients (for example, the Codex VS Code extension)." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
- "The Python SDK controls the local Codex app-server over JSON-RPC. It requires Python 3.10 or later." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
