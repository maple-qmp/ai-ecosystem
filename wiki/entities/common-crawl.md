---
title: Common Crawl
type: entity
tags: [project]
kind: dataset
layer: L1
aliases: ["Common Crawl", "Common Crawl Foundation", "CommonCrawl"]
released: "2008"
competitors: []
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# Common Crawl

## 描述

非营利组织 Common Crawl Foundation 维护的公开网页抓取档案，是几乎所有开放预训练语料的原料。组织 2007 年由 Gil Elbaz 创立（他至今任董事长），2008 年起抓取并公开数据；档案累计超过 10 PB，大约每月发布一次抓取，每次通常超过 20 亿个网页。资金长期主要来自 Elbaz 家族基金会，2023 年起开始接受 AI 行业捐赠。Google 的 C4、BLOOM 的 OSCAR、[[entities/the-pile|The Pile]] 的 Pile-CC 成分和 [[entities/fineweb|FineWeb]] 都是在它的快照上过滤得到的（下游数据集的说法来自 Wikipedia，其余已对照 Common Crawl 官网核实）。数据存放在 AWS 公共数据集和多个学术云平台上，包括原始网页、元数据和抽取后的文本。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 预训练语料（原始网页）
- **下游**：[[entities/fineweb|FineWeb]]、[[entities/the-pile|The Pile]]（Pile-CC）、[[entities/dolma|Dolma]]（Dolma 3 清洗池的网页部分）；Hugging Face 的 datatrove 提供读取 Common Crawl WARC 并抽取、过滤文本的完整流水线

## 时间线

- 2007 Gil Elbaz 创立 Common Crawl Foundation
- 2008 开始抓取并发布数据
- 2023 开始接受 AI 行业捐赠（Wikipedia）

## 相关实体

- [[entities/fineweb|FineWeb]]
- [[entities/the-pile|The Pile]]
- [[entities/dolma|Dolma]]
- [[entities/hugging-face|Hugging Face]]

## 相关概念

- [[concepts/scaling-laws|Scaling Laws]]
- [[concepts/synthetic-data|合成数据]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Common Crawl is a nonprofit 501(c)(3) organisation that crawls the web and freely provides its archives and datasets to the public." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Crawls are published approximately once a month, each typically containing more than two billion web pages." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Unlike in FineWeb, where data was deduplicated per CommonCrawl snapshot, in FineWeb 2, data is deduplicated per language globally." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
