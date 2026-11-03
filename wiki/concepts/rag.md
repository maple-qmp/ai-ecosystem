---
title: 检索增强生成（RAG）
type: concept
tags: [method]
layer: L4
aliases: ["RAG", "Retrieval-Augmented Generation"]
as_of: 2026-06
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: []
---

# 检索增强生成（RAG）

## 定义

在生成前从外部知识库检索相关内容并放入上下文，让模型基于最新或私有资料作答。概念由 Lewis 等（Meta，2020）提出。

## 关键特征

- 降低幻觉、支持私有数据
- 核心环节：切分、嵌入、检索、重排
- 常与向量数据库配合

## 应用

- 企业知识库问答
- 文档助手

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]

## 相关概念

- [[concepts/vector-database|向量数据库]]
- [[concepts/ai-agent|AI Agent]]

## 相关实体

- [[entities/langchain|LangChain]]
- [[entities/meta-ai|Meta AI]]

## 我的判断

## 来源摘录

