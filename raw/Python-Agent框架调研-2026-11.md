---
title: Python Agent 框架调研（2026-11）
captured: 2026-11-06
tags: [notes]
---

# Python Agent 框架调研（2026-11）

一句话：梳理 Python 上开发 AI Agent 的主要框架，覆盖 Microsoft Agent Framework（及其前身 AutoGen、Semantic Kernel）、CrewAI、LlamaIndex（含 Agent Workflows / LlamaAgents）、Pydantic AI、DSPy、smolagents、Agno，并与库中已有的 LangGraph、OpenAI Agents SDK、Google ADK 对照。资料来自官方博客、GitHub README 与仓库元数据、PyPI 元数据，检索日期 2026-11-06。

## 原始链接

- Microsoft Agent Framework 1.0 公告（2026-04-03）：https://devblogs.microsoft.com/agent-framework/microsoft-agent-framework-version-1-0/
- Microsoft Agent Framework 仓库：https://github.com/microsoft/agent-framework
- AutoGen 仓库（已归档）：https://github.com/microsoft/autogen
- Semantic Kernel 仓库：https://github.com/microsoft/semantic-kernel
- CrewAI 仓库：https://github.com/crewAIInc/crewAI ；更新日志：https://docs.crewai.com/en/changelog
- CrewAI Studio Flows 文档：https://docs-platform.crewai.com/platform/en/features/studio-flows
- LlamaIndex 仓库：https://github.com/run-llama/llama_index
- LlamaAgents / Agent Workflows 仓库：https://github.com/run-llama/llama-agents
- LlamaIndex Newsletter 2026-02-24（LlamaCloud 改名 LlamaParse）：https://www.llamaindex.ai/blog/llamaindex-newsletter-2026-02-24
- Pydantic AI 仓库：https://github.com/pydantic/pydantic-ai
- Pydantic AI v2 公告（2026-06-23）：https://pydantic.dev/articles/pydantic-ai-v2.md
- Pydantic AI 版本政策：https://pydantic.dev/docs/ai/project/version-policy/
- DSPy 仓库：https://github.com/stanfordnlp/dspy
- smolagents 仓库：https://github.com/huggingface/smolagents
- Agno 仓库：https://github.com/agno-agi/agno
- ADK 2.0 文档：https://adk.dev/2.0/index.md
- PyPI JSON API：https://pypi.org/pypi/<包名>/json （2026-11-06 读取）
- GitHub REST API：https://api.github.com/repos/<owner>/<repo> （2026-11-06 读取星数、协议、创建日期）

## 官方原文摘录

Microsoft Agent Framework：

- README："Microsoft Agent Framework (MAF) is an open, multi-language framework for building **production-grade AI agents and multi-agent workflows** in **.NET and Python**."
- 1.0 公告："This is the production-ready release: stable APIs, and a commitment to long-term support."
- 1.0 公告："The graph-based workflow engine for composing agents and functions into deterministic, repeatable processes is now stable."

AutoGen README：

- "This project has been archived and is no longer actively maintained by Microsoft."
- "Microsoft Agent Framework (MAF) is the enterprise‑ready successor to AutoGen."

CrewAI README：

- "CrewAI is an open-source Python framework with high-level abstractions and low-level APIs for building production-ready multi-agent workflows."
- "It gives developers autonomous agent collaboration through Crews and precise, event-driven control through Flows."
- "CrewAI is a standalone Python framework with its own primitives for agents, tasks, crews, flows, tools, and orchestration."

LlamaIndex README：

- "The current focus of LlamaIndex is to build the best AI-powered engine for document parsing and extraction."
- "While we still have the OSS framework available as an open toolkit that you're welcome to use, our primary focus has shifted towards LlamaParse, along with liteparse and our benchmarking efforts."

LlamaAgents README："An open-source framework for building and shipping document-centric agents in Python."

Pydantic AI：

- 仓库描述："How Python does AI. Agents, realtime voice, image generation, embeddings. Every model, every interface, typed end to end."
- v2 公告："Pydantic AI v2 is here, and your agents have never been more capable."

DSPy README：

- "DSPy is the framework for _programming—rather than prompting—language models_."
- "DSPy stands for Declarative Self-improving Python."

smolagents README：

- "`smolagents` is a library that enables you to run powerful agents in a few lines of code."
- "Our `CodeAgent` works mostly like classical ReAct agents - the exception being that the LLM engine writes its actions as Python code snippets."

