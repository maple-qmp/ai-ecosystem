---
title: 向量数据库
type: concept
tags: [term]
layer: L1
aliases: ["Vector Database", "向量库"]
as_of: 2026-06
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: []
---

# 向量数据库

> [!info] 种子页面
> 由 Claude 基于训练知识生成（截至 2026-06），尚无来源支撑。核实后补充 `sources`，并把 `reviewed` 设为 `true`。

## 定义

以向量嵌入为索引、支持近似最近邻（ANN）检索的数据库，是 [[concepts/rag|RAG]] 与语义搜索的常用存储层。

## 关键特征

- 存储 embedding 并做相似度检索
- 常用 HNSW 等 ANN 索引
- 专用产品与传统数据库插件（如 pgvector）并存

## 应用

- 语义搜索
- RAG
- 推荐

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]]

## 相关概念

- [[concepts/rag|检索增强生成（RAG）]]

## 相关实体

- [[entities/langchain|LangChain]]

## 我的判断

## 来源摘录

