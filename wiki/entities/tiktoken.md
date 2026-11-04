---
title: tiktoken
type: entity
tags: [project]
kind: infra
layer: L3
aliases: ["tiktoken"]
org: "[[entities/openai]]"
released: "2022-12"
competitors: []
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/openai-developers-survey-2026-11]]"]
---

# tiktoken

## 描述

[[entities/openai|OpenAI]] 开源的 BPE 分词器，MIT 协议，Rust 内核加 Python 接口，用来在本地计算文本对应 OpenAI 模型的 token 数和切分方式。内置 r50k、p50k、cl100k、o200k 等编码，覆盖 GPT-2 到 [[entities/gpt|GPT]]-4o 及之后的模型；[[entities/gpt-oss|gpt-oss]] 用的是 o200k 系的编码。OpenAI 开发者文档的 SDK 页把它列为官方开源工具。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 分词
- **上游依赖**：—
- **竞争 / 替代**：Hugging Face tokenizers

## 脱离 OpenAI 使用

基本独立：计算全在本地，不需要账号。唯一的联网点是编码文件：首次使用某个编码时从 `openaipublic.blob.core.windows.net` 下载并缓存。离线或内网环境可用 `TIKTOKEN_CACHE_DIR` 指向预先放好的缓存目录。

## 时间线

- 2022-12 开源

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/gpt|GPT]]
- [[entities/gpt-oss|gpt-oss]]

## 相关概念

- [[concepts/transformer|Transformer]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