Agno README："Agno is a self-managing agent platform. Build agents for your company, product, or customers. Run them as durable services on AgentOS."

## 版本与仓库数据（2026-11-06 读取）

| 项目 | PyPI 包 | 最新版（日期） | 关键大版本 | GitHub 星数 | 协议 |
|---|---|---|---|---|---|
| Microsoft Agent Framework | agent-framework | 1.24.0（2026-10-30） | 首个 beta 2025-10-01；1.0.0 2026-04-02 | 约 1.46 万 | MIT |
| Semantic Kernel | semantic-kernel | 1.47.0（2026-11-05） | 1.0 系列 2024 | 约 2.87 万 | MIT |
| AutoGen | autogen-agentchat | 0.7.5（2025-09-30） | 0.4.0 2025-01-09 | 约 6.17 万 | CC-BY-4.0（见下注） |
| CrewAI | crewai | 1.15.35（2026-11-03） | 1.0.0 2025-10-20 | 约 6.06 万 | MIT |
| LlamaIndex | llama-index | 0.14.25（2026-09-21） | 0.14.0 2025-09-08 | 约 5.28 万 | MIT |
| LlamaIndex Workflows | llama-index-workflows | 2.26.1（2026-10-21） | 1.0.0 2025-06-25；2.0.0 2025-08-29 | — | MIT |
| Pydantic AI | pydantic-ai | 2.66.0（2026-11-04） | 1.0.0 2025-09-05；2.0.0 2026-06-23 | 约 2.10 万 | MIT |
| DSPy | dspy | 3.4.1（2026-10-12） | 3.0.0 2025-08-12 | 约 3.89 万 | MIT |
| smolagents | smolagents | 1.26.0（2026-05-29） | 1.0.0 2024-12-31 | 约 3.02 万 | Apache-2.0 |
| Agno | agno | 3.1.12（2026-10-29） | 1.0.0 2025-01-30；2.0.0 2025-09-09 | 约 4.31 万 | Apache-2.0 |
| LangGraph | langgraph | 1.2.20（2026-11-05） | 1.0.0 2025-10-17 | — | MIT |
| OpenAI Agents SDK | openai-agents | 0.24.0（2026-10-15） | 首发 2025-03-04 | — | MIT |
| Google ADK（Python） | google-adk | 2.13.0（2026-10-23） | 1.0.0 2025-05-20；2.0.0 2026-05-19 | 约 2.21 万 | Apache-2.0 |

AutoGen 一行的协议：GitHub API 报告的是仓库 LICENSE 文件 CC-BY-4.0；代码协议未单独核实。

## 整理

### 1. 总体格局

Python 是 Agent 框架最密集的语言，几乎所有新特性先在 Python 出现（Google ADK、OpenAI Agents SDK 都是 Python 版领先）。2025 年下半年到 2026 年，主要框架纷纷进入 1.0 或更高的大版本，并出现两个共同方向：

1. **图式 / 事件驱动工作流成为标配**：Microsoft Agent Framework 的 graph workflow、CrewAI Flows、LlamaIndex Agent Workflows、ADK 2.0 Workflow Runtime、LangGraph，都是“确定性编排 + Agent 节点”的组合。
2. **Harness 化**：框架在核心 Agent 循环之外提供文件、shell、记忆、沙箱、上下文压缩等“电池”，例如 Pydantic AI Harness、MAF 的 Agent Harness（预览）、Agno AgentOS。

按定位大致分为：

- **大厂全家桶**：Microsoft Agent Framework、Google ADK、OpenAI Agents SDK。和各自云平台（Foundry、Vertex AI、OpenAI Agents API）深度集成。
- **独立通用框架**：LangGraph、CrewAI、Pydantic AI、Agno。
- **数据 / 文档中心**：LlamaIndex，2026 年重心转向文档解析（LlamaParse）。
- **研究取向 / 极简**：DSPy（把提示当可优化程序）、smolagents（代码即动作）。

### 2. 各项目要点

**Microsoft Agent Framework（MAF）**

