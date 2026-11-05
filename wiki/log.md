<!-- llm-wiki-log-header-start -->
# Wiki 操作日志

每次摄入、Lint 运行和维护操作都会自动记录在这里。推荐使用**操作历史**面板获得更好的可视化呈现：
- Cmd+P → "查看摄入历史"
- 或从 设置 → 自动维护 → 操作历史 进入

---
> 操作日志，按时间倒序记录所有 wiki 操作。

## [2026-11-05] ingest | 推理引擎与本地部署调研

- 来源：vLLM、SGLang、TensorRT-LLM、NVIDIA Dynamo、llm-d、llama.cpp、Ollama、LM Studio（lms）、DeepSpeed、Megatron-LM、EAGLE 的 GitHub README 与文档，GGUF 规范，vLLM 发布博客、LMSYS SGLang 博客、Hugging Face「GGML and llama.cpp join HF」博客原文，PyPI 版本元数据；融资与公司信息来自 TechCrunch、SiliconANGLE、Business Wire 等报道（原文未能打开，标注为二手）（`raw/推理引擎与本地部署调研-2026-11.md`）
- 新建来源页 `sources/inference-engines-survey-2026-11`
- 新建 11 个实体页：`sglang`、`tensorrt-llm`、`nvidia-dynamo`、`llm-d`、`llama-cpp`（含 ggml）、`ollama`、`lm-studio`、`deepspeed`、`megatron-lm`、`inferact`、`radixark`
- 新建 4 个概念页：`kv-cache`、`speculative-decoding`、`disaggregated-serving`、`gguf`
- 重写 `vllm`：去掉种子标记，补能力、时间线、Inferact
- 更新 `nvidia`、`hugging-face`（ggml.ai 加入）、`pytorch`（PyTorch Foundation 托管 vLLM / DeepSpeed）、`microsoft`（DeepSpeed）、`quantization`、`anthropic-messages-api`（Ollama、LM Studio、vLLM 链接），补 sources
- 更新 L3 地图页

## [2026-11-05] ingest | Claude 生态可独立使用的项目与模块调研

- 来源：anthropics、anthropic-experimental、safety-research、modelcontextprotocol、agentskills 组织的 GitHub 仓库元数据与 README，code.claude.com 的第三方部署、LLM 网关、网关兼容、Claude apps gateway、自托管环境、数据使用、Agent SDK 文档，npm / PyPI 元数据，Ollama 与 DeepSeek 的 Anthropic 兼容文档，Petri 捐赠公告，Claude Code 源码泄露报道（`raw/Claude独立可用模块调研-2026-11.md`）
- 新建来源页 `sources/claude-independent-modules-survey-2026-11`（含依赖分级）
- 新建 4 个实体页：`claude-agent-sdk`、`sandbox-runtime`、`circuit-tracer`（含 jacobian-lens）、`petri`（含 Bloom）
- 新建 3 个概念页：`anthropic-messages-api`（兼容端点与网关）、`mcp-bundles`、`claude-constitution`
- 更新 `claude-code`（补协议、脱离 Anthropic 的三档用法、遥测开关、时间线）、`anthropic`（补开源与依赖分级、时间线）、`claude`、`agent-skills`（渐进披露、skills 仓库协议、治理）、`model-context-protocol`（AAIF 治理与协议迁移）；`openai-agents-sdk`、`codex-app-server` 的竞品补链接
- 更新 L3、L4、X 地图页

## [2026-11-04] ingest | OpenAI Developers 可独立使用模块调研

