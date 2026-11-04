---
title: Java Agent 开发生态调研（2026-11）
captured: 2026-11-04
tags: [notes]
---

# Java Agent 开发生态调研（2026-11）

一句话：梳理在 JVM（Java / Kotlin）上开发 AI Agent 的主要框架、协议 SDK 与选型思路，覆盖 Spring AI、LangChain4j（含 Quarkus 集成）、Embabel、Google ADK for Java、JetBrains Koog、AgentScope Java、Spring AI Alibaba、MCP Java SDK、A2A Java SDK。资料来自各项目官方博客、GitHub README、InfoQ 报道和 Maven Central 元数据，检索日期 2026-11-04。

## 原始链接

- Spring AI 2.0.0 GA（2026-06-12）：https://spring.io/blog/2026/06/12/spring-ai-2-0-0-GA-available-now/
- Spring AI 2.1.0-M1（2026-09-25）：https://spring.io/blog/2026/09/25/spring-ai-2-1-0-M1-available-now/
- Spring AI 升级说明：https://docs.spring.io/spring-ai/reference/upgrade-notes.html
- LangChain4j 仓库：https://github.com/langchain4j/langchain4j （发布页 https://github.com/langchain4j/langchain4j/releases ）
- LangChain4j Agentic 讨论（GA 计划）：https://github.com/langchain4j/langchain4j/discussions/4589
- Embabel 仓库：https://github.com/embabel/embabel-agent
- InfoQ：Embabel 1.0（2026-08）：https://www.infoq.com/news/2026/08/embabel-1/
- Google ADK for Java 1.0.0（2026-03-30）：https://developers.googleblog.com/announcing-adk-for-java-100-building-the-future-of-ai-agents-in-java/
- Koog 仓库：https://github.com/JetBrains/koog
- Koog 1.0 公告（2026-05）：https://blog.jetbrains.com/ai/2026/05/koog-1-0-is-out-stable-core-better-interop-and-multiplatform-observability/
- Koog for Java（2026-03）：https://blog.jetbrains.com/ai/2026/03/koog-comes-to-java/
- AgentScope Java 文档：https://java.agentscope.io/
- AgentScope Java 1.0 发布（阿里云社区）：https://www.alibabacloud.com/blog/agentscope-java-v1-0-has-been-released-allowing-java-developers-to-easily-build-enterprise-level-agentic-applications_602736
- Spring AI Alibaba 仓库：https://github.com/alibaba/spring-ai-alibaba
- Spring AI Alibaba 1.1.2.0 发布：https://java2ai.com/en/blog/saa-1120-release/
- MCP Java SDK 仓库：https://github.com/modelcontextprotocol/java-sdk
- Spring AI 对 MCP 2026-07-28 的支持请求：https://github.com/spring-projects/spring-ai/issues/6954
- A2A Java SDK 1.0.0.Final（2026-06-10）：https://quarkus.io/blog/a2a-java-sdk-1-0-0-final-released/
- Semantic Kernel for Java Agents API RC（2025-05-06）：https://devblogs.microsoft.com/agent-framework/preview-release-semantic-kernel-for-java-agents-api/
- Maven Central 元数据：https://repo1.maven.org/maven2/ （各构件的 maven-metadata.xml，2026-11-04 读取）

## 官方原文摘录

Spring AI 2.0 GA：

- "Spring AI 2.0 has been designed to be used with Spring Boot 4.0 / 4.1 and Spring Framework 7.0"
- "Spring AI 2.0 lifts the tool loop into the advisor chain as a first-class, composable component."
- "Streamable HTTP is now the default, replacing the deprecated SSE transport."

Spring AI 2.1.0-M1："with the plan to merge it into Spring AI 3.0 mid next year."

LangChain4j README：

- "The goal of LangChain4j is to simplify integrating LLMs into Java applications."
- "Despite the name, LangChain4j is not a Java port of LangChain (Python) — it is built for Java, not ported to it."

Embabel：

- 仓库描述："Agent framework for the JVM. Pronounced Em-BAY-bel /ɛmˈbeɪbəl/"
- README："Written in Kotlin but offers a natural usage model from Java."
- README（关于 Spring AI）："We build on it, and embrace the Spring component model."
- README 比喻："Spring AI exists at the level of the Servlet API, while Embabel is more like Spring MVC."
- InfoQ 引述："a planner searches for a sequence of actions that satisfies the goal."

