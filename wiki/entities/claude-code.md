---
title: Claude Code
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["Claude Code"]
org: "[[entities/anthropic|Anthropic]]"
released: "2025-02"
competitors: ["[[entities/cursor]]", "[[entities/github-copilot]]", "[[entities/codex-cli]]", "[[entities/mastra-code]]", "[[entities/devin]]", "[[entities/windsurf]]"]
depends_on: ["[[entities/claude]]", "[[entities/bun]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/bun-survey-2026-11]]", "[[sources/claude-independent-modules-survey-2026-11]]", "[[sources/ai-applications-survey-2026-11]]"]
---

# Claude Code

## 描述

[[entities/anthropic|Anthropic]] 的 Agent 式编程工具，可在终端、IDE、桌面应用与浏览器中读代码库、改文件、运行命令，并通过 [[concepts/model-context-protocol|MCP]] 接入外部工具。2025-02 随 Claude 3.7 Sonnet 以研究预览发布，2025-05 随 Claude 4 正式发布，Claude 的 Pro 及以上订阅都包含它（见 [[entities/claude-app|Claude 应用]]）。CLI 以 [[entities/bun|Bun]] 单文件可执行分发，Anthropic 因此在 2025-12 收购了 Bun。它是专有软件：GitHub 仓库 `anthropics/claude-code` 只放文档、插件示例和 issue，LICENSE 写明“All rights reserved”，使用受 Anthropic 商业条款约束。沙箱功能的底层 [[entities/sandbox-runtime|Sandbox Runtime]] 单独开源；把 Agent 循环当库用的是 [[entities/claude-agent-sdk|Claude Agent SDK]]。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 编程 Agent
- **上游依赖**：[[entities/claude|Claude]]、[[entities/bun|Bun]]（运行时）
- **竞争 / 替代**：[[entities/cursor|Cursor]]、[[entities/github-copilot|GitHub Copilot]]、[[entities/codex-cli|Codex CLI]]、[[entities/mastra-code|Mastra Code]]、[[entities/devin|Devin]]、[[entities/windsurf|Windsurf（Devin Desktop）]]

## 脱离 Anthropic 使用

官方只支持 Claude 模型，但 Claude 可以不经 Anthropic 自家服务获取。分三档：

- **不经 Anthropic、仍用 Claude（官方支持）**：设 `CLAUDE_CODE_USE_BEDROCK=1`、`CLAUDE_CODE_USE_VERTEX=1`、`CLAUDE_CODE_USE_FOUNDRY=1` 或 `CLAUDE_CODE_USE_ANTHROPIC_AWS=1`，分别走 Amazon Bedrock、Google Cloud's Agent Platform（原 Vertex AI）、Microsoft Foundry、Claude Platform on AWS；企业可在中间加 LLM 网关，或用内置在 `claude` 二进制里的 Claude apps gateway（`claude gateway --config gateway.yaml`，企业 IdP 登录，数据面不连 Anthropic）。托管设置 `allowedProviders` 可以锁定只用某个提供商
- **换非 Claude 模型（官方不支持）**：Claude Code 只说 [[concepts/anthropic-messages-api|Anthropic Messages API]]，把 `ANTHROPIC_BASE_URL` 指向兼容端点即可，常见是 Ollama（本地，`ollama launch claude`）、[[entities/deepseek|DeepSeek]]、[[entities/glm|智谱 GLM]]、[[entities/kimi|Kimi]]、[[entities/qwen|Qwen]]、OpenRouter。会失去提示缓存、精确 token 计数、引用、PDF、服务端工具等 Claude 专有特性，效果取决于对方模型的工具调用能力和上下文长度
- **关掉回传**：`DISABLE_TELEMETRY=1`（指标）、`DISABLE_ERROR_REPORTING=1`（错误报告）、`CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC=1`（一次关闭非必要流量）、`CLAUDE_CODE_DISABLE_FEEDBACK_SURVEY=1`（会话调查）。走云厂商时指标、错误报告、`/feedback` 默认就是关的，`/feedback` 改写到本地 `~/.claude/feedback-bundles/`
- **仍会连 Anthropic 的地方**：WebFetch 的域名安全检查不论提供商都把主机名发到 `api.anthropic.com`，不受上面的开关影响，要用 `skipWebFetchPreflight: true` 关；fast mode 可用性检查也直连
- **离不开 Anthropic 的部分**：claude.ai 订阅登录、网页版云端会话（自托管 runner 只是把执行放到自己机器上，队列、会话流、推理仍在 Anthropic）、服务端托管设置、Remote Control

