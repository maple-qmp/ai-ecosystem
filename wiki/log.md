<!-- llm-wiki-log-header-start -->
# Wiki 操作日志

每次摄入、Lint 运行和维护操作都会自动记录在这里。推荐使用**操作历史**面板获得更好的可视化呈现：
- Cmd+P → "查看摄入历史"
- 或从 设置 → 自动维护 → 操作历史 进入

---
> 操作日志，按时间正序记录所有 wiki 操作（旧的在前，新记录追加到末尾，与插件写入维护报告的方式一致）。2026-11-05 及以前的手写摄入条目，时间取自对应的 git 提交；提交时间与维护报告的页面数对不上的，不写时间。

## [2026-11-04 04:37] init | 建立 AI 生态知识库骨架

- 新建 7 个层级地图页（`maps/`）、`overview`、`index`、`conventions`、`schema/config`
- 新建 **23 个实体页**和 **10 个概念页**，全部为种子页面（`origin: claude-seed`，`reviewed: false`），内容截至 2026-06，待用真实来源核实
- 新建 `templates/` 下的手写模板

## [2026-11-04 04:37] ingest | MCP 规范 2026-07-28 版

**创建页面**：[[sources/mcp-spec-2026-07-28]], [[concepts/mcp-request-flow]], [[concepts/multi-round-trip-requests]], [[concepts/mcp-extensions]]

**更新页面**：[[concepts/model-context-protocol]], [[maps/L4-开发工具与Agent]], [[entities/anthropic]]

- 来源：官方规范、变更日志、扩展总览（`raw/MCP规范-2026-07-28.md`）
- 新建来源页 `sources/mcp-spec-2026-07-28`
- 新建 3 个概念页：`mcp-request-flow`（7 阶段流程、新旧对照、错误码、弃用清单）、`multi-round-trip-requests`、`mcp-extensions`
- 重写 `model-context-protocol`：去掉种子标记，补充版本演进表，有来源支撑
- 更新 L4 地图页和 `anthropic` 时间线

## [2026-11-04 05:25] Wiki 维护报告


> Wiki 状态概览：共 46 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 4 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。

## [2026-11-04 06:24] ingest | Vercel 开源框架的服务依赖调研

**创建页面**：[[entities/nextjs]], [[entities/turborepo]], [[entities/vercel-ai-sdk]], [[entities/vercel]], [[entities/workflow-devkit]], [[sources/vercel-oss-dependency-survey-2026-11]]

**更新页面**：[[maps/L4-开发工具与Agent]], [[maps/X-横切主题]]

- 来源：Next.js 自托管文档、Adapter API 公告、AI SDK / Workflow DevKit / Turborepo 文档等（`raw/Vercel开源框架服务依赖调研-2026-11.md`）
- 新建来源页 `sources/vercel-oss-dependency-survey-2026-11`
- 新建 5 个实体页：`vercel`（含开源模块四级依赖分级）、`nextjs`、`vercel-ai-sdk`、`workflow-devkit`、`turborepo`
- 更新 L4、X 地图页

## [2026-11-04 06:45] ingest | LangChain 生态深度调研

**创建页面**：[[concepts/agent-harness]], [[entities/deep-agents]], [[entities/langchain-inc]], [[entities/langgraph]], [[entities/langsmith]], [[sources/langchain-ecosystem-survey-2026-11]]

**更新页面**：[[concepts/ai-agent]], [[entities/langchain]], [[maps/L4-开发工具与Agent]], [[maps/X-横切主题]]

- 来源：LangChain / LangGraph 1.0 公告、Interrupt 2026 汇总、2026-08 与 2026-10 通讯、Deep Agents 文档、Fortune 融资报道、Wikipedia（`raw/LangChain生态深度调研-2026-11.md`）
- 新建来源页 `sources/langchain-ecosystem-survey-2026-11`
- 重写 `langchain`：去掉种子标记，补 1.0 变化（create_agent、中间件、标准内容块、langchain-classic）与时间线
- 新建 4 个实体页：`langchain-inc`（公司与融资）、`langgraph`、`langsmith`（产品模块与时间线）、`deep-agents`
- 新建概念页 `agent-harness`；`ai-agent` 补链接与来源
- 更新 L4、X 地图页

## [2026-11-04 14:39] Wiki 维护报告


> Wiki 状态概览：共 58 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 5 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。

## [2026-11-04 15:18] ingest | Mastra 生态深度调研

**创建页面**：[[concepts/observational-memory]], [[entities/mastra-code]], [[entities/mastra-factory]], [[entities/mastra-inc]], [[entities/mastra-platform]], [[entities/mastra]], [[sources/mastra-ecosystem-survey-2026-11]]

**更新页面**：[[concepts/agent-harness]], [[concepts/model-context-protocol]], [[entities/langchain]], [[entities/langgraph]], [[entities/langsmith]], [[entities/vercel-ai-sdk]], [[maps/L4-开发工具与Agent]], [[maps/L5-应用]], [[maps/X-横切主题]]

- 来源：GitHub 仓库、官方文档、Show HN（1.0）、Observational Memory 研究文章、Mastra Code / Agent Controller / MCP / Launch / Knowledge 公告、平台计费说明、A 轮报道（`raw/Mastra生态深度调研-2026-11.md`）
- 新建来源页 `sources/mastra-ecosystem-survey-2026-11`
- 新建 5 个实体页：`mastra`（框架与原语）、`mastra-inc`（公司与融资）、`mastra-platform`（托管平台与套餐）、`mastra-code`、`mastra-factory`
- 新建概念页 `observational-memory`
- 更新 `agent-harness`、`model-context-protocol`（补 Mastra 示例与来源），`vercel-ai-sdk`、`langchain`、`langgraph`、`langsmith`（竞品改为链接）
- 更新 L4、L5、X 地图页

## [2026-11-04 15:18] Wiki 维护报告


> Wiki 状态概览：共 65 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 5 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。

## [2026-11-04 15:31] ingest | Java Agent 开发生态调研

**创建页面**：[[concepts/agent2agent-protocol]], [[concepts/goal-oriented-action-planning]], [[concepts/java-agent-development]], [[entities/a2a-java-sdk]], [[entities/agentscope]], [[entities/embabel]], [[entities/google-adk]], [[entities/jetbrains]], [[entities/koog]], [[entities/langchain4j]], [[entities/mcp-java-sdk]], [[entities/spring-ai-alibaba]], [[entities/spring-ai]], [[sources/java-agent-ecosystem-survey-2026-11]]

**更新页面**：[[concepts/agent-harness]], [[concepts/ai-agent]], [[concepts/model-context-protocol]], [[entities/alibaba]], [[entities/google-deepmind]], [[entities/langchain]], [[maps/L4-开发工具与Agent]], [[maps/X-横切主题]]