- 由 Semantic Kernel（企业级基础：连接器、中间件、过滤器）和 AutoGen（多 Agent 编排模式）合并而成的开源 SDK，支持 .NET 与 Python，Go 版另有仓库 microsoft/agent-framework-go。
- 时间线：PyPI 首个 beta `1.0.0b251001` 于 2025-10-01；1.0.0 于 2026-04-02 上传 PyPI，官方公告 2026-04-03；最新 1.24.0（2026-10-30）。
- 1.0 稳定部分：单 Agent 抽象与 Foundry、Azure OpenAI、OpenAI、Anthropic、Amazon Bedrock、Google Gemini、Ollama 的一方连接器；中间件；可插拔记忆与上下文提供者；带检查点的图式工作流；顺序、并发、handoff、群聊、Magentic-One 五种多 Agent 编排；YAML 声明式 Agent 与工作流。
- 预览部分：DevUI（浏览器本地调试器）、Foundry 托管 Agent、Azure Durable Functions 集成、AG-UI（含 CopilotKit、ChatKit 适配器）、Skills、GitHub Copilot SDK 与 Claude Code SDK harness、Agent Harness。
- 协议：支持 MCP；支持 A2A，但公告称 A2A 1.0 支持尚未完成。
- AutoGen：仓库已归档，微软不再提供修复和安全更新；autogen-agentchat 最后版本 0.7.5（2025-09-30）。官方提供迁移指南与迁移助手。
- Semantic Kernel：仍在发布（1.47.0，2026-11-05），二手资料称微软承诺 MAF GA 后至少支持一年；新项目推荐 MAF。

**CrewAI**（CrewAI Inc.）

- 独立 Python 框架，不依赖 LangChain，自带 agents、tasks、crews、flows、tools 等原语。两种模式：Crews（角色化自主协作）与 Flows（事件驱动的精确控制，可嵌入 Crew 和单次 LLM 调用）。
- 1.0.0 于 2025-10-20；2026 年保持高频小版本，最新 1.15.35（2026-11-03）。更新日志显示 2026-06 前后加入会话式 Flow 的 chat API 与可插拔 Flow 后端；平台侧 Studio 的无代码 Flows 2026-07 起推出。
- 商业产品 CrewAI AMP Suite：托管部署、可观测性、治理、企业支持；Crew Control Plane 有免费层。README 称社区课程认证开发者超过 10 万。
- GitHub 约 6.06 万星，是 Python Agent 框架中星数最高的活跃项目之一（AutoGen 星更多但已归档）。

**LlamaIndex**（LlamaIndex Inc.，仓库 run-llama）

- 2023 年起以 RAG 数据框架闻名（“Interface between LLMs and your data”），核心 `llama-index-core` + 300 多个集成包。
- 2026 年战略转向：README 称公司主要精力已转向 LlamaParse（Agentic OCR、解析、抽取、索引平台），开源框架继续可用。2026-02 起 LlamaCloud 在文档和官网统一改名 LlamaParse。
- Agent 部分：`llama-index-workflows`（事件驱动、异步、基于 step 的编排库）已拆到独立仓库 llama-agents，以 LlamaAgents 名义定位为“面向文档的 Agent 框架”；Workflows 1.0 于 2025-06-25，2.0 于 2025-08-29，最新 2.26.1（2026-10-21）。框架主包仍在 0.x（0.14.25，2026-09-21），2026-09 之后没有新版本。
- 二手资料：llama-deploy 已弃用，LlamaIndex.TS 已弃用；未在一手资料中核实。

**Pydantic AI**（Pydantic 团队）

- 定位“Python AI SDK”：类型化、可扩展的 Agent 循环，模型可用字符串切换并支持回退；配套 Pydantic Evals（评测输出与工具调用轨迹）、Pydantic Graph、Pydantic Logfire（可观测性）和 Pydantic AI Gateway。
- V1：1.0.0 于 2025-09-05（官方版本政策写 2025-09），带 API 稳定承诺、工具调用人工审批、基于 Temporal 的持久执行。
- V2：2.0.0 于 2026-06-23。核心概念改为 capability（把指令、工具、生命周期钩子、模型设置打包成一个可组合单元，可序列化、可从 spec 文件加载）；新增独立包 Pydantic AI Harness（记忆、护栏、上下文管理、文件系统、shell、Code Mode 等），核心保持精简。行为变化：`openai:` 前缀默认走 Responses API（Chat Completions 改用 `openai-chat:`）；Bedrock、Groq、Mistral 等提供方改为可选安装；大版本之间的无破坏窗口从 6 个月缩短到 3 个月。V1 在 V2 发布后至少 6 个月内仍有安全修复。
- 节奏极快：2026-06 的 2.0 到 2026-11-04 的 2.66.0。

