---
title: 超节点与纵向扩展互联
type: concept
tags: [method]
layer: L0
aliases: ["超节点与纵向扩展互联", "超节点", "SuperPod", "scale-up 互联", "NVLink"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# 超节点与纵向扩展互联

把几十到上万颗加速器用专用高速链路连成一个「大芯片」的做法：在节点内部（scale-up）用私有互联保证全互联带宽与低延迟，再用网络把这些节点横向连成集群（scale-out）。2026 年各家的产品单位已经从单卡变成机架与超节点，因为万亿参数模型的张量并行、专家并行和 [[concepts/disaggregated-serving|预填充 / 解码分离]]都要求节点内带宽远高于以太网。

## 关键特征

- **各家各一套**：[[entities/nvidia|NVIDIA]] 的 NVLink / NVL72、NVL144 机架，[[entities/huawei|华为]]的灵衢（UnifiedBus）与 Atlas SuperPoD，[[entities/aws-trainium|AWS]] 的 NeuronLink 与 NeuronSwitch-v1，[[entities/google-tpu|Google TPU]] 的 3D torus ICI，[[entities/amd-instinct|AMD]] 的 Helios / IF128 机架
- **规格以超节点为单位公布**：Atlas 950 SuperPoD 最大 8,192 颗昇腾 950DT、宣称 16 PB/s 互联带宽；Ironwood 的完整 pod 为 9,216 颗芯片、共享约 1.77 PB 内存
- **延迟成为指标**：AWS 称 Enhanced Neuron Fabric 把芯片间通信延迟压到 10 微秒以内
- **开始出现跨厂互通**：AWS 称 Trainium4 将支持 NVIDIA NVLink Fusion
- **厂商数字需打折**：公布的多是最大配置，实机展示规模常远小于此（华为公开展示的 Atlas 950 SuperPoD 为 1,024 张加速卡）

## 应用

训练侧决定并行策略的可行边界（张量并行通常只能在超节点内部展开）；推理侧决定能否把预填充与解码放在不同节点并在其间直传 KV cache（见 [[concepts/kv-cache|KV cache]]），[[entities/nvidia-dynamo|NVIDIA Dynamo]] 的 NIXL 与 [[entities/llm-d|llm-d]] 的分层 KV 卸载都建立在这一层之上。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]]
- **下游**：[[maps/L3-训练与推理|L3-训练与推理]] 的并行与编排策略

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/hbm|HBM]]
- [[concepts/disaggregated-serving|预填充 / 解码分离]]
- [[concepts/kv-cache|KV cache]]

## 相关实体

- [[entities/nvidia|NVIDIA]]
- [[entities/ascend|昇腾]]
- [[entities/aws-trainium|AWS Trainium]]
- [[entities/google-tpu|Google TPU]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Atlas 950 SuperPoD 最大 8,192 颗 950DT（2026 Q4），宣称 8 EFLOPS（FP8）/16 EFLOPS（FP4）、16 PB/s 互联带宽" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