- 来源：Spring AI 2.0 GA / 2.1.0-M1 公告、LangChain4j / Embabel / Koog / Spring AI Alibaba / MCP Java SDK 仓库、Google ADK for Java 1.0 公告、AgentScope Java 文档、A2A Java SDK 1.0.0.Final 公告、InfoQ、Maven Central 元数据（`raw/Java-Agent开发生态调研-2026-11.md`）
- 新建来源页 `sources/java-agent-ecosystem-survey-2026-11`
- 新建 10 个实体页：`spring-ai`、`langchain4j`、`embabel`、`google-adk`、`koog`、`jetbrains`、`agentscope`、`spring-ai-alibaba`、`mcp-java-sdk`、`a2a-java-sdk`
- 新建 3 个概念页：`java-agent-development`（三层格局与选型）、`agent2agent-protocol`、`goal-oriented-action-planning`
- 更新 `model-context-protocol`、`agent-harness`、`ai-agent`（补 Java 示例与来源），`alibaba`、`langchain`、`google-deepmind`（补链接）
- 更新 L4、X 地图页

## [2026-11-04 22:16] Wiki 维护报告


> Wiki 状态概览：共 79 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 5 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。

## [2026-11-04 22:22] ingest | Bun 深度调研

**创建页面**：[[concepts/agent-driven-code-migration]], [[concepts/javascript-runtime]], [[entities/bun]], [[entities/jarred-sumner]], [[entities/oven]], [[sources/bun-survey-2026-11]]

**更新页面**：[[entities/anthropic]], [[entities/claude-code]], [[entities/vercel]], [[maps/L4-开发工具与Agent]], [[maps/X-横切主题]]

- 来源：Bun 官网与 GitHub、Bun 1.2 / 1.3 / 1.4 / v1.4.3 / v1.4.4 发布文、Bun is joining Anthropic、Rewriting Bun in Rust、Anthropic 收购公告、Vercel 支持公告、Andrew Kelley 博文、Wikipedia、DevClass（`raw/Bun深度调研-2026-11.md`）
- 新建来源页 `sources/bun-survey-2026-11`
- 新建 3 个实体页：`bun`（组件与版本时间线）、`oven`（公司与融资）、`jarred-sumner`
- 新建 2 个概念页：`javascript-runtime`（Node.js / Deno / Bun 对比）、`agent-driven-code-migration`（以 Bun 的 Zig → Rust 重写为例）
- 更新 `anthropic`、`claude-code`（补收购、依赖 Bun、时间线与来源），`vercel`（补 Bun 运行时支持）
- 更新 L4、X 地图页

## [2026-11-04 23:58] ingest | OpenAI Developers 可独立使用模块调研

**创建页面**：[[concepts/agent-skills]], [[concepts/agentic-commerce-protocol]], [[concepts/agents-md]], [[concepts/harmony-response-format]], [[entities/chatkit]], [[entities/codex-app-server]], [[entities/codex-cli]], [[entities/gpt-oss]], [[entities/openai-agents-sdk]], [[entities/promptfoo]], [[entities/tiktoken]], [[sources/openai-developers-survey-2026-11]]

**更新页面**：[[concepts/mcp-extensions]], [[entities/deep-agents]], [[entities/gpt]], [[entities/langchain]], [[entities/langgraph]], [[entities/mastra-code]], [[entities/mastra]], [[entities/openai]], [[entities/vercel-ai-sdk]], [[maps/L2-基础模型]], [[maps/L3-训练与推理]], [[maps/L4-开发工具与Agent]]

- 来源：developers.openai.com 与 learn.chatgpt.com 的 Codex、Agents SDK、ChatKit、Plugins、Agentic Commerce、Evals、SDK 文档，openai 组织下 GitHub 仓库元数据，PyPI 元数据，AAIF 成立公告、gpt-oss-safeguard 与 Promptfoo 收购报道（`raw/OpenAI-Developers独立可用模块调研-2026-11.md`）
- 新建来源页 `sources/openai-developers-survey-2026-11`（含依赖分级）
- 新建 7 个实体页：`gpt-oss`（含 gpt-oss-safeguard）、`openai-agents-sdk`、`codex-cli`、`codex-app-server`、`chatkit`、`promptfoo`、`tiktoken`
- 新建 4 个概念页：`harmony-response-format`、`agents-md`、`agent-skills`、`agentic-commerce-protocol`
- 更新 `openai`（补开发者平台依赖分级、时间线与来源）、`gpt`（补 gpt-oss）、`mcp-extensions`（补 MCP Apps 在 ChatGPT 中的实现）；`langchain`、`langgraph`、`deep-agents`、`mastra`、`mastra-code`、`vercel-ai-sdk` 的竞品改为链接
- 更新 L2、L3、L4 地图页

## [2026-11-05 00:22] ingest | Claude 生态可独立使用的项目与模块调研

**创建页面**：[[concepts/anthropic-messages-api]], [[concepts/claude-constitution]], [[concepts/mcp-bundles]], [[entities/circuit-tracer]], [[entities/claude-agent-sdk]], [[entities/petri]], [[entities/sandbox-runtime]], [[sources/claude-independent-modules-survey-2026-11]]

**更新页面**：[[concepts/agent-skills]], [[concepts/model-context-protocol]], [[entities/anthropic]], [[entities/claude-code]], [[entities/claude]], [[entities/codex-app-server]], [[entities/openai-agents-sdk]], [[maps/L3-训练与推理]], [[maps/L4-开发工具与Agent]], [[maps/X-横切主题]]

- 来源：anthropics、anthropic-experimental、safety-research、modelcontextprotocol、agentskills 组织的 GitHub 仓库元数据与 README，code.claude.com 的第三方部署、LLM 网关、网关兼容、Claude apps gateway、自托管环境、数据使用、Agent SDK 文档，npm / PyPI 元数据，Ollama 与 DeepSeek 的 Anthropic 兼容文档，Petri 捐赠公告，Claude Code 源码泄露报道（`raw/Claude独立可用模块调研-2026-11.md`）
- 新建来源页 `sources/claude-independent-modules-survey-2026-11`（含依赖分级）
- 新建 4 个实体页：`claude-agent-sdk`、`sandbox-runtime`、`circuit-tracer`（含 jacobian-lens）、`petri`（含 Bloom）
- 新建 3 个概念页：`anthropic-messages-api`（兼容端点与网关）、`mcp-bundles`、`claude-constitution`
- 更新 `claude-code`（补协议、脱离 Anthropic 的三档用法、遥测开关、时间线）、`anthropic`（补开源与依赖分级、时间线）、`claude`、`agent-skills`（渐进披露、skills 仓库协议、治理）、`model-context-protocol`（AAIF 治理与协议迁移）；`openai-agents-sdk`、`codex-app-server` 的竞品补链接
- 更新 L3、L4、X 地图页

## [2026-11-05 08:21] Wiki 维护报告


> Wiki 状态概览：共 105 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 9 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。

## [2026-11-05 08:22] Wiki 维护报告


> Wiki 状态概览：共 105 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 7 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。

## [2026-11-05 13:36] Wiki 维护报告


> Wiki 状态概览：共 117 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 10 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。

## [2026-11-05] ingest | 推理引擎与本地部署调研

**创建页面**：[[concepts/disaggregated-serving]], [[concepts/gguf]], [[concepts/kv-cache]], [[concepts/speculative-decoding]], [[entities/deepspeed]], [[entities/inferact]], [[entities/llama-cpp]], [[entities/llm-d]], [[entities/lm-studio]], [[entities/megatron-lm]], [[entities/nvidia-dynamo]], [[entities/ollama]], [[entities/radixark]], [[entities/sglang]], [[entities/tensorrt-llm]], [[sources/inference-engines-survey-2026-11]]

