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

- **资料可靠性**：只有 Anthropic 官方博客和各项目 GitHub README、PyPI 元数据是一手；nvidia.com、amd.com、aws.amazon.com、blogs.microsoft.com、openai.com、groq.com、cerebras.ai、huawei.com、wikipedia.org 在本次调研的网络策略下无法打开，芯片规格、发布日期、融资与数据中心规模均为二手报道，厂商宣称的性能倍数没有第三方复现
- **NVIDIA**：FY2027 Q2（截至 2026-07-26）营收 962 亿美元，数据中心占比超 92%，下季指引假设中国数据中心计算营收为零；Vera Rubin 2026 下半年量产；2025-12 以约 200 亿美元非排他许可拿到 Groq 的推理技术
- **CUDA 13.0**：在 SIMT 之外新增 tile 编程模型与 CUDA Tile IR，13.1 推出 cuTile Python（Apache-2.0），统一 Arm 工具链——二十年来编程模型层面最大的一次变化
- **Google TPU**：第七代 Ironwood 每颗 192 GB HBM、4,614 TFLOPS（FP8）、pod 9,216 颗；第八代预览拆成 TPU 8t（训练）/ TPU 8i（推理），台积电 2nm，目标 2027 年底
- **Anthropic 的三平台策略**（一手）：计划用到 100 万颗 TPU、2026 年上线超过 1 GW 容量，同时继续使用 Trainium 与 NVIDIA GPU，Amazon 仍是主要训练伙伴
- **AMD**：ROCm 7.0 于 2025-09 发布，7.2.1 为当前版本；Instinct MI450（CDNA 5、HBM4、2nm）与机架平台 Helios 目标 2026 下半年，Oracle 计划部署 5 万颗
- **华为**：昇腾 950PR（2026 Q1）/ 950DT（2026 Q4）配自研 HBM，Atlas 950 SuperPoD 最大 8,192 颗；CANN 已开放 50+ 代码仓、800+ 算子；vLLM 的昇腾支持由社区插件 `vllm-ascend` 承担
- **AWS**：Trainium3 UltraServer 于 2025-12-02 GA（144 颗/系统、362 PFLOPS FP8），Trainium4 预览并将支持 NVLink Fusion；Project Rainier 为 Anthropic 部署近 50 万颗 Trainium2；2025-11-03 与 OpenAI 签七年约 380 亿美元协议
- **Groq / Cerebras**：Groq 以片上 SRAM 换低延迟、只做推理，技术被 NVIDIA 许可后公司独立存续；Cerebras 2026 年 IPO 定价 185 美元/股、募资约 55.5 亿美元，OpenAI 承诺采购 750 MW 推理算力，但客户集中度极高
- **Stargate**：2025-09 宣布五个新站点，规划容量近 7 GW；旗舰 Abilene 规划 1.2 GW，Epoch AI 卫星追踪估计 2026-04 仅约 0.3 GW 在运，完工预期推迟到 2026 Q4

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
