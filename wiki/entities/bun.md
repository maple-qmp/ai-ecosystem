---
title: Bun
type: entity
tags: [project]
kind: infra
layer: L4
aliases: ["Bun", "Bun 运行时", "oven-sh/bun"]
org: "[[entities/anthropic]]"
released: "2022-07"
competitors: []
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/bun-survey-2026-11]]"]
---

# Bun

## 描述

一体化的 JavaScript / TypeScript 工具链：一个二进制同时是运行时、包管理器、测试运行器和打包器，分别对标 Node.js、npm / pnpm / Yarn、Jest / Vitest、esbuild / Vite。引擎用 Apple 的 JavaScriptCore，不用 V8；原生运行 TypeScript 和 JSX，设计目标是直接替代 Node.js。由 [[entities/jarred-sumner|Jarred Sumner]] 创办的 [[entities/oven|Oven]] 公司开发，2025-12 被 [[entities/anthropic|Anthropic]] 收购，仍以 MIT 协议开源。[[entities/claude-code|Claude Code]] 以 Bun 单文件可执行分发，所以 Bun 成了 Anthropic 编程产品的底层基础设施。2026-07 用 Claude 从 Zig 整体重写为 Rust，Bun 1.4 起是 Rust 版本（见 [[concepts/agent-driven-code-migration|Agent 驱动的代码迁移]]）。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 运行时与构建工具（参见 [[concepts/javascript-runtime|JavaScript 运行时]]）
- **上游依赖**：JavaScriptCore（WebKit）；实现语言 Rust（1.4 起，此前为 Zig）
- **下游**：[[entities/claude-code|Claude Code]]（以 Bun 可执行分发）；[[entities/vercel|Vercel]] 平台可选 Bun 运行时；[[entities/mastra|Mastra]] 等 TS Agent 框架可在 Bun 上运行
- **竞争 / 替代**：Node.js、Deno；包管理 npm / pnpm / Yarn；测试 Jest / Vitest；打包 esbuild / Vite / webpack

## 主要组件

- **运行时**：`Bun.serve()`（HTTP / WebSocket，1.4 实验性 HTTP/2、HTTP/3）、`Bun.SQL`（PostgreSQL / MySQL / SQLite）、Redis 客户端、`Bun.s3`、`bun:sqlite`、`bun:ffi`、Bun Shell、`Bun.WebView`（无头浏览器）、`Bun.Image`、`Bun.markdown`、`Bun.cron()`
- **包管理器**：`bun install`，文本锁文件 `bun.lock`，workspace 隔离安装与全局虚拟存储，依赖 catalog，最短发布时长，Security Scanner API，`bun audit fix`
- **测试运行器**：`bun test`，兼容 Jest API，支持并行、分片、只跑改动
- **打包与开发**：`bun build`（含 `--compile` 单文件可执行、交叉编译、React Compiler），全栈开发服务器与热更新
- **代码质量**：`bun check`（移植自 typescript-go 的类型检查器）、`bun fmt`（兼容 Prettier 的格式化器）

## 时间线

- 2021-04 GitHub 仓库创建；最初把 esbuild 的转译器从 Go 逐行移植到 Zig
- 2022-07-05 v0.1 公开测试，首周约 2 万星
- 2022-08 [[entities/oven|Oven]] 获 700 万美元种子轮
- 2023-09-08 Bun 1.0
- 2024-04-01 Bun 1.1：支持 Windows，跨平台 Bun Shell
- 2025-01-22 Bun 1.2：文本锁文件 `bun.lock` 成为默认，加入 `Bun.s3` 与 Postgres 客户端
- 2025-10-10 Bun 1.3：全栈开发服务器，`Bun.SQL` 统一 MySQL / PostgreSQL / SQLite，Redis 客户端，Security Scanner API
- 2025-10-28 [[entities/vercel|Vercel]] 以公开测试支持 Bun 运行时
- 2025-12-02 宣布加入 [[entities/anthropic|Anthropic]]（金额未披露）；当时月下载 720 万+、8.2 万+ 星
- 2026-07-08 公布用 Claude 在 11 天内完成 Zig → Rust 重写；CLI 月下载 2200 万+
- 2026-07-09 Zig 作者 Andrew Kelley 发文批评这次重写
- 2026-08-20 Bun 1.4：第一个 Rust 版本，`Bun.WebView`，Node.js v26.3.0 测试新增通过 1,517 项，Windows ARM64，全局虚拟存储
- 2026-10-10 v1.4.3：`bun check` 类型检查器
- 2026-10-22 v1.4.4：`bun fmt` 格式化器
- 2026-11 GitHub 约 9.65 万星、5,257 fork

## 相关实体

- [[entities/oven|Oven]]
- [[entities/jarred-sumner|Jarred Sumner]]
- [[entities/anthropic|Anthropic]]
- [[entities/claude-code|Claude Code]]
- [[entities/claude|Claude]]
- [[entities/vercel|Vercel]]
- [[entities/nextjs|Next.js]]

## 相关概念

- [[concepts/javascript-runtime|JavaScript 运行时]]
- [[concepts/agent-driven-code-migration|Agent 驱动的代码迁移]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Runtime, package manager, test runner and bundler in a single binary." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "Bun is designed as a drop-in replacement for Node.js." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "If Bun breaks, Claude Code breaks." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "Bun stays open-source & MIT-licensed" — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "And it rewrites Bun from Zig to Rust." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "`bun check` is an incredibly fast TypeScript type checker that passes 100% of TypeScript 7.0.2's conformance test suite." — [[sources/bun-survey-2026-11|Bun 深度调研]]
