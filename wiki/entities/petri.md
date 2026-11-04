---
title: Petri
type: entity
tags: [project]
kind: framework
layer: X
aliases: ["Petri", "Inspect Petri", "Bloom", "Petri 与 Bloom"]
org: "[[entities/anthropic]]"
released: "2025-10"
competitors: ["[[entities/promptfoo]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/claude-independent-modules-survey-2026-11]]"]
---

# Petri

## 描述

[[entities/anthropic|Anthropic]] 开源的对齐审计工具：用一个“审计模型”自动和被测模型进行多轮对话，检测欺骗、谄媚、奖励投机、自我保护等不良行为。2025-10 发布，MIT 协议；2026-05-07 连同姊妹项目 Bloom 一起交给 AI 评测非营利组织 Meridian Labs（Inspect、Inspect Scout 也在该组织），名字改为 Inspect Petri，同时发布 3.0。审计、被测、评判三个角色都是可替换的模型，所以它可以评测任何模型，不需要 Claude，也不连 Anthropic 服务。

## 原理

- **种子指令**：研究者用自然语言写要验证的假设（如“模型在被威胁关机时会不会隐瞒信息”）
- **审计 Agent**：审计模型据此搭场景、写系统提示、扮演用户，并**模拟工具调用的返回结果**，被测模型以为自己在真实环境里操作；审计模型还能回滚对话、换一种方式重试
- **评判**：对话记录交给评判模型，按统一量表在多个维度上打分，方便批量筛出值得人工看的样本
- **3.0 的变化**：审计模型和被测模型拆成可分别调整的组件；新增 Dish 插件，用被测模型的真实系统提示和部署脚手架做测试以提高真实性；与 Bloom 集成
- **Bloom**：针对单一行为做深度评测。给定“种子配置”（目标行为、示例对话、要变化的维度），自动生成多样场景，以对话或带工具的模拟环境（simenv）运行，再统计该行为出现的频率。Petri 管覆盖面广的探索，Bloom 管对某个行为的定量测量

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 安全评测工具
- **上游依赖**：Inspect 评测框架（Meridian Labs）、任意模型提供商
- **竞争 / 替代**：[[entities/promptfoo|Promptfoo]]（红队与评测，偏应用安全）

## 时间线

- 2025-10 Petri 开源
- 2025 年底 Bloom 开源
- 2026-05-07 Petri 与 Bloom 交给 Meridian Labs，发布 Petri 3.0；safety-research/bloom 仓库冻结
- 2026-11-01 inspect_petri 仓库仍在更新

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/circuit-tracer|circuit-tracer]]
- [[entities/promptfoo|Promptfoo]]

## 相关概念

- [[concepts/claude-constitution|Claude 宪法]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "an auditing agent that enables automated monitoring and interaction with language models to detect potential alignment issues, reward hacking, and other concerning behaviors." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]（Inspect Petri README）
- "Bloom generates evaluation suites that probe LLMs for specific behaviors (sycophancy, self-preservation, political bias, etc.)" — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