Google ADK for Java 1.0：

- "The App class is the new top-level container for an agentic application."
- "The ADK has migrated to use the official A2A Java SDK Client."

Koog README："Koog is a Kotlin-based framework designed to build and run AI agents entirely in idiomatic Kotlin and Java API."

AgentScope Java 文档："The Java Harness requires JDK 17 or later and credentials for your chosen model."

Spring AI Alibaba：

- 仓库描述："Agentic AI Framework for Java Developers"
- README："A production-ready framework for building Agentic, Workflow, and Multi-agent applications."

MCP Java SDK 仓库描述："The official Java SDK for Model Context Protocol servers and clients. Maintained in collaboration with Spring AI"

A2A Java SDK 1.0.0.Final："If you’ve been tracking the pre-releases, you can upgrade from CR1 with no breaking changes."

## 整理

### 1. 总体格局

JVM 上的 Agent 开发在 2026 年从“调模型的客户端库”走到“完整 Agent 框架”。可以分三层看：

1. **协议 SDK（最底层）**：MCP Java SDK（工具与上下文）、A2A Java SDK（Agent 之间通信）。几乎所有框架都依赖这两个。
2. **LLM 应用框架（中间层）**：Spring AI、LangChain4j。提供模型抽象、ChatClient / AI Service、工具调用、RAG、记忆、结构化输出、可观测性。
3. **Agent 框架（上层）**：Embabel（构建在 Spring AI 之上）、LangChain4j Agentic 模块、Google ADK for Java、Koog、AgentScope Java、Spring AI Alibaba Agent Framework，以及计划中的 Spring AI Agents。负责规划、多 Agent 编排、长时会话、人工审批、上下文压缩。

另有 Microsoft Semantic Kernel for Java（2025-05 发布 Agents API 候选版）；二手资料称新的 Microsoft Agent Framework 以 .NET / Python 为主，Java 处于 beta，未经一手核实。

### 2. 各项目要点

**Spring AI**（Broadcom 旗下 Spring 团队）

- 2.0.0 GA：2026-06-12。基线 Spring Boot 4.0 / 4.1、Spring Framework 7.0；迁移到 Jackson 3、JSpecify 空安全注解，选项对象改为不可变 builder。
- 工具循环移入 Advisor 链：`ToolCallingAdvisor` 自动注册；`ToolSearchToolCallingAdvisor` 按需逐步暴露工具；`StructuredOutputValidationAdvisor` 在结构化输出校验失败时重试。
- 核心只保留 OpenAI、Anthropic、Amazon Bedrock、Google GenAI、Mistral AI、DeepSeek、Ollama；其他集成交给厂商维护（如 OCI Generative AI、Azure Cosmos DB）。
- MCP：内置 MCP Java SDK 2.0.0（对应规范 2025-11-25）；`mcp-annotations` 并入，提供 `@McpTool`、`@McpResource`、`@McpPrompt`；WebMVC / WebFlux 传输从 SDK 移进 Spring AI；Streamable HTTP 成为默认，SSE 弃用；STDIO 保留。
- 社区项目：spring-ai-session（事件溯源的会话记忆）、spring-ai-agent-utils（Agent Skills、文件 / shell 工具）。
- 1.1.x 线继续面向 Spring Boot 3.5.x，固定 MCP SDK 0.18.3；有用户请求把 MCP SDK 2.x 回移到 Boot 3.5（issue #6954）。
- 2.1.0-M1（2026-09-25）新增 `OpenAiResponsesChatModel`（对接 OpenAI `/v1/responses`）。官方计划 2026-11 以 Spring Projects Experimental 下的独立项目发布 “Spring AI Agents”，2027 年中并入 Spring AI 3.0。截至 2026-11-04 未找到已发布的仓库。
- Maven Central（2026-11-04）：最新正式版 2.0.2，预发布 2.1.0-RC1。

**LangChain4j**（社区项目，Quarkus 与 Spring Boot 都有集成）

