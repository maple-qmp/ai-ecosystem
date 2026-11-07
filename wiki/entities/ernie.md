---
title: 文心（ERNIE）
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["文心", "文心大模型", "ERNIE", "ERNIE 4.5", "ERNIE 5.0", "ERNIE 5.1", "ERNIE 5.5 Flash"]
org: "[[entities/baidu]]"
released: "2023-03"
open_weights: true
competitors: ["[[entities/qwen]]", "[[entities/doubao]]", "[[entities/hunyuan]]", "[[entities/deepseek-v]]", "[[entities/glm]]", "[[entities/kimi]]"]
depends_on: ["[[entities/kunlunxin]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/baidu-ernie-survey-2026-11]]"]
---

# 文心（ERNIE）

## 描述

[[entities/baidu|百度]]的大模型家族，2023-03 随文心一言亮相，驱动[[entities/ernie-app|文心 App]]、百度搜索中的文心助手和千帆平台 API。开放程度随版本变化：2025-06 的 ERNIE 4.5 系列共 10 个模型（0.3B 至 424B，含 300B-A47B [[concepts/mixture-of-experts|MoE]] 和多模态版）以 Apache-2.0 开放权重；ERNIE 5.0（原生全模态，2025-11 预览、2026-01 上线）和 5.1（2026-05）只提供 API。2026-11-05 开源的 ERNIE 5.5 Flash Base 是 280B 总参数、14B 激活的 MoE，用 33.5T token 从头预训练，支持 1M 上下文，但只放出预训练检查点，并改用带地域与收入门槛的自定义许可证。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（部分开放权重）
- **上游依赖**：[[entities/kunlunxin|昆仑芯]]（百度数据中心与 NVIDIA GPU 混用；5.5 Flash 技术博客只提到 GPU）；框架飞桨 PaddlePaddle
- **下游**：[[entities/ernie-app|文心 App]]、千帆 API；自部署用 [[entities/sglang|SGLang]]、[[entities/vllm|vLLM]]
- **竞争 / 替代**：[[entities/qwen|Qwen]]、[[entities/doubao|豆包]]、[[entities/hunyuan|混元]]、[[entities/deepseek-v|DeepSeek-V]]、[[entities/glm|GLM]]、[[entities/kimi|Kimi]]

## 主要版本

- **ERNIE 3.5 / 4.0**（2023）：文心一言早期底座，4.0 于 2023-10 发布
- **ERNIE 4.5 / X1**（2025-03）：4.5 为多模态基座，X1 为[[concepts/reasoning-model|推理模型]]；2025-06 起 4.5 全系开放权重（Apache-2.0，提供 PyTorch 与飞桨两种格式）
- **ERNIE 5.0**（2025-11 预览，2026-01 上线）：原生全模态；媒体普遍称 2.4T 参数、激活不到 3%，百度未确认；LMArena 2026-01-15 榜单全球第 8、国内第一
- **ERNIE 5.1**（2026-05）：基于 5.0 预训练底座，总参数约为 5.0 的 1/3；百度称预训练成本约为同级模型的 6%；闭源
- **ERNIE 5.5 Flash Base**（2026-11-05）：280B / 14B 激活；43 层，37 层 Heavily Compressed Attention + 6 层 MLA 与 DSA 稀疏注意力；每层 512 个路由专家（top-10）的 Multi-Router MoE；ECHO 用主干最后一层代替 MTP 模块，并兼作[[concepts/speculative-decoding|投机解码]]草稿模型；Muon 优化器；后训练版“will follow”

## 许可证

- ERNIE 4.5 系列：Apache-2.0
- ERNIE 5.0 / 5.1：不开放权重
- ERNIE 5.5 Flash Base：自定义 ERNIE 5.5 Flash Base Model License v1.0
  - 许可地域不含欧盟、英国、韩国
  - 非商用免费；相关产品年收入不超过 5000 万美元可免费商用，但须署名 “Powered by ERNIE” 并发一次性通知；超过须事先取得书面商用授权
  - 禁止用模型或其输出改进其他 AI 模型
- 对比：[[entities/hunyuan|混元]] 2026 年改为 Apache-2.0，方向相反；[[entities/glm|GLM-5.3]] 门槛 100 亿美元，[[entities/kimi|Kimi K3]] 与 [[entities/stepfun-step|Step 5 Preview]] 为 2000 万美元

## 时间线

- 2023-03-16 文心一言邀请测试
- 2023-06 ERNIE 3.5
- 2023-10-17 ERNIE 4.0
- 2024-06 ERNIE 4.0 Turbo
- 2025-03-16 ERNIE 4.5、ERNIE X1；2025-04 两者的 Turbo 版
- 2025-06 ERNIE 4.5 系列开源（Apache-2.0）
- 2025-09 ERNIE-4.5-21B-A3B-Thinking 开源
- 2025-11-13 ERNIE 5.0 预览
- 2026-01 ERNIE 5.0 正式上线
- 2026-04 开源 ERNIE-Image 图像模型
- 2026-04-30 ERNIE-5.1-Preview；05-08 / 09 ERNIE 5.1
- 2026-11-05 ERNIE 5.5 Flash Base 开源

## 相关实体

- [[entities/baidu|百度]]
- [[entities/ernie-app|文心 App]]
- [[entities/kunlunxin|昆仑芯]]
- [[entities/hunyuan|混元（Tencent HY）]]
- [[entities/qwen|Qwen]]
- [[entities/deepseek-v|DeepSeek-V]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/speculative-decoding|投机解码]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "**ERNIE 5.5 Flash** is an efficient sparse Mixture-of-Experts (MoE) language model with **280B total parameters and 14B activated per token**, pre-trained from scratch on **33.5T tokens** with a training context of up to **128K**; fine-tuning and inference support a **1M-token** context." — [[sources/baidu-ernie-survey-2026-11|百度文心与昆仑芯调研]]（ERNIE 5.5 Flash Base 模型卡）
- "1.11 "Territory" means all geographical areas worldwide other than the European Union, the United Kingdom and South Korea." — [[sources/baidu-ernie-survey-2026-11|百度文心与昆仑芯调研]]（ERNIE 5.5 Flash Base 许可证）
- "The post-trained ERNIE 5.5 Flash will follow." — [[sources/baidu-ernie-survey-2026-11|百度文心与昆仑芯调研]]（ERNIE 技术博客）
