---
title: Voyage AI
type: entity
tags: [organization]
kind: company
layer: X
aliases: ["Voyage AI", "VoyageAI"]
competitors: ["[[entities/cohere]]", "[[entities/openai]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Voyage AI

## 描述

专做[[concepts/embedding|嵌入]]和重排模型的公司，创始人是马腾宇（Tengyu Ma），模型家族见 [[entities/voyage-embeddings|Voyage]]。2025-02-24 被数据库公司 MongoDB 收购（本库尚无 MongoDB 页面）：第一阶段继续通过 Voyage 官网和 AWS、Azure Marketplace 提供模型，第二阶段并入 MongoDB Atlas，先做 Vector Search 的自动嵌入，再加原生重排。2026-01-15 的 Voyage 4 系列已直接集成进 Atlas，也可用于本地部署的 MongoDB 社区版。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 公司（L2 嵌入模型，现属 MongoDB）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/cohere|Cohere]]、[[entities/openai|OpenAI]]

## 时间线

- 2025-02-24 被 MongoDB 收购
- 2026-01-15 Voyage 4 系列 GA，集成进 MongoDB Atlas

## 相关实体

- [[entities/voyage-embeddings|Voyage]]
- [[entities/cohere|Cohere]]

## 相关概念

- [[concepts/embedding|嵌入（Embedding）]]
- [[concepts/vector-database|向量数据库]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "NEW YORK—February 24, 2025—MongoDB, Inc. (NASDAQ: MDB), the leading database for modern applications, today announced it has acquired Voyage AI, a pioneer in state-of-the-art embedding and reranking models that power next-generation AI applications." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（MongoDB 新闻稿）