- README 强调它不是 Python LangChain 的移植。Apache-2.0，GitHub 约 1.34 万星。
- 统一接入 20+ 模型厂商、30+ 嵌入存储；声明式 AI Service、工具调用、RAG（easy-rag）、护栏、skills、观测与指标。
- Agentic 模块：`langchain4j-agentic`（把 Agent 声明为 Java 接口，用 AgenticScope 共享状态，支持顺序、循环、条件、并行组合及 supervisor 路由）、`langchain4j-agentic-patterns`（如 voting、Confidence Cascade）、`langchain4j-agentic-mcp`、`langchain4j-agentic-a2a`。
- 发布节奏约每月一个小版本；1.23.0（2026-10-28）加入 Ollama decision models、Confidence Cascade 模式、汇总一次 AI Service 调用的观测事件、`langchain4j-test` 里的 LLM 评审与断言、decision agents。
- 成熟度：核心 `langchain4j-core` 1.23.0 为正式版；`langchain4j-agentic` 在 Maven Central 上仍是 `1.23.0-beta33`（2026-11-02）。维护者 2026-02 表示 beta 标签只因 API 仍有小改动，计划晚春 / 初夏去掉，至 2026-11 尚未去掉。
- Quarkus 集成（Quarkiverse 的 quarkus-langchain4j）提供 `quarkus-langchain4j-agentic`。

**Embabel**（Spring 创始人 Rod Johnson 联合创建）

- JVM Agent 框架，用 Kotlin 写成，Java 可自然使用；Apache-2.0，GitHub 约 4500 星。
- 构建在 Spring AI 之上：用 Spring AI 的 `ChatModel`、`@Tool`，MCP 配置走 `spring.ai.mcp`。
- 核心：用类型化领域对象定义 goals、actions、conditions；默认用 GOAP（目标导向行动规划）规划器在运行时搜索满足目标的动作序列，条件变化时可重新规划；规划器可插拔，也支持 Utility AI；可与显式状态机混用；每个动作可指定模型或角色别名（如 best、cheapest）。可消费 MCP 服务器，也可作为 MCP 服务器运行。
- 时间线：2026-04 在 Microsoft JDConf 公开介绍；1.0 GA 约 2026-07（InfoQ 报道 2026-08-03）；Devoxx Belgium 2026 有 v1.5 演讲。Maven Central 最新 1.5.4（2026-10-28）。

**Google ADK for Java**（Agent Development Kit 的 Java 版，另有 Python、Go、TypeScript、Kotlin 版）

- 1.0.0：2026-03-30（Guillaume Laforge 发文）。Python 版是领先实现，新功能通常先在 Python 出现再移植。
- `App` 作为顶层容器，持有根 Agent、全局设置（如事件压缩）和插件；内置 `LoggingPlugin`、`ContextFilterPlugin`、`GlobalInstructionPlugin`。
- 事件压缩：保留近期事件的滑动窗口，较早历史做摘要，控制上下文长度与成本。
- 人工审批：基于 `ToolConfirmation`，工具可暂停执行请求批准。
- 工具：`GoogleMapsTool`、`UrlContextTool`、`ContainerCodeExecutor`、`VertexAiCodeExecutor`、`ComputerUseTool`。
- 会话 / 记忆 / 产物服务：内存版、Vertex AI、Firestore、GCS。
- A2A：改用官方 A2A Java SDK 客户端；`RemoteA2AAgent` 包装远程 Agent，本地 Agent 可通过 A2A `AgentExecutor` 暴露。
- Maven Central 最新 1.14.0（2026-11-02）。ADK for Kotlin 1.0 约 2026-09。

**Koog**（JetBrains）

- 面向 JVM（Java 与 Kotlin）的 Agent 框架，强调可预测、容错、企业级；多平台目标含 JVM、JS、WasmJS、iOS（描述中也提到 Android）。Apache-2.0，GitHub 约 4700 星；JVM 上需 JDK 17+。
- 2026-03 推出 Koog for Java：fluent builder API、线程池执行器、Spring Boot 集成，支持函数式、图、规划三类工作流策略。
- 2026-05 KotlinConf 2026 发布 1.0：稳定核心并承诺 1 年 API 稳定期；HTTP 传输解耦；各目标平台支持 OpenTelemetry。
- 功能：图式工作流、MCP 工具、ACP（Agent Client Protocol）集成、Agent 状态持久化与断点恢复、内置重试、OpenTelemetry 导出到 W&B Weave、Langfuse。
- Maven Central 最新 1.3.0（2026-09-23）。

**AgentScope Java**（阿里巴巴开源 AgentScope 项目的 Java 实现）

