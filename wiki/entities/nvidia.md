---
title: NVIDIA
type: entity
tags: [organization]
kind: company
layer: L0
aliases: ["NVIDIA", "英伟达"]
competitors: ["[[entities/amd]]", "[[entities/google-tpu]]", "[[entities/aws-trainium]]", "[[entities/huawei]]"]
depends_on: ["[[concepts/hbm]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]", "[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# NVIDIA

GPU 与 AI 加速计算的主导厂商，其数据中心 GPU 与 [[entities/cuda|CUDA]] 软件栈构成大模型训练和推理的事实标准底座。规模上几乎没有可比对手：FY2027 Q2（截至 2026-07-26）总营收 962 亿美元、同比 +106%，其中数据中心 890 亿美元、同比 +117%，占比超过 92%，而下季 1080 亿美元的指引**假设中国数据中心计算营收为零**。软件上它维护推理库 [[entities/tensorrt-llm|TensorRT-LLM]]、推理编排栈 [[entities/nvidia-dynamo|NVIDIA Dynamo]] 和训练库 [[entities/megatron-lm|Megatron Core]]，并参与发起 [[entities/llm-d|llm-d]]；风投部门 NVentures 投资了 SGLang 团队的 [[entities/radixark|RadixArk]]。2025 年底它还以报道约 200 亿美元的非排他许可拿到 [[entities/groq|Groq]] 的推理技术，创始人与总裁转入 NVIDIA。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 公司
- **上游依赖**：[[concepts/hbm|HBM]] 与先进封装产能、台积电制程
- **护城河**：[[entities/cuda|CUDA]] 生态、[[concepts/scale-up-interconnect|NVLink 与机架级超节点]]
- **竞争 / 替代**：云厂商自研（[[entities/google-tpu|Google TPU]]、[[entities/aws-trainium|AWS Trainium]]、Azure Maia）、通用 GPU 替代（[[entities/amd-instinct|AMD Instinct]] + [[entities/rocm|ROCm]]）、专用架构（[[entities/groq|Groq]]、[[entities/cerebras|Cerebras]]）、中国市场的[[entities/ascend|昇腾]]

## 时间线

- 2006 CUDA 发布
- 2022 起数据中心 GPU 供不应求
- 2025-03-22 TensorRT-LLM 完全开源
- 2025-09-24 TensorRT-LLM 1.0，改为 PyTorch 架构
- 2025-10 GTC Washington 首次展示 Vera Rubin 超级芯片，黄仁勋称 2026 下半年量产
- 2025-12 以报道约 200 亿美元与 [[entities/groq|Groq]] 达成非排他推理技术许可
- 2026-03 GTC 发布 Dynamo 1.0
- 2026-05-05 NVentures 参投 RadixArk 1 亿美元种子轮
- 2026-07 Megatron Core 在 GB300 NVL72 上预训练 DeepSeek-V3，每 GPU 1,648 TFLOPs/s
- 2026-08-26 公布 FY2027 Q2 财报：营收 962 亿美元，数据中心 890 亿美元
- 2026 下半年 Vera Rubin 量产目标，各大云宣布提供其实例；NVIDIA 宣称 NVL144 的 FP4 推理 3.6 EFLOPS、FP8 训练 1.2 EFLOPS，为 GB300 NVL72 的 3.3 倍（厂商数字）

## 相关实体

- [[entities/cuda|CUDA]]
- [[entities/pytorch|PyTorch]]
- [[entities/vllm|vLLM]]
- [[entities/tensorrt-llm|TensorRT-LLM]]
- [[entities/nvidia-dynamo|NVIDIA Dynamo]]
- [[entities/megatron-lm|Megatron-LM]]
- [[entities/llm-d|llm-d]]
- [[entities/radixark|RadixArk]]
- [[entities/groq|Groq]]
- [[entities/amd|AMD]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/hbm|HBM]]
- [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]
- [[concepts/quantization|量化]]
- [[concepts/disaggregated-serving|预填充 / 解码分离]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The open-source, datacenter-scale inference stack." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "FY2027 Q2（截至 2026-07-26）总营收 962 亿美元、同比 +106%，其中数据中心 890 亿美元、同比 +117%，占比超过 92%" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "下季指引 1080 亿美元，且假设中国数据中心计算业务营收为零" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
