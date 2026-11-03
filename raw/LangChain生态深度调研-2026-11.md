---
title: LangChain 生态深度调研（2026-11）
captured: 2026-11-04
tags: [notes]
---

# LangChain 生态深度调研（2026-11）

一句话：梳理 LangChain 公司及其开源框架（LangChain、LangGraph、Deep Agents）和商业平台（LangSmith）的产品结构、版本演进与融资情况。资料来自官方博客、文档、GitHub、Fortune 报道和 Wikipedia，检索日期 2026-11-04。

## 原始链接

- LangChain 与 LangGraph 1.0 公告（2025-10-22）：https://www.langchain.com/blog/langchain-langgraph-1dot0
- Interrupt 2026 发布汇总（2026-05-14）：https://www.langchain.com/blog/interrupt-2026-overview
- 2026 年 8 月通讯（2026-08-26）：https://www.langchain.com/blog/august-2026-langchain-newsletter
- 2026 年 10 月通讯（2026-10-15）：https://www.langchain.com/blog/october-2026-langchain-newsletter
- Managed Deep Agents 公开测试（2026-08-07）：https://www.langchain.com/blog/managed-deep-agents-is-now-in-public-beta
- Deep Agents 文档：https://docs.langchain.com/oss/python/deepagents/overview
- LangSmith Fleet 发布（2026-03-19）：https://www.langchain.com/blog/introducing-langsmith-fleet
- 产品更名公告（LangGraph Platform → LangSmith Deployment）：https://changelog.langchain.com/announcements/ann_NXVDQVGqbwBqW
- Fortune：LangChain 成为独角兽（2025-10-20）：https://fortune.com/2025/10/20/exclusive-early-ai-darling-langchain-is-now-a-unicorn-with-a-fresh-125-million-in-funding/
- Wikipedia：https://en.wikipedia.org/wiki/LangChain
- GitHub 仓库：https://github.com/langchain-ai/langchain

## 官方原文摘录

LangChain 与 LangGraph 1.0 公告：

- "The new `create_agent` function uses LangGraph under the hood to run this loop."
- "Middleware defines a set of hooks that allow you to customize behavior in the agent loop"
- "Legacy functionality moves to `langchain-classic` for backwards compatibility."
- "LangChain agents are built on LangGraph, so you're not locked in."
- "These 1.0 releases mark our commitment to stability for our open source libraries and no breaking changes until 2.0."

Interrupt 2026：

- "Each sandbox runs in a hardware-virtualized microVM, isolated from your services and from other sandboxes."
- "LangChain Labs is an applied research effort focused on continual learning for agents."

Deep Agents：

- "Deep Agents is the agent harness for complex, multi-step work."
- "Today, Managed Deep Agents is available in public beta."（2026-08-07）
- "This release simplifies the base harness, resulting in 65% fewer base input tokens at comparable performance."（v0.7）

LangSmith：

- "LLM Gateway sits between your agents and the models they call."
- "LangChain now supports FastMCP through the `langchain.mcp` namespace."（LangChain v1.4.0）

GitHub 仓库描述："The agent engineering platform."

## 检索要点（二手整理，非逐字）

### 公司与融资

- 2022-10：Harrison Chase 在机器学习创业公司 Robust Intelligence 任职期间以开源项目形式发布 LangChain；Ankush Gola 后与其共同创办公司。
- 2023-04：公司成立；Benchmark 领投 1000 万美元种子轮，约一周后 Sequoia 领投新一轮。
- 2024-02：发布闭源的 LangSmith（可观测性与评测平台），宣布 Sequoia 领投的 2500 万美元 A 轮，估值 2 亿美元。
- 2025-10-20：1.25 亿美元 B 轮，估值 12.5 亿美元，IVP 领投；Sequoia、Benchmark 跟投，新投资方包括 CapitalG、Sapphire Ventures、ServiceNow Ventures、Workday Ventures、Cisco Investments、Datadog、Databricks、Frontline。TechCrunch 2025-07 估计 ARR 1200–1600 万美元，公司称该估计偏低，尚未盈利。客户包括 Cisco、Replit、Clay、Cloudflare、Workday、ServiceNow。
- 二级市场平台 Forge Global 2026-09 列出约 30 亿美元估值，但公司未宣布 C 轮，属估计值。

