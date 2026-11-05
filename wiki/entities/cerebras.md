---
title: Cerebras
type: entity
tags: [organization]
kind: company
layer: L0
aliases: ["Cerebras", "Cerebras Systems", "WSE-3", "晶圆级引擎"]
competitors: ["[[entities/nvidia]]", "[[entities/groq]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# Cerebras

做晶圆级芯片的公司：WSE-3 把整片晶圆当作一颗芯片，以巨大的片上内存与带宽绕开 [[concepts/hbm|HBM]] 瓶颈，面向训练与超低延迟推理。官方的参考实现与 CLI 是开源的 Cerebras Model Zoo。2026 年它完成了当年最大的美股科技 IPO（以下金融数字均为二手报道，cerebras.ai 与 sec.gov 对自动化客户端返回 403，未能核对招股书）：定价 185 美元/股、高于 150–160 美元区间，募资约 55.5 亿美元；[[entities/openai|OpenAI]] 承诺采购 750 MW 推理算力并有到 2030 年追加 1.25 GW 的选择权，Cerebras 向其发行最多 3,340 万股认股权证。主要风险是客户集中度——有报道称阿联酋客户占 2025 年收入约 86%。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 公司
- **上游依赖**：先进制程与晶圆级封装
- **下游**：自有云服务与 Model Zoo；WSE-3 也将部署进 [[entities/aws|AWS]] 数据中心（「分离式架构」）
- **竞争 / 替代**：[[entities/nvidia|NVIDIA]]、[[entities/groq|Groq]]；云厂商自研芯片

## 时间线

- 2016 成立
- 2024-08-27 `cerebras-cloud-sdk` 首个 PyPI 版本
- 2024 首次 IPO 计划推迟
- 2025-12 OpenAI 承诺采购 750 MW 推理算力（报道金额 100 亿或 200 亿美元以上，口径不一）
- 2026-04 重新递交 S-1
- 2026 纳斯达克 IPO：定价 185 美元/股，募资约 55.5 亿美元；估值口径从约 400 亿到首日翻倍后的 950 亿–1000 亿美元不等，须按招股书核实
- 2026 AWS 同意在其数据中心部署 WSE-3

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/aws|AWS]]
- [[entities/nvidia|NVIDIA]]
- [[entities/groq|Groq]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/hbm|HBM]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The Cerebras Model Zoo is a collection of deep learning models and utilities optimized to run on Cerebras hardware." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
