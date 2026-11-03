# Wiki Index

> 此文件是 wiki 的内容目录，按类别组织所有页面，每页一行摘要。
> LLM 在回答查询时优先阅读此文件以定位相关页面。

## Overview

- [[overview|Overview]] — AI 生态分层总览与维护看板
- [[conventions|使用约定]] — 本知识库的组织规则

## Maps

- [[maps/L0-算力与硬件|L0-算力与硬件]] — 芯片、加速器、云与数据中心
- [[maps/L1-数据|L1-数据]] — 数据集、合成数据、向量数据库、数据工程
- [[maps/L2-基础模型|L2-基础模型]] — LLM、多模态、图像/视频/语音模型；开源与闭源
- [[maps/L3-训练与推理|L3-训练与推理]] — 训练框架、推理引擎、微调、量化、部署
- [[maps/L4-开发工具与Agent|L4-开发工具与Agent]] — SDK、Agent 框架、RAG、评测、可观测性、协议
- [[maps/L5-应用|L5-应用]] — 编程助手、对话助手、搜索、办公、创意、垂直行业
- [[maps/X-横切主题|X-横切主题]] — 组织与人物、安全对齐、政策法规、开源社区、关键论文

## Entities

- [[entities/alibaba|阿里巴巴（通义）]] — 公司，X
- [[entities/anthropic|Anthropic]] — AI 实验室，X
- [[entities/claude|Claude]] — 模型家族，L2
- [[entities/claude-code|Claude Code]] — 应用产品，L5
- [[entities/cuda|CUDA]] — 基础设施，L0
- [[entities/cursor|Cursor]] — 应用产品，L5
- [[entities/deepseek|DeepSeek]] — AI 实验室，X
- [[entities/deepseek-r1|DeepSeek-R1]] — 模型，L2
- [[entities/gemini|Gemini]] — 模型家族，L2
- [[entities/github-copilot|GitHub Copilot]] — 应用产品，L5
- [[entities/google-deepmind|Google DeepMind]] — AI 实验室，X
- [[entities/gpt|GPT]] — 模型家族，L2
- [[entities/hugging-face|Hugging Face]] — 公司，L1
- [[entities/langchain|LangChain]] — 框架，L4
- [[entities/llama|Llama]] — 模型家族，L2
- [[entities/meta-ai|Meta AI]] — AI 实验室，X
- [[entities/microsoft|Microsoft]] — 公司，X
- [[entities/mistral-ai|Mistral AI]] — AI 实验室，X
- [[entities/nvidia|NVIDIA]] — 公司，L0
- [[entities/openai|OpenAI]] — AI 实验室，X
- [[entities/pytorch|PyTorch]] — 框架，L3
- [[entities/qwen|Qwen]] — 模型家族，L2
- [[entities/vllm|vLLM]] — 框架，L3

## Concepts

- [[concepts/ai-agent|AI Agent]] — L4
- [[concepts/lora|LoRA]] — L3
- [[concepts/mixture-of-experts|混合专家（MoE）]] — L2
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]] — L4，当前版本 2026-07-28
- [[concepts/mcp-request-flow|MCP 请求流程（2026-07-28）]] — L4，无状态协议的 7 阶段端到端流程与新旧对照
- [[concepts/multi-round-trip-requests|多轮往返请求（MRTR）]] — L4，input_required 加重试，取代服务端主动请求
- [[concepts/mcp-extensions|MCP 扩展]] — L4，Tasks / Apps / Skills / Auth 扩展与生命周期
- [[concepts/quantization|量化]] — L3
- [[concepts/rag|检索增强生成（RAG）]] — L4
- [[concepts/reasoning-model|推理模型]] — L2
- [[concepts/scaling-laws|规模定律]] — X
- [[concepts/transformer|Transformer]] — L2
- [[concepts/vector-database|向量数据库]] — L1

## Sources

- [[sources/mcp-spec-2026-07-28|MCP 规范 2026-07-28 版]] — 无状态化、server/discover、MRTR、subscriptions/listen、弃用清单 (2026-11-04)
