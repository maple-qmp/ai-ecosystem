---
title: Qwen3-Embedding
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Qwen3-Embedding", "Qwen3-Reranker", "Qwen3-VL-Embedding", "Qwen3-VL-Reranker", "通义千问嵌入模型"]
org: "[[entities/alibaba|阿里巴巴（通义）]]"
released: "2025-06"
open_weights: true
competitors: ["[[entities/bge]]", "[[entities/openai-embeddings]]", "[[entities/voyage-embeddings]]", "[[entities/cohere-embed]]"]
depends_on: ["[[entities/qwen]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Qwen3-Embedding

## 描述

[[entities/alibaba|阿里巴巴]] Qwen 团队基于 [[entities/qwen|Qwen3]] 稠密模型做的开放权重[[concepts/embedding|嵌入]]与重排模型，2025-06 发布。嵌入模型和重排模型各有 0.6B、4B、8B 三档，序列长度都是 32K，嵌入维度分别为 1024、2560、4096，支持 MRL（可自定义输出维度）和按任务写指令（官方称写指令一般能提升 1%～5%），覆盖 100 多种语言和编程语言。8B 嵌入模型截至 2025-06-05 在 MTEB 多语言榜排第一（70.58）。2026-01 发布的 Qwen3-VL-Embedding / Reranker（2B、8B，Apache-2.0）基于 Qwen3-VL，能把文本、图像、截图、视频和混合输入编码进同一向量空间。它是 [[concepts/rag|RAG]] 和[[concepts/vector-database|向量数据库]]里最常用的开放权重嵌入之一。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重，文本与多模态嵌入、重排）
- **上游依赖**：[[entities/qwen|Qwen]]（Qwen3 / Qwen3-VL 基座）
- **竞争 / 替代**：[[entities/bge|BGE]]、[[entities/openai-embeddings|OpenAI text-embedding]]、[[entities/voyage-embeddings|Voyage]]、[[entities/cohere-embed|Cohere Embed]]

## 时间线

- 2025-06-03 Qwen3-Embedding 与 Qwen3-Reranker（0.6B / 4B / 8B）上传 Hugging Face
- 2025-06-05 8B 嵌入模型居 MTEB 多语言榜第一（70.58）
- 2026-01-07 Qwen3-VL-Embedding 2B / 8B 上传 Hugging Face；01-08 技术报告
- 截至 2026-11 没有更新的 Qwen 嵌入模型

## 相关实体

- [[entities/qwen|Qwen]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/bge|BGE]]
- [[entities/openai-embeddings|OpenAI text-embedding]]

## 相关概念

- [[concepts/embedding|嵌入（Embedding）]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/vector-database|向量数据库]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The 8B size embedding model ranks No.1 in the MTEB multilingual leaderboard (as of June 5, 2025, score 70.58), while the reranking model excels in various text retrieval scenarios." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（QwenLM/Qwen3-Embedding README，原文加粗已去掉）
- "State-of-the-art multimodal embedding and reranking models built on Qwen3-VL, supporting text, images, screenshots, videos, and mixed-modal inputs for advanced information retrieval and cross-modal understanding." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（QwenLM/Qwen3-VL-Embedding README）
