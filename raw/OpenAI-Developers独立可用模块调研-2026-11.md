---
title: OpenAI Developers 可独立使用模块调研（2026-11）
captured: 2026-11-04
tags: [notes]
---

# OpenAI Developers 可独立使用模块调研（2026-11）

一句话：逐个查看 OpenAI 开发者门户 developers.openai.com 下的产品、SDK、开源项目和规范，判断哪些能脱离 OpenAI 的服务（API、ChatGPT 账号、OpenAI 云端）独立使用，再对能独立使用的模块做深入调研。资料来自官方文档的 Markdown 版本、GitHub 仓库和 API 元数据、网页检索，检索日期 2026-11-04。

## 原始链接

- 门户首页与站点索引：https://developers.openai.com/ ，https://developers.openai.com/llms.txt
- Codex 开源组件（已迁到 learn.chatgpt.com）：https://learn.chatgpt.com/docs/open-source.md
- Codex 高级配置：https://learn.chatgpt.com/docs/config-file/config-advanced.md
- Codex 配置参考：https://learn.chatgpt.com/docs/config-file/config-reference.md
- Codex SDK：https://learn.chatgpt.com/docs/codex-sdk.md
- Codex App Server：https://learn.chatgpt.com/docs/app-server.md
- AGENTS.md：https://learn.chatgpt.com/docs/agent-configuration/agents-md.md
- 构建技能：https://learn.chatgpt.com/docs/build-skills.md
- Codex Security CLI FAQ：https://learn.chatgpt.com/docs/security/cli/faq.md
- Agents SDK 总览：https://developers.openai.com/api/docs/guides/agents/sdk
- Agents SDK（Python）模型、追踪、工具、沙箱：https://openai.github.io/openai-agents-python/models/ ，/tracing/ ，/tools/ ，/sandbox_agents/
- ChatKit：https://developers.openai.com/api/docs/guides/chatkit ，https://github.com/openai/chatkit-js ，https://github.com/openai/chatkit-python
- Plugins（原 Apps SDK）UI：https://developers.openai.com/plugins/build/chatgpt-ui.md
- Agentic Commerce 关键概念：https://developers.openai.com/commerce/guides/key-concepts.md
- 规范站：https://www.agenticcommerce.dev/
- SDK 与库列表：https://developers.openai.com/api/docs/libraries.md
- Evals 指南（弃用说明）：https://developers.openai.com/api/docs/guides/evals.md
- Promptfoo 指南：https://developers.openai.com/api/docs/guides/promptfoo-codex.md
- gpt-oss：https://github.com/openai/gpt-oss ，https://developers.openai.com/learn/gpt-oss
- harmony：https://github.com/openai/harmony
- tiktoken：https://github.com/openai/tiktoken
- Skills 仓库：https://github.com/openai/skills
- Agentic AI Foundation 成立公告：https://www.linuxfoundation.org/press/linux-foundation-announces-the-formation-of-the-agentic-ai-foundation
- Stripe 关于 ACP：https://stripe.com/blog/developing-an-open-standard-for-agentic-commerce
- gpt-oss-safeguard 技术报告：https://openai.com/index/gpt-oss-safeguard-technical-report
- Promptfoo 收购报道：https://securityboulevard.com/2026/03/openai-acquires-security-startup-promptfoo-to-fortify-ai-agents

## 门户结构（2026-11）

站点索引 `llms.txt` 把门户分成这些文档集：OpenAI API（Responses、Realtime、工具、Evals、微调、模型）、Ads API、Sign in with ChatGPT、ChatGPT plugins and Apps SDK、Workspace Agents API、Codex 开发者工具、Agentic Commerce Protocol、开发者博客、Cookbook、Learn、Showcase。Codex 文档已整体迁到 learn.chatgpt.com（旧链接 308 跳转）。Apps SDK 已并入“Plugins”文档集：插件 = 技能 + MCP 服务器 + 可选 UI。

## 官方文档摘录

### Codex 开源组件（open-source.md，转述）

- Codex CLI 在 `openai/codex`；Codex SDK 在同仓库 `sdk/`；Codex App Server 在 `codex-rs/app-server`
- Codex Security CLI 与 TypeScript SDK 在 `openai/codex-security`
- Skills 在 `openai/skills`，Plugins 在 `openai/plugins`，Codex 云端基础镜像在 `openai/codex-universal`
- IDE 扩展和 Codex cloud 不开源；`openai/codex` 不接受外部代码贡献和 PR，只接受 issue