**DSPy**（斯坦福 NLP 起源）

- “编程而非提示”：用签名（signature）和模块写组合式 Python 程序，再用优化器自动优化提示和权重。名字是 Declarative Self-improving Python 的缩写。
- 3.0.0 于 2025-08-12；2026 年依次发布 3.2.0（2026-04，dspy.RLM 改进，开始与 LiteLLM 解耦）、3.3.0（2026-08，dspy.Flex 让 GEPA 同时优化代码与提示，dspy.ReActV2 支持原生和并行工具调用）、3.4.0（2026-09，新优化器 ReAnchor）、3.4.1（2026-10-12）。这些小版本内容来自维护者 Isaac Miller 的 X 帖子与二手资料。
- README 称当前 LM 集成使用内置的 lm15 引擎，已不再依赖 LiteLLM。
- 相关论文：DSPy（2023-10）、MIPRO（2024-06）、GEPA（2025-07，反思式提示进化）。

**smolagents**（Hugging Face）

- 极简 Agent 库，Agent 逻辑约 1000 行；主打 CodeAgent：LLM 把动作写成 Python 代码片段，而不是输出工具调用 JSON；README 引用论文称可少用约 30% 步骤。代码可在 E2B、Docker 等沙箱中执行。
- 模型、模态、工具都不绑定：支持本地 transformers / Ollama、Hub 推理服务、LiteLLM；工具可来自 MCP、LangChain、Hub Space。
- 1.0.0 于 2024-12-31；1.25.0（2026-05）修补远程执行器漏洞并去掉 pickle；1.26.0（2026-05-29）移除远程 WasmExecutor。此后到 2026-11-06 没有新版本，更新明显放缓。网传的“smolagents v2”无官方依据。

**Agno**（前身 Phidata）

- 2026 年定位从 Agent 框架扩展为“自管理 Agent 平台”：用 Agno、Claude Agent SDK 或 Codex SDK 构建 Agent，组合成 teams 与 workflows；AgentOS 把 Agent 跑成持久服务，自带 API 与 MCP 服务器、鉴权、RBAC、恢复 / 重放、人工审批、调度、持久执行；Company OS 让 Agent 承担职责、项目与例行任务。
- PyPI：1.0.0 于 2025-01-30，2.0.0 于 2025-09-09，最新 3.1.12（2026-10-29）。仓库创建于 2022-05，Phidata 改名为 Agno 的说法来自训练知识，未在本次一手资料中核实。

**库中已有项目的 Python 版对照**

- LangGraph：1.0.0 于 2025-10-17，最新 1.2.20（2026-11-05）。
- OpenAI Agents SDK（Python）：首发 2025-03-04，最新 0.24.0（2026-10-15），仍在 0.x。
- Google ADK（Python）：1.0.0 于 2025-05-20；2.0.0 于 2026-05-19，从分层 Agent 执行器改为图式 Workflow Runtime（Agent 作为图中节点，`BaseAgent` 继承 `BaseNode`），新增 Task API 做结构化 Agent 间委派；最新 2.13.0（2026-10-23）。2.0 写入的会话只能被 1.28+ 读取。

### 3. 选型参考（整理者归纳，非官方结论）

- Azure / Foundry / .NET 混合团队，或手上有 Semantic Kernel、AutoGen 代码：Microsoft Agent Framework。
- 需要显式状态图、检查点、人工介入，且不想绑定云：LangGraph。
- 想用“角色 + 任务”快速搭多 Agent 原型，或需要商业控制面：CrewAI。
- 重视类型安全、结构化输出、FastAPI 式开发体验：Pydantic AI。
- 以文档解析、抽取为核心的流水线：LlamaIndex Agent Workflows + LlamaParse。
- 有评测数据、想自动优化提示而非手调：DSPy（可与其他框架组合）。
- 研究、教学、开源模型和代码执行型 Agent：smolagents（注意 2026-05 后更新放缓）。
- 想直接得到带 API、鉴权、调度的 Agent 服务平台：Agno AgentOS。
- 深度绑定 Gemini / Vertex AI：Google ADK；深度绑定 OpenAI：OpenAI Agents SDK。
