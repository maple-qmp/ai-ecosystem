---
title: 训练与后训练方法调研（2026-11）
type: source
tags: [notes]
source_note: "[[训练与后训练方法调研-2026-11]]"
url: https://github.com/huggingface/trl
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[concepts/pretraining]]"
  - "[[concepts/supervised-fine-tuning]]"
  - "[[concepts/rlhf]]"
  - "[[concepts/dpo]]"
  - "[[concepts/grpo]]"
  - "[[concepts/rlvr]]"
  - "[[concepts/knowledge-distillation]]"
  - "[[concepts/lora]]"
  - "[[concepts/quantization]]"
  - "[[entities/trl]]"
  - "[[entities/unsloth]]"
  - "[[entities/axolotl]]"
  - "[[entities/llama-factory]]"
  - "[[entities/verl]]"
---

# 训练与后训练方法调研（2026-11）

## Summary

梳理 L3 层训练一侧的方法与工具，补齐此前以推理为主的 L3 地图。方法按流水线排列：[[concepts/pretraining|预训练]]得到基座模型，[[concepts/supervised-fine-tuning|监督微调（SFT）]]教会它遵循指令，[[concepts/rlhf|RLHF]] 与 [[concepts/dpo|DPO]] 做偏好对齐，[[concepts/grpo|GRPO]] 与 [[concepts/rlvr|RLVR]] 用可验证奖励的强化学习训练推理能力，[[concepts/knowledge-distillation|知识蒸馏]]把大模型的能力迁移给小模型。同时依据原论文仓库核实了 [[concepts/lora|LoRA]]（含 QLoRA）和[[concepts/quantization|量化]]（GPTQ、AWQ、LLM.int8()、NF4、QAT）两个种子页。

工具一侧收录五个开源项目：[[entities/hugging-face|Hugging Face]] 的 [[entities/trl|TRL]] 是底层库，[[entities/unsloth|Unsloth]]、[[entities/axolotl|Axolotl]]、[[entities/llama-factory|LLaMA-Factory]] 都依赖它；[[entities/bytedance|字节跳动]] Seed 发起的 [[entities/verl|verl]] 代表另一类，即把训练后端（FSDP、[[entities/megatron-lm|Megatron]]）和推理引擎 rollout（[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]）编排在一起的大规模 RL 框架。2025–2026 年的主线是后训练重心从偏好对齐转向可验证奖励的强化学习：[[entities/deepseek-r1|DeepSeek-R1]] 让 GRPO 成为[[concepts/reasoning-model|推理模型]]的标准配方，五个工具都把 GRPO 做成一等功能。

## Key Points

- **资料可靠性**：论文作者仓库 README、工具 README 与 PyPI 元数据为一手；arxiv.org 在调研会话中被网络策略拦截，论文编号取自作者仓库的引用条目；Tülu 3、Hinton 蒸馏论文的编号与日期、TRL v1.0 博客说法、Unsloth 公司信息来自搜索摘要，已在素材中标注「二手」
- **RLHF**：InstructGPT（2022）确立 SFT → 奖励模型 → PPO 三阶段；1.3B InstructGPT 比 175B GPT-3 更受偏好
- **DPO**（2023）：证明奖励可由策略与参考模型的对数概率比表示，去掉奖励模型与在线采样
- **GRPO**（DeepSeekMath，2024-02）：组内相对优势替代价值模型；R1-Zero 不经 SFT、纯 RL 激发推理；DAPO 等改进完全基于 verl
- **RLVR**（Tülu 3，2024-11）：奖励来自可程序验证的正确性，与 GRPO 正交、常组合使用
- **蒸馏**：R1 用约 80 万条推理样本蒸馏出 6 个 Qwen2.5 / Llama3 稠密模型，效果好于小模型直接 RL
- **LoRA / QLoRA**：LoRA 在 GLUE 上以 0.8M 对 125M 可训练参数达到同等效果；QLoRA 单张 48GB GPU 微调 65B 模型
- **工具版本**：TRL 1.0.0（2026-03-30）→ 1.17.1（2026-10-30）；Unsloth 2026.11.2；Axolotl 0.21.1；LLaMA-Factory 0.9.5（2026-05）；verl 0.9.1（2026-09），2026-01 迁入 verl-project 组织

## Mentioned Pages

- [[concepts/pretraining|预训练]]
- [[concepts/supervised-fine-tuning|监督微调（SFT）]]
- [[concepts/rlhf|RLHF]]
- [[concepts/dpo|DPO]]
- [[concepts/grpo|GRPO]]
- [[concepts/rlvr|RLVR]]
- [[concepts/knowledge-distillation|知识蒸馏]]
- [[concepts/lora|LoRA]]
- [[concepts/quantization|量化]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/scaling-laws|规模定律]]
- [[concepts/gguf|GGUF]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[entities/trl|TRL]]
- [[entities/unsloth|Unsloth]]
- [[entities/axolotl|Axolotl]]
- [[entities/llama-factory|LLaMA-Factory]]
- [[entities/verl|verl]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/bytedance|字节跳动]]
- [[entities/deepseek|DeepSeek]]
- [[entities/deepseek-r1|DeepSeek-R1]]
- [[entities/microsoft|Microsoft]]
- [[entities/openai|OpenAI]]
- [[entities/pytorch|PyTorch]]
- [[entities/deepspeed|DeepSpeed]]
- [[entities/megatron-lm|Megatron-LM]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/qwen|Qwen]]
- [[entities/llama|Llama]]
