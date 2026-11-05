---
title: 扩散模型
type: concept
tags: [method]
layer: L2
aliases: ["扩散模型", "Diffusion Model", "潜空间扩散", "Latent Diffusion", "Flow Matching", "DiT"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# 扩散模型

## 定义

一类生成模型：训练时学会把逐步加噪的数据还原，生成时从随机噪声出发，按文本等条件一步步去噪，得到图像、视频或音频。它是 2022 年以来图像和视频生成的主流方法。

## 关键特征

- **潜空间扩散**：CompVis 的 Latent Diffusion（2021-12）先用 VAE 把图像压到低维潜空间，在潜空间里去噪，再解码回像素，大幅降低算力需求；[[entities/stable-diffusion|Stable Diffusion]] v1 因此只需 10GB 显存
- **文本条件**：用冻结的文本编码器（CLIP、T5）把提示词编码后注入去噪网络，[[entities/imagen|Imagen]] 和 Stable Diffusion 都采用这一做法
- **主干从 UNet 换成 Transformer（DiT）**：SD3 / 3.5 改用 MM-DiT；[[entities/flux|FLUX.2]] [dev] 是 32B 参数的 flow matching transformer。Flow matching 是扩散的变体，学习从噪声到数据的速度场
- **蒸馏提速**：FLUX.2 [klein] 蒸馏版只需 4 步，Base 版 50 步
- **视频扩散**：在时间维度上一起去噪；阿里 Wan2.2 还把[[concepts/mixture-of-experts|混合专家（MoE）]]引入视频扩散，按去噪阶段分配专家
- **与语言模型融合**：闭源厂商开始让多模态 LLM 直接出图（[[entities/gpt-image|GPT Image]]、Gemini 的 Nano Banana），本次调研没有找到其内部架构的公开说明

## 应用

- 文生图、图像编辑与多参考图组合
- 文生视频、图生视频（[[entities/veo|Veo]]、[[entities/kling|可灵]]、[[entities/seedance|Seedance]]、[[entities/sora|Sora]]）
- 社区微调：[[concepts/lora|LoRA]]、ControlNet

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]]（图像、视频生成模型的基础方法）

## 相关概念

- [[concepts/transformer|Transformer]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/lora|LoRA]]
- [[concepts/quantization|量化]]

## 相关实体

- [[entities/stable-diffusion|Stable Diffusion]]
- [[entities/flux|FLUX]]
- [[entities/imagen|Imagen]]
- [[entities/gpt-image|GPT Image]]
- [[entities/veo|Veo]]
- [[entities/kling|可灵 Kling]]
- [[entities/seedance|Seedance / 即梦]]
- [[entities/sora|Sora]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Stable Diffusion is a latent text-to-image diffusion model." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（CompVis/stable-diffusion README）
- "Wan2.2 introduces a Mixture-of-Experts (MoE) architecture into video diffusion models." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Wan-Video/Wan2.2 README）
