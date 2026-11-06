---
title: 多模态与嵌入模型调研：图像、视频、语音、嵌入（2026-11）
type: source
tags: [notes]
source_note: "[[多模态与嵌入模型调研-2026-11]]"
url: https://github.com/black-forest-labs/flux2
created: 2026-11-05
updated: 2026-11-06
sources:
  - "[[entities/stable-diffusion]]"
  - "[[entities/stability-ai]]"
  - "[[entities/flux]]"
  - "[[entities/black-forest-labs]]"
  - "[[entities/gpt-image]]"
  - "[[entities/imagen]]"
  - "[[entities/sora]]"
  - "[[entities/veo]]"
  - "[[entities/kling]]"
  - "[[entities/kuaishou]]"
  - "[[entities/seedance]]"
  - "[[entities/whisper]]"
  - "[[entities/elevenlabs]]"
  - "[[entities/openai-embeddings]]"
  - "[[entities/qwen3-embedding]]"
  - "[[entities/bge]]"
  - "[[entities/baai]]"
  - "[[entities/voyage-embeddings]]"
  - "[[entities/voyage-ai]]"
  - "[[entities/cohere-embed]]"
  - "[[entities/cohere]]"
  - "[[concepts/diffusion-model]]"
  - "[[concepts/embedding]]"
  - "[[concepts/text-to-speech]]"
  - "[[entities/openai]]"
  - "[[entities/google-deepmind]]"
  - "[[entities/bytedance]]"
  - "[[entities/alibaba]]"
---

# 多模态与嵌入模型调研：图像、视频、语音、嵌入（2026-11）

## Summary

为 L2 补上语言模型以外的四类基础模型：图像生成（[[entities/stable-diffusion|Stable Diffusion]]、[[entities/flux|FLUX]]、[[entities/gpt-image|GPT Image]]、[[entities/imagen|Imagen]]）、视频生成（[[entities/sora|Sora]]、[[entities/veo|Veo]]、[[entities/kling|可灵]]、[[entities/seedance|Seedance / 即梦]]）、语音（[[entities/whisper|Whisper]]、[[entities/elevenlabs|ElevenLabs]]、[[concepts/text-to-speech|TTS]]）和嵌入（[[entities/openai-embeddings|OpenAI text-embedding]]、[[entities/qwen3-embedding|Qwen3-Embedding]]、[[entities/bge|BGE]]、[[entities/voyage-embeddings|Voyage]]、[[entities/cohere-embed|Cohere Embed]]）。首轮（2026-11-05）只能访问 GitHub，一手材料仅为各项目 README，其余来自报道；2026-11-06 网络放开后，用 Wikipedia 和厂商官方页面（OpenAI 弃用表与 changelog、Gemini API changelog、Cohere changelog、MongoDB 新闻稿、BFL / ElevenLabs 博客、ByteDance Seed 官网、快手新闻稿）逐条核实，更正了 5 处并补充大量日期，见原文第 6 节。

## Key Points

- **图像**：开放权重主力从 Stable Diffusion 转到原作者另立的 FLUX；闭源侧图像生成并入多模态 LLM：GPT Image 是自回归模型（gpt-image-2 2026-04 出图前推理，2.5 / 2.6 分 Sunburst / Flare 两档），Gemini 的 Nano Banana；DALL·E 2026-05、Imagen 4 2026-08、gpt-image-1 2026-10 先后在 API 下线
- **视频**：Veo 3（2025-05）起原生音频成为标配；OpenAI 2026-03 宣布关停 Sora（据报道每天运营成本约 100 万美元），API 2026-09-24 下线；Google 没有发 Veo 4，转向 Gemini Omni（11-05 Omni 1.2 Flash GA）；可灵 4.0、Seedance 2.5 都做到单次 30 秒；FLUX 3 用一个模型同时生成图像、视频和音频；Seedance 2.0 因生成真人与知名 IP 被迪士尼 2026-02-13 发函
- **语音**：Whisper（2022-09，MIT）仍是开源识别基线，但 OpenAI 的 whisper-1、tts-1、gpt-4o-mini-tts 等旧语音 API 都将在 2027 年初下线，统一迁到 GPT-Realtime / GPT-Live / GPT-Transcribe；ElevenLabs 2026-09 发布 Eleven v4，估值 220 亿美元；Kokoro-82M、CosyVoice 3 等开源 TTS 已够用
- **嵌入**：开放权重的 Qwen3-Embedding（MTEB 多语言第一）、BGE-M3 与闭源持平，但 2026 年没有新一代；2026 年主线是多模态嵌入（Qwen3-VL-Embedding、Gemini Embedding 2、voyage-multimodal-3.5、Cohere Embed 5）和嵌入并入数据库（MongoDB 收购 Voyage AI）；Cohere 同年宣布收购 Aleph Alpha，见 [[concepts/embedding|嵌入]]、[[concepts/rag|RAG]]、[[concepts/vector-database|向量数据库]]
- **方法**：图像 / 视频模型的共同基础是[[concepts/diffusion-model|扩散模型]]，主干已从 UNet 换成 Transformer（MM-DiT、flow matching）
- **版权**：Getty 诉 Stability（英国 2025-11 基本败诉，美国仍在审）、Seedance 2.0 被迪士尼发函和美国参议员要求关停，是这一层的主要法律风险；迪士尼则选择与 OpenAI 合作授权（随 Sora 关停结束）

## Mentioned Pages

- [[entities/stable-diffusion|Stable Diffusion]]
- [[entities/stability-ai|Stability AI]]
- [[entities/flux|FLUX]]
- [[entities/black-forest-labs|Black Forest Labs]]
- [[entities/gpt-image|GPT Image（含 DALL·E）]]
- [[entities/imagen|Imagen]]
- [[entities/sora|Sora]]
- [[entities/veo|Veo]]
- [[entities/kling|可灵 Kling]]
- [[entities/kuaishou|快手]]
- [[entities/seedance|Seedance / 即梦]]
- [[entities/whisper|Whisper]]
- [[entities/elevenlabs|ElevenLabs]]
- [[entities/openai-embeddings|OpenAI text-embedding]]
- [[entities/qwen3-embedding|Qwen3-Embedding]]
- [[entities/bge|BGE]]
- [[entities/baai|北京智源人工智能研究院（BAAI）]]
- [[entities/voyage-embeddings|Voyage]]
- [[entities/voyage-ai|Voyage AI]]
- [[entities/cohere-embed|Cohere Embed]]
- [[entities/cohere|Cohere]]
- [[entities/openai|OpenAI]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/gemini|Gemini]]
- [[entities/bytedance|字节跳动]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/qwen|Qwen]]
- [[concepts/diffusion-model|扩散模型]]
- [[concepts/embedding|嵌入（Embedding）]]
- [[concepts/text-to-speech|语音合成（TTS）]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/vector-database|向量数据库]]
