---
title: LangChain 生态深度调研（2026-11）
type: source
tags: [notes]
source_note: "[[LangChain生态深度调研-2026-11]]"
url: https://www.langchain.com/blog/langchain-langgraph-1dot0
created: 2026-11-04
updated: 2026-11-04
sources:
  - "[[entities/langchain]]"
  - "[[entities/langchain-inc]]"
  - "[[entities/langgraph]]"
  - "[[entities/langsmith]]"
  - "[[entities/deep-agents]]"
  - "[[concepts/agent-harness]]"
  - "[[concepts/ai-agent]]"
---

# LangChain 生态深度调研（2026-11）

## Summary

梳理 [[entities/langchain-inc|LangChain 公司]]的产品结构：开源侧是三层框架，最底层的 [[entities/langgraph|LangGraph]] 是有状态的 Agent 编排运行时，中间的 [[entities/langchain|LangChain]] 自 1.0 起改为构建在 LangGraph 上的高层 Agent API（`create_agent` + 中间件），最上层的 [[entities/deep-agents|Deep Agents]] 是开箱即用的 [[concepts/agent-harness|Agent harness]]（规划、文件系统、子 Agent、记忆）。商业侧是闭源的 [[entities/langsmith|LangSmith]]，从可观测性和评测起家，2025–2026 年扩展为覆盖部署、无代码 Agent（Fleet）、托管 Deep Agents、沙箱、LLM 网关和微调的 Agent 工程平台。公司 2025-10 完成 1.25 亿美元 B 轮，估值 12.5 亿美元。

## Key Points

- **1.0 稳定版**（2025-10-22）：LangChain 与 LangGraph 同日发布 1.0，承诺 2.0 之前无破坏性变更；`create_react_agent` 弃用，改用 `langchain.agents.create_agent`；旧功能移入 `langchain-classic`
- **中间件**：在 Agent 循环每一步提供钩子，内置人工审批、对话摘要、PII 脱敏
- **标准内容块**：跨厂商统一推理、引用、工具调用的输出格式
- **Deep Agents**：v0.6（2026-05）加入程序化工具调用和前端流式；v0.7（2026-08）基础输入 token 减少 65%
- **LangSmith 产品线**：Observability、Evaluation、Deployment（原 LangGraph Platform，2025-10 更名）、Studio、Fleet（原 Agent Builder，2026-03 更名）、Engine、Sandboxes、LLM Gateway、Managed Deep Agents、Fine-Tuning
- **MCP**：LangChain v1.4.0（2026-10）通过 `langchain.mcp` 支持 FastMCP
- **融资**：种子轮 1000 万美元（Benchmark，2023-04）→ A 轮 2500 万美元、估值 2 亿（Sequoia，2024-02）→ B 轮 1.25 亿美元、估值 12.5 亿（IVP，2025-10-20）

## Mentioned Pages

- [[entities/langchain-inc|LangChain 公司]]
- [[entities/langchain|LangChain]]
- [[entities/langgraph|LangGraph]]
- [[entities/langsmith|LangSmith]]
- [[entities/deep-agents|Deep Agents]]
- [[entities/vercel-ai-sdk|AI SDK]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/rag|检索增强生成（RAG）]]