### Codex 配置

- "Codex can run against a local "open source" provider such as Ollama or LM Studio when you pass `--oss`."
- "Choose one for a single run with `--local-provider`, or set `oss_provider` as the default."
- "If neither is set, the interactive CLI prompts you to choose; `codex exec` exits with an error."
- "A model provider defines how Codex connects to a model (base URL, wire API, authentication, and optional HTTP headers)."
- 保留的提供商 ID：`openai`、`ollama`、`lmstudio`、`amazon-bedrock`、`amazon-bedrock-runtime`、`gcp`
- `model_providers.<id>.wire_api`："`responses` is the only supported value, and it is the default when omitted."
- `analytics.enabled`："Setting this to `false` disables the built-in Statsig metrics exporter."
- "If `exporter = "none"` Codex records events but sends nothing."
- `feedback.enabled`："Enable feedback submission via `/feedback` across local clients (default: true)."

### Codex SDK 与 App Server

- "The TypeScript library lets your application start, continue, and resume local Codex threads."
- "The Python SDK controls the local Codex app-server over JSON-RPC. It requires Python 3.10 or later. Published SDK builds include a pinned Codex CLI runtime dependency."
- "Codex app-server is the interface Codex uses to power rich clients (for example, the Codex VS Code extension)."
- "Like MCP, `codex app-server` supports bidirectional communication using JSON-RPC 2.0 messages (with the `"jsonrpc":"2.0"` header omitted on the wire)."
- 传输：stdio（默认，JSONL）、WebSocket（实验性、不受支持）、Unix socket、off
- "The `codex mcp-server` command and standalone `codex-mcp-server` binary have been removed."

### Agents SDK

- "The Agents SDK runs in your application; the Agents API runs a managed harness in OpenAI's service."
- "Any-LLM support is included on a best-effort, beta basis."
- "LiteLLM support is included on a best-effort, beta basis."
- 非 OpenAI 提供商可用 `set_default_openai_client`、自定义 `ModelProvider`、`OpenAIChatCompletionsModel`；文档说明 "many LLM providers still do not support the Responses API."
- 追踪默认上传到 OpenAI；没有 OpenAI key 时会 401，建议 "disabling tracing via `set_tracing_disabled()`, or setting up a different tracing processor."
- "You can globally disable tracing by setting the env var `OPENAI_AGENTS_DISABLE_TRACING=1`"
- `set_trace_processors()` 替换默认处理器；"Tracing is unavailable for organizations that use OpenAI's APIs under a Zero Data Retention (ZDR) policy."
- "OpenAI offers a few built-in tools when using the OpenAIResponsesModel"：WebSearchTool、FileSearchTool、CodeInterpreterTool、HostedMCPTool、ImageGenerationTool、ToolSearchTool 等
- 沙箱 Agent："For trusted local development, start with `UnixLocalSandboxClient`."；Linux 上它不做系统级隔离，不可信命令建议用 Docker 或托管沙箱

### ChatKit

- Agent Builder 托管路径："scheduled to shut down on November 30, 2026"
- 自托管路径可以 "connect to any agentic service, including one built with the Agents SDK"，新项目推荐 "with your own server-side agent implementation"
- chatkit-js README 的示例从 `https://cdn.platform.openai.com/deployments/chatkit/chatkit.js` 加载脚本；自定义后端用 `api: { url, domainKey }` 配置

### Plugins / MCP Apps

- "ChatGPT implements the open MCP Apps standard for UI returned by an MCP server."
- "This standards-first foundation lets the same UI run in ChatGPT and other compatible MCP Apps hosts."
- 标准字段与 ChatGPT 别名对照：`_meta.ui.resourceUri` ↔ `_meta["openai/outputTemplate"]`；`ui/notifications/tool-result` ↔ `window.openai.toolOutput`；`tools/call` ↔ `window.openai.callTool`；`ui/message` ↔ `window.openai.sendFollowUpMessage`
- 只有 ChatGPT 有的扩展：Instant Checkout（`window.openai.requestCheckout`）、文件上传与下载、宿主模态框、`widgetState` 持久化

