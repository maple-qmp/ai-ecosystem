---
title: 多模态与嵌入模型调研：图像、视频、语音、嵌入（2026-11）
type: source
tags: [notes]
source_note: "[[多模态与嵌入模型调研-2026-11]]"
url: https://github.com/black-forest-labs/flux2
created: 2026-11-05
updated: 2026-11-05
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

为 L2 补上语言模型以外的四类基础模型：图像生成（[[entities/stable-diffusion|Stable Diffusion]]、[[entities/flux|FLUX]]、[[entities/gpt-image|GPT Image]]、[[entities/imagen|Imagen]]）、视频生成（[[entities/sora|Sora]]、[[entities/veo|Veo]]、[[entities/kling|可灵]]、[[entities/seedance|Seedance / 即梦]]）、语音（[[entities/whisper|Whisper]]、[[entities/elevenlabs|ElevenLabs]]、[[concepts/text-to-speech|TTS]]）和嵌入（[[entities/openai-embeddings|OpenAI text-embedding]]、[[entities/qwen3-embedding|Qwen3-Embedding]]、[[entities/bge|BGE]]、[[entities/voyage-embeddings|Voyage]]、[[entities/cohere-embed|Cohere Embed]]）。一手材料是各项目 GitHub README（2026-11-05 读取）；Wikipedia 和厂商文档站在本次云端环境中被网络策略拦截，其余事实来自报道，原文逐条标了 URL 和“二手 / 单一来源”。

## Key Points

- **图像**：开放权重主力从 Stable Diffusion 转到原作者另立的 FLUX（FLUX.2 [dev] 32B，[klein] 4B 用 Apache-2.0）；闭源侧图像生成并入多模态 LLM：gpt-image-2（2026-04，出图前推理）、Gemini 的 Nano Banana；DALL·E 2026-05、Imagen 4 2026-08 先后在 API 下线
- **视频**：Veo 3（2025-05）起原生音频成为标配；OpenAI 2026-03 宣布关停 Sora，API 2026-09-24 下线；Google 没有发 Veo 4，转向 Gemini Omni；可灵 4.0（2026-10）单次 30 秒，年化收入约 5 亿美元并筹划分拆上市；Seedance 2.0 因生成真人与知名 IP 被迪士尼等投诉
- **语音**：Whisper（2022-09，MIT）仍是开源识别基线，OpenAI 已用 gpt-4o-transcribe / GPT-Transcribe 接替；ElevenLabs 2026-02 估值 110 亿美元，9 月员工股出售约 220 亿美元；Kokoro-82M、CosyVoice 3 等开源 TTS 已够用
- **嵌入**：开放权重的 Qwen3-Embedding（MTEB 多语言第一）、BGE-M3 与闭源持平；2026 年主线是多模态嵌入（Qwen3-VL-Embedding、Gemini Embedding 2、voyage-multimodal-3.5、Cohere Embed 4）和嵌入并入数据库（MongoDB 收购 Voyage AI），见 [[concepts/embedding|嵌入]]、[[concepts/rag|RAG]]、[[concepts/vector-database|向量数据库]]
- **方法**：图像 / 视频模型的共同基础是[[concepts/diffusion-model|扩散模型]]，主干已从 UNet 换成 Transformer（MM-DiT、flow matching）
- **版权**：Getty 诉 Stability（英国 2025-11 基本败诉，美国仍在审）、Seedance 2.0 被好莱坞投诉，是这一层的主要法律风险

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
