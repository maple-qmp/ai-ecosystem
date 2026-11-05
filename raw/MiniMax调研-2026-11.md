---
title: MiniMax 时间线调研（2026-11）
captured: 2026-11-05
tags: [notes]
---

# MiniMax 时间线调研（2026-11）

一句话：整理 MiniMax（稀宇科技）从 2021 年成立到 2026-11 的公司、上市、消费产品与模型时间线，重点是 MiniMax-01 / M1 的长上下文混合注意力路线、M2 系列的小激活编码 Agent 模型，以及 M3 的多模态与许可证收紧。资料来自 Hugging Face 模型卡与 API 元数据、Wikipedia 及其引用的 Bloomberg / Reuters / NYT / SCMP，以及上市报道，检索日期 2026-11-05。

## 原始链接

- Hugging Face 组织页：https://huggingface.co/MiniMaxAI
- MiniMax-Text-01 模型卡：https://huggingface.co/MiniMaxAI/MiniMax-Text-01
- MiniMax-M1 模型卡：https://huggingface.co/MiniMaxAI/MiniMax-M1-80k
- MiniMax-M2 模型卡：https://huggingface.co/MiniMaxAI/MiniMax-M2 （许可证 https://github.com/MiniMax-AI/MiniMax-M2/blob/main/LICENSE ）
- MiniMax-M2.1 / M2.5 / M2.7 模型卡：https://huggingface.co/MiniMaxAI/MiniMax-M2.1 、https://huggingface.co/MiniMaxAI/MiniMax-M2.5 、https://huggingface.co/MiniMaxAI/MiniMax-M2.7
- MiniMax-M3 模型卡与许可证：https://huggingface.co/MiniMaxAI/MiniMax-M3 ；MSA 算子：https://github.com/MiniMax-AI/MSA
- MiniMax-M3.1-Flash 模型卡：https://huggingface.co/MiniMaxAI/MiniMax-M3.1-Flash
- MiniMax-H3 模型卡：https://huggingface.co/MiniMaxAI/MiniMax-H3
- MiniMax Code（Agent 产品）：https://agent.minimax.io/
- Wikipedia：https://en.wikipedia.org/wiki/MiniMax_(company)
- The Star 2026-01-12（上市首日）：https://www.thestar.com.my/business/business-news/2026/01/12/minimax-shares-double-in-ipo-debut
- RTHK 2026-01-09：https://news.rthk.hk/rthk/en/component/k2/1839255-20260109.htm
- NYT 2026-02-23（Anthropic 指控蒸馏）：https://www.nytimes.com/2026/02/23/technology/anthropic-chinese-startups-distillation.html
- 阿里云百炼上架第三方模型（2026-05-20 峰会报道）：https://www.yzwb.net/news/ch/202605/t20260520_354889.html
- AgentScope README（2026-09 更新）：https://github.com/agentscope-ai/agentscope

## 官方原文摘录

MiniMax-Text-01 模型卡："MiniMax-Text-01 adopts a hybrid architecture that combines Lightning Attention, Softmax Attention and Mixture-of-Experts (MoE)."

MiniMax-M1 模型卡："We introduce MiniMax-M1, the world's first open-weight, large-scale hybrid-attention reasoning model."

MiniMax-M2 模型卡："It's a compact, fast, and cost-effective MoE model (230 billion total parameters with 10 billion active parameters) built for elite performance in coding and agentic tasks"

MiniMax-M2.1 模型卡："Our product MiniMax Code, built on MiniMax-M2.1, is now publicly available"

MiniMax-M2.5 模型卡："It costs just $1 to run the model continuously for an hour at a rate of 100 tokens per second."

MiniMax-M2.7 模型卡："M2.7 initiates a cycle of model self-evolution"

MiniMax-M3 模型卡：

- "MiniMax-M3 is a native multimodal model with 1M context. It has ~428B parameters and ~23B activated parameters."
- "M3 delivers 9× prefill and 15× decode speedups compared to M2 at 1M context, reducing per-token compute to 1/20."

MiniMax-M3 许可证（社区许可证）：免费授权限于 "non-commercial purposes"；商用时，年收入超过 2000 万美元的产品须 "obtain a separate, prior written authorization from MiniMax"，否则只需向 api@minimax.io 发一次性通知。

MiniMax-M3.1-Flash 模型卡："Building on MiniMax-M3, M3.1-Flash improves task performance and inference efficiency with sparse attention throughout the model, quantization-aware training, and DSpark speculative decoding."

AgentScope README："MiniMax chat models supported via `MiniMaxChatModel` (MiniMax-M3 by default)."

## 整理

### 1. 公司概况

- 2021-12 在上海成立，创始团队来自商汤，CEO 闫俊杰；早期获米哈游投资。公司名取自博弈论的 Minimax 算法。
- 业务两条线：消费产品（海外 Talkie、国内星野，视频平台海螺 Hailuo AI，语音、音乐）和开放平台 API（platform.minimax.io / 国内 minimaxi.com）。
- 2026-01-09 在港交所上市（股票代码 0100），是继智谱之后第二家上市的中国大模型公司。