### Agentic Commerce

- "The checkout session is rendered in the OpenAI UI, but the actual checkout state and payment processing occurs on the merchant's systems."
- "OpenAI is not the merchant of record in the Agentic Commerce Protocol."
- Stripe 的 Shared Payment Token 是第一个兼容 Delegated Payment Spec 的实现

### 其他

- Evals："OpenAI is deprecating the Evals platform."，平台计划 2026-11-30 关闭，2026-10-31 起对现有用户停止新建
- Promptfoo 指南："Promptfoo is part of OpenAI."
- libraries 页列出的开源工具：tiktoken（计数 token）、simple-evals、mle-bench、gym
- harmony："gpt-oss should not be used without using the harmony format as it will not work correctly."
- gpt-oss README：gpt-oss-120b 用于 "production, general purpose, high reasoning use cases that fit into a single 80GB GPU"；gpt-oss-20b 用于 "lower latency, and local or specialized use cases"
- Skills 仓库 README："This repository is deprecated."，新示例改放 `openai/plugins`；"Agent Skills are folders of instructions, scripts, and resources that AI agents can discover and use to perform at specific tasks."

## 仓库元数据（GitHub API，2026-11-04）

| 仓库 | 星标 | 协议 | 主语言 | 创建 | 最新版本 |
|---|---|---|---|---|---|
| openai/codex | 133k | Apache-2.0 | Rust | 2025-04 | rust-v0.166.0（2026-10-29 稳定），0.168.0-alpha.1 |
| openai/openai-agents-python | 30.5k | MIT | Python | 2025-03 | v0.24.0（2026-10-15） |
| openai/openai-agents-js | 4.0k | MIT | TypeScript | 2025-05 | 0.21.0（2026-10-20） |
| openai/chatkit-js | 2.0k | Apache-2.0 | TypeScript | 2025-10 | — |
| openai/chatkit-python | 0.4k | Apache-2.0 | Python | 2025-10 | v1.6.5（2026-05-19） |
| openai/gpt-oss | 20.5k | Apache-2.0 | Python | 2025-06 | — |
| openai/harmony | 4.5k | Apache-2.0 | Rust | 2025-07 | — |
| openai/tiktoken | 19.6k | MIT | Python | 2022-12 | — |
| openai/skills | 28.5k | 未声明 | Python | 2025-11 | 已弃用 |
| openai/plugins | 7.7k | 未声明 | JavaScript | 2026-03 | — |
| openai/codex-universal | 1.1k | 未声明 | Dockerfile | 2025-05 | — |
| openai/codex-security | 11.3k | Apache-2.0 | TypeScript | 2026-07 | npm-v0.8.3（2026-11-03） |
| openai/apps-sdk-ui | 1.0k | MIT | TypeScript | 2025-10 | — |
| openai/openai-apps-sdk-examples | 2.4k | MIT | TypeScript | 2025-10 | — |
| openai/openai-guardrails-python | 0.3k | MIT | Python | 2025-04 | v0.3.6（2026-10-26） |
| openai/simple-evals | 4.7k | MIT | Python | 2024-04 | — |
| openai/evals | 19.7k | 其他 | Python | 2023-01 | — |
| promptfoo/promptfoo | 26.8k | MIT | TypeScript | 2023-04 | 0.125.1（2026-10-25） |
| agentic-commerce-protocol/agentic-commerce-protocol | 1.6k | Apache-2.0 | JavaScript | 2025-09 | — |

PyPI `openai-agents` 0.24.0 的可选依赖：any-llm、litellm、docker、e2b、modal、daytona、cloudflare、vercel、runloop、blaxel（沙箱）；redis、sqlalchemy、mongodb、dapr、s3、encrypt（会话与存储）；temporal（持久执行）；realtime、voice、viz。PyPI `openai-chatkit` 1.6.5 依赖 `openai` 和 `openai-agents>=0.3.2`。

tiktoken 源码：编码文件从 `openaipublic.blob.core.windows.net` 下载，可用 `TIKTOKEN_CACHE_DIR` 指定缓存目录（离线环境需预先放好）。

## 检索要点（二手整理，非逐字）

