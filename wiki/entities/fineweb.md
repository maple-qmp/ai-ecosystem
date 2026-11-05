---
title: FineWeb
type: entity
tags: [project]
kind: dataset
layer: L1
aliases: ["FineWeb", "FineWeb-Edu", "FineWeb 2", "FineWeb2", "HuggingFaceFW/fineweb"]
org: "[[entities/hugging-face]]"
released: "2024"
competitors: ["[[entities/dolma]]", "[[entities/the-pile]]"]
depends_on: ["[[entities/common-crawl]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# FineWeb

## 描述

[[entities/hugging-face|Hugging Face]] 发布的开放网页预训练数据集系列。FineWeb 是 15 万亿 token 的英文语料，取自 96 个 [[entities/common-crawl|Common Crawl]] 快照，磁盘约 44 TB，论文发表在 NeurIPS 2024 数据集与基准赛道，称用它训练的模型优于其他开放预训练数据集。FineWeb-Edu 是用自训练分类器筛出的教育类子集，有 1.3 万亿 token（高阈值）和 5.4 万亿 token（较低阈值）两档。两者都以 ODC-By 1.0 发布，同时受 Common Crawl 使用条款约束（以上数字为二手报道）。FineWeb 2 把流程扩展到 1000 多种语言：用 GlotLID 识别语言，按语言全局去重、按语言单独调参过滤并匿名化 PII；它保留每个去重簇的大小，可以按簇大小“回填”上采样。整个流程可以用 Hugging Face 的数据处理库 datatrove 复现。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 预训练语料
- **上游依赖**：[[entities/common-crawl|Common Crawl]]
- **竞争 / 替代**：[[entities/dolma|Dolma]]、[[entities/the-pile|The Pile]]

## 时间线

- 2023-12-06 datatrove 首个版本（PyPI）
- 2024 发布 FineWeb 与 FineWeb-Edu（论文 arXiv 2406.17557，NeurIPS 2024）
- 2025-06 FineWeb 2 论文（arXiv 2506.20920）
- 2026-09-30 datatrove 0.10.1

## 相关实体

- [[entities/hugging-face|Hugging Face]]
- [[entities/common-crawl|Common Crawl]]
- [[entities/dolma|Dolma]]
- [[entities/the-pile|The Pile]]

## 相关概念

- [[concepts/synthetic-data|合成数据]]
- [[concepts/scaling-laws|Scaling Laws]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "FineWeb 2 is the second iteration of the popular 🍷 FineWeb dataset, bringing high quality pretraining data to over 1000 🗣️ languages." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Unlike in FineWeb, where data was deduplicated per CommonCrawl snapshot, in FineWeb 2, data is deduplicated per language globally." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
