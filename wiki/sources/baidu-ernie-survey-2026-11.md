---
title: 百度文心（ERNIE）、文心 App 与昆仑芯调研（2026-11）
type: source
tags: [notes]
source_note: "[[百度-文心调研-2026-11]]"
url: https://huggingface.co/baidu
created: 2026-11-07
updated: 2026-11-07
sources:
  - "[[entities/baidu]]"
  - "[[entities/ernie]]"
  - "[[entities/ernie-app]]"
  - "[[entities/kunlunxin]]"
---

# 百度文心（ERNIE）、文心 App 与昆仑芯调研（2026-11）

## Summary

整理[[entities/baidu|百度]]的[[entities/ernie|文心（ERNIE）]]模型家族、[[entities/ernie-app|文心 App]]（文心一言 → 文小言 → 文心）和自研 AI 芯片子公司[[entities/kunlunxin|昆仑芯]]。开源策略三次转向：2025-06 的 ERNIE 4.5 以 Apache-2.0 开放权重；ERNIE 5.0（2025-11 预览、2026-01 上线）和 5.1（2026-05）闭源；2026-11-05 开源 ERNIE 5.5 Flash Base（280B / 14B 激活），但改用自定义许可证：排除欧盟、英国、韩国，相关产品年收入超 5000 万美元须另取书面授权。昆仑芯 2026-01 向港交所秘密递表。模型参数与许可证以 Hugging Face 模型卡和许可证原文为准（2026-11-07 读取）。

## Key Points

- **文心一言**：2023-03-16 邀请测试，2023-08-31 向公众开放；2024-09 改名文小言，2025-11 随 ERNIE 5.0 改名文心
- **ERNIE 4.5（2025-06）**：0.3B 至 424B 共 10 个模型开放权重，含 300B-A47B [[concepts/mixture-of-experts|MoE]] 与多模态版，Apache-2.0，提供 PyTorch 与飞桨两种权重
- **ERNIE 5.0 / 5.1**：原生全模态；5.0 媒体称 2.4T 参数（百度未确认），LMArena 2026-01 国内第一；5.1 称预训练成本约为同级模型的 6%；均不开放权重
- **ERNIE 5.5 Flash Base（2026-11-05）**：33.5T token 从头预训练、1M 上下文，混合 MLA / HCA 注意力、Multi-Router MoE、ECHO 代替 MTP；只放出预训练检查点，后训练版待发
- **许可证收紧**：地域限制与 [[entities/hunyuan|腾讯旧版混元许可证]]相同；还禁止用模型或输出改进其他模型
- **昆仑芯**：P800 为主力；2025-11 公布 M100（2026）、M300（2027）与天池超节点；百度持股约 59%，2026 年筹划港股与科创板双重上市
- **部署**：[[entities/sglang|SGLang]] 与 [[entities/vllm|vLLM]]（`vLLM-ERNIE` 插件）

## Mentioned Pages

- [[entities/baidu|百度]]
- [[entities/ernie|文心（ERNIE）]]
- [[entities/ernie-app|文心 App]]
- [[entities/kunlunxin|昆仑芯]]
- [[entities/hunyuan|混元（Tencent HY）]]
- [[entities/glm|GLM]]
- [[entities/kimi|Kimi]]
- [[entities/deepseek-r1|DeepSeek-R1]]
- [[entities/nvidia|NVIDIA]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/ai-accelerator|AI 加速器]]