- **gpt-oss**：2025-08 发布，Apache-2.0。120b 总参数 117B、激活 5.1B；20b 总参数 21B、激活 3.6B；MoE 权重以 MXFP4 后训练，120b 单张 80GB GPU、20b 16GB 内存可跑；推理强度 low / medium / high 可调；参考实现有 PyTorch（教学用，需 4×H100）、Triton、Apple Metal，另有浏览器工具与 Python 工具参考实现；支持 Transformers、vLLM、Ollama、LM Studio。
- **gpt-oss-safeguard**：2025-10-29 发布研究预览，120b / 20b 两个尺寸，分别由 gpt-oss 微调而来，Apache-2.0。输入“开发者写的策略 + 待分类内容”，输出判定和推理过程；策略在推理时提供，改规则不用重训。与 Discord、SafetyKit、ROOST 合作。官方提示：有大量标注数据时，专门训练的分类器在复杂高风险场景仍可能更准，且它对全量内容跑分类成本较高。
- **Agentic AI Foundation（AAIF）**：2025-12-09 由 Linux Foundation 宣布成立，创始项目为 MCP（Anthropic 捐出）、goose（Block 捐出）、AGENTS.md（OpenAI 捐出）。公告称 AGENTS.md 已被 6 万多个开源项目和 Agent 框架采用，包括 Amp、Codex、Cursor、Devin、Factory、Gemini CLI、GitHub Copilot、Jules、VS Code。
- **Agentic Commerce Protocol**：2025-09 由 OpenAI 与 Stripe 联合发布，Apache-2.0，规范站 agenticcommerce.dev；包括 Agentic Checkout Spec、Delegated Payment Spec、商品 Feed 规范。商家可用任意兼容的支付服务商。
- **Promptfoo**：2026-03-09 宣布被 OpenAI 收购；官方表示项目保持开源、继续 MIT 协议，技术会并入 OpenAI 企业平台 Frontier。也有评论指出未来代码的协议与治理没有书面保证。
- **Codex 本地模型**：社区指南常用 Ollama（`http://localhost:11434/v1`）和 LM Studio（`http://localhost:1234/v1`）跑 gpt-oss 或其他本地编码模型；部分旧指南用 `wire_api = "chat"`，但当前官方配置参考只支持 `responses`，自定义提供商必须提供 Responses 兼容接口。
- **ChatKit 自托管**：后端用 chatkit-python 自己实现，模型选择完全在后端；社区有用 LiteLLM 接多模型、用 Gemini 的示例（非官方）。前端组件仍从 OpenAI CDN 加载，`domainKey` 是否必须在 OpenAI 后台登记未在官方页面确认。

## 依赖分级（调研结论）

- **完全独立（代码、权重或规范，不连 OpenAI 服务）**：gpt-oss 与 gpt-oss-safeguard（开放权重）、harmony、tiktoken（首次需下载编码文件或预置缓存）、AGENTS.md（AAIF 治理）、Agent Skills 格式（agentskills.io 开放标准）、MCP Apps 标准与 `@openai/apps-sdk-ui` 组件库、Agentic Commerce Protocol 规范、Promptfoo、simple-evals、codex-universal 镜像
- **默认连 OpenAI，可改配置脱离**：Agents SDK（换模型提供商 + 关闭或替换追踪；托管工具不可用）、Codex CLI（`--oss` 或自定义 Responses 兼容提供商；关闭 Statsig 统计与反馈）、Codex SDK 与 App Server（继承 CLI 的提供商配置）、OpenAI 官方 SDK（`base_url` 指向 vLLM、Ollama 等兼容服务）、Guardrails（Moderation 检查需 OpenAI，其余可接兼容端点）
- **部分独立**：ChatKit（后端与模型自定，前端脚本从 OpenAI CDN 加载）
- **离不开 OpenAI 服务**：Responses / Realtime / GPT-Live / Agents API、托管工具（web search、file search、code interpreter 等）、Evals 平台（2026-11-30 关闭）、微调、Assistants、Agent Builder（2026-11-30 关闭）、OpenAI CLI、Terraform provider、Codex cloud、IDE 扩展（闭源）、Codex Security CLI / SDK（开源但需 ChatGPT 登录或 API key 计费）、Codex GitHub Action、Plugins 上架与 `window.openai` 扩展、Sign in with ChatGPT、Ads、Workspace Agents、Sites、dots
