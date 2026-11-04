---
title: circuit-tracer
type: entity
tags: [project]
kind: framework
layer: X
aliases: ["circuit-tracer", "Circuit Tracer", "电路追踪", "归因图工具"]
org: "[[entities/anthropic]]"
released: "2025-05"
competitors: []
depends_on: ["[[entities/pytorch]]", "[[entities/llama]]", "[[entities/qwen]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/claude-independent-modules-survey-2026-11]]"]
---

# circuit-tracer

## 描述

开源的可解释性库，用来在**开放权重模型**上画“归因图”（attribution graph），也就是找出模型从输入到某个输出经过了哪些内部特征。方法来自 [[entities/anthropic|Anthropic]] 2025 年的两篇电路追踪论文（Ameisen 等、Lindsey 等），库由 Anthropic Fellows 项目成员开发，2025-05 发布，MIT 协议。仓库原在 safety-research 组织，现归 decoderesearch 组织。它不需要 Claude，也不连 Anthropic 服务：支持 Gemma-2（2B）、Llama-3.2（1B），Neuronpedia 上另有 Qwen3-4B 的 transcoder；Gemma-2 2B 在 Colab 的免费 GPU 上就能跑。

## 原理

- **替换模型**：先为每层 MLP 训练（跨层）transcoder，用稀疏、可解释的特征近似原 MLP 的输出；transcoder 解释不了的部分记为“误差节点”
- **归因**：给定一个提示和目标输出（某个 logit），计算每个非零特征、误差节点和输入 token 对其他特征和输出的**直接效应**，得到一张有向图；再剪枝，只留下贡献大的路径
- **标注**：在可视化界面里给特征起名、分组，读出“模型先想到 Dallas → 得出 Texas → 输出 Austin”这类多步推理路径
- **干预验证**：把某些特征设成任意值，观察输出怎么变，用来检验图里的解释是不是真的
- 三种用法：在 Neuronpedia 网页上直接用；Python 脚本或 notebook；命令行（需要自己的 GPU）

## 相关工具

- **jacobian-lens**（`anthropics/jacobian-lens`，2026-07，Apache-2.0）：读出某层激活“倾向于让模型说出什么”。做法是把任一层的残差向量乘以该层到最后一层的平均输入—输出雅可比矩阵 `J_l = E[∂h_final / ∂h_l]`，再用模型自己的反嵌入解码成词表排名。在开放权重的解码器模型上拟合，约 100 条提示即可用；配套论文讨论“可言说的表征构成全局工作空间”。参考实现，不维护
- **persona_vectors**（safety-research，Apache-2.0）：在激活空间里找出对应某种性格特征（如谄媚、恶意）的方向，用来监测和调控
- 这些工具都只依赖 Hugging Face 上的开放权重模型，Anthropic 不公开 Claude 自己的权重或 transcoder

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 安全与可解释性工具
- **上游依赖**：[[entities/pytorch|PyTorch]]、开放权重模型（Gemma-2、[[entities/llama|Llama]] 3.2、[[entities/qwen|Qwen]]3）、预训练 transcoder
- **相关平台**：Neuronpedia（在线托管归因图与特征浏览）

## 时间线

- 2025-03 Anthropic 发表归因图方法论文，前端代码 `attribution-graphs-frontend` 开源
- 2025-05 circuit-tracer 开源，与 Neuronpedia 合作提供在线界面
- 2025-08 Qwen3-4B transcoder 发布
- 2026-07 jacobian-lens 开源
- 2026 年仓库转到 decoderesearch 组织（原地址自动跳转）

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/petri|Petri]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/llama|Llama]]
- [[entities/qwen|Qwen]]

## 相关概念

- [[concepts/transformer|Transformer]]
- [[concepts/claude-constitution|Claude 宪法]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "This library implements tools for finding circuits using features from (cross-layer) MLP transcoders" — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
- "The Jacobian lens reads out what an internal activation is disposed to make the model say." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]（jacobian-lens）
