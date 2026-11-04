# Wiki Index

> 自动生成的知识库目录

> Note: Text in backticks after page names shows aliases — alternative names, abbreviations, or translations.


## 实体

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
- [[entities/openai|openai]] `aliases: OpenAI, Open AI` - 2015 年成立的 AI 研究与产品公司。推出 [[entities/gpt|GPT]] 系列模型和 ChatGPT（2022-11），后者引爆了生成式 AI 浪潮；2024 年起推出以 o1 为首的
- [[entities/nvidia|nvidia]] `aliases: 英伟达` - GPU 与 AI 加速计算的主导厂商。其数据中心 GPU 与 [[entities/cuda|CUDA]] 软件栈构成大模型训练和推理的事实标准底座，是整个生态最上游的瓶颈环节之一。
- [[entities/mistral-ai|mistral-ai]] `aliases: Mistral` - 2023 年成立于巴黎的欧洲模型公司，早期以小而强的开放权重模型和 Mixtral（[[concepts/mixture-of-experts|MoE]]）著称，同时提供商业 API。
- [[entities/microsoft|microsoft]] `aliases: 微软` - OpenAI 的主要投资方与云合作伙伴，通过 Azure 提供模型服务；旗下 GitHub 推出 [[entities/github-copilot|GitHub Copilot]]。微软研究院提出了
- [[entities/meta-ai|meta-ai]] `aliases: FAIR, Meta` - Meta 的 AI 部门（含 FAIR 研究院）。以开放权重的 [[entities/llama|Llama]] 系列推动了开源模型生态；[[entities/pytorch|PyTorch]] 也起
- [[entities/llama|llama]] `aliases: LLaMA` - [[entities/meta-ai|Meta]] 发布的开放权重模型家族。Llama 2 起允许商用，带动了大量社区微调（[[concepts/lora|LoRA]]）与本地部署工具，是开源 LLM
- [[entities/langchain|langchain]] `aliases: LangChain, LangChain.js, langchain` `source: langchain-ecosystem-survey-2026-11` - [[entities/langchain-inc|LangChain 公司]]维护的开源 LLM 应用与 Agent 开发框架，MIT 协议，有 Python 和 JavaScript/TypeScr
- [[entities/hugging-face|hugging-face]] `aliases: HF, 抱抱脸` - 开源 AI 社区与平台：模型/数据集 Hub、`transformers` 等库。几乎所有开放权重模型（[[entities/llama|Llama]]、[[entities/qwen|Qwen]]、
- [[entities/gpt|gpt]] `aliases: GPT 系列, ChatGPT 模型` - [[entities/openai|OpenAI]] 的生成式预训练 Transformer 系列模型，从 GPT-1（2018）到 GPT-4/GPT-5 代，驱动 ChatGPT 与 OpenAI
- [[entities/google-deepmind|google-deepmind]] `aliases: DeepMind, Google AI` - Google 的 AI 研究主体，2023 年由 Google Brain 与 DeepMind 合并而成。负责 [[entities/gemini|Gemini]] 模型家族。Google 研究员 
- [[entities/github-copilot|github-copilot]] `aliases: Copilot` - GitHub（[[entities/microsoft|Microsoft]]）的 AI 编程助手，2021 年预览，是第一个大规模普及的 AI 编程产品，后扩展为聊天与 Agent 模式并支持多家模
- [[entities/gemini|gemini]] `aliases: Google Gemini` - [[entities/google-deepmind|Google DeepMind]] 的原生多模态模型家族，覆盖 Pro / Flash 等档位，深度集成进 Google 搜索、Workspace
- [[entities/deepseek|deepseek]] `aliases: 深度求索` - 总部位于杭州的中国 AI 公司，由量化基金幻方支持。以较低训练成本做出接近一线水平的开放权重模型而闻名，代表作 [[entities/deepseek-r1|DeepSeek-R1]] 与 DeepS
- [[entities/deepseek-r1|deepseek-r1]] `aliases: R1` - [[entities/deepseek|DeepSeek]] 于 2025-01 以 MIT 许可开放权重的[[concepts/reasoning-model|推理模型]]，基于 MoE 架构的 D
- [[entities/cursor|cursor]] `aliases: Cursor, Cursor 编辑器` - Anysphere 公司基于 VS Code 打造的 AI 代码编辑器，可接入 [[entities/claude|Claude]]、[[entities/gpt|GPT]] 等多家模型，以补全、多文
- [[entities/cuda|cuda]] `aliases: CUDA, Compute Unified Device Architecture` - [[entities/nvidia|NVIDIA]] 的 GPU 并行计算平台与编程模型。[[entities/pytorch|PyTorch]]、[[entities/vllm|vLLM]] 等几乎
- [[entities/claude|claude]] `aliases: Claude 模型` - [[entities/anthropic|Anthropic]] 的闭源大模型家族，按能力分为 Haiku / Sonnet / Opus 等档位，提供 API、claude.ai 应用及云平台分发。
- [[entities/claude-code|claude-code]] `aliases: Claude Code` - [[entities/anthropic|Anthropic]] 的 Agent 式编程工具，可在终端、IDE、桌面与网页中读写代码、运行命令，并通过 [[concepts/model-context
- [[entities/anthropic|anthropic]] `aliases: Anthropic PBC` - AI 安全与研究公司，2021 年由 Dario Amodei、Daniela Amodei 等前 OpenAI 成员创立，总部位于旧金山。主力产品是 [[entities/claude|Claude
- [[entities/alibaba|alibaba]] `aliases: Alibaba, 阿里云, 通义` - 阿里巴巴集团及阿里云，研发 [[entities/qwen|Qwen（通义千问）]] 系列，是全球下载量最大的开放权重模型家族之一，同时通过阿里云提供算力与模型服务。

## 概念

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

- [[sources/langchain-ecosystem-survey-2026-11|langchain-ecosystem-survey-2026-11]]
- [[sources/vercel-oss-dependency-survey-2026-11|vercel-oss-dependency-survey-2026-11]]
- [[sources/mcp-spec-2026-07-28|mcp-spec-2026-07-28]]
