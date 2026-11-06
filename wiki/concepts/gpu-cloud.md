---
title: GPU 云
type: concept
tags: [term]
layer: L0
aliases: ["GPU 云", "neocloud", "新云", "AI 云厂商"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# GPU 云

专门出租 GPU 算力的云服务商，与三大综合云（[[entities/aws|AWS]]、[[entities/azure|Azure]]、[[entities/google-cloud|Google Cloud]]）的区别是只做加速计算这一层，不铺完整的云产品矩阵。代表是 [[entities/coreweave|CoreWeave]]、Nebius、Lambda、Nscale，业内常称「neocloud」。典型做法是先与模型公司签多年长约，再用这些合同融资或举债去买 GPU 和租数据中心。

## 关键特征

- **积压订单即商业模式**：CoreWeave 2026 Q2 积压订单约 1,040 亿美元，Nebius 在 2026 Q2 电话会称约 400 亿美元；收入的绝大部分来自已签长约
- **杠杆与客户集中**：规模靠债务换取，而少数客户（[[entities/openai|OpenAI]]、[[entities/microsoft|Microsoft]]、Meta 等）占收入大头，单一合同变动即影响全局
- **交付周期是核心能力**：抢到最新一代 GPU 的供应配额、拿到电力与机房，比软件层的差异更决定竞争力
- **与综合云既竞争又互补**：微软向 Nebius 采购算力（报道金额最高 174 亿美元、至 2031 年），同时自己也卖 GPU 实例
- **向上延伸**：多数在裸算力之上加托管推理服务，与 [[maps/L3-训练与推理|L3]] 的推理栈接壤（Nebius 的 Token Factory、CoreWeave 对 [[entities/llm-d|llm-d]] 的参与）

## 应用

模型公司用它补足自建与综合云之外的弹性容量；推理服务商用它承载突发流量。对使用者来说，选型关注的是能拿到哪一代芯片、互联拓扑（见 [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]）和长约价格，而非 API 形态。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]]
- **上游**：[[entities/nvidia|NVIDIA]] 等加速器供应、数据中心与电力
- **下游**：模型公司与推理服务；[[entities/stargate|Stargate]] 这类自建项目是它的替代路径

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]

## 相关实体

- [[entities/coreweave|CoreWeave]]
- [[entities/stargate|Stargate]]
- [[entities/aws|AWS]]
- [[entities/azure|Microsoft Azure]]
- [[entities/google-cloud|Google Cloud]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "CoreWeave 2026 Q2 营收约 25.8 亿美元（上年同期 12.1 亿）、积压订单约 1,040 亿美元，Q3 初又新增 250 亿美元以上承诺，同时季度净亏约 6.26 亿美元" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
