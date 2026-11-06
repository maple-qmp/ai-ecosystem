---
title: FineWeb
type: entity
tags: [project]
kind: dataset
layer: L1
aliases: ["FineWeb", "FineWeb-Edu", "FineWeb 2", "FineWeb2", "HuggingFaceFW/fineweb"]
org: "[[entities/hugging-face]]"
released: "2024-04"
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

[[entities/hugging-face|Hugging Face]] 发布的开放网页预训练数据集系列。FineWeb 是清洗、去重后的英文网页语料，取自 2013 年以来的全部 [[entities/common-crawl|Common Crawl]] 快照。2024-04 首发时为 15 万亿 token、96 个快照（论文发表在 NeurIPS 2024 数据集与基准赛道，称用它训练的模型优于其他开放预训练数据集）；此后持续加入新快照，到 v1.4.0（2025-07）已超过 18.5 万亿 token。FineWeb-Edu 是用自训练的教育类分类器从 FineWeb 中筛出的子集，有 1.3 万亿 token 和 5.4 万亿 token（score-2）两档，分类器也一并开源。FineWeb 2 把流程扩展到多语言：取自 96 个快照（2013 年夏至 2024-04），约 20 TB、50 亿文档，覆盖 1,868 个语言—文字组合；它用 GlotLID 识别语言，按语言全局去重、按语言单独调参过滤并匿名化 PII，保留每个去重簇的大小以便按簇大小“回填”上采样，还公开了被过滤掉的数据。三者都以 ODC-By 1.0 许可发布。整个流程可以用 Hugging Face 的数据处理库 datatrove 复现。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 预训练语料
- **上游依赖**：[[entities/common-crawl|Common Crawl]]
- **竞争 / 替代**：[[entities/dolma|Dolma]]、[[entities/the-pile|The Pile]]

## 时间线

- 2023-12-06 datatrove 首个版本（PyPI）
- 2024-04-21 FineWeb v1.0.0（15 万亿 token）
- 2024-06-02 FineWeb-Edu v1.0.0
- 2024-06-25 FineWeb 论文（arXiv 2406.17557，后发表于 NeurIPS 2024）
- 2025-01-31 FineWeb v1.3.0：补全部分快照，并因一份停止侵权通知（C&D）移除特定域名
- 2025-06-26 FineWeb2 论文（arXiv 2506.20920）
- 2025-07-11 FineWeb v1.4.0：加入 2025 年 1–6 月的 6 个快照，总量超过 18.5 万亿 token
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

- "The 🍷 FineWeb dataset consists of more than 18.5T tokens (originally 15T tokens) of cleaned and deduplicated english web data from CommonCrawl." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "we introduce FineWeb, a 15-trillion token dataset derived from 96 Common Crawl snapshots that produces better-performing LLMs than other open pretraining datasets." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "FineWeb 2 is the second iteration of the popular 🍷 FineWeb dataset, bringing high quality pretraining data to over 1000 🗣️ languages." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Unlike in FineWeb, where data was deduplicated per CommonCrawl snapshot, in FineWeb 2, data is deduplicated per language globally." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
