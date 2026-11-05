---
title: Dolma
type: entity
tags: [project]
kind: dataset
layer: L1
aliases: ["Dolma", "Dolma Toolkit", "Dolma 3", "allenai/dolma"]
released: "2023"
competitors: ["[[entities/fineweb]]", "[[entities/the-pile]]"]
depends_on: []
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

Allen Institute for AI（Ai2）的开放预训练语料，同时也是一个数据整理工具包。数据集初版有 3 万亿 token，混合网页、学术论文、代码、图书和百科，是 Ai2 的 OLMo 模型的训练语料，以 ODC-BY 许可在 Hugging Face 发布，论文为 arXiv 2402.00159。工具包（`pip install dolma`，Apache-2.0）可以并行处理数十亿文档，内置 Gopher、C4、OpenWebText 风格的质量标注器，用 Rust 写的 Bloom 过滤器做快速去重。Olmo 3 使用的 Dolma 3 分为三段：约 6 万亿 token 的预训练混合（取自约 9 万亿 token 的清洗池，含经 olmOCR 处理的科学 PDF）、约 1000 亿 token 的中训练集 Dolmino、约 500 亿 token 的长上下文集 Longmino（Dolma 3 数字为二手报道，各来源略有出入）。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 预训练语料 + 数据工具
- **竞争 / 替代**：[[entities/fineweb|FineWeb]]（及其 datatrove 工具链）、[[entities/the-pile|The Pile]]

## 时间线

- 2023-07-09 dolma 工具包首个 PyPI 版本 0.6.0
- 2024 Dolma 论文（arXiv 2402.00159）
- 2025-07-07 dolma 工具包 1.2.1
- 2025 随 Olmo 3 发布 Dolma 3（二手报道）

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

- "Dolma is an open dataset of 3 trillion tokens from a diverse mix of web content, academic publications, code, books, and encyclopedic materials." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "It was created as a training corpus for OLMo, a language model from the Allen Institute for AI (AI2)." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
