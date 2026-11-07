---
title: AI Agent 框架横向对比调研（2026-11）
type: source
tags: [notes]
source_note: "[[AI-Agent框架横向对比调研-2026-11]]"
url: https://github.com/earendil-works/pi
created: 2026-11-07
updated: 2026-11-07
sources:
  - "[[concepts/agent-framework-selection]]"
  - "[[entities/pi-agent]]"
  - "[[entities/opencode]]"
  - "[[entities/openclaw]]"
  - "[[entities/hermes-agent]]"
  - "[[entities/deepseek-harness]]"
  - "[[entities/claude-agent-sdk]]"
  - "[[entities/openai-agents-sdk]]"
  - "[[entities/deep-agents]]"
---

# AI Agent 框架横向对比调研（2026-11）

## Summary

横向比较 8 个 Agent 框架 / harness：[[entities/claude-agent-sdk|Claude Agent SDK]]、[[entities/openai-agents-sdk|OpenAI Agents SDK]]、[[entities/deep-agents|Deep Agents]]、[[entities/pi-agent|Pi]]、[[entities/opencode|OpenCode]]、[[entities/openclaw|OpenClaw]]、[[entities/hermes-agent|Hermes Agent]]、[[entities/deepseek-harness|DeepSeek Harness]]，结论与选型建议见 [[concepts/agent-framework-selection|AI Agent 框架选型]]。可分三类：嵌入式 SDK（前三者）、可编程编码 Agent（Pi、OpenCode、DeepSeek Harness）、常驻自主助理（OpenClaw、Hermes Agent）。资料来自官方仓库 README、官方文档与官网、npm / PyPI 元数据（2026-11-07 读取）、Wikipedia 和第三方评测；本会话 GitHub API 不可用，星数取自网页。

## Key Points

- **下载量**（2026-10-31 至 11-06 一周）：Claude Agent SDK npm 1848 万 + PyPI 870 万，遥遥领先；OpenCode SDK 3657 万（被大量工具当集成层）；Pi 新包 606 万；OpenAI Agents SDK PyPI 483 万 + npm 245 万；OpenClaw 260 万；Deep Agents PyPI 203 万 + npm 67 万；DeepSeek Harness 84 万
- **星数**（网页）：OpenClaw 约 39.4 万、DeepSeek Harness 约 27.6 万、Hermes Agent 约 26.1 万、OpenCode 约 22.5 万、Pi 约 12.1 万
- **Pi**：四个核心工具 + 扩展的极简 harness；2026-04 归 Earendil，npm 包 2026-05 迁到 `@earendil-works`；0.99.0（2026-09-29）加入 MCP，1.0 于 2026-10-01
- **OpenCode**：Anomaly（原 SST 团队）开发，客户端 / 服务端架构，OpenAPI 3.1 + SDK；2026-01 被 Anthropic 切断 Claude 订阅登录
- **OpenClaw**：Peter Steinberger 2025-11 首发，三次改名，2026-02 移交 OpenClaw Foundation；Gateway + 20 多个聊天渠道；安全隐患多次被曝；2.0 于 2026-08-30
- **Hermes Agent**：Nous Research 2026-02-25 发布，Python，学习循环自动生成和改进技能，六种执行后端，可从 OpenClaw 一键迁移
- **DeepSeek Harness**：DeepSeek 2026-08-13 开源，Cordis 插件框架、一切皆插件，开发者预览；沙箱只限制写不限制读；能委派 Claude Code、Codex
- **其他发现**：`deepagents-cli` 已弃用，改为 Managed Deep Agents 的 `mda`；PyPI 上同名 `deepseek-harness` 是第三方项目

## Mentioned Pages

- [[concepts/agent-framework-selection|AI Agent 框架选型]]
- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[entities/openai-agents-sdk|OpenAI Agents SDK]]
- [[entities/deep-agents|Deep Agents]]
- [[entities/pi-agent|Pi]]
- [[entities/opencode|OpenCode]]
- [[entities/openclaw|OpenClaw]]
- [[entities/hermes-agent|Hermes Agent]]
- [[entities/deepseek-harness|DeepSeek Harness]]
- [[entities/deepseek|DeepSeek]]
- [[entities/anthropic|Anthropic]]
- [[entities/claude-code|Claude Code]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/langgraph|LangGraph]]
- [[entities/ollama|Ollama]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
