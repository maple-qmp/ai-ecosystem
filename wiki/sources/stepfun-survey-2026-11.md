---
title: 阶跃星辰（StepFun）与 Step 模型调研（2026-11）
type: source
tags: [notes]
source_note: "[[阶跃星辰-Step调研-2026-11]]"
url: https://huggingface.co/stepfun-ai
created: 2026-11-07
updated: 2026-11-07
sources:
  - "[[entities/stepfun]]"
  - "[[entities/stepfun-step]]"
---

# 阶跃星辰（StepFun）与 Step 模型调研（2026-11）

## Summary

整理上海[[entities/stepfun|阶跃星辰（StepFun）]]从 2023-04 成立到 2026-11 的融资、上市准备和 [[entities/stepfun-step|Step 模型家族]]。创始人姜大昕等来自微软，投资方含腾讯和上海国资，被称为“AI 六小虎”之一。2026 年的 Step 3.5 Flash（196B / 11B 激活）与 Step 3.7 Flash（198B 视觉语言）以 Apache-2.0 开放权重；2026-09 的旗舰 Step 5 Preview（600B / 27B 激活、1M 上下文、文本 + 图像 + 视频）改用自定义 StepFun Model License 1.0，硬件厂商和年收入超 2000 万美元的模型服务商商用须另签许可。模型参数与许可证以 Hugging Face 模型卡为准（2026-11-07 读取）。

## Key Points

- **公司**：2023-04-06 上海成立；创始人姜大昕、朱亦博、焦斌星（均来自微软）；股东含[[entities/tencent|腾讯]]、启明创投、上海国投
- **融资与上市**：2026-01 超 50 亿元 B+ 轮；2026-05 近 25 亿美元 Pre-IPO 轮，资方多为手机与终端产业链；2026-06 传秘密递表港交所
- **Step3（2025-07）**：321B / 38B 多模态推理 [[concepts/mixture-of-experts|MoE]]，Apache-2.0；同期与[[entities/huawei|华为]]等国产芯片厂商成立“模芯生态创新联盟”
- **Step 3.5 Flash（2026-02）**：196B / 11B，MTP-3 多 token 预测，256K 上下文；之后开源 Base 与 Midtrain 权重和训练框架 Steptron
- **Step 3.7 Flash（2026-05）**：196B 语言主干 + 1.8B 视觉编码器，上架 OpenRouter 与 NVIDIA NIM
- **Step 5 Preview（2026-09）**：600B / 27B，1M 上下文，主打 Agent 与金融任务；权重公开但许可证收紧
- **多模态分支**：Step-Video、Step-Audio、Step1X-Edit、NextStep、GOT-OCR2.0
- **部署**：[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/llama-cpp|llama.cpp]]，OpenAI 兼容 API 分国内与海外两区

## Mentioned Pages

- [[entities/stepfun|阶跃星辰（StepFun）]]
- [[entities/stepfun-step|Step（阶跃星辰模型）]]
- [[entities/tencent|腾讯]]
- [[entities/huawei|华为]]
- [[entities/kimi|Kimi]]
- [[entities/minimax-m|MiniMax-M]]
- [[entities/glm|GLM]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/llama-cpp|llama.cpp]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/speculative-decoding|投机解码]]