**更新页面**：[[concepts/anthropic-messages-api]], [[concepts/quantization]], [[entities/hugging-face]], [[entities/microsoft]], [[entities/nvidia]], [[entities/pytorch]], [[entities/vllm]], [[maps/L3-训练与推理]]

- 来源：vLLM、SGLang、TensorRT-LLM、NVIDIA Dynamo、llm-d、llama.cpp、Ollama、LM Studio（lms）、DeepSpeed、Megatron-LM、EAGLE 的 GitHub README 与文档，GGUF 规范，vLLM 发布博客、LMSYS SGLang 博客、Hugging Face「GGML and llama.cpp join HF」博客原文，PyPI 版本元数据；融资与公司信息来自 TechCrunch、SiliconANGLE、Business Wire 等报道（原文未能打开，标注为二手）（`raw/推理引擎与本地部署调研-2026-11.md`）
- 新建来源页 `sources/inference-engines-survey-2026-11`
- 新建 11 个实体页：`sglang`、`tensorrt-llm`、`nvidia-dynamo`、`llm-d`、`llama-cpp`（含 ggml）、`ollama`、`lm-studio`、`deepspeed`、`megatron-lm`、`inferact`、`radixark`
- 新建 4 个概念页：`kv-cache`、`speculative-decoding`、`disaggregated-serving`、`gguf`
- 重写 `vllm`：去掉种子标记，补能力、时间线、Inferact
- 更新 `nvidia`、`hugging-face`（ggml.ai 加入）、`pytorch`（PyTorch Foundation 托管 vLLM / DeepSpeed）、`microsoft`（DeepSpeed）、`quantization`、`anthropic-messages-api`（Ollama、LM Studio、vLLM 链接），补 sources
- 更新 L3 地图页

## [2026-11-05 13:38] ingest | 中国模型生态：月之暗面、智谱、MiniMax、字节跳动时间线调研

**创建页面**：[[entities/bytedance]], [[entities/doubao]], [[entities/glm]], [[entities/kimi]], [[entities/minimax-m]], [[entities/minimax]], [[entities/moonshot-ai]], [[entities/zhipu-ai]], [[sources/bytedance-doubao-survey-2026-11]], [[sources/minimax-survey-2026-11]], [[sources/moonshot-ai-survey-2026-11]], [[sources/zhipu-ai-survey-2026-11]]

**更新页面**：[[concepts/anthropic-messages-api]], [[entities/agentscope]], [[entities/alibaba]], [[entities/claude-code]], [[entities/deepseek]], [[entities/qwen]], [[entities/spring-ai-alibaba]], [[maps/L2-基础模型]], [[maps/X-横切主题]]

- 来源：四家的 Hugging Face 模型卡、许可证与仓库元数据，Kimi K3 博客，ByteDance Seed 2.0 博客，Wikipedia 及其引用的 Bloomberg / TechCrunch / CNBC / Reuters / NYT / SCMP 等报道，上市报道，阿里云百炼 2026-05 峰会报道，AgentScope / Spring AI Alibaba README（`raw/月之暗面-Kimi调研-2026-11.md`、`raw/智谱-GLM调研-2026-11.md`、`raw/MiniMax调研-2026-11.md`、`raw/字节-豆包调研-2026-11.md`）
- 新建 4 个来源页：`sources/moonshot-ai-survey-2026-11`、`sources/zhipu-ai-survey-2026-11`、`sources/minimax-survey-2026-11`、`sources/bytedance-doubao-survey-2026-11`
- 新建 8 个实体页：组织 `moonshot-ai`、`zhipu-ai`、`minimax`、`bytedance`；模型家族 `kimi`、`glm`、`minimax-m`、`doubao`
- 更新 `alibaba`（新增“与其他中国模型公司的关系”：投资、百炼上架第三方模型、框架侧接入）、`agentscope`（新增模型提供方一节）、`spring-ai-alibaba`（新增接入其他中国模型一节）、`qwen`、`deepseek`（竞品与时间线）；`anthropic-messages-api`、`claude-code` 中的 GLM / Kimi / MiniMax 改为链接
- 更新 L2、X 地图页

## [2026-11-05] ingest | 前沿闭源与开放权重旗舰模型时间线调研（核实 L2 种子页）

**创建页面**：[[entities/deepseek-v]], [[entities/grok]], [[entities/mistral-models]], [[entities/muse]], [[entities/xai]], [[sources/frontier-closed-models-survey-2026-11]], [[sources/open-weight-flagships-survey-2026-11]]

**更新页面**：[[entities/alibaba]], [[entities/anthropic]], [[entities/claude]], [[entities/cursor]], [[entities/deepseek-r1]], [[entities/deepseek]], [[entities/gemini]], [[entities/google-deepmind]], [[entities/gpt]], [[entities/llama]], [[entities/meta-ai]], [[entities/mistral-ai]], [[entities/openai]], [[entities/qwen]], [[maps/L2-基础模型]], [[maps/X-横切主题]]

- 来源：OpenAI 模型页与 API changelog，Anthropic 模型总览、弃用表与 Opus 4.8 / Opus 5 / Fable 5.1 模型页，Gemini API 模型页与 changelog，DeepSeek-V4、Qwen3.8、Mistral Large 4 的 Hugging Face 模型卡、许可证与 API 元数据，Wikipedia（GPT-5、Claude、Gemini、Grok、xAI、Llama、Qwen、DeepSeek、Mistral AI 等，经 MediaWiki API 读取）；Gemini 4 Argon 预览、GPT-6 Astra 准入和 Muse Spark Open 只有二手报道（`raw/前沿闭源模型时间线调研-2026-11.md`、`raw/开放权重旗舰模型时间线调研-2026-11.md`）
- 新建 2 个来源页：`sources/frontier-closed-models-survey-2026-11`、`sources/open-weight-flagships-survey-2026-11`
- 新建 5 个实体页：`grok`、`xai`、`muse`、`deepseek-v`、`mistral-models`
- 重写 8 个种子页并改为 `origin: source`：`gpt`、`claude`、`gemini`、`llama`（status 改为 deprecated）、`qwen`、`deepseek`、`deepseek-r1`、`mistral-ai`
- 更新 `openai`、`anthropic`、`google-deepmind`、`meta-ai`、`alibaba`、`cursor`（被 SpaceX 收购）的时间线与 sources
- 更新 L2、X 地图页

## [2026-11-05 21:54] Wiki 维护报告


> Wiki 状态概览：共 140 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 10 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。

## [2026-11-05 22:40] ingest | 多模态与嵌入模型调研：图像、视频、语音、嵌入