### 2. 时间线

注：“HF 仓库”日期是 Hugging Face 仓库创建日，常早于公开发布几天；公开日期优先取官方公告或主流报道。

| 时间 | 事件 |
|---|---|
| 2021-12 | 公司在上海成立 |
| 2022-04 / 10 | abab1 文本模型；abab3 与首个消费应用 Glow |
| 2023-03 | Glow 在国内应用商店下架，原因未公开 |
| 2023-06 / 09 | 海外版 Talkie；国内版星野 |
| 2024-03 | 阿里巴巴领投 6 亿美元，估值约 25 亿美元（腾讯、红杉中国、IDG 等参与）；海螺 AI 上线 |
| 2024-04-17 | abab 6.5 系列 MoE 模型 |
| 2024-09 | 视频生成模型 video-01（海螺） |
| 2025-01 | **MiniMax-01** 开放权重：Text-01 与 VL-01，456B 总参数、45.9B 激活，Lightning Attention 混合架构 |
| 2025-04 | Speech-02 语音合成（30+ 语言） |
| 2025-06 | **MiniMax-M1** 开放权重推理模型（Apache-2.0），456B / 45.9B，原生 1M 上下文 |
| 2025-09 | 迪士尼、环球、华纳兄弟探索在美起诉海螺 AI 侵犯版权角色（Reuters） |
| 2025-10 | **MiniMax-M2**：230B 总参数、10B 激活，主打编码与 Agent，Modified MIT |
| 2025-12 | **MiniMax-M2.1** 开源；基于它的 Agent 产品 **MiniMax Code** 公开可用 |
| 2026-01-09 | 港交所上市（0100），发行价 165 港元，募资约 48.2 亿港元（约 6.19 亿美元），首日收盘 345 港元 |
| 2026-02 | **MiniMax-M2.5** 与 M2.5-Lightning；同月 Anthropic 指控其参与蒸馏 Claude |
| 2026-03 / 04 | **MiniMax-M2.7**（Wikipedia 记为 3 月，HF 仓库 04-09）：强调“模型自我进化”，SWE-Pro 56.22% |
| 2026-05-20 | 阿里云百炼上架第三方模型，首批含 MiniMax M2.7 |
| 2026-06-01 | **MiniMax-M3**：原生多模态（文本、图像、视频），约 428B 总参数、23B 激活，1M 上下文，MiniMax Sparse Attention（MSA）；改用 MiniMax 社区许可证 |
| 2026-07 下旬 | 开源 MiniMax-H3 音视频生成系统（最高 2K、15 秒，原生立体声），预处理模块 H3-Context-IR 只提供 API |
| 2026-08 | MiniMax-Music3 |
| 2026-09 | AgentScope（Python）新增 `MiniMaxChatModel`，默认模型 MiniMax-M3 |
| 2026-10 | **MiniMax-M3.1-Flash**：同为约 428B / 23B，全模型稀疏注意力、量化感知训练、DSpark 推测解码，面向编码、Agent、计算机操作与网络安全 |

### 3. 技术路线

- **长上下文优先**：MiniMax-01 / M1 用 Lightning Attention（线性注意力）与 Softmax 注意力混合，原生 1M 上下文；M2 系列回到小激活参数（10B）以降低 Agent 场景的延迟与成本；M3 用自研 MSA 稀疏注意力在 1M 上下文上把每 token 计算降到 M2 的 1/20。
- **小激活、低价**：M2.5 卡片称以每秒 100 token 连续运行一小时只需 1 美元。

### 4. 许可证演变

- MiniMax-01：Hugging Face 标签未标注许可证（本次未读许可证全文）；M1：Apache-2.0；M2 / M2.1 / M2.5 / M2.7：Modified MIT。
- M3 / M3.1-Flash：MiniMax 社区许可证。免费授权限于非商用；商用需向 MiniMax 发一次性通知，年收入超 2000 万美元的产品需事先书面授权。这是四家中对商用限制最严的开放权重许可证。
- H3：单独的 MiniMax H3 社区许可协议。

### 5. 与阿里生态的关系

- 资本：阿里巴巴 2024-03 领投。
- 分发：2026-05-20 起阿里云百炼可通过统一 API 调用 MiniMax M2.7。
- 框架：AgentScope（Python）2026-09 起内置 `MiniMaxChatModel`；Spring AI Alibaba 未单列，可通过 OpenAI 兼容接口接入（整理者归纳）。

### 6. 待核实

- 上市募资额：多数来源为 48.2 亿港元，一处为 55.4 亿港元（可能含超额配售）。
- 首日涨幅：收盘约 +109%，不同来源报 54%、78%、91%，多为盘中数据。
- M3 权重实际上线日：模型公告 06-01，有报道称权重延后一周左右。
