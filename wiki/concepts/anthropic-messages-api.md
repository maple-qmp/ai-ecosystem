---
title: Anthropic Messages API
type: concept
tags: [standard]
layer: L3
aliases: ["Anthropic Messages API", "Messages API", "Anthropic 兼容接口", "/v1/messages", "ANTHROPIC_BASE_URL"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/claude-independent-modules-survey-2026-11]]", "[[sources/inference-engines-survey-2026-11]]"]
---

# Anthropic Messages API

## 定义

[[entities/anthropic|Anthropic]] 的模型调用接口格式：客户端向 `/v1/messages` 发送 `system`、`messages`、`tools` 等字段，响应由类型化的内容块（`text`、`tool_use`、`thinking` 等）组成，流式输出是一串固定顺序的 SSE 事件（`message_start` → 各内容块 → `message_delta` → `message_stop`）。它本是 [[entities/claude|Claude]] 的私有 API，但因为 [[entities/claude-code|Claude Code]] 只说这一种“语言”，许多别家模型服务也实现了兼容端点，它就成了和 OpenAI Chat Completions 并列的事实标准。

## 关键特征

- **一个变量换后端**：Claude Code、[[entities/claude-agent-sdk|Agent SDK]] 和官方 SDK 都读 `ANTHROPIC_BASE_URL`；指向谁，就把谁当成 Claude API，客户端“看不出背后转发到了哪里”
- **云厂商的变体**：Amazon Bedrock（InvokeModel）和 Google Cloud（rawPredict）用自己的封装，Microsoft Foundry 和 Claude Platform on AWS 直接用 Messages 格式
- **必需与可选**：网关只需提供 `/v1/messages`；`/v1/messages/count_tokens` 可选，缺了 Claude Code 就按字符数估算上下文用量；`anthropic-beta`、`anthropic-version` 头要原样转发
- **对流式的硬要求**：不能缓冲整个响应，必须给出完整事件序列；长时间没有字节会触发空闲超时
- **兼容的代价**：Claude 专有的字段往往被忽略或不支持。Ollama 不支持 token 计数、`tool_choice`、提示缓存、Batches、Citations、PDF；DeepSeek 忽略 `cache_control`、`mcp_servers`、`citations`，不支持 `document`、`redacted_thinking`、MCP 工具块等

## 应用

- **企业 LLM 网关**：在 Claude Code 和模型提供商之间统一鉴权、计费、限流、审计；Anthropic 自己的 Claude apps gateway 内置在 `claude` 二进制里（`claude gateway --config gateway.yaml`），用企业 IdP 登录，数据面不连 Anthropic
- **用别家模型驱动 Claude Code**（官方不支持）：
  - [[entities/ollama|Ollama]]（v0.14.0 起，2026-01）：`ANTHROPIC_BASE_URL=http://localhost:11434`，令牌随便填；或 `ollama launch claude` 一键配置；本地模型需要足够大的上下文
  - DeepSeek：`https://api.deepseek.com/anthropic`
  - 智谱 GLM：`https://api.z.ai/api/anthropic`（国内 `open.bigmodel.cn/api/anthropic`）
  - [[entities/lm-studio|LM Studio]]（0.4.x 起，`http://localhost:1234`）、[[entities/vllm|vLLM]]（服务端内置 Anthropic Messages API）
  - Kimi、MiniMax、Qwen、OpenRouter 等也有兼容端点（地址以各家文档为准）
  - 一般还要用 `ANTHROPIC_MODEL` 等变量把 Opus / Sonnet / Haiku 档位映射到对方的模型名
- **仍会访问 Anthropic 的地方**：WebFetch 的域名安全检查把主机名发到 `api.anthropic.com`，不受“关闭非必要流量”影响，需用 `skipWebFetchPreflight: true` 关掉；fast mode 可用性检查也直连 `api.anthropic.com`

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 推理服务接口
- **竞争 / 替代**：OpenAI Chat Completions 与 Responses API（[[entities/codex-cli|Codex CLI]] 只支持 Responses）
- **互补**：[[concepts/model-context-protocol|MCP]] 统一的是“工具从哪来”，Messages API 统一的是“怎么调模型”

## 相关概念

- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/harmony-response-format|harmony 响应格式]]

## 相关实体

- [[entities/claude-code|Claude Code]]
- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[entities/claude|Claude]]
- [[entities/deepseek|DeepSeek]]
- [[entities/qwen|Qwen]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/ollama|Ollama]]
- [[entities/lm-studio|LM Studio]]
- [[entities/vllm|vLLM]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Anthropic Messages format: the developer sets `ANTHROPIC_BASE_URL` to your gateway. Claude Code treats the gateway as the Claude API and can't tell which upstream you forward to." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
- "Anthropic doesn't endorse, maintain, or audit third-party gateway products, and doesn't support routing Claude Code to non-Claude models through any gateway." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
- "Token-counting endpoints are the only optional ones: when they're absent, Claude Code falls back to a character-based estimate of context usage." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
