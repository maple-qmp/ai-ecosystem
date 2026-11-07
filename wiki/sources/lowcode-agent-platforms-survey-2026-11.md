---
title: 低代码 Agent 平台与 LLM 网关调研（2026-11）
type: source
tags: [notes]
source_note: "[[低代码Agent平台调研-2026-11]]"
url: https://github.com/langgenius/dify
created: 2026-11-07
updated: 2026-11-07
sources:
  - "[[entities/dify]]"
  - "[[entities/coze]]"
  - "[[entities/n8n]]"
  - "[[entities/litellm]]"
---

# 低代码 Agent 平台与 LLM 网关调研（2026-11）

## Summary

补 L4 中可视化搭建 Agent / 工作流的一类平台：[[entities/dify|Dify]]（LangGenius）、[[entities/coze|Coze / 扣子]]（[[entities/bytedance|字节跳动]]，含开源的 Coze Studio 与 Coze Loop）、[[entities/n8n|n8n]]，以及多模型统一调用层 [[entities/litellm|LiteLLM]]（BerriAI）。三家低代码平台出身不同：Dify 从 LLM 应用开发平台起步，Coze 从字节的 Bot 搭建平台起步，n8n 从通用工作流自动化起步，到 2026 年都收敛到“画布 + Agent 节点 + MCP + 人工审批节点”。三者的开源协议都有限制或分层：Dify 是附加条件的 Apache 2.0，n8n 是 fair-code 的 Sustainable Use License，Coze 只开源核心引擎。LiteLLM 是本库多页提到、此前没有页面的基础件，2026-03 在 PyPI 被投毒，波及 [[entities/dspy|DSPy]]、[[entities/crewai|CrewAI]] 等下游并导致 [[entities/mercor|Mercor]] 数据泄露。

## Key Points

- **资料可靠性**：一手为 GitHub 仓库首页、PyPI / npm 元数据、Dify 与 n8n 博客、LiteLLM 文档和官方安全 issue；Coze 2.0 / 3.0 只见媒体报道。本会话 GitHub API 不可用，星数取自网页，为约数
- **Dify**：GitHub 约 16.1 万星；v1.0（2025-02）插件生态，v1.6（2025-07）双向 MCP，v1.13（2026-03）人工输入节点，difyctl（2026-07）；2026-03 Pre-A 轮 3000 万美元，运行在 140 多万台机器上
- **Coze**：2025-07-29 开源 Coze Studio 与 Coze Loop（Apache-2.0）；扣子 2.0（2026-01）Agent Skills / Plan / Office / Coding；扣子 3.0（2026-05 或 06）多人多 Agent 协作
- **n8n**：fair-code，GitHub 约 21 万星；2025-10 C 轮 1.8 亿美元、估值 25 亿美元；2025-12 发布 2.0
- **LiteLLM**：Python SDK + 自托管 Proxy（LLM Gateway），100 多家提供商、虚拟密钥、成本追踪、回退；2026-03-24 恶意版本 1.82.7 / 1.82.8；2026 年下半年引入 Rust 核心
- **待核实**：Dify 估值、Coze 官方发布日期、n8n 2026 年估值、LiteLLM 事件根因细节

## Mentioned Pages

- [[entities/dify|Dify]]
- [[entities/coze|Coze / 扣子]]
- [[entities/n8n|n8n]]
- [[entities/litellm|LiteLLM]]
- [[entities/bytedance|字节跳动]]
- [[entities/dspy|DSPy]]
- [[entities/crewai|CrewAI]]
- [[entities/openai-agents-sdk|OpenAI Agents SDK]]
- [[entities/mercor|Mercor]]
- [[entities/langgraph|LangGraph]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/ai-agent|AI Agent]]