**创建页面**：[[concepts/diffusion-model]], [[concepts/embedding]], [[concepts/text-to-speech]], [[entities/baai]], [[entities/bge]], [[entities/black-forest-labs]], [[entities/cohere]], [[entities/cohere-embed]], [[entities/elevenlabs]], [[entities/flux]], [[entities/gpt-image]], [[entities/imagen]], [[entities/kling]], [[entities/kuaishou]], [[entities/openai-embeddings]], [[entities/qwen3-embedding]], [[entities/seedance]], [[entities/sora]], [[entities/stability-ai]], [[entities/stable-diffusion]], [[entities/veo]], [[entities/voyage-ai]], [[entities/voyage-embeddings]], [[entities/whisper]], [[sources/multimodal-embedding-models-survey-2026-11]]

**更新页面**：[[concepts/rag]], [[concepts/vector-database]], [[entities/alibaba]], [[entities/bytedance]], [[entities/gemini]], [[entities/google-deepmind]], [[entities/gpt]], [[entities/openai]], [[entities/qwen]], [[maps/L2-基础模型]]

- 来源：Stable Diffusion / SD3.5、FLUX / FLUX.2、Whisper、Qwen3-Embedding、Qwen3-VL-Embedding、FlagEmbedding（BGE）、CosyVoice、Kokoro、Wan2.2、HunyuanVideo 的 GitHub README（一手）；其余事实来自 VentureBeat、9to5Google、CBS、SiliconANGLE、Bloomberg Law 等报道及 Gemini API changelog、Cohere changelog 的搜索摘要（二手，原文逐条标注）。本次云端环境无法访问 Wikipedia 和厂商文档站（`raw/多模态与嵌入模型调研-2026-11.md`）
- 新建来源页 `sources/multimodal-embedding-models-survey-2026-11`
- 新建 14 个模型家族页：图像 `stable-diffusion`、`flux`、`gpt-image`、`imagen`；视频 `sora`、`veo`、`kling`、`seedance`；语音 `whisper`；嵌入 `openai-embeddings`、`qwen3-embedding`、`bge`、`voyage-embeddings`、`cohere-embed`
- 新建 7 个组织页（layer X）：`stability-ai`、`black-forest-labs`、`kuaishou`、`elevenlabs`、`baai`、`voyage-ai`、`cohere`
- 新建 3 个概念页：`diffusion-model`、`embedding`、`text-to-speech`
- 更新 `openai`、`google-deepmind`、`bytedance`、`alibaba` 的时间线与相关实体；`qwen`、`gemini`、`gpt` 加相关实体链接；`rag`、`vector-database` 只加嵌入相关链接（仍为种子页）
- 更新 L2 地图页：新增「多模态」「嵌入」分组和 3 个概念

## [2026-11-05 22:40] ingest | AI 算力与硬件调研（补 L0 层）

**创建页面**：[[sources/ai-compute-hardware-survey-2026-11]], [[entities/google-cloud]], [[entities/google-tpu]], [[entities/amd]], [[entities/amd-instinct]], [[entities/rocm]], [[entities/huawei]], [[entities/ascend]], [[entities/cann]], [[entities/aws]], [[entities/aws-trainium]], [[entities/azure]], [[entities/groq]], [[entities/cerebras]], [[entities/coreweave]], [[entities/stargate]], [[concepts/ai-accelerator]], [[concepts/hbm]], [[concepts/scale-up-interconnect]], [[concepts/gpu-cloud]]

**更新页面**：[[entities/nvidia]], [[entities/cuda]], [[entities/vllm]], [[entities/sglang]], [[entities/glm]], [[entities/deepseek]], [[entities/deepseek-v]], [[maps/L0-算力与硬件]]

- 来源：Anthropic「Expanding our use of Google Cloud TPUs and services」官方博客（唯一可逐字核对的一手网页），ROCm / HIP / AWS Neuron SDK / vllm-ascend / TorchNPU / vLLM TPU / JAX / Cerebras Model Zoo / groq-python 的 GitHub README，PyPI 版本元数据；芯片规格、发布日期、融资与数据中心规模均来自新闻报道，nvidia.com、amd.com、aws.amazon.com、blogs.microsoft.com、openai.com、groq.com、cerebras.ai、huawei.com、wikipedia.org 在本次调研中被网络策略拦截，无法打开原文，已在素材里逐条标注「二手报道」（`raw/AI算力与硬件调研-2026-11.md`）
- 新建来源页 `sources/ai-compute-hardware-survey-2026-11`
- 新建 16 个实体页：芯片厂商 `amd`、`huawei`、`groq`、`cerebras`；加速器 `google-tpu`、`amd-instinct`、`ascend`、`aws-trainium`；软件栈 `rocm`、`cann`；云与算力 `aws`、`azure`、`google-cloud`、`coreweave`；数据中心项目 `stargate`
- 新建 4 个概念页：`ai-accelerator`、`hbm`、`scale-up-interconnect`、`gpu-cloud`
- 重写 `nvidia`、`cuda` 两个种子页并改为 `origin: source`：补 FY2027 Q2 财务、Vera Rubin、Groq 许可、CUDA 13.0 的 tile 编程模型，补齐竞争对手与上游依赖字段（未设 `reviewed`）
- 补技术上游：`glm` 与 `deepseek`、`deepseek-v` 的 `depends_on` 加入 `ascend`（GLM-Image 称全程在昇腾训练；DeepSeek-V4 的昇腾推理适配与后训练口径分歧已在页面写明）；`vllm`、`sglang` 的硬件一行改为指向 `amd-instinct`、`google-tpu`、`ascend`、`aws-trainium` 的链接
- 更新 L0 地图页的手工列表，按芯片厂商 / 加速器 / 软件栈 / 云与算力服务 / 数据中心项目 / 概念分组

## [2026-11-05 22:45] ingest | 训练与后训练方法调研（L3 训练部分，核实 LoRA / 量化种子页）

**创建页面**：[[sources/training-methods-survey-2026-11]], [[concepts/pretraining]], [[concepts/supervised-fine-tuning]], [[concepts/rlhf]], [[concepts/dpo]], [[concepts/grpo]], [[concepts/rlvr]], [[concepts/knowledge-distillation]], [[entities/trl]], [[entities/unsloth]], [[entities/axolotl]], [[entities/llama-factory]], [[entities/verl]]

**更新页面**：[[concepts/lora]], [[concepts/quantization]], [[concepts/reasoning-model]], [[entities/deepseek-r1]], [[entities/hugging-face]], [[entities/bytedance]], [[maps/L3-训练与推理]]

- 来源：InstructGPT、DPO、DeepSeekMath、DeepSeek-R1、LoRA、QLoRA、GPTQ、AWQ、DAPO、Ai2 open-instruct 的作者仓库 README（论文摘要与引用条目），TRL、Unsloth、Axolotl、LLaMA-Factory、verl、PEFT、bitsandbytes 的 GitHub README，PyPI 版本元数据；arxiv.org 被网络策略拦截，Tülu 3 与 Hinton 蒸馏论文的编号、TRL v1.0 博客说法、Unsloth 公司信息来自搜索摘要（标注为二手）（`raw/训练与后训练方法调研-2026-11.md`）
- 新建来源页 `sources/training-methods-survey-2026-11`
- 新建 7 个概念页：`pretraining`、`supervised-fine-tuning`、`rlhf`、`dpo`、`grpo`、`rlvr`、`knowledge-distillation`
- 新建 5 个实体页（kind: framework）：`trl`、`unsloth`、`axolotl`、`llama-factory`、`verl`
- 重写 `lora`（并入 QLoRA）、`quantization`（补 GPTQ、AWQ、bitsandbytes、QAT），改为 `origin: source`
- `deepseek-r1`、`reasoning-model` 中的 GRPO / RL 加链接；`hugging-face`、`bytedance` 的相关实体追加 TRL、verl
- L3 地图页新增「训练方法」「训练工具」两组

