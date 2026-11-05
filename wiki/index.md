# Wiki Index

> 自动生成的知识库目录

> Note: Text in backticks after page names shows aliases — alternative names, abbreviations, or translations.


## 实体

- [[entities/petri|petri]] `aliases: Petri, Inspect Petri, Bloom, Petri 与 Bloom` `source: claude-independent-modules-survey-2026-11` - [[entities/anthropic|Anthropic]] 开源的对齐审计工具：用一个“审计模型”自动和被测模型进行多轮对话，检测欺骗、谄媚、奖励投机、自我保护等不良行为。2025-10 发布，
- [[entities/circuit-tracer|circuit-tracer]] `aliases: circuit-tracer, Circuit Tracer, 电路追踪, 归因图工具` `source: claude-independent-modules-survey-2026-11` - 开源的可解释性库，用来在**开放权重模型**上画“归因图”（attribution graph），也就是找出模型从输入到某个输出经过了哪些内部特征。方法来自 [[entities/anthropic|
- [[entities/sandbox-runtime|sandbox-runtime]] `aliases: Sandbox Runtime, Anthropic Sandbox Runtime, srt, @anthropic-ai/sandbox-runtime` `source: claude-independent-modules-survey-2026-11` - [[entities/anthropic|Anthropic]] 开源的轻量沙箱工具，在操作系统层面限制任意进程能读写哪些文件、能连哪些网络，不需要容器。它是 [[entities/claude-co
- [[entities/claude-agent-sdk|claude-agent-sdk]] `aliases: Claude Agent SDK, Claude Code SDK, claude-agent-sdk, @anthropic-ai/claude-agent-sdk` `source: claude-independent-modules-survey-2026-11` - [[entities/anthropic|Anthropic]] 把 [[entities/claude-code|Claude Code]] 的 Agent 循环做成库，供开发者嵌进自己的程序，原名
- [[entities/tiktoken|tiktoken]] `aliases: tiktoken` `source: openai-developers-survey-2026-11` - [[entities/openai|OpenAI]] 开源的 BPE 分词器，MIT 协议，Rust 内核加 Python 接口，用来在本地计算文本对应 OpenAI 模型的 token 数和切分方式
- [[entities/promptfoo|promptfoo]] `aliases: Promptfoo, promptfoo` `source: openai-developers-survey-2026-11` - 开源的 LLM 应用评测与红队测试工具，MIT 协议，TypeScript 编写（约 2.7 万星），也有 pip 包装。用 `promptfooconfig.yaml` 写提示、模型提供商和测试用例
- [[entities/chatkit|chatkit]] `aliases: ChatKit, OpenAI ChatKit, chatkit-js, chatkit-python` `source: openai-developers-survey-2026-11` - [[entities/openai|OpenAI]] 在 2025-10 DevDay 推出的嵌入式聊天界面套件，用来把 Agent 对话界面放进自己的网站。分前后端两部分：前端 `chatkit-j
- [[entities/codex-app-server|codex-app-server]] `aliases: Codex App Server, codex app-server, Codex SDK, @openai/codex-sdk` `source: openai-developers-survey-2026-11` - 把 [[entities/codex-cli|Codex CLI]] 的 Agent 内核嵌入到其他程序的接口层，源码在 `openai/codex` 仓库的 `codex-rs/app-server
- [[entities/codex-cli|codex-cli]] `aliases: Codex CLI, OpenAI Codex CLI, @openai/codex` `source: openai-developers-survey-2026-11` - [[entities/openai|OpenAI]] 开源的终端编码 Agent，在本机读写代码、执行命令，Apache-2.0 协议，仓库 `openai/codex`（约 13 万星）。最初用 T
- [[entities/openai-agents-sdk|openai-agents-sdk]] `aliases: OpenAI Agents SDK, Agents SDK, openai-agents` `source: openai-developers-survey-2026-11` - [[entities/openai|OpenAI]] 开源的轻量 [[concepts/ai-agent|AI Agent]] 框架，有 Python（`openai-agents`）和 TypeSc
- [[entities/gpt-oss|gpt-oss]] `aliases: gpt-oss, gpt-oss-120b, gpt-oss-20b, gpt-oss-safeguard` `source: openai-developers-survey-2026-11` - [[entities/openai|OpenAI]] 在 2025-08 发布的开放权重推理模型家族，Apache-2.0 协议，是 OpenAI 自 GPT-2 以来第一次放出语言模型权重。两个尺寸
- [[entities/jarred-sumner|jarred-sumner]] `aliases: Jarred Sumner` `source: bun-survey-2026-11` - [[entities/bun|Bun]] 的作者，[[entities/oven|Oven]] 公司创始人。Bun 起步时，他把 esbuild 的 JavaScript / TypeScript 转
- [[entities/oven|oven]] `aliases: Oven, Oven Inc., oven-sh` `source: bun-survey-2026-11` - [[entities/jarred-sumner|Jarred Sumner]] 为开发 [[entities/bun|Bun]] 成立的公司，总部旧金山，GitHub 组织名 oven-sh。202
- [[entities/bun|bun]] `aliases: Bun, Bun 运行时, oven-sh/bun` `source: bun-survey-2026-11` - 一体化的 JavaScript / TypeScript 工具链：一个二进制同时是运行时、包管理器、测试运行器和打包器，分别对标 Node.js、npm / pnpm / Yarn、Jest / Vi
- [[entities/a2a-java-sdk|a2a-java-sdk]] `aliases: A2A Java SDK, a2a-java, org.a2aproject.sdk` `source: java-agent-ecosystem-survey-2026-11` - [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]的官方 Java 实现，由 Red Hat 的 Quarkus 与 WildFly 团队和 G
- [[entities/mcp-java-sdk|mcp-java-sdk]] `aliases: MCP Java SDK, modelcontextprotocol/java-sdk, io.modelcontextprotocol.sdk` `source: java-agent-ecosystem-survey-2026-11` - [[concepts/model-context-protocol|Model Context Protocol（MCP）]]官方的 Java SDK，用来编写 MCP 服务器和客户端，与 [[ent
- [[entities/spring-ai-alibaba|spring-ai-alibaba]] `aliases: Spring AI Alibaba, SAA, spring-ai-alibaba` `source: java-agent-ecosystem-survey-2026-11` - [[entities/alibaba|阿里巴巴]]开源的 Java Agent 框架（Apache-2.0，GitHub 约 1.11 万星），构建在 [[entities/spring-ai|Spr
- [[entities/agentscope|agentscope]] `aliases: AgentScope, AgentScope Java, agentscope-java` `source: java-agent-ecosystem-survey-2026-11` - [[entities/alibaba|阿里巴巴]]开源的 Agent 框架，有 Python 与 Java 两个实现；本页侧重 Java 版（java.agentscope.io）。AgentScop
- [[entities/jetbrains|jetbrains]] `aliases: JetBrains` `source: java-agent-ecosystem-survey-2026-11` - 开发者工具公司，Kotlin 语言和 IntelliJ 系列 IDE 的开发方。在 AI 生态里，它开源了 JVM / Kotlin Multiplatform Agent 框架 [[entities
- [[entities/koog|koog]] `aliases: Koog, Koog for Java, ai.koog` `source: java-agent-ecosystem-survey-2026-11` - [[entities/jetbrains|JetBrains]] 开源的 Agent 框架（Apache-2.0，GitHub 约 4700 星），用 Kotlin 写成，同时提供惯用的 Kotlin
- [[entities/google-adk|google-adk]] `aliases: Google ADK, Agent Development Kit, ADK for Java, adk-java` `source: java-agent-ecosystem-survey-2026-11` - Google 开源的 Agent Development Kit，有 Python、Java、Go、TypeScript、Kotlin 多个语言版本；Python 版是领先实现，新功能通常先在 Pyt
- [[entities/embabel|embabel]] `aliases: Embabel, Embabel Agent Framework, embabel-agent` `source: java-agent-ecosystem-survey-2026-11` - Spring 框架创始人 Rod Johnson 联合创建的 JVM Agent 框架（Apache-2.0，GitHub 约 4500 星），用 Kotlin 写成，Java 也能自然使用。它构建在
- [[entities/langchain4j|langchain4j]] `aliases: LangChain4j, LangChain for Java, quarkus-langchain4j` `source: java-agent-ecosystem-survey-2026-11` - 开源 Java LLM 应用与 Agent 库（Apache-2.0，GitHub 约 1.34 万星），统一接入 20+ 模型厂商和 30+ 嵌入存储，提供声明式 AI Service、工具调用（含
- [[entities/spring-ai|spring-ai]] `aliases: Spring AI, spring-ai` `source: java-agent-ecosystem-survey-2026-11` - Spring 官方的 LLM 应用框架，由 Broadcom 旗下的 Spring 团队维护，提供 ChatClient、Advisor 链、工具调用、结构化输出、对话记忆、向量存储与 RAG、可观测
- [[entities/mastra-factory|mastra-factory]] `aliases: Mastra Factory` `source: mastra-ecosystem-survey-2026-11` - [[entities/mastra-inc|Mastra 公司]]的开源、Agent 驱动的软件交付环境，在用户自己控制的 Web 应用里运行持久编程 Agent，用 [[entities/mastr
- [[entities/mastra-code|mastra-code]] `aliases: Mastra Code, mastracode` `source: mastra-ecosystem-survey-2026-11` - [[entities/mastra-inc|Mastra 公司]]的开源终端（TUI）编程 Agent，2026-02-24 发布，用 [[entities/mastra|Mastra]] 框架构建。
- [[entities/mastra-platform|mastra-platform]] `aliases: Mastra Platform, Mastra Cloud, Mastra Observability` `source: mastra-ecosystem-survey-2026-11` - [[entities/mastra-inc|Mastra 公司]]的闭源托管平台，给用 [[entities/mastra|Mastra]] 框架写的 Agent 提供部署、环境管理、可观测性、告警、
- [[entities/mastra-inc|mastra-inc]] `aliases: Mastra Inc., Mastra 公司` `source: mastra-ecosystem-survey-2026-11` - 总部位于旧金山的 Agent 开发公司，2024 年成立，创始人是 Sam Bhagwat（CEO）、Abhi Aiyer（CTO）和 Shane Thomas（CPO），三人都来自前端框架 Gats
- [[entities/mastra|mastra]] `aliases: Mastra, Mastra 框架, @mastra/core` `source: mastra-ecosystem-survey-2026-11` - [[entities/mastra-inc|Mastra 公司]]开发的开源 TypeScript Agent 框架（npm 核心包 `@mastra/core`），把 Agent、工作流、记忆、RA
- [[entities/deep-agents|deep-agents]] `aliases: Deep Agents, deepagents, Managed Deep Agents` `source: langchain-ecosystem-survey-2026-11` - [[entities/langchain-inc|LangChain 公司]]的开源 [[concepts/agent-harness|Agent harness]]（`deepagents` 包），
- [[entities/langsmith|langsmith]] `aliases: LangSmith, LangSmith Deployment, LangSmith Fleet, LangGraph Platform` `source: langchain-ecosystem-survey-2026-11` - [[entities/langchain-inc|LangChain 公司]]的闭源商业平台，也是公司的主要收入来源。2024-02 以 LLM 应用的可观测性（追踪）与评测工具发布，框架无关，不使用
- [[entities/langgraph|langgraph]] `aliases: LangGraph, LangGraph.js` `source: langchain-ecosystem-survey-2026-11` - [[entities/langchain-inc|LangChain 公司]]的底层 Agent 编排框架，把 Agent 或工作流建模为由节点和边构成的状态图，开源，提供 Python 与 JS 实
- [[entities/langchain-inc|langchain-inc]] `aliases: LangChain Inc., LangChain 公司, LangChain, Inc.` `source: langchain-ecosystem-survey-2026-11` - 总部位于美国的 Agent 工程公司，由 Harrison Chase 与 Ankush Gola 创办。Chase 2022-10 在 Robust Intelligence 任职时发布开源框架 [
- [[entities/workflow-devkit|workflow-devkit]] `aliases: Workflow DevKit, WDK, useworkflow` `source: vercel-oss-dependency-survey-2026-11` - [[entities/vercel|Vercel]] 开源的持久化工作流框架（npm 包 `workflow`），用 `"use workflow"` 和 `"use step"` 指令把普通 Typ
- [[entities/vercel|vercel]] `aliases: Vercel, Vercel Inc.` `source: vercel-oss-dependency-survey-2026-11` - 美国前端云平台公司，前身为 ZEIT（2015 年由 Guillermo Rauch 创立，2020 年更名）。商业模式是“开源框架 + 托管平台”：维护 [[entities/nextjs|Next
- [[entities/vercel-ai-sdk|vercel-ai-sdk]] `aliases: AI SDK, Vercel AI SDK` `source: vercel-oss-dependency-survey-2026-11` - [[entities/vercel|Vercel]] 维护的 TypeScript LLM 开发库（npm 包 `ai`），Apache-2.0 协议。核心层（AI SDK Core）统一了文本生成、
- [[entities/turborepo|turborepo]] `aliases: Turborepo, turbo` `source: vercel-oss-dependency-survey-2026-11` - JavaScript / TypeScript monorepo 构建系统，用 Rust 编写，MIT 协议，2021-12 被 [[entities/vercel|Vercel]] 收购。它按任务图
- [[entities/nextjs|nextjs]] `aliases: Next.js, NextJS` `source: vercel-oss-dependency-survey-2026-11` - [[entities/vercel|Vercel]] 维护的 React 全栈框架，MIT 协议，支持服务端组件、流式渲染、ISR、Cache Components、Server Functions 
- [[entities/vllm|vllm]] `aliases: vLLM` - 源自 UC Berkeley 的开源 LLM 推理与服务引擎，核心是 PagedAttention 显存管理，大幅提升吞吐量，是部署 [[entities/llama|Llama]]、[[entiti
- [[entities/qwen|qwen]] `aliases: 通义千问` - [[entities/alibaba|阿里巴巴]]的模型家族，覆盖从小参数到大型 [[concepts/mixture-of-experts|MoE]] 的多种尺寸，以及代码、视觉、语音等分支；多数以
- [[entities/pytorch|pytorch]] `aliases: PyTorch, torch` - 主流深度学习框架，起源于 [[entities/meta-ai|Meta]]，2022 年起由 Linux Foundation 下的 PyTorch Foundation 托管。研究与工业界训练大模
- [[entities/openai|openai]] `aliases: OpenAI, Open AI` `source: openai-developers-survey-2026-11` - 2015 年成立的 AI 研究与产品公司。推出 [[entities/gpt|GPT]] 系列模型和 ChatGPT（2022-11），后者引爆了生成式 AI 浪潮；2024 年起推出以 o1 为首的
- [[entities/nvidia|nvidia]] `aliases: 英伟达` - GPU 与 AI 加速计算的主导厂商。其数据中心 GPU 与 [[entities/cuda|CUDA]] 软件栈构成大模型训练和推理的事实标准底座，是整个生态最上游的瓶颈环节之一。
- [[entities/mistral-ai|mistral-ai]] `aliases: Mistral` - 2023 年成立于巴黎的欧洲模型公司，早期以小而强的开放权重模型和 Mixtral（[[concepts/mixture-of-experts|MoE]]）著称，同时提供商业 API。
- [[entities/microsoft|microsoft]] `aliases: 微软` - OpenAI 的主要投资方与云合作伙伴，通过 Azure 提供模型服务；旗下 GitHub 推出 [[entities/github-copilot|GitHub Copilot]]。微软研究院提出了
- [[entities/meta-ai|meta-ai]] `aliases: FAIR, Meta` - Meta 的 AI 部门（含 FAIR 研究院）。以开放权重的 [[entities/llama|Llama]] 系列推动了开源模型生态；[[entities/pytorch|PyTorch]] 也起
- [[entities/llama|llama]] `aliases: LLaMA` - [[entities/meta-ai|Meta]] 发布的开放权重模型家族。Llama 2 起允许商用，带动了大量社区微调（[[concepts/lora|LoRA]]）与本地部署工具，是开源 LLM
- [[entities/langchain|langchain]] `aliases: LangChain, LangChain.js, langchain` `source: langchain-ecosystem-survey-2026-11` - [[entities/langchain-inc|LangChain 公司]]维护的开源 LLM 应用与 Agent 开发框架，MIT 协议，有 Python 和 JavaScript/TypeScr
- [[entities/hugging-face|hugging-face]] `aliases: HF, 抱抱脸` - 开源 AI 社区与平台：模型/数据集 Hub、`transformers` 等库。几乎所有开放权重模型（[[entities/llama|Llama]]、[[entities/qwen|Qwen]]、
- [[entities/gpt|gpt]] `aliases: GPT 系列, ChatGPT 模型` `source: openai-developers-survey-2026-11` - [[entities/openai|OpenAI]] 的生成式预训练 Transformer 系列模型，从 GPT-1（2018）到 GPT-4/GPT-5 代，驱动 ChatGPT 与 OpenAI
- [[entities/google-deepmind|google-deepmind]] `aliases: DeepMind, Google AI` - Google 的 AI 研究主体，2023 年由 Google Brain 与 DeepMind 合并而成。负责 [[entities/gemini|Gemini]] 模型家族。Google 研究员 
- [[entities/github-copilot|github-copilot]] `aliases: Copilot` - GitHub（[[entities/microsoft|Microsoft]]）的 AI 编程助手，2021 年预览，是第一个大规模普及的 AI 编程产品，后扩展为聊天与 Agent 模式并支持多家模
- [[entities/gemini|gemini]] `aliases: Google Gemini` - [[entities/google-deepmind|Google DeepMind]] 的原生多模态模型家族，覆盖 Pro / Flash 等档位，深度集成进 Google 搜索、Workspace
- [[entities/deepseek|deepseek]] `aliases: 深度求索` - 总部位于杭州的中国 AI 公司，由量化基金幻方支持。以较低训练成本做出接近一线水平的开放权重模型而闻名，代表作 [[entities/deepseek-r1|DeepSeek-R1]] 与 DeepS
- [[entities/deepseek-r1|deepseek-r1]] `aliases: R1` - [[entities/deepseek|DeepSeek]] 于 2025-01 以 MIT 许可开放权重的[[concepts/reasoning-model|推理模型]]，基于 MoE 架构的 D
- [[entities/cursor|cursor]] `aliases: Cursor, Cursor 编辑器` - Anysphere 公司基于 VS Code 打造的 AI 代码编辑器，可接入 [[entities/claude|Claude]]、[[entities/gpt|GPT]] 等多家模型，以补全、多文
- [[entities/cuda|cuda]] `aliases: CUDA, Compute Unified Device Architecture` - [[entities/nvidia|NVIDIA]] 的 GPU 并行计算平台与编程模型。[[entities/pytorch|PyTorch]]、[[entities/vllm|vLLM]] 等几乎
- [[entities/claude|claude]] `aliases: Claude 模型` `source: claude-independent-modules-survey-2026-11` - [[entities/anthropic|Anthropic]] 的闭源大模型家族，按能力分为 Haiku / Sonnet / Opus 等档位，提供 API、claude.ai 应用及云平台分发。
- [[entities/claude-code|claude-code]] `aliases: Claude Code` `source: bun-survey-2026-11` - [[entities/anthropic|Anthropic]] 的 Agent 式编程工具，可在终端、IDE、桌面与网页中读写代码、运行命令，并通过 [[concepts/model-context
- [[entities/anthropic|anthropic]] `aliases: Anthropic PBC` `source: bun-survey-2026-11` - AI 安全与研究公司，2021 年由 Dario Amodei、Daniela Amodei 等前 OpenAI 成员创立，总部位于旧金山。主力产品是 [[entities/claude|Claude
- [[entities/alibaba|alibaba]] `aliases: Alibaba, 阿里云, 通义` `source: java-agent-ecosystem-survey-2026-11` - 阿里巴巴集团及阿里云，研发 [[entities/qwen|Qwen（通义千问）]] 系列，是全球下载量最大的开放权重模型家族之一，同时通过阿里云提供算力与模型服务。在 Java Agent 开发方向

## 概念

- [[concepts/claude-constitution|claude-constitution]] `aliases: Claude 宪法, Claude's Constitution, Claude 的宪法` `source: claude-independent-modules-survey-2026-11` - [[entities/anthropic|Anthropic]] 公开的一份基础文档，写明希望 [[entities/claude|Claude]] 具备的价值观以及背后的理由，涵盖怎样在保持安全和合
- [[concepts/mcp-bundles|mcp-bundles]] `aliases: MCP Bundles, MCPB, .mcpb, Desktop Extensions, DXT` `source: claude-independent-modules-survey-2026-11` - 一种打包本地 [[concepts/model-context-protocol|MCP]] 服务器的文件格式：`.mcpb` 是一个 zip 包，里面放服务器的全部代码和依赖，再加一份描述服务器及其
- [[concepts/anthropic-messages-api|anthropic-messages-api]] `aliases: Anthropic Messages API, Messages API, Anthropic 兼容接口, /v1/messages, ANTHROPIC_BASE_URL` `source: claude-independent-modules-survey-2026-11` - [[entities/anthropic|Anthropic]] 的模型调用接口格式：客户端向 `/v1/messages` 发送 `system`、`messages`、`tools` 等字段，响应
- [[concepts/agentic-commerce-protocol|agentic-commerce-protocol]] `aliases: Agentic Commerce Protocol, ACP, Agentic Checkout Spec, Delegated Payment Spec` `source: openai-developers-survey-2026-11` - 让 AI Agent 代用户向商家下单的开放协议，2025-09 由 [[entities/openai|OpenAI]] 与 Stripe 联合发布，Apache-2.0，规范站 agenticco
- [[concepts/agent-skills|agent-skills]] `aliases: Agent Skills, 技能, SKILL.md, agentskills.io` `source: openai-developers-survey-2026-11` - 一种给 [[concepts/ai-agent|AI Agent]] 打包能力的开放格式：一个技能就是一个文件夹，里面有说明文件 `SKILL.md`（frontmatter 写名称和描述，正文写操作
- [[concepts/agents-md|agents-md]] `aliases: AGENTS.md, AGENTS.override.md` `source: openai-developers-survey-2026-11` - 放在代码仓库里、写给编码 Agent 看的 Markdown 说明文件，相当于“给 Agent 的 README”：构建命令、测试方法、代码风格、注意事项。由 [[entities/openai|Op
- [[concepts/harmony-response-format|harmony-response-format]] `aliases: harmony 响应格式, harmony response format, OpenAI Harmony, openai-harmony` `source: openai-developers-survey-2026-11` - [[entities/openai|OpenAI]] 为开放权重模型 [[entities/gpt-oss|gpt-oss]] 定义的对话结构格式，规定提示词如何拼接、模型输出如何切分。gpt-oss
- [[concepts/agent-driven-code-migration|agent-driven-code-migration]] `aliases: Agent 驱动的代码迁移, AI 辅助代码迁移, AI 重写, agent-driven code migration` `source: bun-survey-2026-11` - 让多个编程 Agent 并行工作，把大型代码库从一种语言或框架整体移植到另一种。人负责设计流程和验收标准，Agent 负责逐文件翻译、修编译错误和评审。目前规模最大的公开案例是 [[entities/
- [[concepts/javascript-runtime|javascript-runtime]] `aliases: JavaScript 运行时, JavaScript runtime, JS 运行时, 服务端 JavaScript 运行时` `source: bun-survey-2026-11` - 在浏览器之外执行 JavaScript / TypeScript 的程序：一个 JS 引擎（V8 或 JavaScriptCore）加上文件、网络、进程等系统 API 和模块加载器。服务端、命令行工具
- [[concepts/java-agent-development|java-agent-development]] `aliases: Java Agent 开发, JVM Agent 开发, Java AI Agent` `source: java-agent-ecosystem-survey-2026-11` - 在 JVM（Java / Kotlin）上构建 [[concepts/ai-agent|AI Agent]] 的技术栈。2026 年它从“调模型的客户端库”发展成完整的三层：底层是协议 SDK，中间是
- [[concepts/goal-oriented-action-planning|goal-oriented-action-planning]] `aliases: 目标导向行动规划（GOAP）, Goal-Oriented Action Planning, GOAP` `source: java-agent-ecosystem-survey-2026-11` - 源自游戏 AI 的规划方法：给 Agent 一组带前置条件和效果的动作，再给一个目标，由规划器在运行时搜索一条能达成目标的动作序列。[[entities/embabel|Embabel]] 把它用作 
- [[concepts/agent2agent-protocol|agent2agent-protocol]] `aliases: Agent2Agent 协议（A2A）, Agent2Agent, A2A, A2A 协议` `source: java-agent-ecosystem-survey-2026-11` - 让不同框架、不同语言写成的 Agent 互相发现、委派任务和交换结果的开放协议，由 Linux Foundation 托管。它和 [[concepts/model-context-protocol|M
- [[concepts/observational-memory|observational-memory]] `aliases: Observational Memory, 观察式记忆, OM` `source: mastra-ecosystem-survey-2026-11` - [[entities/mastra|Mastra]] 2026-02 提出的 Agent 记忆方法：主 Agent 旁边常驻两个后台 Agent，Observer 把对话历史压缩成一份带日期、带优先级
- [[concepts/agent-harness|agent-harness]] `aliases: Agent Harness, Agent 运行框架, harness` `source: langchain-ecosystem-survey-2026-11` - 包裹在模型外面、让 [[concepts/ai-agent|AI Agent]] 能完成长时多步任务的一整套默认运行环境：工具调用循环之外，还预置规划、文件、上下文管理、子 Agent 和记忆等能力。
- [[concepts/vector-database|vector-database]] `aliases: Vector Database, 向量库` - 以向量嵌入为索引、支持近似最近邻（ANN）检索的数据库，是 [[concepts/rag|RAG]] 与语义搜索的常用存储层。
- [[concepts/transformer|transformer]] `aliases: 变换器, Attention Is All You Need` - 2017 年 Google 论文《Attention Is All You Need》提出的神经网络架构，以自注意力机制取代循环结构，是当今几乎所有大语言模型的基础。
- [[concepts/scaling-laws|scaling-laws]] `aliases: Scaling Laws, 缩放定律` - 描述模型性能随参数量、数据量与算力增长而可预测提升的经验规律。代表工作有 Kaplan 等（2020）与 DeepMind Chinchilla（2022，强调数据与参数应同比扩展）。
- [[concepts/reasoning-model|reasoning-model]] `aliases: Reasoning Model, 思考模型` - 在给出答案前先生成较长思维链、并通过强化学习训练这种能力的模型，把“推理时计算”作为新的扩展维度。代表有 OpenAI o 系列、DeepSeek-R1，以及各家模型的思考模式。
- [[concepts/rag|rag]] `aliases: RAG, Retrieval-Augmented Generation` - 在生成前从外部知识库检索相关内容并放入上下文，让模型基于最新或私有资料作答。概念由 Lewis 等（Meta，2020）提出。
- [[concepts/quantization|quantization]] `aliases: Quantization, 模型量化` - 把模型权重（和激活）从 16/32 位浮点压缩为 8 位、4 位等低精度表示，以减少显存并加速推理，代价是可能的精度损失。
- [[concepts/multi-round-trip-requests|multi-round-trip-requests]] `aliases: MRTR, Multi Round-Trip Requests, InputRequiredResult` `source: mcp-spec-2026-07-28` - [[concepts/model-context-protocol|MCP]] 2026-07-28 版引入的交互模式（SEP-2322），取代服务端主动向客户端发请求的旧做法。服务端需要额外信息时，
- [[concepts/model-context-protocol|model-context-protocol]] `aliases: MCP, 模型上下文协议` `source: mcp-spec-2026-07-28` - [[entities/anthropic|Anthropic]] 于 2024-11 发布的开放协议，基于 JSON-RPC 2.0，统一 AI 应用连接外部工具和数据源的方式，常被比作“AI 的 U
- [[concepts/mcp-request-flow|mcp-request-flow]] `aliases: MCP 流程, MCP 2026-07-28, MCP 无状态协议` `source: mcp-spec-2026-07-28` - [[concepts/model-context-protocol|MCP]] 2026-07-28 版规定的端到端交互流程。最大的变化是**没有了“连接—握手—会话”**：任何一个请求都可以单独发给
- [[concepts/mixture-of-experts|mixture-of-experts]] `aliases: MoE, Mixture of Experts` - 一种稀疏模型架构：每层包含多个“专家”子网络，由路由器为每个 token 只激活其中少数几个，从而在总参数很大的同时控制单次计算量。
- [[concepts/mcp-extensions|mcp-extensions]] `aliases: MCP Extensions, MCP Apps, MCP Tasks, Skills over MCP` `source: mcp-spec-2026-07-28` - [[concepts/model-context-protocol|MCP]] 核心协议之外的可选能力。2026-07-28 版在 `ClientCapabilities` / `ServerCapa
- [[concepts/lora|lora]] `aliases: Low-Rank Adaptation, 低秩适配` - Microsoft 研究者 2021 年提出的参数高效微调方法：冻结原模型，只训练插入的低秩矩阵，大幅降低微调显存与存储成本。
- [[concepts/ai-agent|ai-agent]] `aliases: 智能体, Agent` `source: langchain-ecosystem-survey-2026-11` - 以 LLM 为核心、能自主规划并循环调用工具（搜索、代码执行、API）来完成多步任务的系统。

## 来源

- [[sources/claude-independent-modules-survey-2026-11|claude-independent-modules-survey-2026-11]]
- [[sources/openai-developers-survey-2026-11|openai-developers-survey-2026-11]]
- [[sources/bun-survey-2026-11|bun-survey-2026-11]]
- [[sources/java-agent-ecosystem-survey-2026-11|java-agent-ecosystem-survey-2026-11]]
- [[sources/mastra-ecosystem-survey-2026-11|mastra-ecosystem-survey-2026-11]]
- [[sources/langchain-ecosystem-survey-2026-11|langchain-ecosystem-survey-2026-11]]
- [[sources/vercel-oss-dependency-survey-2026-11|vercel-oss-dependency-survey-2026-11]]
- [[sources/mcp-spec-2026-07-28|mcp-spec-2026-07-28]]
