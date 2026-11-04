---
title: Promptfoo
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Promptfoo", "promptfoo"]
org: "[[entities/openai]]"
released: "2023"
competitors: ["[[entities/langsmith]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/openai-developers-survey-2026-11]]"]
---

# Promptfoo

## 描述

开源的 LLM 应用评测与红队测试工具，MIT 协议，TypeScript 编写（约 2.7 万星），也有 pip 包装。用 `promptfooconfig.yaml` 写提示、模型提供商和测试用例，每个用例带断言，可比较不同提示和模型、定位失败；红队功能用对抗输入探测越狱、提示注入、数据泄露等风险。2026-03 被 [[entities/openai|OpenAI]] 收购，现在是 OpenAI 开发者文档里推荐的评测方案，接替即将关闭的 Evals 平台。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 评测与红队
- **上游依赖**：—
- **竞争 / 替代**：[[entities/langsmith|LangSmith]] 评测、Braintrust、DeepEval、OpenAI simple-evals

## 脱离 OpenAI 使用

完全独立。本地命令行运行，提供商不限于 OpenAI（Anthropic、Google、本地 Ollama、任意 HTTP 端点都可），结果存在本地。官方表示收购后保持开源、继续 MIT 协议；也有评论指出未来代码的协议和治理没有书面保证。

## 同类：OpenAI 自家的评测工具

- **Evals 平台**（API 内）：2026-10-31 起停止新建，2026-11-30 关闭
- **openai/evals**：早期的评测框架和基准注册表，协议非标准（GitHub 标为其他）
- **simple-evals**（MIT）：OpenAI 发布模型时用的轻量评测脚本，可改成调其他模型

## 时间线

- 2023 开源发布
- 2026-03-09 宣布被 OpenAI 收购，技术计划并入企业平台 Frontier
- 2026-10 发布 0.125.x

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/langsmith|LangSmith]]
- [[entities/codex-cli|Codex CLI]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Promptfoo is part of OpenAI." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
