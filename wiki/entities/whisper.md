---
title: Whisper
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Whisper", "OpenAI Whisper", "whisper-large-v3", "large-v3-turbo"]
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
updated: 2026-11-05
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Whisper

## 描述

[[entities/openai|OpenAI]] 2022-09-21 以 MIT 许可开源的通用语音识别模型，用 68 万小时网络音频以弱监督方式训练。它是 [[concepts/transformer|Transformer]] 编码器-解码器，同一个模型就能做多语言转写、译成英语、语种识别和语音活动检测。共六档：tiny 39M、base 74M、small 244M、medium 769M、large 1550M，以及 2024-10 的 turbo（large-v3 的解码器从 32 层减到 4 层，809M，约快 8 倍，但没有为翻译训练）。2025-03 OpenAI 推出闭源的 gpt-4o-transcribe 作为后继，并称它的词错误率更低；但开源权重的 Whisper 仍被广泛用于本地语音识别。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重，语音识别）
- **上游依赖**：[[entities/pytorch|PyTorch]]、[[entities/tiktoken|tiktoken]]（分词）
- **竞争 / 替代**：OpenAI 自家的 gpt-4o-transcribe / GPT-Transcribe、[[entities/elevenlabs|ElevenLabs]] Scribe

## 时间线

- 2022-09-21 开源，论文 "Robust Speech Recognition via Large-Scale Weak Supervision"
- 2024-10-01 large-v3-turbo（809M，约快 8 倍）
- 2025-03-20 gpt-4o-transcribe / gpt-4o-mini-transcribe 与 gpt-4o-mini-tts 进 API，官方定位为 Whisper 的后继
- 2026 OpenAI 模型页的语音线为 GPT-Realtime 2.x、GPT-Live 1、GPT-Transcribe（见 [[entities/gpt|GPT]]）

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
