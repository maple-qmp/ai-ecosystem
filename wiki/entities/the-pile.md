---
title: The Pile
type: entity
tags: [project]
kind: dataset
layer: L1
aliases: ["The Pile", "Pile", "EleutherAI Pile"]
released: "2020-12"
competitors: ["[[entities/fineweb]]", "[[entities/dolma]]"]
depends_on: ["[[entities/common-crawl]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# The Pile

## 描述

EleutherAI 构建的开源英文语言建模数据集，由 22 个较小的数据集组合而成，2020-12-31 发布论文与数据，规模 825 GiB，许多子集来自学术或专业来源。按各成分的权重和 epoch 计算，有效规模约 1254 GiB；最大成分是 [[entities/common-crawl|Common Crawl]] 过滤而来的 Pile-CC（227 GiB，权重约 18%），其后是 PubMed Central、Books3、OpenWebText2、ArXiv、GitHub 等。它是开放预训练语料的早期标杆，也是版权争议的焦点：Books3 成分来自盗版站 Bibliotik，2023 年丹麦反盗版组织 Rights Alliance 发出 DMCA 通知后，托管方 The Eye 下架了 Books3，社区随后发布了去掉受版权内容的版本（Books3 下架为二手报道）。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 预训练语料
- **上游依赖**：[[entities/common-crawl|Common Crawl]]（Pile-CC）及 PubMed、arXiv、GitHub 等公开来源
- **竞争 / 替代**：后来的 [[entities/fineweb|FineWeb]]、[[entities/dolma|Dolma]]

## 时间线

- 2020-12-31 论文「The Pile: An 800GB Dataset of Diverse Text for Language Modeling」提交 arXiv（2101.00027），数据同时公开
- 2022-01-13 发布数据表（arXiv 2201.07311）
- 2023-08 Books3 被 The Eye 下架（TorrentFreak 2023-08-16 报道）

## 相关实体

- [[entities/common-crawl|Common Crawl]]
- [[entities/fineweb|FineWeb]]
- [[entities/dolma|Dolma]]

## 相关概念

- [[concepts/scaling-laws|Scaling Laws]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "we present the Pile: an 825 GiB English text corpus targeted at training large-scale language models." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "The Pile is a large, diverse, open source language modelling data set that consists of many smaller datasets combined together." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
