---
title: JavaScript 运行时
type: concept
tags: [term]
layer: L4
aliases: ["JavaScript 运行时", "JavaScript runtime", "JS 运行时", "服务端 JavaScript 运行时"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/bun-survey-2026-11]]"]
---

# JavaScript 运行时

## 定义

在浏览器之外执行 JavaScript / TypeScript 的程序：一个 JS 引擎（V8 或 JavaScriptCore）加上文件、网络、进程等系统 API 和模块加载器。服务端、命令行工具和桌面应用都靠它运行。在 AI 生态里，TypeScript Agent 框架、MCP 服务器和终端编程 Agent（如 [[entities/claude-code|Claude Code]]）都跑在某个 JS 运行时上。

## 关键特征

- **引擎**：Node.js 和 Deno 用 V8；[[entities/bun|Bun]] 用 JavaScriptCore
- **Node.js 兼容**：npm 生态以 Node API 为准，新运行时都把兼容 Node 当作首要目标；Bun 用 Node.js 官方测试套件衡量兼容度
- **一体化程度**：Node.js 只提供运行时，包管理、测试、打包靠第三方；Bun 把运行时、包管理器、测试运行器、打包器做进一个二进制，后来又加入类型检查和格式化
- **TypeScript**：Bun、Deno 原生运行 TS；Node.js 后来支持去除类型后直接运行
- **单文件分发**：运行时可把应用和自身打包成一个可执行文件，CLI 工具借此免去用户装 Node 的步骤

## 应用

- 服务端与 API：HTTP、WebSocket 服务，[[entities/vercel|Vercel]] 等托管平台可选运行时
- 命令行工具与终端 Agent：[[entities/claude-code|Claude Code]] 以 Bun 单文件可执行分发
- TS Agent 框架与 MCP 服务器：[[entities/mastra|Mastra]]、[[entities/vercel-ai-sdk|AI SDK]] 等运行在 Node.js 或 Bun 上

## 主要运行时

| 运行时 | 引擎 | 实现语言 | 维护方 |
|---|---|---|---|
| Node.js | V8 | C++ | OpenJS 基金会 |
| Deno | V8 | Rust | Deno Land |
| Bun | JavaScriptCore | Rust（1.4 前为 Zig） | Anthropic（原 Oven） |

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 运行时与构建工具

## 相关概念

- [[concepts/agent-driven-code-migration|Agent 驱动的代码迁移]]
- [[concepts/ai-agent|AI Agent]]

## 相关实体

- [[entities/bun|Bun]]
- [[entities/claude-code|Claude Code]]
- [[entities/vercel|Vercel]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Bun is designed as a drop-in replacement for Node.js." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "Claude Code ships to millions of developers as a Bun executable." — [[sources/bun-survey-2026-11|Bun 深度调研]]
