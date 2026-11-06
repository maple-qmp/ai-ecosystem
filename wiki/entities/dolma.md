---
title: Dolma
type: entity
tags: [project]
kind: dataset
layer: L1
aliases: ["Dolma", "Dolma Toolkit", "Dolma 3", "allenai/dolma"]
released: "2023"
competitors: ["[[entities/fineweb]]", "[[entities/the-pile]]"]
depends_on: ["[[entities/common-crawl]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# Dolma

## 描述

Allen Institute for AI（Ai2）的开放预训练语料，同时也是一个数据整理工具包。数据集初版有 3 万亿 token，混合网页、科学论文、代码、公版图书、社交媒体和百科，是 Ai2 OLMo 模型的训练语料，在 Hugging Face 发布，2024-04 起改用 ODC-BY 许可，论文为 arXiv 2402.00159。工具包（`pip install dolma`，Apache-2.0）可以并行处理数十亿文档，内置 Gopher、C4、OpenWebText 风格的质量标注器，用 Rust 写的 Bloom 过滤器做快速去重。2025 年随 Olmo 3 发布的 Dolma 3 分三个训练阶段：预训练混合 5.93 万亿 token（23.7 TB、38.7 亿文档），取自 9.31 万亿 token 的清洗池，池中含 Common Crawl 网页和经 olmOCR 处理的科学 PDF；第二阶段退火用的 Dolmino 混合 1000 亿 token；第三阶段长上下文用的 Longmino 混合 500 亿 token。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 预训练语料 + 数据工具
- **上游依赖**：[[entities/common-crawl|Common Crawl]]（Dolma 3 清洗池的网页部分）
- **竞争 / 替代**：[[entities/fineweb|FineWeb]]（及其 datatrove 工具链）、[[entities/the-pile|The Pile]]

## 时间线

- 2023-07-09 dolma 工具包首个 PyPI 版本 0.6.0
- 2023-08-18 Dolma v1 发布
- 2023-10-31 v1.5（约 3 万亿 token，训练 OLMo-1B）
- 2024-01-31 v1.6；同日 Dolma 论文提交 arXiv（2402.00159）
- 2024-04-15 许可改为 ODC-BY
- 2024-04-17 v1.7，训练 OLMo-7B-v1.7
- 2025-07-07 dolma 工具包 1.2.1
- 2025-09 至 2025-11 Dolma 3 各数据集陆续上传 Hugging Face，用于 Olmo 3 7B / 32B

## 相关实体

- [[entities/fineweb|FineWeb]]
- [[entities/the-pile|The Pile]]
- [[entities/common-crawl|Common Crawl]]
- [[entities/hugging-face|Hugging Face]]

## 相关概念

- [[concepts/scaling-laws|Scaling Laws]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The Dolma 3 pool is a dataset of over 9 trillion tokens from a diverse mix of web content, academic publications, code, and more." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Dolma is an open dataset of 3 trillion tokens from a diverse mix of web content, academic publications, code, books, and encyclopedic materials." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "It was created as a training corpus for OLMo, a language model from the Allen Institute for AI (AI2)." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
