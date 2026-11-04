---
title: Claude 生态可独立使用的项目与模块调研（2026-11）
type: source
tags: [notes]
source_note: "[[Claude独立可用模块调研-2026-11]]"
url: https://github.com/anthropics
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[entities/anthropic]]"
  - "[[entities/claude]]"
  - "[[entities/claude-code]]"
  - "[[entities/claude-agent-sdk]]"
  - "[[entities/sandbox-runtime]]"
  - "[[entities/circuit-tracer]]"
  - "[[entities/petri]]"
  - "[[concepts/anthropic-messages-api]]"
  - "[[concepts/mcp-bundles]]"
  - "[[concepts/claude-constitution]]"
  - "[[concepts/agent-skills]]"
  - "[[concepts/model-context-protocol]]"
---

# Claude 生态可独立使用的项目与模块调研（2026-11）

## Summary

逐个检查 [[entities/anthropic|Anthropic]] 及其关联组织在 GitHub 上的公开项目（anthropics、anthropic-experimental、safety-research、modelcontextprotocol、agentskills），以及 [[entities/claude-code|Claude Code]] 官方文档里关于第三方提供商、网关和遥测的说明，判断哪些能脱离 Anthropic 的服务（Claude API、claude.ai 账号、Anthropic 云端）使用，并分析原理。

和 [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]] 的结论不同：OpenAI 把 Codex CLI 整个开源，能换模型；Anthropic 的核心产品 Claude Code 和 Agent SDK 是**专有软件**，官方只支持 Claude 模型。Anthropic 可独立使用的部分集中在三类：

- **开放标准**：[[concepts/model-context-protocol|MCP]]（已捐给 Linux Foundation 下的 AAIF）、[[concepts/agent-skills|Agent Skills]]、[[concepts/mcp-bundles|MCP Bundles]]
- **从产品里拆出来的基础设施**：[[entities/sandbox-runtime|Sandbox Runtime]]（Claude Code 的沙箱）、[[entities/bun|Bun]]
- **研究工具与公开文档**：[[entities/circuit-tracer|circuit-tracer]]、jacobian-lens（可解释性，跑在开放权重模型上）、[[entities/petri|Petri / Bloom]]（对齐评测，已交给 Meridian Labs）、[[concepts/claude-constitution|Claude 宪法]]（CC0）

另外有一条“事实上的”脱离路径：Claude Code 只认 [[concepts/anthropic-messages-api|Anthropic Messages API]] 的请求格式，而 Ollama、DeepSeek、智谱 GLM、Kimi 等都提供了这一格式的兼容端点，于是把 `ANTHROPIC_BASE_URL` 指过去就能用别家模型驱动 Claude Code。官方文档明确不支持这么做。

## Key Points

- **完全独立**：MCP 规范与 SDK、Inspector、Registry；MCPB 格式与 CLI（MIT）；Agent Skills 格式及 skills 仓库里 Apache-2.0 的示例；srt（Apache-2.0，macOS 用 Seatbelt、Linux 用 bubblewrap、Windows 用专用账户 + WFP，网络一律走主机上的过滤代理）；Claude 宪法（CC0）；circuit-tracer（MIT，Gemma-2 / Llama-3.2 / Qwen3）；jacobian-lens（Apache-2.0）；persona_vectors；Petri 3.0 / Bloom（MIT，基于 Inspect）；safety-tooling；hh-rlhf、evals 等数据集；buffa（Rust protobuf）、claudes-c-compiler（CC0）、FlashProve（推理零知识证明原型）
- **需要 Claude、不需要 Anthropic**：Claude Code、Agent SDK、claude-code-action、security-review 等可走 Amazon Bedrock、Google Cloud、Microsoft Foundry、Claude Platform on AWS；走云厂商时指标、错误报告、`/feedback` 默认关闭；Claude apps gateway 内置在 `claude` 二进制里，数据面不连 Anthropic
- **能接非 Claude 模型但官方不支持**：`ANTHROPIC_BASE_URL` 指向 Anthropic 兼容端点；会失去提示缓存、token 计数、引用、PDF、服务端工具等；WebFetch 域名检查和 fast mode 检查仍直连 api.anthropic.com
- **离不开 Anthropic**：claude.ai 与桌面端、Claude Code 云端会话（自托管 runner 也要 Anthropic 控制面）、Developer Platform 服务端功能、订阅登录、Claude Security / OSS Scanner、docx / pdf / pptx / xlsx 文档技能（source-available，协议限定用于 Anthropic 服务）
- **协议细节**：Claude Code 仓库是“All rights reserved”，只放文档和插件；TS 版 Agent SDK 用商业条款，Python 版 MIT 但自带专有的 CLI；2026-03-31 的 source map 泄露没有改变协议
- **治理转移**：MCP → AAIF（2025-12）；Petri、Bloom → Meridian Labs（2026-05）；circuit-tracer → decoderesearch 组织

## Mentioned Pages

- [[entities/anthropic|Anthropic]]
- [[entities/claude|Claude]]
- [[entities/claude-code|Claude Code]]
- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[entities/sandbox-runtime|Sandbox Runtime（srt）]]
- [[entities/circuit-tracer|circuit-tracer]]
- [[entities/petri|Petri]]
- [[entities/bun|Bun]]
- [[entities/codex-cli|Codex CLI]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]
- [[concepts/mcp-bundles|MCP Bundles（MCPB）]]
- [[concepts/claude-constitution|Claude 宪法]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