### 开源框架

- **LangChain**（Python / JS，MIT 协议，GitHub 约 14.9 万星）：2023 Q3 推出 LCEL（声明式组合链），2023-10 推出 LangServe。2025-10-22 发布 1.0：以 `create_agent` 为核心，底层运行在 LangGraph 上；中间件（middleware）在 Agent 循环的每一步提供钩子，内置人工审批、摘要、PII 脱敏等；标准内容块（standard content blocks）统一各厂商输出的推理、引用、工具调用格式；旧功能移入 `langchain-classic`；要求 Python 3.10+。承诺 2.0 之前无破坏性变更。2026-10 的 v1.4.0 通过 `langchain.mcp` 命名空间支持 FastMCP。集成以独立包形式发布（模型、嵌入、工具、向量库连接器）。
- **LangGraph**：底层 Agent 编排运行时，提供持久状态、内置持久化（checkpoint）、人工介入控制。2024 年推出，2025-10-22 发布 1.0；唯一明显变更是弃用 `langgraph.prebuilt`，其中的 `create_react_agent` 改由 `langchain.agents` 的 `create_agent` 取代。
- **Deep Agents**（`deepagents` 包）：建立在 LangChain 与 LangGraph 之上的 Agent harness，面向复杂多步任务，提供任务规划、虚拟文件系统、子 Agent 委派、持久记忆、技能加载、敏感操作人工审批等能力。v0.6（2026-05）加入代码解释器式的程序化工具调用、类型化流式输出、React/Vue/Svelte/Angular 前端流式支持和 `DeltaChannel`；v0.7（2026-08）基础输入 token 减少 65%。

### 商业平台 LangSmith

- 2024-02 发布，覆盖可观测性（追踪）、评测、部署。2025-05-14 LangGraph Platform GA；2025-10 更名为 LangSmith Deployment，LangGraph Studio 更名为 LangSmith Studio（仅改名，价格与 API 不变）。
- 2025-10 推出 Agent Builder（无代码 Agent）；2026-03-19 更名并扩展为 LangSmith Fleet，提供权限、Agent 身份与凭证、人工审批收件箱、Slack 机器人。
- 2026-05-14 Interrupt 大会：LangSmith Engine（公开测试，自动聚类线上失败、诊断根因并提出修复与评测）、SmithDB（新的可观测性数据库，最高 15 倍加速）、Managed Deep Agents（托管运行时）、LangSmith Sandboxes GA（硬件虚拟化 microVM）、Context Hub（管理 AGENTS.md、技能、策略等文件的版本）、LLM Gateway（私测，花费上限、PII 与密钥脱敏）、Fleet 五个预置 Agent（编码 Agent 基于 Open SWE）、Developer / Plus 套餐免费模型额度（Fireworks 推理）、LangChain Labs（Agent 持续学习研究，合作方含 Harvey、NVIDIA、Prime Intellect、Fireworks、Baseten）。
- 2026-08：Managed Deep Agents 公开测试（08-07，仅 LangSmith Cloud 美国区，CLI 优先）；LLM Gateway 公开测试（成本控制、限流、模型回退、敏感数据处理）；BYOC 在 AWS 上 GA。
- 2026-09：Managed Deep Agents v0.8 内置 Parallel 网页搜索；LangSmith Engine v2。
- 2026-10（Interrupt 纽约 / 伦敦）：Managed Deep Agents v0.9（按次配置、Slack 集成、用户级记忆与工具、定时任务）、Engine v2（红队测试、检测低效 Agent 行为、自动测试修复方案）、AI Search（语义搜索追踪）、Trajectories（主 Agent 与子 Agent 时间线视图）、Custom Apps、Fine-Tuning（用线上轨迹经 Baseten 或 Fireworks 微调模型）。另有 v0.10 加入浏览器操作和异步子 Agent 的说法（2026-10-29），未在一手页面核实。

### 竞品（检索中常见）

LlamaIndex、CrewAI、Vercel AI SDK、OpenAI Agents SDK、Mastra、Microsoft Agent Framework。
