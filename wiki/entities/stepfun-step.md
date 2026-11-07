---
title: Step（阶跃星辰模型）
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Step", "Step 模型", "阶跃星辰 Step", "Step3", "Step 3.5 Flash", "Step 3.7 Flash", "Step 5 Preview"]
org: "[[entities/stepfun]]"
released: "2024-07"
open_weights: true
competitors: ["[[entities/kimi]]", "[[entities/minimax-m]]", "[[entities/glm]]", "[[entities/qwen]]", "[[entities/hunyuan]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/stepfun-survey-2026-11]]"]
---

# Step（阶跃星辰模型）

## 描述

[[entities/stepfun|阶跃星辰]]的模型家族，从一开始就偏多模态。2025-07 的 Step3 是 321B 总参数、38B 激活的多模态推理 [[concepts/mixture-of-experts|MoE]]，用 MFA 注意力和 Attention-FFN 分离（AFD）降低解码成本。2026 年转向高吞吐的 Flash 系列：Step 3.5 Flash 196B 总参数、只激活 11B，靠 3 路多 token 预测（MTP-3）达到每秒 100–300 token；Step 3.7 Flash 加上 1.8B 视觉编码器成为视觉语言模型。两者都以 Apache-2.0 开放权重，可在 Mac Studio、DGX Spark 等大内存设备本地运行。2026-09 的旗舰 Step 5 Preview 扩大到 600B / 27B 激活、1M 上下文，接受文本、图像和视频输入，主打 Agent 与金融任务，权重公开但改用自定义许可证。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重）
- **上游依赖**：—
- **下游**：阶跃开放平台（国内 / 海外两区，OpenAI 兼容）、OpenRouter、NVIDIA NIM；自部署用 [[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/llama-cpp|llama.cpp]]
- **竞争 / 替代**：[[entities/kimi|Kimi]]、[[entities/minimax-m|MiniMax-M]]、[[entities/glm|GLM]]、[[entities/qwen|Qwen]]、[[entities/hunyuan|混元]]

## 主要版本

- **Step-2**（2024-07）：万亿参数语言模型（闭源）；同期 Step-1.5V 多模态、Step-1X 图像生成
- **Step-Video-T2V / Step-Audio**（2025-02）：与吉利联合开源
- **Step3**（2025-07）：321B / 38B 激活，多模态推理，Apache-2.0
- **Step 3.5 Flash**（2026-02）：196B / 11B 激活；每层 288 个路由专家 + 1 个共享专家、top-8；256K 上下文（滑动窗口与全注意力 3:1）；厂商自报 SWE-bench Verified 74.4%、Terminal-Bench 2.0 51.0%；2026-03 补开源 Base、Midtrain 权重与训练框架 Steptron
- **Step 3.7 Flash**（2026-05）：196B 语言主干 + 1.8B 视觉编码器，约 11B 激活，256K 上下文，最高每秒 400 token
- **Step 5 Preview**（2026-09）：600B / 27B 激活，1M 上下文，文本 + 图像 + 视频输入；另有 FP8、BF16、NVFP4 权重

## 许可证

- Step3、Step 3.5 Flash、Step 3.7 Flash：Apache-2.0
- Step 5 Preview：StepFun Model License 1.0
  - 商用产品月活超 1 亿或月收入超 2000 万美元须显著标注 “Powered by StepFun AI”
  - 手机、汽车、眼镜、机器人等硬件厂商把模型作为设备功能商用前须另签许可
  - 经营 MaaS 业务、12 个月总收入超 2000 万美元的公司商用须另签许可
- 对比：门槛与 [[entities/kimi|Kimi K3]] 相同；[[entities/glm|GLM-5.3]] 为 100 亿美元，[[entities/ernie|ERNIE 5.5 Flash]] 为 5000 万美元且有地域限制

## 时间线

- 2024-07 Step-2、Step-1.5V、Step-1X
- 2024-09 开源 GOT-OCR2.0
- 2025-02 Step-Video-T2V、Step-Audio
- 2025-04 Step-R1-V-Mini；开源 Step1X-Edit
- 2025-07-28 Step3 开源
- 2025-08 起 Step-Audio 2 mini、NextStep-1、StepFun-Prover / Formalizer
- 2026-01 Step3-VL-10B
- 2026-02-01 / 02 Step 3.5 Flash
- 2026-03-02 Step 3.5 Flash Base / Midtrain 与 Steptron
- 2026-05-23 Step 3.7 Flash
- 2026-09-18 / 20 Step 5 Preview
- 2026-10-14 Step 5 Preview NVFP4 权重

## 相关实体

- [[entities/stepfun|阶跃星辰（StepFun）]]
- [[entities/kimi|Kimi]]
- [[entities/minimax-m|MiniMax-M]]
- [[entities/glm|GLM]]
- [[entities/vllm|vLLM]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/speculative-decoding|投机解码]]
- [[concepts/reasoning-model|推理模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Built on a sparse Mixture of Experts (MoE) architecture, it selectively activates only 11B of its 196B parameters per token." — [[sources/stepfun-survey-2026-11|阶跃星辰与 Step 调研]]（Step 3.5 Flash 模型卡）
- "Step 5 Preview is a sparse Mixture-of-Experts (MoE) model with 600B total parameters and 27B active parameters. It supports up to 1 million tokens of context and accepts text, images, and video" — [[sources/stepfun-survey-2026-11|阶跃星辰与 Step 调研]]（Step 5 Preview 模型卡）
