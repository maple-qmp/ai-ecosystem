---
title: OpenAI Developers 可独立使用模块调研（2026-11）
type: source
tags: [notes]
source_note: "[[OpenAI-Developers独立可用模块调研-2026-11]]"
url: https://developers.openai.com/
created: 2026-11-04
updated: 2026-11-04
sources:
  - "[[entities/openai]]"
  - "[[entities/gpt]]"
  - "[[entities/gpt-oss]]"
  - "[[entities/openai-agents-sdk]]"
  - "[[entities/codex-cli]]"
  - "[[entities/codex-app-server]]"
  - "[[entities/chatkit]]"
  - "[[entities/promptfoo]]"
  - "[[entities/tiktoken]]"
  - "[[concepts/harmony-response-format]]"
  - "[[concepts/agents-md]]"
  - "[[concepts/agent-skills]]"
  - "[[concepts/agentic-commerce-protocol]]"
  - "[[concepts/mcp-extensions]]"
---

# OpenAI Developers 可独立使用模块调研（2026-11）

## Summary

逐个检查 [[entities/openai|OpenAI]] 开发者门户 developers.openai.com 下的产品、SDK、开源项目和规范，判断哪些能脱离 OpenAI 的服务（API、ChatGPT 账号、OpenAI 云端）使用。门户大部分内容是 OpenAI API 和 ChatGPT 平台的接入文档，离不开 OpenAI。能独立使用的分三类：

- **开放权重与本地工具**：[[entities/gpt-oss|gpt-oss]]（含 gpt-oss-safeguard）、[[concepts/harmony-response-format|harmony 格式]]、[[entities/tiktoken|tiktoken]]
- **开放标准**：[[concepts/agents-md|AGENTS.md]]、[[concepts/agent-skills|Agent Skills]]、MCP Apps（见 [[concepts/mcp-extensions|MCP 扩展]]）、[[concepts/agentic-commerce-protocol|Agentic Commerce Protocol]]
- **默认连 OpenAI、能改配置脱离的开源框架**：[[entities/openai-agents-sdk|Agents SDK]]、[[entities/codex-cli|Codex CLI]] 及其嵌入层 [[entities/codex-app-server|Codex SDK / App Server]]、[[entities/chatkit|ChatKit]]（部分），以及被 OpenAI 收购但保持 MIT 的 [[entities/promptfoo|Promptfoo]]

和 Vercel 的情况（见 [[sources/vercel-oss-dependency-survey-2026-11|Vercel 开源框架的服务依赖调研]]）类似，绑定通常发生在默认值上：默认模型提供商是 OpenAI，默认追踪上传到 OpenAI，默认统计发给 OpenAI。另一个绑定点是 Responses API：Codex 自定义提供商只支持 `wire_api = "responses"`，Agents SDK 的托管工具只在 OpenAI 的 Responses 模型上可用。

## Key Points

- **完全独立**：gpt-oss / gpt-oss-safeguard（Apache-2.0 开放权重）、harmony（Apache-2.0，gpt-oss 必须用它）、tiktoken（MIT，首次运行需下载编码文件或预置缓存）、AGENTS.md（2025-12 捐给 Linux Foundation 下的 AAIF）、Agent Skills 格式（agentskills.io）、MCP Apps 标准与 `@openai/apps-sdk-ui`（MIT）、ACP 规范（Apache-2.0，与 Stripe 共建）、Promptfoo、simple-evals、codex-universal 镜像
- **默认连 OpenAI、可改配置**：Agents SDK（LiteLLM / Any-LLM / Chat Completions 接其他模型，`set_tracing_disabled` 或自定义追踪处理器；托管工具不可用）、Codex CLI（`--oss` 接 Ollama / LM Studio，或自定义 Responses 兼容提供商；`analytics.enabled = false` 关统计）、Codex SDK 与 App Server（继承 CLI 配置）、OpenAI 官方 SDK（改 `base_url`）、Guardrails（Moderation 检查除外）
- **部分独立**：ChatKit 后端用 chatkit-python 自己实现、模型自选，但前端脚本从 OpenAI CDN 加载
- **离不开 OpenAI**：Responses / Realtime / GPT-Live / Agents API、托管工具、Evals 平台与 Agent Builder（都在 2026-11-30 关闭）、微调、Assistants、OpenAI CLI、Terraform provider、Codex cloud、IDE 扩展、Codex Security CLI / SDK（开源但按 OpenAI 用量计费）、Codex GitHub Action、Plugins 上架与 `window.openai` 扩展、Sign in with ChatGPT、Ads、Workspace Agents、Sites、dots
- **门户变化**：Codex 文档迁到 learn.chatgpt.com；Apps SDK 并入 Plugins（技能 + MCP 服务器 + 可选 UI）；`codex mcp-server` 已移除，改用 App Server；`openai/skills` 仓库已弃用，示例移到 `openai/plugins`

## Mentioned Pages

- [[entities/openai|OpenAI]]
- [[entities/gpt|GPT]]
- [[entities/gpt-oss|gpt-oss]]
- [[entities/openai-agents-sdk|OpenAI Agents SDK]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/codex-app-server|Codex App Server]]
- [[entities/chatkit|ChatKit]]
- [[entities/promptfoo|Promptfoo]]
- [[entities/tiktoken|tiktoken]]
- [[concepts/harmony-response-format|harmony 响应格式]]
- [[concepts/agents-md|AGENTS.md]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/agentic-commerce-protocol|Agentic Commerce Protocol]]
- [[concepts/mcp-extensions|MCP 扩展]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
