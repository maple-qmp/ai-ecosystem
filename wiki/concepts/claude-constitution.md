---
title: Claude 宪法
type: concept
tags: [standard]
layer: X
aliases: ["Claude 宪法", "Claude's Constitution", "Claude 的宪法"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/claude-independent-modules-survey-2026-11]]"]
---

# Claude 宪法

## 定义

[[entities/anthropic|Anthropic]] 公开的一份基础文档，写明希望 [[entities/claude|Claude]] 具备的价值观以及背后的理由，涵盖怎样在保持安全和合乎伦理的前提下提供帮助，以及遇到冲突时如何取舍。现行版本是 2026-01 发布的新版，放在 GitHub 仓库 `anthropics/claude-constitution`，以 CC0 1.0 发布，也就是放弃版权、任何人都可以自由使用和改写。

## 关键特征

- **用于训练**：它是 Anthropic 训练 Claude 时用来塑造行为的依据，延续了 Constitutional AI（用一组原则让模型自我批评、修正）的思路
- **讲理由，不只列规则**：文档着重解释为什么这样做，而不是给出一张禁止清单
- **公开透明**：发布目的是让外界了解 Anthropic 如何引导 Claude；仓库会随版本更新，旧版归档保留
- **完全独立**：CC0 意味着其他团队可以直接拿来改写成自己模型的行为规范或评测依据

## 应用

- 给自研或开放权重模型写行为规范时作为参考范本
- 对齐评测：用 [[entities/petri|Petri]]、Bloom 这类工具检验模型是否符合某份规范
- 研究与政策讨论：比较各家公开的模型规范

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 安全与对齐
- **类似文档**：OpenAI 的 Model Spec

## 相关概念

- [[concepts/agents-md|AGENTS.md]]
- [[concepts/reasoning-model|推理模型]]

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/claude|Claude]]
- [[entities/petri|Petri]]
- [[entities/circuit-tracer|circuit-tracer]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "This repository contains Claude's Constitution—the foundational document that describes the values we want Claude to embody and the reasoning behind them." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
- "Released under CC0 1.0." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