## [2026-11-05 22:46] ingest | AI 应用产品调研（补全 L5 应用层，核实编程类种子页）

**创建页面**：[[entities/chatgpt]], [[entities/claude-app]], [[entities/devin]], [[entities/doubao-app]], [[entities/gemini-app]], [[entities/kimi-app]], [[entities/midjourney]], [[entities/perplexity]], [[entities/suno]], [[entities/windsurf]], [[sources/ai-applications-survey-2026-11]]

**更新页面**：[[entities/claude-code]], [[entities/cursor]], [[entities/github-copilot]], [[maps/L5-应用]]

- 来源：Anthropic 官网新闻（Claude 2、Claude 3.7 Sonnet and Claude Code、Claude 4、Claude Design、SpaceX 算力、Claude Tag、Agent Skills 捐赠）、Claude 定价页与产品页、Claude Code 文档、npm `@anthropic-ai/claude-code` 元数据、GitHub 官方文档仓库中的 Copilot 页面与模型表；其余产品官网被网络策略拦截，来自新闻报道与搜索摘要，标注为二手（`raw/AI应用产品调研-2026-11.md`）
- 新建来源页 `sources/ai-applications-survey-2026-11`
- 新建 10 个实体页（layer: L5，kind: app）：对话助手 `chatgpt`、`claude-app`、`gemini-app`、`doubao-app`、`kimi-app`；搜索 `perplexity`；编程 `devin`、`windsurf`；创意 `midjourney`、`suno`
- 重写 `claude-code`、`cursor`、`github-copilot` 并改为 `origin: source`：补发布日期、套餐、支持模型、收购与营收，`## 我的判断` 未改动
- 未建 Sora、Veo、可灵、FLUX 等生成模型页（由 L2 多模态调研负责），正文中只用普通文字提到
- 更新 L5 地图页：手工列表按对话助手 / 搜索 / 编程 / 创意分组

## [2026-11-05 23:20] update | 用官方原文核实 L0 层（网络解禁后回查）

**更新页面**：[[sources/ai-compute-hardware-survey-2026-11]], [[entities/nvidia]], [[entities/cuda]], [[entities/google-tpu]], [[entities/google-cloud]], [[entities/rocm]], [[entities/amd-instinct]], [[entities/ascend]], [[entities/huawei]], [[entities/aws-trainium]], [[entities/azure]], [[entities/groq]], [[entities/cerebras]], [[entities/coreweave]], [[entities/stargate]]

- 来源：首轮调研被网络策略拦住的厂商域名解禁后逐条回查官方原文——NVIDIA FY2027 Q2 财报新闻稿、CUDA Toolkit 13.0 技术博客、Ironwood 的 Cloud Next 25 发布博客与 2025-11-06 GA 公告及 Cloud TPU 的 TPU7x 文档、Maia 200 官方博客、Trainium3 新闻稿、徐直军 Huawei Connect 2025 演讲全文、Groq 新闻室公告、ROCm 官方版本发布史与 10.1.0 兼容性矩阵、Epoch AI 的 Abilene 数据中心页（`raw/AI算力与硬件调研-2026-11.md` 的「核实记录」一节）
- 更正 `rocm`：当前版本不是 7.2.1，而是 10.1.0（2026-10-05），补全 7.0.0 起的发布日期；10.1.0 的兼容性矩阵尚未列出 MI450，已写入 `amd-instinct`
- 更正 `google-tpu`、`google-cloud`：Ironwood 是 2025-04 Cloud Next 25 发布、2025-11-06 宣布 GA，定位从「专为推理」扩回训练 / RL / 推理兼顾；补 ICI 9.6 Tb/s、42.5 EFLOPS、1.77 PB 共享 HBM、256 / 9,216 两种规模与官方性能口径
- 更正 `nvidia`：Vera Rubin 已满产（财报新闻稿原文「now in full production」），不再写作「2026 下半年量产目标」
- 更正 `cuda`：tile 编程模型是 13.0 本身引入并分两层提供，不只是「铺路」；删去无法核实的「13.1 推出 cuTile Python」
- 更正 `aws-trainium`：补官方口径（算力 4.4 倍、能效 4 倍、访存带宽近 4 倍、延迟四分之一），删去新闻稿里不存在的 NeuronSwitch-v1 与「10 微秒以内」
- 更正 `stargate`：Abilene 已是运行状态，引用 Oracle 2026-09-10 电话会「6 of the 8 campus buildings, representing 618 megawatts and 75% of total capacity」与 Epoch 的 824 MW / 101.9 万张 H100 等效估计，替换 2026-04 的旧快照
- 补细节：`azure`（Maia 200 的 216 GB HBM3e、272 MB SRAM、FP4 10 PFLOPS、750 W、服务 GPT-5.2、Maia SDK）、`ascend`（950DT 的 144 GB / 4 TB/s、2 TB/s 互联、Atlas 950 / 960 SuperPoD 完整规格、UnifiedBus 2.0）、`groq`（官方公告不提金额，200 亿美元出自 CNBC；Simon Edwards 接任 CEO）
- 仍无法核实并已在页面标注为二手：openai.com、investors.coreweave.com、sec.gov、cerebras.ai、amd.com 对自动化客户端返回 403，故 Stargate 站点清单、CoreWeave 财务、Cerebras IPO 与 AMD 的 ROCm 7 性能宣称、MI450 规格仍为新闻报道口径

## [2026-11-06 05:06] ingest | AI 数据层调研：向量库、预训练语料、合成数据与数据公司

**创建页面**：[[sources/ai-data-layer-survey-2026-11]], [[entities/milvus]], [[entities/zilliz]], [[entities/qdrant]], [[entities/pgvector]], [[entities/pinecone]], [[entities/weaviate]], [[entities/chroma]], [[entities/common-crawl]], [[entities/fineweb]], [[entities/the-pile]], [[entities/dolma]], [[entities/scale-ai]], [[entities/surge-ai]], [[entities/mercor]], [[concepts/synthetic-data]], [[concepts/data-labeling]]

**更新页面**：[[entities/hugging-face]], [[concepts/vector-database]], [[concepts/rag]], [[entities/meta-ai]], [[entities/langchain]], [[maps/L1-数据]]