- 来源：developers.openai.com 与 learn.chatgpt.com 的 Codex、Agents SDK、ChatKit、Plugins、Agentic Commerce、Evals、SDK 文档，openai 组织下 GitHub 仓库元数据，PyPI 元数据，AAIF 成立公告、gpt-oss-safeguard 与 Promptfoo 收购报道（`raw/OpenAI-Developers独立可用模块调研-2026-11.md`）
- 新建来源页 `sources/openai-developers-survey-2026-11`（含依赖分级）
- 新建 7 个实体页：`gpt-oss`（含 gpt-oss-safeguard）、`openai-agents-sdk`、`codex-cli`、`codex-app-server`、`chatkit`、`promptfoo`、`tiktoken`
- 新建 4 个概念页：`harmony-response-format`、`agents-md`、`agent-skills`、`agentic-commerce-protocol`
- 更新 `openai`（补开发者平台依赖分级、时间线与来源）、`gpt`（补 gpt-oss）、`mcp-extensions`（补 MCP Apps 在 ChatGPT 中的实现）；`langchain`、`langgraph`、`deep-agents`、`mastra`、`mastra-code`、`vercel-ai-sdk` 的竞品改为链接
- 更新 L2、L3、L4 地图页

## [2026-11-04] ingest | Bun 深度调研

- 来源：Bun 官网与 GitHub、Bun 1.2 / 1.3 / 1.4 / v1.4.3 / v1.4.4 发布文、Bun is joining Anthropic、Rewriting Bun in Rust、Anthropic 收购公告、Vercel 支持公告、Andrew Kelley 博文、Wikipedia、DevClass（`raw/Bun深度调研-2026-11.md`）
- 新建来源页 `sources/bun-survey-2026-11`
- 新建 3 个实体页：`bun`（组件与版本时间线）、`oven`（公司与融资）、`jarred-sumner`
- 新建 2 个概念页：`javascript-runtime`（Node.js / Deno / Bun 对比）、`agent-driven-code-migration`（以 Bun 的 Zig → Rust 重写为例）
- 更新 `anthropic`、`claude-code`（补收购、依赖 Bun、时间线与来源），`vercel`（补 Bun 运行时支持）
- 更新 L4、X 地图页

## [2026-11-04] ingest | Java Agent 开发生态调研

- 来源：Spring AI 2.0 GA / 2.1.0-M1 公告、LangChain4j / Embabel / Koog / Spring AI Alibaba / MCP Java SDK 仓库、Google ADK for Java 1.0 公告、AgentScope Java 文档、A2A Java SDK 1.0.0.Final 公告、InfoQ、Maven Central 元数据（`raw/Java-Agent开发生态调研-2026-11.md`）
- 新建来源页 `sources/java-agent-ecosystem-survey-2026-11`
- 新建 10 个实体页：`spring-ai`、`langchain4j`、`embabel`、`google-adk`、`koog`、`jetbrains`、`agentscope`、`spring-ai-alibaba`、`mcp-java-sdk`、`a2a-java-sdk`
- 新建 3 个概念页：`java-agent-development`（三层格局与选型）、`agent2agent-protocol`、`goal-oriented-action-planning`
- 更新 `model-context-protocol`、`agent-harness`、`ai-agent`（补 Java 示例与来源），`alibaba`、`langchain`、`google-deepmind`（补链接）
- 更新 L4、X 地图页

## [2026-11-04] ingest | Mastra 生态深度调研

- 来源：GitHub 仓库、官方文档、Show HN（1.0）、Observational Memory 研究文章、Mastra Code / Agent Controller / MCP / Launch / Knowledge 公告、平台计费说明、A 轮报道（`raw/Mastra生态深度调研-2026-11.md`）
- 新建来源页 `sources/mastra-ecosystem-survey-2026-11`
- 新建 5 个实体页：`mastra`（框架与原语）、`mastra-inc`（公司与融资）、`mastra-platform`（托管平台与套餐）、`mastra-code`、`mastra-factory`
- 新建概念页 `observational-memory`
- 更新 `agent-harness`、`model-context-protocol`（补 Mastra 示例与来源），`vercel-ai-sdk`、`langchain`、`langgraph`、`langsmith`（竞品改为链接）
- 更新 L4、L5、X 地图页

## [2026-11-04] ingest | LangChain 生态深度调研

