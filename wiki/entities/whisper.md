---
title: Whisper
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Whisper", "OpenAI Whisper", "whisper-1", "whisper-large-v3", "large-v3-turbo"]
org: "[[entities/openai|OpenAI]]"
released: "2022-09"
open_weights: true
competitors: ["[[entities/elevenlabs]]"]
depends_on: ["[[entities/pytorch]]", "[[entities/tiktoken]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Whisper

## 描述

[[entities/openai|OpenAI]] 2022-09-21 以 MIT 许可开源的通用语音识别模型。它用 68 万小时网络音频弱监督训练，其中 11.7 万小时是 96 种非英语语言。结构是标准的 [[concepts/transformer|Transformer]] 编码器-解码器：输入 30 秒一段的 log-Mel 频谱，靠特殊 token 在同一个模型里切换多语言转写、译成英语、语种识别和语音活动检测。据《纽约时报》报道，OpenAI 当初做它的一个目的是把 YouTube 视频和播客转写成文本来训练语言模型。权重有六档（tiny 39M 到 large 1550M，以及 2024-10 的 turbo 809M）。开源权重至今仍可用；但 OpenAI 的 API 版本 whisper-1 已于 2026-08-26 宣布弃用、2027-02-26 下线，OpenAI 自己的语音识别已改用闭源的 GPT-Transcribe、GPT-Live-Transcribe 和 GPT-Realtime-Whisper。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重，语音识别）
- **上游依赖**：[[entities/pytorch|PyTorch]]、[[entities/tiktoken|tiktoken]]（分词）
- **竞争 / 替代**：OpenAI 自家的 GPT-Transcribe 系列、[[entities/elevenlabs|ElevenLabs]] Scribe

## 时间线

- 2022-09-21 开源，论文 "Robust Speech Recognition via Large-Scale Weak Supervision"
- 2022-12-08 large-v2
- 2023-11 large-v3（DevDay）
- 2024-10-01 large-v3-turbo（809M，约快 8 倍）
- 2025-03-20 gpt-4o-transcribe / gpt-4o-mini-transcribe，官方定位为 Whisper 的后继
- 2026-05-07 GPT-Realtime-Whisper（流式识别）
- 2026-07-28 GPT-Transcribe 与 GPT-Live-Transcribe
- 2026-08-26 宣布 whisper-1 与 gpt-4o-transcribe 系列弃用，2027-02-26 从 API 移除

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/gpt|GPT]]
- [[entities/elevenlabs|ElevenLabs]]

## 相关概念

- [[concepts/text-to-speech|语音合成（TTS）]]
- [[concepts/transformer|Transformer]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Whisper is a general-purpose speech recognition model." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（openai/whisper README）
- "the `turbo` model is an optimized version of `large-v3` that offers faster transcription speed with a minimal degradation in accuracy." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（openai/whisper README）
- "On August 26, 2026, we notified developers using whisper-1, gpt-4o-transcribe, gpt-4o-mini-transcribe, and gpt-4o-transcribe-diarize of their deprecation and removal from the API on February 26, 2027." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（OpenAI 弃用表）
