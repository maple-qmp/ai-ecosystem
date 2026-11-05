---
title: 语音合成（TTS）
type: concept
tags: [field]
layer: L2
aliases: ["语音合成", "TTS", "Text-to-Speech", "文本转语音", "语音模型"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# 语音合成（TTS）

## 定义

把文本转成自然语音的模型与技术。本页同时记录它的反方向语音识别（ASR），以及把两者合成一个模型的实时语音对话，三者合起来是 L2 的语音模型。

## 关键特征

- **合成（TTS）**：闭源有 [[entities/elevenlabs|ElevenLabs]] Eleven v3（2025-06，70 多种语言、多人对话、音频标签控制情绪）、OpenAI gpt-4o-mini-tts（2025-03，可用指令控制语气，只有预置音色）、Gemini 2.5 TTS；开放权重有 Kokoro-82M（Apache）、阿里 Fun-CosyVoice 3.0（基于 LLM 的零样本多语种，0.5B）、Sesame CSM、Chatterbox、Dia、Orpheus
- **声音克隆**：零样本克隆已很普遍（CosyVoice、Chatterbox），Kokoro 这类小模型不支持
- **识别（ASR）**：开源的 [[entities/whisper|Whisper]]（2022-09，MIT）仍是基线；闭源后继有 gpt-4o-transcribe / GPT-Transcribe 和 ElevenLabs Scribe
- **语音到语音**：OpenAI 推荐低延迟场景直接用 Realtime API 的 speech-to-speech 模型，2026 年有 GPT-Realtime 2.x 和全双工的 GPT-Live 1；Google 有 Gemini Live；ElevenLabs 有 Eleven v3 Conversational。这些主要服务语音 [[concepts/ai-agent|AI Agent]]

## 应用

- 语音助手与语音 Agent、客服
- 配音、有声书、视频旁白
- 会议转写、字幕

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]]（语音模型）

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/transformer|Transformer]]

## 相关实体

- [[entities/whisper|Whisper]]
- [[entities/elevenlabs|ElevenLabs]]
- [[entities/openai|OpenAI]]
- [[entities/gpt|GPT]]
- [[entities/gemini|Gemini]]
- [[entities/minimax|MiniMax]]
- [[entities/stability-ai|Stability AI]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Kokoro is an open-weight TTS model with 82 million parameters." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（hexgrad/kokoro README）
- "Whisper is a general-purpose speech recognition model." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（openai/whisper README）
