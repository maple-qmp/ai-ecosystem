---
title: ElevenLabs
type: entity
tags: [organization]
kind: company
layer: X
aliases: ["ElevenLabs", "Eleven Labs", "Eleven v3", "Eleven v4", "Scribe", "Eleven Realtime"]
released: "2022"
competitors: ["[[entities/openai]]", "[[entities/google-deepmind]]", "[[entities/minimax]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# ElevenLabs

## 描述

总部在伦敦的语音 AI 公司，2022 年由两位波兰人创立：Mati Staniszewski（CEO，前 Palantir）和 Piotr Dąbkowski（CTO，前 Google）。名字里的 Eleven 指波兰独立日 11 月 11 日。它自研语音合成与识别模型，在此之上做配音、有声书和语音 Agent 平台 ElevenAgents。模型都闭源、只走 API，主要有三条线：
- **合成**：Eleven v3（2025-06 alpha，70 多种语言、多人对话、音频标签）；Eleven v4 与 v4 Turbo（2026-09-28），官方称是“最有情感表现力”的模型。
- **识别**：Scribe（2025-02）。
- **实时 Agent**：Eleven Realtime（2026-10-20）。

估值增长很快：2024-01 首次超过 10 亿美元，2025-01 达到 33 亿，2026-02 的 D 轮为 110 亿，2026-09-30 官方宣布员工股出售估值达 220 亿美元。它的声音克隆也引发过滥用事件：2024-01 新罕布什尔州冒充拜登的 AI 电话，就被追溯到它的工具。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 公司（L2 语音模型，见 [[maps/L2-基础模型|L2-基础模型]]「语音」）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/openai|OpenAI]]（GPT-Realtime / GPT-Live、[[entities/whisper|Whisper]] 的后继）、[[entities/google-deepmind|Google DeepMind]]（Gemini TTS / Live）、[[entities/minimax|MiniMax]]（语音）

## 时间线

- 2022 成立
- 2023-01 公开 beta；200 万美元预种子轮
- 2023-06 A 轮 1900 万美元，估值约 1 亿美元
- 2024-01-22 B 轮 8000 万美元，估值 11 亿美元
- 2025-01-30 C 轮 1.8 亿美元，估值 33 亿美元
- 2025-02 Scribe 语音识别
- 2025-06-03 Eleven v3（alpha）
- 2025-09 员工股出售，估值 66 亿美元
- 2026-02 Eleven v3 Conversational
- 2026-02-04 D 轮 5 亿美元，Sequoia 领投，估值 110 亿美元
- 2026-09-10 与环球音乐签多年战略协议
- 2026-09-28 Eleven v4 与 Eleven v4 Turbo
- 2026-09-30 宣布估值升至 220 亿美元（员工股出售）
- 2026-10-20 Eleven Realtime

## 相关实体

- [[entities/whisper|Whisper]]
- [[entities/openai|OpenAI]]
- [[entities/minimax|MiniMax]]
- [[entities/stability-ai|Stability AI]]（同样转向音频与唱片公司合作）

## 相关概念

- [[concepts/text-to-speech|语音合成（TTS）]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "ElevenLabs Inc. is a software company that specializes in developing natural-sounding speech synthesis software using deep learning." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Wikipedia）