- 来源：Milvus、Qdrant、pgvector、Weaviate、Chroma、FineWeb 2、datatrove、Cosmopedia、transformers、Dolma、The Pile 的 GitHub README 与 CHANGELOG，PyPI 版本元数据；融资、公司与论文数字来自 Business Wire、TechCrunch、Reuters、Bloomberg、Wikipedia 等报道与搜索摘要（huggingface.co、arxiv.org、commoncrawl.org 及公司官网被网络策略拦截，标注为二手）（`raw/AI数据层调研-2026-11.md`）
- 新建来源页 `sources/ai-data-layer-survey-2026-11`
- 新建 14 个实体页：向量库 `milvus`、`qdrant`、`pgvector`、`pinecone`、`weaviate`、`chroma`；语料 `common-crawl`、`fineweb`、`the-pile`、`dolma`；公司 `zilliz`、`scale-ai`、`surge-ai`、`mercor`
- 新建 2 个概念页：`synthetic-data`、`data-labeling`
- 核实重写 3 个种子页并改为 `origin: source`：`hugging-face`（补 FineWeb、datatrove、Cosmopedia、融资与出售报道）、`vector-database`、`rag`（补 Lewis 等 2020 论文细节）
- `meta-ai` 时间线补入股 Scale AI；`langchain` 的向量库集成改为链接到各向量库页
- 更新 L1 地图页（按 向量库 / 语料 / 数据公司 / 概念 分组）

## [2026-11-06 05:08] ingest | AI 评测基准与政策法规调研（X 横切主题，核实规模定律种子页）

**创建页面**：[[sources/ai-benchmarks-survey-2026-11]], [[sources/ai-policy-survey-2026-11]], [[concepts/swe-bench]], [[concepts/chatbot-arena]], [[concepts/humanitys-last-exam]], [[concepts/gpqa]], [[concepts/mmlu]], [[concepts/arc-agi]], [[concepts/terminal-bench]], [[concepts/tau-bench]], [[concepts/benchmark-contamination]], [[concepts/eu-ai-act]], [[concepts/china-generative-ai-measures]], [[concepts/us-federal-ai-policy]], [[concepts/california-sb-53]], [[concepts/frontier-safety-frameworks]]

**更新页面**：[[concepts/scaling-laws]], [[entities/promptfoo]], [[entities/langsmith]], [[entities/anthropic]], [[entities/openai]], [[maps/X-横切主题]]

- 来源：SWE-bench、SWE-bench Pro、FastChat、HLE、GPQA、MMLU、MMLU-Pro、ARC-AGI、Terminal-Bench、Harbor、τ²-bench 的 GitHub README，Kaplan 2020 与 Chinchilla 2022 论文摘要（GitHub 镜像）；欧盟 AI Act 第 51/53/55/101/113 条、《生成式人工智能服务管理暂行办法》、《互联网信息服务算法推荐管理规定》、加州 SB 53 的原文（GitHub 镜像），Anthropic RSP 页面与 v3 公告；排行榜分数、美国行政令、纽约 RAISE Act、备案数量、OpenAI Preparedness Framework 来自搜索摘要，标为二手（`raw/AI评测基准调研-2026-11.md`、`raw/AI政策法规调研-2026-11.md`）
- 新建 2 个来源页：`sources/ai-benchmarks-survey-2026-11`、`sources/ai-policy-survey-2026-11`
- 新建 14 个概念页（layer: X）：评测基准 8 个 + `benchmark-contamination`；政策法规 5 个
- 重写 `scaling-laws`：依据两篇原始论文摘要改为 `origin: source`，补推理时计算扩展与监管算力门槛
- `promptfoo`、`langsmith` 链到评测基准页，`anthropic`、`openai` 链到前沿模型安全框架页
- 更新 X 地图页：新增「评测基准」「政策法规」分组

## [2026-11-06 05:21] update | 训练与后训练方法调研：arXiv 与一手页面复核

**更新页面**：[[sources/training-methods-survey-2026-11]], [[concepts/grpo]], [[concepts/rlvr]], [[concepts/dpo]], [[concepts/knowledge-distillation]], [[concepts/quantization]], [[entities/trl]], [[entities/unsloth]], [[entities/verl]]

- 网络放开后，用 arXiv API 核对了素材所引 13 篇论文的编号、标题、首次提交日期与摘要，并读了 Tülu 3、Hinton 蒸馏、DeepSeekMath、DeepSeek-R1 的正文；读了 Hugging Face「TRL v1.0」博客原文，以及 Y Combinator、Lightspeed 的 Unsloth 页面（`raw/训练与后训练方法调研-2026-11.md` 新增 arXiv 元数据表和论文引文）
- 去掉全部「二手」标记：Tülu 3 / RLVR 的定义、Hinton 蒸馏的温度与软目标、DeepSeek-R1 的规则奖励（准确性 + 格式）、TRL v1.0（博客 2026-03-31，75+ 种方法）、Unsloth（YC S24，2023 年成立，位于旧金山）均已确认
- 更正：GPTQ 的论文标题以 arXiv 为准（仓库 README 用的是旧标题）；HybridFlow 首次提交日期由 2024-08 改为 2024-09-28；删除一手页面找不到的“悉尼创办”和种子轮金额

## [2026-11-06 05:25] ingest | AI 数据层调研：第二轮核实（网络放开后对照一手资料）

**更新页面**：[[sources/ai-data-layer-survey-2026-11]], [[entities/fineweb]], [[entities/common-crawl]], [[entities/the-pile]], [[entities/dolma]], [[entities/milvus]], [[entities/zilliz]], [[entities/qdrant]], [[entities/pgvector]], [[entities/pinecone]], [[entities/chroma]], [[entities/scale-ai]], [[entities/surge-ai]], [[entities/mercor]], [[entities/hugging-face]], [[concepts/vector-database]], [[concepts/rag]], [[concepts/synthetic-data]], [[concepts/data-labeling]]

- 来源：Hugging Face 数据集卡片（FineWeb、FineWeb-Edu、FineWeb 2、Cosmopedia、Dolma、Dolma 3），arXiv 摘要，Nature 原文，Common Crawl 官网，Zilliz、Qdrant、Pinecone、Scale AI、Chroma 官方公告，TechCrunch 原文，Wikipedia（Surge AI），Semafor（`raw/AI数据层调研-2026-11.md` 第七节）
- 更正：FineWeb 现为 18.5 万亿 token 以上（首发 15 万亿）；Dolma 3 预训练混合 5.93 万亿 token、清洗池 9.31 万亿；Milvus 3.0 发布日以 Zilliz 新闻稿 2026-07-16 为准；Scale AI 交易日为 2025-06-12；Pinecone 已有开源的 pg_pinecone，不再是“没有开源仓库”
- 新事实：Chroma 2026-10 宣布并入 Replit，Chroma Cloud 2026-12 关停；Pinecone 2026 年 Nexus、全文检索、BYOC GA；Mercor 2026-03 数据泄露、Meta 暂停合同；报道称 NVIDIA 同意以约 129 亿美元收购 Hugging Face（无官方公告）
- 多处“二手报道”标注改为一手来源，并补充原文摘录

## [2026-11-06 10:04] ingest | AI 评测基准与政策法规调研：一手来源二次核实

**更新页面**：[[sources/ai-benchmarks-survey-2026-11]], [[sources/ai-policy-survey-2026-11]], [[concepts/swe-bench]], [[concepts/chatbot-arena]], [[concepts/humanitys-last-exam]], [[concepts/gpqa]], [[concepts/mmlu]], [[concepts/arc-agi]], [[concepts/terminal-bench]], [[concepts/tau-bench]], [[concepts/benchmark-contamination]], [[concepts/eu-ai-act]], [[concepts/china-generative-ai-measures]], [[concepts/us-federal-ai-policy]], [[concepts/california-sb-53]], [[concepts/frontier-safety-frameworks]], [[concepts/scaling-laws]]

