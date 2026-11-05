---
title: GLM
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["GLM", "ChatGLM", "智谱清言", "GLM-4.5", "GLM-5", "GLM-5.2", "GLM-5.3"]
org: "[[entities/zhipu-ai]]"
released: "2023-03"
open_weights: true
competitors: ["[[entities/kimi]]", "[[entities/minimax-m]]", "[[entities/qwen]]", "[[entities/deepseek-r1]]", "[[entities/doubao]]"]
depends_on: ["[[entities/ascend]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/zhipu-ai-survey-2026-11]]", "[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# GLM

## 描述

[[entities/zhipu-ai|智谱（Z.ai）]]的模型家族，名称来自 2022 年的 GLM 预训练方法（自回归空白填充）。2023-03 开源的 ChatGLM-6B 是国内最早被广泛本地部署的开源对话模型之一。GLM-4.5（2025-07）起旗舰改为大型 [[concepts/mixture-of-experts|MoE]]，统一推理、编码与 Agent 能力，以 MIT 协议开放权重。GLM-5 扩到 744B 总参数、40B 激活；GLM-5.2 在 IndexShare 稀疏注意力上做到稳定的 1M 上下文；GLM-5.3 沿用 5.2 的基座，只靠后训练提升编码与长程任务，许可证改为自定义协议。家族还包括视觉（GLM-4.xV）、OCR、ASR / TTS、图像、视频（CogVideoX）和手机 Agent（AutoGLM）等分支。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/kimi|Kimi]]、[[entities/minimax-m|MiniMax-M]]、[[entities/qwen|Qwen]]、[[entities/deepseek-r1|DeepSeek-R1]]、[[entities/doubao|豆包]]（闭源）

## 主要版本

- **ChatGLM-6B / 2 / 3**（2023）：6B 对话模型，常用于本地部署和微调
- **GLM-4-9B**（2024-06）：含 1M 上下文版和 GLM-4V-9B
- **GLM-4-0414 / GLM-Z1**（2025-04）：32B / 9B，含推理模型，MIT
- **GLM-4.5 / 4.5-Air**（2025-07-28）：355B / 32B 和 106B / 12B，引入交错思考（Interleaved Thinking）
- **GLM-4.6**（2025-09-30）、**GLM-4.7**（2025-12-22）：4.7 增加保留思考（Preserved Thinking）和按轮思考（Turn-level Thinking）
- **GLM-5**（2026-02）：744B / 40B，异步强化学习框架 slime
- **GLM-5.1**（2026-04）、**GLM-5.2**（2026-06-16）：5.2 实现稳定的 1M 上下文，IndexShare 让每 4 层稀疏注意力共用一个索引器，1M 长度下每 token FLOPs 降为 1/2.9
- **GLM-5.3 / 5.3-Flash**（2026-08）：5.3 与 5.2 同一基座，只改后训练；`reasoning_effort` 分 low / high / max 三档

## 许可证

- 2025-04 至 GLM-5.2：标准 MIT，GLM-5.2 还特别声明“无地区限制”
- GLM-5.3：自定义 GLM-5.3 License。模型服务商及关联方连续 12 个月收入超过 100 亿美元时，商用前要通过 Z.ai 安全审查；审查的标准、费用和时限没有写明。GLM-5.3-Flash 仍为 MIT
- 对比：[[entities/kimi|Kimi K3]] 的同类门槛是 2000 万美元，[[entities/minimax-m|MiniMax-M3]] 的商用需通知或授权

## 开发者接入

- Z.ai API 与国内 bigmodel.cn；提供 [[concepts/anthropic-messages-api|Anthropic Messages API]] 兼容端点（`api.z.ai/api/anthropic`），常用于驱动 [[entities/claude-code|Claude Code]]；官方的 Terminal-Bench、CyberGym 等成绩也在 Claude Code 中测得
- GLM Coding Plan 编码订阅；2026-07 起有自有桌面应用 ZCode
- 阿里云百炼（2026-05 起上架 GLM-5.1）
- 自部署：Hugging Face 上同时提供 BF16 与 FP8 权重

## 时间线

- 2022-05 GLM 论文（ACL）
- 2023-03 ChatGLM-6B
- 2024-06 GLM-4-9B
- 2024-08 CogVideoX
- 2025-04 GLM-4-0414、GLM-Z1（MIT）
- 2025-07-28 GLM-4.5
- 2025-08-11 GLM-4.5V
- 2025-09-30 GLM-4.6
- 2025-12-22 GLM-4.7
- 2026-01-14 与[[entities/huawei|华为]]联合开源图像模型 GLM-Image，称自回归基座从数据预处理到大规模预训练全流程在[[entities/ascend|昇腾]] Atlas 800T A2 上完成，框架为昇思 MindSpore
- 2026-02 GLM-5
- 2026-04-07 GLM-5.1 开源
- 2026-06-16 GLM-5.2
- 2026-08 GLM-5.3 与 GLM-5.3-Flash，权重月底放出

## 相关实体

- [[entities/zhipu-ai|智谱（Z.ai）]]
- [[entities/kimi|Kimi]]
- [[entities/minimax-m|MiniMax-M]]
- [[entities/qwen|Qwen]]
- [[entities/claude-code|Claude Code]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "GLM-5.3 uses the same base model as GLM-5.2 — every gain comes from post-training." — [[sources/zhipu-ai-survey-2026-11|智谱与 GLM 调研]]（GLM-5.3 模型卡）
- "**Pure Open**: An MIT open-source license — no regional limits, technical access without borders" — [[sources/zhipu-ai-survey-2026-11|智谱与 GLM 调研]]（GLM-5.2 模型卡）
- "They are released under the MIT open-source license and can be used commercially and for secondary development." — [[sources/zhipu-ai-survey-2026-11|智谱与 GLM 调研]]（GLM-4.5 模型卡）
