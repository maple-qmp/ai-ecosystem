---
title: AI 算力与硬件调研（2026-11）
type: source
tags: [notes]
source_note: "[[AI算力与硬件调研-2026-11]]"
url: https://www.anthropic.com/news/expanding-our-use-of-google-cloud-tpus-and-services
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[entities/google-cloud]]"
  - "[[entities/google-tpu]]"
  - "[[entities/amd]]"
  - "[[entities/amd-instinct]]"
  - "[[entities/rocm]]"
  - "[[entities/huawei]]"
  - "[[entities/ascend]]"
  - "[[entities/cann]]"
  - "[[entities/aws]]"
  - "[[entities/aws-trainium]]"
  - "[[entities/azure]]"
  - "[[entities/groq]]"
  - "[[entities/cerebras]]"
  - "[[entities/coreweave]]"
  - "[[entities/stargate]]"
  - "[[entities/nvidia]]"
  - "[[entities/cuda]]"
  - "[[concepts/ai-accelerator]]"
  - "[[concepts/hbm]]"
  - "[[concepts/scale-up-interconnect]]"
  - "[[concepts/gpu-cloud]]"
---

# AI 算力与硬件调研（2026-11）

## Summary

梳理 L0 层。加速器一侧，[[entities/nvidia|NVIDIA]] 仍占绝对主导（FY2027 Q2 数据中心营收 890 亿美元、同比 +117%），挑战者分三类：云厂商自研（[[entities/google-tpu|Google TPU]]、[[entities/aws-trainium|AWS Trainium]]、Azure Maia）、通用 GPU 替代（[[entities/amd-instinct|AMD Instinct]] + [[entities/rocm|ROCm]]）、专用架构（[[entities/groq|Groq]] 的 LPU、[[entities/cerebras|Cerebras]] 的晶圆级芯片）。中国市场自成一路，[[entities/huawei|华为]][[entities/ascend|昇腾]]配[[entities/cann|CANN]]，并开始承接部分国产模型的训练与推理。

软件栈的竞争仍然是硬件竞争的决定项：[[entities/cuda|CUDA]] 在 13.0 引入 tile 编程模型，ROCm 用 HIP 贴近 CUDA 接口降低移植成本，CANN 则以「全面开源开放」争取框架适配，三者的真实差距在长尾算子和内核库成熟度上。

算力的交付形态同样在变：[[entities/coreweave|CoreWeave]] 等 [[concepts/gpu-cloud|GPU 云]]以长约加债务换规模（积压订单约 1,040 亿美元），[[entities/stargate|Stargate]] 这类项目把单位从机架换成吉瓦。[[concepts/hbm|HBM]] 供应与 [[concepts/scale-up-interconnect|超节点互联]]是所有路线共同的瓶颈。

## Key Points

