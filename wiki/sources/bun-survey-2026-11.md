---
title: Bun 深度调研（2026-11）
type: source
tags: [notes]
source_note: "[[Bun深度调研-2026-11]]"
url: https://bun.com/
created: 2026-11-04
updated: 2026-11-04
sources:
  - "[[entities/bun]]"
  - "[[entities/oven]]"
  - "[[entities/jarred-sumner]]"
  - "[[entities/anthropic]]"
  - "[[entities/claude-code]]"
  - "[[entities/vercel]]"
  - "[[concepts/javascript-runtime]]"
  - "[[concepts/agent-driven-code-migration]]"
---

# Bun 深度调研（2026-11）

## Summary

梳理 JavaScript 运行时 [[entities/bun|Bun]]：一个二进制同时提供运行时、包管理器、测试运行器和打包器，引擎用 JavaScriptCore，定位是 Node.js 的直接替代。作者 [[entities/jarred-sumner|Jarred Sumner]] 创办 [[entities/oven|Oven]] 公司开发它，累计融资约 2600 万美元。2025-12 被 [[entities/anthropic|Anthropic]] 收购，原因是 [[entities/claude-code|Claude Code]] 以 Bun 单文件可执行分发。2026-07 Bun 用 Claude 在 11 天内从 Zig 重写为 Rust，2026-08 的 Bun 1.4 是第一个 Rust 版本。这是一次很有代表性的 [[concepts/agent-driven-code-migration|Agent 驱动的大规模代码迁移]]，也引来 Zig 作者的公开批评。

## Key Points

- **组件**：运行时、包管理器、测试运行器、打包器，同一个二进制；内置 HTTP / WebSocket 服务器、SQL（PostgreSQL / MySQL / SQLite）、Redis、S3、Shell、FFI、单文件可执行
- **版本**：v0.1（2022-07）→ 1.0（2023-09）→ 1.1 支持 Windows（2024-04）→ 1.2 文本锁文件、S3、Postgres（2025-01）→ 1.3 全栈开发服务器、统一 SQL、安全扫描（2025-10）→ 1.4 Rust 版、`Bun.WebView`（2026-08）→ v1.4.3 `bun check`、v1.4.4 `bun fmt`（2026-10）
- **融资**：种子轮 700 万美元（2022-08，Kleiner Perkins 领投）+ A 轮 1900 万美元（Khosla Ventures 领投，官方自述），收购前收入为 0
- **收购**（2025-12-02 / 03）：金额未披露；Bun 保持 MIT 开源、团队不变；同日 Anthropic 宣布 Claude Code 年化收入达 10 亿美元
- **Rust 重写**（2026-07-08 公布）：预发布 Claude Fable 5、约 50 个工作流、最多 64 个并行 Claude、11 天、6,502 次提交、合并 diff +100 万行、API 价约 16.5 万美元；测试套件六平台全过，19 个回归均已修复
- **规模**：月下载 720 万+（2025-10）→ 2200 万+（2026-07）；GitHub 96,535 星（2026-11-04）
- **争议**：Zig 作者 Andrew Kelley 认为问题在工程实践而非语言，并质疑重写的性能和测试说法

## Mentioned Pages

- [[entities/bun|Bun]]
- [[entities/oven|Oven]]
- [[entities/jarred-sumner|Jarred Sumner]]
- [[entities/anthropic|Anthropic]]
- [[entities/claude-code|Claude Code]]
- [[entities/claude|Claude]]
- [[entities/vercel|Vercel]]
- [[entities/nextjs|Next.js]]
- [[entities/mastra|Mastra]]
- [[concepts/javascript-runtime|JavaScript 运行时]]
- [[concepts/agent-driven-code-migration|Agent 驱动的代码迁移]]
- [[concepts/agent-harness|Agent Harness]]