- 来源：网络策略放开后，补读 arXiv 摘要、swebench.com 与 Scale AI 官方排行榜、arena.ai、lastexam.ai、arcprize.org、tbench.ai 博客、联邦公报行政令原文、欧盟出版局的 Regulation (EU) 2026/1744 正文与元数据、欧盟委员会实践准则签署方名单、网信办标识办法发布稿、OpenAI Preparedness Framework v2 PDF；更新两份素材 `raw/AI评测基准调研-2026-11.md`、`raw/AI政策法规调研-2026-11.md`
- 更正：SWE-bench Verified 官方榜最高 79.2%（首轮聚合站的 93.9%–96.4% 删除）；GPQA 专家准确率 65%（非 81%）；GSM1k 掉分最多 8%；τ-bench 成绩改用论文表述；实践准则不授予合规推定；纽约 RAISE Act 的事件报告时限为 72 小时
- 补充：Terminal-Bench 2.1 / 3.0 / 4.0 与排行榜诚信规则，HLE-Rolling / HLE-Diamond，SWE-Bench Pro 公开榜，ARC Prize 2026 赛程，EO 14409、EO 14434，Omnibus 新增禁止条款与第 50(2) 条过渡期，2026-08 备案数量（1,112 款），实践准则签署方官方名单

## [2026-11-06 10:09] ingest | AI 应用产品调研：网络放开后用一手资料复核

**更新页面**：[[sources/ai-applications-survey-2026-11]], [[entities/chatgpt]], [[entities/claude-app]], [[entities/claude-code]], [[entities/cursor]], [[entities/devin]], [[entities/doubao-app]], [[entities/gemini-app]], [[entities/github-copilot]], [[entities/kimi-app]], [[entities/midjourney]], [[entities/perplexity]], [[entities/suno]], [[entities/windsurf]]

- 来源：Claude 帮助中心 release notes 与 claude.com 博客、Google 博客与 Alphabet 2025 Q4 / 2026 Q2 / Q3 财报讲话、GitHub 博客与 changelog、Cognition / Cursor / Suno 官方博客、Midjourney 官方更新页、Kimi 帮助中心、IT之家（QuestMobile 半年报），以及 12 个 Wikipedia 词条（`raw/AI应用产品调研-2026-11.md` 重写，末尾附更正记录）
- 更正：Copilot coding agent 正式可用为 2025-09-25、Agent HQ 发布于 2025-10-28；Windsurf 的依赖由 GLM 改为 Kimi（SWE-1.7 基于 Kimi K2.7，SWE-1.5 的基座未具名）；Cognition 2026-09 E 轮估值 480 亿美元；Midjourney V8.1 为 04-14 alpha、06-11 成为默认；豆包 3.82 亿月活的时点为 2026-05；Cowork 于 2026-09-16 与聊天合并
- 新增依赖：Cursor、Devin 加 `kimi`（Composer 2 基于 Kimi K2.5，Devin 使用基于 Kimi 的 SWE 模型）；Perplexity 改为 `llama`（Sonar）、`deepseek-r1`（R1 1776）、`gpt`、`claude`、`grok`
- openai.com、perplexity.ai 返回 403，ChatGPT、Perplexity 的部分事实仍为二手报道或 Wikipedia

## [2026-11-06 10:14] update | 多模态与嵌入模型调研：网络放开后的一手核实

**更新页面**：[[concepts/diffusion-model]], [[concepts/embedding]], [[concepts/text-to-speech]], [[entities/baai]], [[entities/bge]], [[entities/black-forest-labs]], [[entities/bytedance]], [[entities/cohere]], [[entities/cohere-embed]], [[entities/elevenlabs]], [[entities/flux]], [[entities/gpt-image]], [[entities/imagen]], [[entities/kling]], [[entities/kuaishou]], [[entities/openai]], [[entities/openai-embeddings]], [[entities/qwen3-embedding]], [[entities/seedance]], [[entities/sora]], [[entities/stability-ai]], [[entities/veo]], [[entities/voyage-ai]], [[entities/voyage-embeddings]], [[entities/whisper]], [[maps/L2-基础模型]], [[sources/multimodal-embedding-models-survey-2026-11]]

- 来源：Wikipedia（Sora、Veo、Kling AI、Imagen、GPT Image、DALL-E、Flux、Seedance、Stability AI、Whisper、ElevenLabs、Cohere、Kuaishou、BAAI 的 wikitext 原文），OpenAI 弃用表 / 模型页 / API changelog，Gemini API changelog，Google DeepMind Veo 页与 Gemini Embedding 2 公告，Cohere changelog，MongoDB 新闻稿，BFL、ElevenLabs、Voyage 博客，ByteDance Seed 官网，快手 Kling 4.0 新闻稿，Hugging Face API；写入 `raw/多模态与嵌入模型调研-2026-11.md` 第 6 节
- 更正 5 处：Cohere Embed 5 已于 2026-09-30 发布（原写“未找到”）；Seedance 2.0 的停止侵权函是 2026-02-13（原写 3 月）；Veo 3.1 Lite 是 2026-03-31；GPT Image 是自回归而非扩散模型；whisper-1 API 将于 2027-02-26 下线
- 新增：FLUX 3 多模态系列（2026-07 起）、GPT-Image-2.5 / 2.6、Eleven v4、Seedance 2.5、Seedream 5.0 Pro、Gemini Omni、Rerank 5、Cohere 收购 Aleph Alpha、OpenAI 旧 TTS 弃用等
- 原先空着的「来源摘录」都补上了官方或 Wikipedia 原文
- 字节页把 Seedance 发函时间改为 2026-02-13；OpenAI 页补 whisper-1 下线日期；L2 地图页更新注释


## [2026-11-06 10:36] Wiki 维护报告


> Wiki 状态概览：共 242 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 16 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。



## [2026-11-06 10:57] ingest | 主要 AI 实验室与公司调研：七个种子组织页核实

**创建页面**：[[sources/major-ai-orgs-survey-2026-11]]

**更新页面**：[[entities/openai]], [[entities/anthropic]], [[entities/google-deepmind]], [[entities/meta-ai]], [[entities/microsoft]], [[entities/alibaba]], [[entities/vercel]]

