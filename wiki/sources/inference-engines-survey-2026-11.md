---
title: 推理引擎与本地部署调研（2026-11）
type: source
tags: [notes]
source_note: "[[推理引擎与本地部署调研-2026-11]]"
url: https://github.com/vllm-project/vllm
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[entities/vllm]]"
  - "[[entities/sglang]]"
  - "[[entities/tensorrt-llm]]"
  - "[[entities/nvidia-dynamo]]"
  - "[[entities/llm-d]]"
  - "[[entities/llama-cpp]]"
  - "[[entities/ollama]]"
  - "[[entities/lm-studio]]"
  - "[[entities/deepspeed]]"
  - "[[entities/megatron-lm]]"
  - "[[entities/inferact]]"
  - "[[entities/radixark]]"
  - "[[entities/nvidia]]"
  - "[[entities/hugging-face]]"
  - "[[entities/pytorch]]"
  - "[[entities/microsoft]]"
  - "[[concepts/kv-cache]]"
  - "[[concepts/speculative-decoding]]"
  - "[[concepts/disaggregated-serving]]"
  - "[[concepts/gguf]]"
  - "[[concepts/quantization]]"
  - "[[concepts/anthropic-messages-api]]"
---

# 推理引擎与本地部署调研（2026-11）

## Summary

梳理 L3 层的推理与训练基础设施。数据中心推理以 [[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/tensorrt-llm|TensorRT-LLM]] 三个引擎为主，上面一层是 [[entities/nvidia-dynamo|NVIDIA Dynamo]]、[[entities/llm-d|llm-d]] 这类多节点编排栈。本地推理以 [[entities/llama-cpp|llama.cpp]] 和它的 [[concepts/gguf|GGUF]] 格式为底座，[[entities/ollama|Ollama]]、[[entities/lm-studio|LM Studio]] 在上面做成面向用户的产品。训练侧收录 [[entities/deepspeed|DeepSpeed]] 和 [[entities/megatron-lm|Megatron]]。三项横跨各引擎的技术单列概念页：[[concepts/kv-cache|KV cache 管理]]、[[concepts/speculative-decoding|推测解码]]、[[concepts/disaggregated-serving|预填充 / 解码分离]]。

2026 年的两条主线：一是开源推理引擎公司化，vLLM 团队成立 [[entities/inferact|Inferact]]（1.5 亿美元种子轮），SGLang 团队成立 [[entities/radixark|RadixArk]]（1 亿美元种子轮）；二是本地推理平台化，ggml.ai 团队加入 [[entities/hugging-face|Hugging Face]]，Ollama 推出云端模型与按 token 计费，并完成 6500 万美元 B 轮。几乎所有引擎都提供 OpenAI 兼容接口，vLLM、Ollama、LM Studio 还提供 [[concepts/anthropic-messages-api|Anthropic Messages API]] 兼容端点，可以直接驱动 [[entities/claude-code|Claude Code]] 等编程 Agent。

## Key Points

- **资料可靠性**：README、官方博客原文与 PyPI 元数据为一手；融资、公司与部分日期来自新闻与搜索摘要，原文域名在调研会话中被网络策略拦截，未逐字核对，已在素材中标注「二手报道」
- **vLLM**：2023-06 发布 PagedAttention；V1 引擎 2025 年取代 V0；2025-05 进入 PyTorch Foundation；2000+ 贡献者；0.33.0（2026-11-02）
- **SGLang**：2024-01 发布 RadixAttention；由 LMSYS 托管；扩展到扩散模型、语音与 RL rollout；0.5.23（2026-10-30）
- **TensorRT-LLM**：2025-03 完全开源；1.0（2025-09）改为 PyTorch 架构为默认；只面向 NVIDIA GPU
- **编排层**：Dynamo（Rust + Python，1.0 于 2026-03）与 llm-d（CNCF 沙箱，Red Hat / Google Cloud / IBM / CoreWeave / NVIDIA 发起）都不替代引擎，而是在其上做 KV 感知路由、分离式服务与自动扩缩
- **本地推理**：llama.cpp 纯 C/C++、覆盖十余种硬件后端；2026-02 ggml.ai 并入 HF，项目保持独立自治；Ollama 2026 年加入 `ollama launch`、Anthropic 兼容、云端模型；LM Studio 2025-07 起工作使用免费，双引擎 llama.cpp + MLX
- **训练框架**：DeepSpeed（ZeRO，2025 年移交 Linux Foundation 后进入 PyTorch Foundation）；Megatron Core（TP / PP / DP / EP / CP 并行，GB300 上 DeepSeek-V3 每 GPU 1,648 TFLOPs/s）
- **公司化**：Inferact 2026-01-22，1.5 亿美元、估值 8 亿美元；RadixArk 2026-05-05，1 亿美元、估值 4 亿美元，NVIDIA 风投参投

## Mentioned Pages

- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/tensorrt-llm|TensorRT-LLM]]
- [[entities/nvidia-dynamo|NVIDIA Dynamo]]
- [[entities/llm-d|llm-d]]
- [[entities/llama-cpp|llama.cpp]]
- [[entities/ollama|Ollama]]
- [[entities/lm-studio|LM Studio]]
- [[entities/deepspeed|DeepSpeed]]
- [[entities/megatron-lm|Megatron-LM]]
- [[entities/inferact|Inferact]]
- [[entities/radixark|RadixArk]]
- [[entities/nvidia|NVIDIA]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/pytorch|PyTorch]]
- [[entities/microsoft|Microsoft]]
- [[entities/cuda|CUDA]]
- [[entities/claude-code|Claude Code]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/gpt-oss|gpt-oss]]
- [[concepts/kv-cache|KV cache]]
- [[concepts/speculative-decoding|推测解码]]
- [[concepts/disaggregated-serving|预填充 / 解码分离]]
- [[concepts/gguf|GGUF]]
- [[concepts/quantization|量化]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
