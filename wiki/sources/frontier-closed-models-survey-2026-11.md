---
title: 前沿闭源模型时间线调研：GPT、Claude、Gemini、Grok（2026-11）
type: source
tags: [notes]
source_note: "[[前沿闭源模型时间线调研-2026-11]]"
url: https://developers.openai.com/api/docs/changelog
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[entities/gpt]]"
  - "[[entities/claude]]"
  - "[[entities/gemini]]"
  - "[[entities/grok]]"
  - "[[entities/xai]]"
  - "[[entities/openai]]"
  - "[[entities/anthropic]]"
  - "[[entities/google-deepmind]]"
  - "[[entities/cursor]]"
---

# 前沿闭源模型时间线调研：GPT、Claude、Gemini、Grok（2026-11）

## Summary

核实 [[entities/gpt|GPT]]、[[entities/claude|Claude]]、[[entities/gemini|Gemini]] 三个种子页，并新增 [[entities/grok|Grok]] 与 [[entities/xai|xAI（SpaceX Super Intelligence）]]。模型日期取 OpenAI、Anthropic、Google 的官方模型页、API changelog 和弃用表（2026-11-05 读取）；公司事件取 Wikipedia。到 2026-11，三家旗舰都是 1M 级上下文，并且都把最强的一档先给受信机构：OpenAI 的 GPT-6 Astra（2026-09）、Anthropic 的 Mythos（2026-04 起）、Google 的 Gemini 4 Argon（2026-09 预览）。xAI 2026-02 被 SpaceX 收购，之后又收购 Cursor，Grok 4.5 起与 Cursor 共同开发。

## Key Points

- **GPT**：GPT-5（2025-08-07）把快速模型、推理模型和路由器合成一个系统，o 系列并入主线；5.x 每 1～2 个月一版；GPT-5.6（2026-07）起按 Sol / Terra / Luna 分档；GPT-6 Astra（2026-09-03）是当前旗舰，$10 / $50，1.05M 上下文
- **Claude**：Haiku / Sonnet / Opus 之上新增 Mythos 档（只给经验证的组织）和面向公众、带安全限制的 Fable；当前阵容 Fable 5.1、Opus 5.5（官方推荐默认）、Sonnet 5.5、Haiku 5.5，全部 1M 上下文；2026-06 曾因美国商务部指令暂停 Mythos 级模型对外国人的访问
- **Gemini**：1.5 起 MoE 与 1M 上下文；3.x 时期 Flash 系列几乎每月一版；Gemini 4 Argon 2026-10-13 GA；2.5 Pro / Flash 2026-12-01 起自动转发到新模型
- **Grok**：Grok-1 曾开放权重，Grok 2.5 以 source-available 许可放出；之后都是闭源；Grok 4.5（2026-07-08）先在 Grok Build 和 Cursor 上线
- **xAI**：2025-03 并入 X，2026-02 并入 SpaceX，2026-10 改名 SpaceX Super Intelligence；2026-08 完成 600 亿美元收购 [[entities/cursor|Cursor]]
- **模型生命周期**：OpenAI 2026-02 在 ChatGPT 下线 GPT-4o；Anthropic 承诺长期保存退役模型权重，并给每个模型标注最早退役日；Google 用自动转发处理旧模型
- **共同趋势**：最强模型先走受信准入（网络安全、生物等高风险能力），再逐步放开；见 [[concepts/reasoning-model|推理模型]]

## Mentioned Pages

- [[entities/gpt|GPT]]
- [[entities/claude|Claude]]
- [[entities/gemini|Gemini]]
- [[entities/grok|Grok]]
- [[entities/xai|xAI（SpaceX Super Intelligence）]]
- [[entities/openai|OpenAI]]
- [[entities/anthropic|Anthropic]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/cursor|Cursor]]
- [[entities/gpt-oss|gpt-oss]]
- [[entities/claude-code|Claude Code]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
