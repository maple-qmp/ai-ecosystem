---
title: Hugging Face
type: entity
tags: [organization]
kind: company
layer: L1
aliases: ["Hugging Face", "HF", "抱抱脸"]
competitors: []
depends_on: ["[[entities/pytorch]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]", "[[sources/ai-data-layer-survey-2026-11]]"]
---

# Hugging Face

## 描述

开源 AI 社区与平台，核心是模型 / 数据集 Hub 和 `transformers` 等库，CEO Clément Delangue。几乎所有开放权重模型（[[entities/llama|Llama]]、[[entities/qwen|Qwen]]、[[entities/deepseek-r1|DeepSeek-R1]]）都在 Hub 上分发，2026-08 社区统计称公开模型已超过 300 万个。`transformers` 把自己定位为文本、视觉、音频、视频和多模态模型的“模型定义框架”，[[entities/llama-cpp|llama.cpp]]、mlx 等库复用它的模型定义。在数据层，HF 发布了开放预训练语料 [[entities/fineweb|FineWeb]]（超过 18.5 万亿 token）/ FineWeb-Edu / FineWeb 2、数据处理库 datatrove 和合成数据集 Cosmopedia。2026-02 本地推理引擎 [[entities/llama-cpp|llama.cpp]] 的维护公司 ggml.ai 团队加入 HF，目标是让新模型从 transformers 几乎一键进入 llama.cpp，项目仍由 Georgi Gerganov 团队自治；2026-08 起多家媒体报道 [[entities/nvidia|NVIDIA]] 将收购 HF：The Information 先报道双方接近达成约 130 亿美元的交易，Semafor 2026-09-03 报道 NVIDIA 已同意以 129 亿美元收购，并称 HF 有 1800 万用户。截至 2026-11-05，HF 博客和 NVIDIA 新闻室都没有发布官方公告，交割状态不明（二手报道）。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 公司
- **上游依赖**：[[entities/pytorch|PyTorch]]
- **竞争 / 替代**：—

## 时间线

- 2016 成立（二手报道）
- 2023 D 轮 2.35 亿美元，估值 45 亿美元，Google、Amazon、NVIDIA、IBM、Salesforce 等参投（二手报道）
- 2023-12-06 数据处理库 datatrove 首个 PyPI 版本
- 2024 发布 [[entities/fineweb|FineWeb]] 与 FineWeb-Edu（NeurIPS 2024 论文）
- 2025-06 FineWeb 2 论文，覆盖 1000 多种语言
- 2026-02-20 ggml.ai（llama.cpp、ggml 的维护团队）加入 HF，财务条款未披露
- 2026-08 社区统计 Hub 公开模型超过 300 万个；Business Insider 报道其探索出售，The Information 报道 NVIDIA 接近以约 130 亿美元收购（二手报道）
- 2026-09-03 Semafor 报道 NVIDIA 已同意以 129 亿美元收购 HF，官方未公告（二手报道）

## 相关实体

- [[entities/llama|Llama]]
- [[entities/qwen|Qwen]]
- [[entities/pytorch|PyTorch]]
- [[entities/llama-cpp|llama.cpp]]
- [[entities/trl|TRL]]
- [[entities/fineweb|FineWeb]]
- [[entities/common-crawl|Common Crawl]]
- [[entities/weaviate|Weaviate]]
- [[entities/nvidia|NVIDIA]]

## 相关概念

- [[concepts/transformer|Transformer]]
- [[concepts/lora|LoRA]]
- [[concepts/gguf|GGUF]]
- [[concepts/synthetic-data|合成数据]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "We are super happy to announce that GGML, creators of Llama.cpp, are joining HF in order to keep future AI open." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "The project will continue to be 100% open-source and community driven as it is now." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "Transformers acts as the model-definition framework for state-of-the-art machine learning with text, computer vision, audio, video, and multimodal models, for both inference and training." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "The 🍷 FineWeb dataset consists of more than 18.5T tokens (originally 15T tokens) of cleaned and deduplicated english web data from CommonCrawl." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "FineWeb 2 is the second iteration of the popular 🍷 FineWeb dataset, bringing high quality pretraining data to over 1000 🗣️ languages." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