- **资料可靠性**：首轮调研时多数厂商域名被网络策略拦截，只有 Anthropic 官方博客、各项目 GitHub README 与 PyPI 元数据是一手。网络解禁后已回查官方原文：NVIDIA 财报新闻稿、CUDA 13.0 技术博客、Ironwood 的发布与 GA 两篇公告及 Cloud TPU 文档、Maia 200 官方博客、Trainium3 新闻稿、徐直军 Huawei Connect 2025 演讲全文、Groq 新闻室公告、ROCm 官方版本发布史与兼容性矩阵均已核对（详见素材的「核实记录」）。仍未能核实的是 openai.com、investors.coreweave.com、sec.gov、cerebras.ai、amd.com——这些站点对自动化客户端返回 403，故 Stargate 站点清单、CoreWeave 财务、Cerebras IPO 与 AMD 的 ROCm 7 / MI450 宣称仍为二手报道。厂商宣称的性能倍数均无第三方复现
- **NVIDIA**（已核实）：FY2027 Q2（截至 2026-07-26）营收 962 亿美元、数据中心 890 亿美元、同比 +117%，下季指引 1080 亿美元且假设中国数据中心计算营收为零；黄仁勋在同一份新闻稿里称 Vera Rubin「now in full production」；2025-12-24 与 Groq 达成非排他推理技术许可（官方不提金额，约 200 亿美元出自 CNBC）
- **CUDA 13.0**（已核实，2025-08-06）：在 SIMT 之外新增 tile 编程模型，分高层 API / DSL 与 CUDA Tile IR 两层提供，tile 直接映射 Tensor Core；统一 Arm 工具链（Orin 除外）——二十年来编程模型层面最大的一次变化。此前二手来源说的「13.1 推出 cuTile Python」未能在官方页面核到，已不采用
- **Google TPU**（已核实）：第七代 Ironwood 2025-04 发布时称「首个专为推理设计」，2025-11-06 的 GA 公告改为训练 / RL / 推理兼顾，峰值为 TPU v5p 的 10 倍、单颗为 Trillium 的 4 倍以上；每颗 192 GiB HBM、约 7.37 TB/s、峰值 4,614 TFLOPs，superpod 9,216 颗、42.5 EFLOPS、ICI 9.6 Tb/s、共享 1.77 PB HBM。第八代拆成 TPU 8t / TPU 8i 仍为二手报道
- **Anthropic 的三平台策略**（一手）：计划用到 100 万颗 TPU、2026 年上线超过 1 GW 容量，同时继续使用 Trainium 与 NVIDIA GPU，Amazon 仍是主要训练伙伴
- **AMD**：ROCm 7.0.0 于 2025-09-16 发布，但当前版本已是 **10.1.0（2026-10-05）**（官方发布史核实）；10.1.0 的兼容性矩阵尚未列出 MI450，最新 Instinct 为 MI355X / MI350X。MI450（CDNA 5、HBM4、2nm）与机架平台 Helios 的 2026 下半年目标、Oracle 5 万颗部署仍为二手报道
- **华为**：昇腾 950PR（2026 Q1）/ 950DT（2026 Q4）配自研 HBM，Atlas 950 SuperPoD 最大 8,192 颗；CANN 已开放 50+ 代码仓、800+ 算子；vLLM 的昇腾支持由社区插件 `vllm-ascend` 承担
- **AWS**（Trainium3 已核实）：Trn3 UltraServer 于 re:Invent 2025 GA，最多 144 颗、362 PFLOPS（FP8），相对 Trainium2 UltraServer 算力最高 4.4 倍、能效 4 倍、访存带宽近 4 倍、延迟降至四分之一；官方新闻稿未提 NeuronSwitch 与 10 微秒延迟。Trainium4 预览、Project Rainier 的近 50 万颗、与 OpenAI 的 380 亿美元协议仍为二手报道
- **Groq / Cerebras**：Groq 以片上 SRAM 换低延迟、只做推理，技术被 NVIDIA 许可后公司独立存续；Cerebras 2026 年 IPO 定价 185 美元/股、募资约 55.5 亿美元，OpenAI 承诺采购 750 MW 推理算力，但客户集中度极高
- **Stargate**：2025-09 宣布五个新站点、规划容量近 7 GW（二手）；旗舰 Abilene 已在运行——Oracle 2026-09-10 财报电话会称 8 栋楼中 6 栋、618 MW、总容量 75% 已交付，Epoch AI 估计余下两栋 2026-11 投运后达 824 MW、约 101.9 万张 H100 等效、312 亿美元资本开支

## Mentioned Pages

- [[entities/nvidia|NVIDIA]]
- [[entities/cuda|CUDA]]
- [[entities/google-cloud|Google Cloud]]
- [[entities/google-tpu|Google TPU]]
- [[entities/amd|AMD]]
- [[entities/amd-instinct|AMD Instinct]]
- [[entities/rocm|ROCm]]
- [[entities/huawei|华为]]
- [[entities/ascend|昇腾]]
- [[entities/cann|CANN]]
- [[entities/aws|AWS]]
- [[entities/aws-trainium|AWS Trainium]]
- [[entities/azure|Microsoft Azure]]
- [[entities/groq|Groq]]
- [[entities/cerebras|Cerebras]]
- [[entities/coreweave|CoreWeave]]
- [[entities/stargate|Stargate]]
- [[entities/microsoft|Microsoft]]
- [[entities/openai|OpenAI]]
- [[entities/anthropic|Anthropic]]
- [[entities/deepseek|DeepSeek]]
- [[entities/deepseek-v|DeepSeek-V 系列]]
- [[entities/glm|GLM]]
- [[entities/zhipu-ai|智谱 AI]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/llama-cpp|llama.cpp]]
- [[entities/pytorch|PyTorch]]
- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/hbm|HBM]]
- [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]
- [[concepts/gpu-cloud|GPU 云]]