- 1.0 约 2025 年末发布，同时发布 AgentScope Runtime（安全沙箱、A2A Agent、部署到阿里云）；支持把 Agent Card 注册到 Nacos。
- 2.0 文档分两部分：AgentScope Harness SDK（自建 Agent 应用）与 AgentScope Service（托管平台），共享 HarnessAgent 内核；HarnessAgent 沿用 ReActAgent 的推理—工具循环；Java 工具与 MCP、子 Agent 委派、每步构建上下文、长历史压缩、按需加载记忆 / skills / 工作文件、持久会话（事件日志与检查点）、本地或沙箱执行工具。需 JDK 17+。
- 官方称在阿里巴巴集团内部 13+ 个业务单元生产使用。
- Maven Central：`agentscope-core` 最新正式版 2.0.4，预发布 2.1.0-BETA1（2026-10-08）。

**Spring AI Alibaba**（阿里巴巴，构建在 Spring AI 之上）

- 仓库描述“Agentic AI Framework for Java Developers”；Apache-2.0，GitHub 约 1.11 万星。
- 三层：Agent Framework（ReactAgent、顺序 / 并行 / 路由 / 循环等预置模式、上下文工程、人工介入）→ Graph（持久化、编排、流式的底层运行时，可导出 PlantUML / Mermaid）→ Spring AI。另有 Admin（可视化开发、观测、评测、MCP 管理，可导出独立 Java 项目）与 Studio（嵌入式调试界面）。
- 1.1 线：ReactAgent 钩子、`AgentTool`（Agent 当工具）、`asNode()`（Agent 嵌入图）、`LlmRoutingAgent`、A2A + Nacos 注册；1.1.2.0 升级到 Spring AI 1.1.2，加入 Agent Skills、并行子 Agent；1.1.2.2 集成 AgentScope、单 Agent handoff 模式。
- Maven Central：agent-framework 最新正式版 1.1.2.x，2.0.0-M1.1 预发布（预计对应 Spring AI 2.x）。

**MCP Java SDK**（MCP 官方 Java SDK，与 Spring AI 团队合作维护）

- 模块：`mcp-bom`、`mcp-core`（STDIO、JDK HttpClient、Servlet 参考实现与 JSON 绑定接口）、`mcp-json-jackson2` / `mcp-json-jackson3`、`mcp`（core + Jackson 3）、`mcp-test`。Spring 相关传输（WebClient、WebFlux、WebMVC）从 2.0 起放到 Spring AI。
- 2.0.0 对应规范 2025-11-25；截至 issue #6954 尚不支持 2026-07-28 版。Maven Central 最新正式版 2.1.0，预发布 2.2.0-M2（2026-11-02）。GitHub 约 3800 星。

**A2A Java SDK**（A2A 项目官方 Java 实现，Red Hat 的 Quarkus 与 WildFly 团队和 Google 合作发起）

- 1.0.0.Final：2026-06-10，首个 GA，对齐 A2A 规范 1.0.0；历经 7 个预发布、17 位贡献者；相对 0.3.x 完全重设计。
- groupId 从 `io.github.a2asdk` 改为 `org.a2aproject.sdk`，包名同步改。
- 传输：JSON-RPC、gRPC、HTTP+JSON/REST 同等支持；参考实现基于 Quarkus，WildFly / Jakarta EE 有社区集成；附带基于 Quarkus 的跨 SDK 合规测试工具（ITK）。
- A2A 协议由 Linux Foundation 托管。Maven Central 最新 1.5.0.Final（2026-11-03）。

### 3. 选型参考（整理者归纳，非官方结论）

- 已在 Spring Boot 4 上、要稳定 API：Spring AI 2.0；需要更强的 Agent 规划时叠加 Embabel。
- 已在 Spring Boot 3.5：Spring AI 1.1.x（注意 MCP SDK 停在 0.18.x）或 LangChain4j。
- Quarkus / 云原生、要声明式接口和多 Agent 模式：LangChain4j + quarkus-langchain4j（agentic 仍 beta）。
- 深度绑定 Google Cloud / Gemini / Vertex AI：ADK for Java。
- Kotlin 优先、多平台（含移动端）或要 1 年 API 稳定承诺：Koog。
- 阿里云 / 通义 / Nacos 体系：Spring AI Alibaba 或 AgentScope Java。
- 跨语言、跨框架的 Agent 互通：A2A Java SDK；工具接入统一走 MCP Java SDK。
