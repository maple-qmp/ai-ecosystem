---
title: Stable Diffusion
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Stable Diffusion", "SD", "SDXL", "Stable Diffusion 3.5", "SD 3.5"]
org: "[[entities/stability-ai|Stability AI]]"
released: "2022-08"
open_weights: true
competitors: ["[[entities/flux]]", "[[entities/gpt-image]]", "[[entities/imagen]]"]
depends_on: ["[[entities/pytorch]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Stable Diffusion

## 描述

开放权重的文生图模型家族，基于 CompVis 的 Latent Diffusion（潜空间[[concepts/diffusion-model|扩散模型]]）论文，2022-08 由 CompVis 与 [[entities/stability-ai|Stability AI]]、Runway 合作发布：Stability 提供算力，在 LAION-5B 子集上训练。v1 用 860M 的 UNet 加冻结的 CLIP ViT-L/14 文本编码器，10GB 显存即可运行，这让本地出图和社区微调（[[concepts/lora|LoRA]]、ControlNet）成为可能。SD3 / 3.5（2024-10）把 UNet 换成 MM-DiT，用 CLIP-L、OpenCLIP bigG、T5-XXL 三个文本编码器，以 Community License 发布，年收入 100 万美元以下可免费商用。截至 2026-11 没有官方的 SD 4，开放权重图像模型的主力已转到原作者另立的 [[entities/flux|FLUX]]。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重，图像生成）
- **上游依赖**：[[entities/pytorch|PyTorch]]；LAION 数据集；CLIP / T5 文本编码器
- **竞争 / 替代**：[[entities/flux|FLUX]]、[[entities/gpt-image|GPT Image]]、[[entities/imagen|Imagen]]

## 时间线

- 2021-12 CompVis 发表 Latent Diffusion 论文（CVPR 2022 Oral）
- 2022-08 Stable Diffusion v1 发布
- 2024-10-22 SD 3.5 Large / Large Turbo；10-29 SD 3.5 Medium；11-26 SD 3.5 Large ControlNets
- 2025-11 英国高等法院在 Getty Images 诉 Stability AI 案中基本支持 Stability（二手）
- 2026-04 美国 Getty 诉讼继续审理，驳回动议大部分被拒（二手）
- 2026-09 仍无官方 SD 4（二手，多个指南）

## 相关实体

- [[entities/stability-ai|Stability AI]]
- [[entities/black-forest-labs|Black Forest Labs]]
- [[entities/flux|FLUX]]
- [[entities/hugging-face|Hugging Face]]

## 相关概念

- [[concepts/diffusion-model|扩散模型]]
- [[concepts/lora|LoRA]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Stable Diffusion is a latent text-to-image diffusion model." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（CompVis/stable-diffusion README）
- "Contains code for the text encoders (OpenAI CLIP-L/14, OpenCLIP bigG, Google T5-XXL) (these models are all public), the VAE Decoder (similar to previous SD models, but 16-channels and no postquantconv step), and the core MM-DiT (entirely new)." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Stability-AI/sd3.5 README）
