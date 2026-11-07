---
title: 混元（Tencent HY）
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["混元", "腾讯混元", "Hunyuan", "Tencent Hunyuan", "Tencent HY", "Hy3", "Hy4", "HunyuanVideo"]
org: "[[entities/tencent]]"
released: "2023-09"
open_weights: true
competitors: ["[[entities/qwen]]", "[[entities/doubao]]", "[[entities/deepseek-v]]", "[[entities/glm]]", "[[entities/kimi]]", "[[entities/ernie]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/tencent-hunyuan-survey-2026-11]]"]
---

# 混元（Tencent HY）

## 描述

[[entities/tencent|腾讯]]的自研大模型家族，2023-09 发布，2025-12 起国际品牌改为 Tencent HY，新模型写作 Hy3、Hy4。2024–2025 年开源的 Hunyuan-Large、Hunyuan-A13B（80B 总参数、13B 激活）用自定义社区许可证，许可地域不含欧盟、英国、韩国。2026 年起旗舰改用 Apache-2.0：Hy3 是 295B 总参数、21B 激活的 [[concepts/mixture-of-experts|MoE]]；Hy4 preview 扩大到 770B 总参数、49B 激活和 1M 上下文，注意力借鉴 [[entities/deepseek-v|DeepSeek]] 的稀疏注意力与 [[entities/glm|GLM]] 的跨层索引复用。模型与腾讯自家产品联合调优，直接服务[[entities/yuanbao|腾讯元宝]]、CodeBuddy、WorkBuddy。家族还包括视频生成 HunyuanVideo、翻译 Hy-MT、3D 世界模型和具身智能等分支。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重）
- **上游依赖**：—
- **下游**：[[entities/yuanbao|腾讯元宝]]、CodeBuddy、WorkBuddy、腾讯云 API；自部署用 [[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]
- **竞争 / 替代**：[[entities/qwen|Qwen]]、[[entities/doubao|豆包]]、[[entities/deepseek-v|DeepSeek-V]]、[[entities/glm|GLM]]、[[entities/kimi|Kimi]]、[[entities/ernie|文心]]

## 主要版本

- **Hunyuan-Large**（2024-11）：大型 MoE，技术报告 arXiv:2411.02265，自定义腾讯许可证
- **Hunyuan T1 / Turbo S**（2025-02 / 03）：推理模型和快思考模型，元宝内上线
- **Hunyuan-A13B**（2025-06）：80B / 13B 激活，256K 上下文
- **混元 2.0（Tencent HY 2.0）**（2025-12-05）：Think 与 Instruct 两版，腾讯称 406B / 32B 激活
- **Hy3**（2026-07）：295B / 21B 激活 + 3.8B MTP 层，256K 上下文；`reasoning_effort` 分 no_think / low / high
- **Hy4 preview**（2026-08-27）：770B / 49B 激活，1M 上下文；78 层，每个 MoE 层 256 个路由专家 + 1 个共享专家；Gated DSA + IndexCache；模型卡自认推理过长、过度自检等已知问题
- **Hy4**（2026-11-04）：增加视觉理解与操作电脑能力

## 许可证

- Hunyuan-Large、Hunyuan-A13B 等：Tencent Hunyuan Community License，地域不含欧盟、英国、韩国；发布时上月月活超 1 亿的被许可方须另行申请授权
- Hy3、Hy4 preview：Apache-2.0
- 对比：同期[[entities/ernie|文心]] ERNIE 5.5 Flash 反而采用了与混元旧许可证相同的地域排除

## 时间线

- 2023-09 混元发布，通过腾讯云向企业开放
- 2024-11 开源 Hunyuan-Large
- 2024-12 开源 HunyuanVideo；2025-11-21 HunyuanVideo-1.5
- 2025-02-19 推理模型混元 T1 全量上线；03-01 混元 Turbo S
- 2025-06 开源 Hunyuan-A13B
- 2025-07 开源 0.5B–7B 小模型
- 2025-12-05 混元 2.0；12-09 品牌改为 Tencent HY
- 2026-04 下旬 Hy3 preview 开源
- 2026-05 翻译模型 Hy-MT2 开源
- 2026-07-06 Hy3 正式版（Apache-2.0），接入元宝
- 2026-08-27 Hy4 preview 开源（Apache-2.0）
- 2026-10 Hy-Memory、Hy-SimulMT 同传模型开源
- 2026-11-04 Hy4 正式版

## 相关实体

- [[entities/tencent|腾讯]]
- [[entities/yuanbao|腾讯元宝]]
- [[entities/deepseek-v|DeepSeek-V]]
- [[entities/glm|GLM]]
- [[entities/qwen|Qwen]]
- [[entities/ernie|文心（ERNIE）]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/diffusion-model|扩散模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "**Hy3** is a 295B-parameter Mixture-of-Experts (MoE) model with 21B active parameters and 3.8B MTP layer parameters, developed by the Tencent Hy Team." — [[sources/tencent-hunyuan-survey-2026-11|腾讯混元与元宝调研]]（Hy3 模型卡）
- "The model comprises 770B total parameters, of which 49B are activated per token." — [[sources/tencent-hunyuan-survey-2026-11|腾讯混元与元宝调研]]（Hy4 preview 模型卡）
- "THIS LICENSE AGREEMENT DOES NOT APPLY IN THE EUROPEAN UNION, UNITED KINGDOM AND SOUTH KOREA AND IS EXPRESSLY LIMITED TO THE TERRITORY, AS DEFINED BELOW." — [[sources/tencent-hunyuan-survey-2026-11|腾讯混元与元宝调研]]（Hunyuan-A13B 许可证）