和 [[entities/codex-cli|Codex CLI]] 的区别：Codex CLI 是 Apache-2.0 开源，官方支持 `--oss` 接本地模型；Claude Code 闭源，换模型只能靠兼容端点。

## 时间线

- 2025-02-24 随 Claude 3.7 Sonnet 以有限研究预览发布，定位命令行 Agent 式编程工具；npm 包同日创建
- 2025-05-22 随 Claude 4 正式发布：支持通过 GitHub Actions 跑后台任务，原生集成 VS Code 与 JetBrains；npm 1.0.0 同日发布
- 2025-08-20 进入 Team / Enterprise 商业套餐
- 2025-09-29 Anthropic 发布「Enabling Claude Code to work more autonomously」；npm 2.0.0 同日发布
- 2025-10 开源 [[entities/sandbox-runtime|Sandbox Runtime]]，随沙箱功能发布
- 2025-11 年化收入达 10 亿美元（公开发布约 6 个月）
- 2025-12 [[entities/anthropic|Anthropic]] 收购 [[entities/bun|Bun]]；Bun 此前已参与 Claude Code 原生安装器
- 2026-01 Ollama v0.14.0 提供 Anthropic Messages 兼容接口，可用本地模型驱动 Claude Code
- 2026-01-12 Cowork 研究预览，把 Claude Code 的 Agent 能力带进 Claude 桌面应用（二手报道）
- 2026-03-31 npm 包 2.1.88 误带 source map，完整 TypeScript 源码外泄；Anthropic 撤下该版本，称是打包失误、无客户数据泄露；代码协议不变
- 2026-05-06 Pro、Max、Team 与按席位 Enterprise 的五小时限额翻倍，Pro / Max 取消高峰时段限额下调
- 2026-06-23 Claude Tag 发布，Anthropic 称它是「Claude Code 演进的开始」，产品团队 65% 的代码由内部版 Claude Tag 生成
- 2026-07 Bun 用 Claude Code 跑约 50 个工作流完成 Zig → Rust 重写，见 [[concepts/agent-driven-code-migration|Agent 驱动的代码迁移]]
- 2026-08 Bun 1.4 发布，Claude Code 的 p99 CPU 从 24% 降到 10%（Bun 自报）
- 2026-11-04 发布 2.1.318（npm `latest`），`stable` 标签为 2.1.311；npm 上累计 557 个版本

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/claude|Claude]]
- [[entities/bun|Bun]]
- [[entities/cursor|Cursor]]
- [[entities/github-copilot|GitHub Copilot]]
- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[entities/sandbox-runtime|Sandbox Runtime（srt）]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/claude-app|Claude 应用]]
- [[entities/devin|Devin]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/agent-driven-code-migration|Agent 驱动的代码迁移]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/mcp-bundles|MCP Bundles（MCPB）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Claude Code ships as a Bun executable to millions of users." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "If Bun breaks, Claude Code breaks." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "By default, error reporting, telemetry, and bug reporting are disabled when using Amazon Bedrock, Google Cloud's Agent Platform, Microsoft Foundry, or Claude Platform on AWS." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
- "This check runs regardless of which model provider you use and is not affected by `CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC`." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]（WebFetch 域名检查）
- "Claude Code is available as a limited research preview, and enables developers to delegate substantial engineering tasks to Claude directly from their terminal." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Anthropic 2025-02-24）
- "Claude Code is an agentic coding tool that reads your codebase, edits files, runs commands, and integrates with your development tools. Available in your terminal, IDE, desktop app, and browser." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Claude Code 文档）
- "We see Claude Tag as the beginning of an evolution of Claude Code: it makes the model even more proactive, and it works better with a full team." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]
