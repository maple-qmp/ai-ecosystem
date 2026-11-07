---
title: 腾讯混元（Tencent HY）与元宝调研（2026-11）
type: source
tags: [notes]
source_note: "[[腾讯-混元调研-2026-11]]"
url: https://huggingface.co/tencent
created: 2026-11-07
updated: 2026-11-07
sources:
  - "[[entities/tencent]]"
  - "[[entities/hunyuan]]"
  - "[[entities/yuanbao]]"
---

# 腾讯混元（Tencent HY）与元宝调研（2026-11）

## Summary

整理[[entities/tencent|腾讯]]自研大模型[[entities/hunyuan|混元（Tencent HY）]]从 2023-09 发布到 2026-11 Hy4 正式版的时间线，以及 AI 助手 App [[entities/yuanbao|腾讯元宝]]。2025-12 国际品牌由 Tencent Hunyuan 改为 Tencent HY。2026 年的 Hy3（295B / 21B 激活）和 Hy4 preview（770B / 49B 激活、1M 上下文）都以 Apache-2.0 开放权重，而早期的 Hunyuan-Large、Hunyuan-A13B 用的是排除欧盟、英国、韩国的自定义许可证。模型参数与许可证以 Hugging Face 模型卡为准（2026-11-07 读取）。

## Key Points

- **品牌**：2023-09 发布混元；2025-12-05 混元 2.0（Tencent HY 2.0），12-09 国际品牌改为 Tencent HY
- **早期开源**：Hunyuan-Large（2024-11）、HunyuanVideo（2024-12）、Hunyuan-A13B（2025-06，80B / 13B 激活），均为自定义 Tencent Hunyuan Community License，许可地域不含欧盟、英国、韩国
- **Hy3（2026-07）**：295B 总参数、21B 激活 [[concepts/mixture-of-experts|MoE]]，256K 上下文，Apache-2.0；04 月下旬先出 preview，正式版当即接入元宝并降价
- **Hy4 preview（2026-08-27）**：770B / 49B，1M 上下文，借鉴 [[entities/deepseek|DeepSeek]] 与 [[entities/glm|GLM]] 的稀疏注意力（Gated DSA + IndexCache），Apache-2.0；与 CodeBuddy、WorkBuddy 联合设计
- **Hy4 正式版（2026-11-04）**：增加视觉理解和操作电脑能力；权重是否开放待核实
- **部署**：[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]] 官方镜像，OpenAI 兼容接口
- **元宝**：2024-05-30 上线；2025-02-13 起同时接入 [[entities/deepseek-r1|DeepSeek-R1]]；2026-02 春节红包活动后腾讯称 MAU 1.14 亿
- **团队**：前 OpenAI 研究员姚顺雨任腾讯首席 AI 科学家（入职时间待核实）

## Mentioned Pages

- [[entities/tencent|腾讯]]
- [[entities/hunyuan|混元（Tencent HY）]]
- [[entities/yuanbao|腾讯元宝]]
- [[entities/deepseek|DeepSeek]]
- [[entities/deepseek-r1|DeepSeek-R1]]
- [[entities/glm|GLM]]
- [[entities/doubao-app|豆包 App]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]