- 来源：LangChain / LangGraph 1.0 公告、Interrupt 2026 汇总、2026-08 与 2026-10 通讯、Deep Agents 文档、Fortune 融资报道、Wikipedia（`raw/LangChain生态深度调研-2026-11.md`）
- 新建来源页 `sources/langchain-ecosystem-survey-2026-11`
- 重写 `langchain`：去掉种子标记，补 1.0 变化（create_agent、中间件、标准内容块、langchain-classic）与时间线
- 新建 4 个实体页：`langchain-inc`（公司与融资）、`langgraph`、`langsmith`（产品模块与时间线）、`deep-agents`
- 新建概念页 `agent-harness`；`ai-agent` 补链接与来源
- 更新 L4、X 地图页

## [2026-11-04] ingest | Vercel 开源框架的服务依赖调研

- 来源：Next.js 自托管文档、Adapter API 公告、AI SDK / Workflow DevKit / Turborepo 文档等（`raw/Vercel开源框架服务依赖调研-2026-11.md`）
- 新建来源页 `sources/vercel-oss-dependency-survey-2026-11`
- 新建 5 个实体页：`vercel`（含开源模块四级依赖分级）、`nextjs`、`vercel-ai-sdk`、`workflow-devkit`、`turborepo`
- 更新 L4、X 地图页

## [2026-11-04] ingest | MCP 规范 2026-07-28 版

- 来源：官方规范、变更日志、扩展总览（`raw/MCP规范-2026-07-28.md`）
- 新建来源页 `sources/mcp-spec-2026-07-28`
- 新建 3 个概念页：`mcp-request-flow`（7 阶段流程、新旧对照、错误码、弃用清单）、`multi-round-trip-requests`、`mcp-extensions`
- 重写 `model-context-protocol`：去掉种子标记，补充版本演进表，有来源支撑
- 更新 L4 地图页和 `anthropic` 时间线

## [2026-11-04] init | 建立 AI 生态知识库骨架

- 新建 7 个层级地图页（`maps/`）、`overview`、`index`、`conventions`、`schema/config`
- 新建 **23 个实体页**和 **10 个概念页**，全部为种子页面（`origin: claude-seed`，`reviewed: false`），内容截至 2026-06，待用真实来源核实
- 新建 `templates/` 下的手写模板


## [2026-11-04 05:08] Wiki 维护报告


> Wiki 状态概览：共 46 个页面，7 个缺失别名，重复 0 个，断链 7 个（其中 0 个涉及重复页面），孤立 1 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 1 个。本次 Lint 耗时 3 秒

> 检测到 7 个页面缺少别名

### 缺失别名的页面（程序检测）[共 7 个]

- [[entities/vllm]]
- [[entities/pytorch]]
- [[entities/openai]]
- [[entities/langchain]]
- [[entities/cursor]]
- [[entities/cuda]]
- [[entities/claude-code]]

### 断链（程序检测）[共 7 个]

- [[overview]] → **maps/L0-算力与硬件\**（页面不存在）
- [[overview]] → **maps/L1-数据\**（页面不存在）
- [[overview]] → **maps/L2-基础模型\**（页面不存在）
- [[overview]] → **maps/L3-训练与推理\**（页面不存在）
- [[overview]] → **maps/L4-开发工具与Agent\**（页面不存在）
- [[overview]] → **maps/L5-应用\**（页面不存在）
- [[overview]] → **maps/X-横切主题\**（页面不存在）

### 标签越界（程序检测）[共 1 个]

- [[sources/mcp-spec-2026-07-28]] — 无效：mcp, specification

### 孤立页面（程序检测）[共 1 个]

- [[conventions]] — 无其他 Wiki 页面链接至此




## [2026-11-04 05:25] Wiki 维护报告


> Wiki 状态概览：共 46 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 4 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。




## [2026-11-04 14:39] Wiki 维护报告


> Wiki 状态概览：共 58 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 5 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。




## [2026-11-04 15:18] Wiki 维护报告


> Wiki 状态概览：共 65 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 5 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。




## [2026-11-04 22:16] Wiki 维护报告


> Wiki 状态概览：共 79 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 5 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。




## [2026-11-05 08:21] Wiki 维护报告


> Wiki 状态概览：共 105 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 9 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。




## [2026-11-05 08:22] Wiki 维护报告


> Wiki 状态概览：共 105 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 7 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。