- 来源：Microsoft 官方博客（2025-10-28 OpenAI 新协议、2025-11-18 与 NVIDIA 和 Anthropic 合作）、Anthropic G 轮与 H 轮公告、Meta Newsroom（Muse Spark）、Vercel 博客（F 轮），以及 OpenAI、Anthropic、Google DeepMind、Meta AI、Meta Superintelligence Labs、Microsoft、Microsoft AI、Alibaba Group、Qwen、Vercel 的 Wikipedia 原文；素材为 `raw/主要AI实验室与公司调研-2026-11.md`。openai.com 返回 403
- 七页 `origin` 由 `claude-seed` 改为 `source`，`reviewed` 仍为 false，等你人工核实
- 主要补充：OpenAI 2025-10 改制为 OpenAI Group PBC，持股结构为 Foundation 26%、Microsoft 27%、其余 47%，2026-04 估值 8520 亿美元；Anthropic G 轮、H 轮（9650 亿美元）和 2026-10-26 的 S-1（Nasdaq: ANT）；DeepMind 2010 年创立、2014 年被收购；Meta 2025-06 成立 MSL，LeCun 离职，Muse Glimmer 与 Muse Spark Open 开放权重；Microsoft AI 与 MAI 自研模型；阿里 3800 亿元投资计划、千问 App；Vercel F 轮与 2026-04 安全事件
- 更正：Google DeepMind 的 `released` 由 2023 改为 2010-11，别名删掉不准确的“Google AI”；Meta AI 补 `released: 2013`
- 待核实：Microsoft 与 OpenAI 2026-04 改约的具体条款；Anthropic S-1 的亏损数字；OpenAI 停供 Cursor 的原因，已写入 OpenAI 页的 `## Contradictions`


## [2026-11-06 11:57] ingest | Python Agent 框架调研

**创建页面**：[[sources/python-agent-frameworks-survey-2026-11]], [[concepts/python-agent-development]], [[entities/microsoft-agent-framework]], [[entities/crewai]], [[entities/llamaindex]], [[entities/pydantic-ai]], [[entities/dspy]], [[entities/smolagents]], [[entities/agno]]

**更新页面**：[[entities/langgraph]], [[entities/google-adk]], [[entities/openai-agents-sdk]], [[entities/microsoft]], [[entities/hugging-face]], [[maps/L4-开发工具与Agent]]

- 来源：Microsoft Agent Framework 1.0 公告、Pydantic AI v2 公告、ADK 2.0 文档，以及各项目 GitHub README；版本号和发布日期取自 PyPI JSON API，星数和协议取自 GitHub API（均为 2026-11-06 读取）；素材为 `raw/Python-Agent框架调研-2026-11.md`
- AutoGen 不单独建页，作为前身写进 Microsoft Agent Framework 页（仓库已归档）；Semantic Kernel 同样并入
- LangGraph 补 Python 版时间线，并记下 PyPI 1.0.0 上传日期（2025-10-17）与官方公告日期（2025-10-22）不同；Google ADK 补 Python 2.0（图式 Workflow Runtime）
- 待核实：Agno 前身是 Phidata 的说法（来自训练知识）；DSPy 3.2–3.4 的内容来自维护者 X 帖子与二手资料；AutoGen 仓库的代码协议


## [2026-11-06 12:13] Wiki 维护报告


> Wiki 状态概览：共 251 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 14 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。




## [2026-11-06 18:44] ingest | 上下文工程与 Agent 记忆、AI 应用评测与可观测性

**创建页面**：[[concepts/context-engineering]], [[concepts/agent-memory]], [[concepts/context-compaction]], [[concepts/longmemeval]], [[concepts/ai-application-evaluation]], [[concepts/llm-as-judge]], [[concepts/llm-observability]], [[entities/langfuse]], [[entities/arize-phoenix]], [[sources/context-memory-survey-2026-11]], [[sources/ai-evaluation-observability-survey-2026-11]]

**更新页面**：[[concepts/agent-harness]], [[concepts/observational-memory]], [[concepts/rag]], [[entities/langsmith]], [[entities/promptfoo]], [[concepts/benchmark-contamination]], [[maps/L4-开发工具与Agent]], [[maps/X-横切主题]]

- 来源：两份 raw 调研，依据官方工程文档、原始论文及 OpenTelemetry 规范；查询日期 2026-11-06。
- 新增 7 个概念、2 个实体、2 个来源页；2 份原始研究包含来源表、案例与未运行的实验方案。
- 保留原有“我的判断”，未设置人工已审核；没有部署服务或声称已完成应用实测。


## [2026-11-06 18:45] Wiki 维护报告


> Wiki 状态概览：共 262 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 14 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。


## [2026-11-07 18:28] ingest | AI 应用扩容调研 + 低代码 Agent 平台与 LLM 网关调研

**创建页面**：[[sources/ai-applications-expansion-survey-2026-11]], [[sources/lowcode-agent-platforms-survey-2026-11]], [[entities/microsoft-365-copilot]], [[entities/notion-ai]], [[entities/salesforce-agentforce]], [[entities/harvey]], [[entities/openevidence]], [[entities/abridge]], [[entities/rogo]], [[entities/runway]], [[entities/character-ai]], [[entities/dify]], [[entities/coze]], [[entities/n8n]], [[entities/litellm]], [[concepts/computer-use]], [[concepts/ai-browser]]

**更新页面**：[[entities/perplexity]], [[entities/chatgpt]], [[entities/gemini-app]], [[entities/claude-app]], [[entities/claude]], [[entities/microsoft]], [[entities/bytedance]], [[entities/sora]], [[entities/kling]], [[entities/seedance]], [[entities/openai-agents-sdk]], [[entities/mercor]], [[entities/dspy]], [[entities/smolagents]], [[entities/chatkit]], [[concepts/data-labeling]], [[maps/L5-应用]], [[maps/L4-开发工具与Agent]]

- 来源：两份 raw 调研 `raw/AI应用扩容调研-2026-11.md`、`raw/低代码Agent平台调研-2026-11.md`，依据 Microsoft 新闻中心、Notion releases、Salesforce 新闻稿与投资者资料、Harvey / OpenEvidence / Abridge / Rogo / Runway / Character.AI 官方页面、Anthropic 新闻，以及 Dify / Coze Studio / n8n / LiteLLM 的 GitHub 仓库、PyPI / npm 元数据、官方博客与 LiteLLM 安全 issue #24518；查询日期 2026-11-07。本会话 GitHub API 不可用，星数取自网页
- ChatGPT Atlas、Perplexity Comet 已是现有页面的别名，不重复建页，改建 [[concepts/ai-browser]] 做横向对照；可灵、Seedance、Sora 只补指向 [[entities/runway]] 的应用侧链接
- LiteLLM 建页后，把 Mercor、数据标注、DSPy、smolagents、ChatKit 正文里的首次提及改为链接，OpenAI Agents SDK 在「相关实体」加链接
- 新发现：Character.AI 2026-10-12 申请 Chapter 11 破产保护；ChatGPT Atlas 2026-08 已关停；Copilot Cowork 采用 Claude Cowork 技术
- 腾讯元宝、文心等国内厂商应用由另一会话负责，本次未建
- 待核实：Harvey 155 亿美元一轮的日期；OpenEvidence 2026-09 估值 150 亿美元；Abridge 2026 年融资；Microsoft E7 与 Agent 365 价格；Dify 估值 1.8 亿美元；Coze 2.0 / 3.0 官方发布日期；n8n 2026 年估值；LiteLLM 事件的 Trivy 根因；以及标「训练知识」的若干条（Character.AI 创立与 Google 授权协议、Atlassian 收购 The Browser Company、Operator 并入 ChatGPT、Notion AI / Microsoft 365 Copilot / Dify / 扣子 / Runway / Abridge / Harvey / OpenEvidence 的首发时间）
- 所有新页 `origin: source`、`reviewed: false`，未改动任何「我的判断」

