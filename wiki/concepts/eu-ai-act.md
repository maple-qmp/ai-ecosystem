---
title: 欧盟《人工智能法》
type: concept
tags: [standard]
layer: X
aliases: ["欧盟《人工智能法》", "EU AI Act", "AI Act", "Artificial Intelligence Act", "Regulation (EU) 2024/1689", "人工智能法案", "Digital Omnibus on AI", "Regulation (EU) 2026/1744"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/ai-policy-survey-2026-11]]"]
---

# 欧盟《人工智能法》

## 定义

欧盟按风险分级监管 AI 的统一法规（Regulation (EU) 2024/1689），2024-07-12 刊登官方公报，2024-08-01 生效，在所有成员国直接适用。内容分四块：禁止的做法、高风险 AI 系统、透明度义务、通用目的 AI（GPAI）模型义务。2026-07-27 生效的 Digital Omnibus on AI（Regulation (EU) 2026/1744，2026-07-08 签署，07-24 刊登公报）推迟了高风险义务，并新增两项禁止，GPAI 义务没有推迟。

## 关键特征

### 适用时间表（第 113 条，Omnibus 修订后）

- 2025-02-02：总则（含 AI 素养义务）与禁止的做法
- 2025-08-02：GPAI 义务（第五章）、治理、罚则开始适用，GPAI 罚款（第 101 条）除外
- 2026-08-02：一般适用，包括第 50 条透明度义务，以及委员会对 GPAI 的执法和罚款权
- 2026-12-02：新增禁止条款开始适用；2026-08-02 前已上市的生成式系统，第 50(2) 条标记义务的过渡期截止
- 2027-12-02：附件三高风险系统（招聘、信用评分、教育、边境管控等），原定 2026-08-02
- 2028-08-02：附件一高风险系统（嵌入医疗器械、机械等受监管产品），原定 2027-08-02

### Omnibus 新增的禁止

- 未经本人明确同意，生成或篡改可识别自然人私密部位或性行为的逼真图像、视频、音频（非自愿私密深度伪造）
- 生成儿童性虐待材料
- 只有当这类生成是系统的预期用途，或系统的设计、训练、能力使其成为可合理预见、可复现的结果时，投放市场才被禁止

### GPAI 义务

- **所有 GPAI 提供者（第 53 条）**：维护模型技术文档，应要求提供给 AI Office；向下游集成方提供文档；制定遵守欧盟版权法的政策，尊重权利保留（opt-out）；按 AI Office 模板公开训练数据摘要
- **开源豁免**：以自由开源许可发布，并公开权重、架构和使用信息的模型，免除前两项文档义务；有系统性风险的模型不豁免
- **系统性风险（第 51、55 条）**：训练算力超过 10^25 FLOP 推定为系统性风险模型，另需做模型评测和对抗测试、评估并缓解欧盟层面的系统性风险、报告严重事件、保障网络安全
- **罚款（第 101 条）**：最高为全球年营业额 3% 或 1500 万欧元，取较高者

### GPAI 实践准则

- 2025-07-10 发布，分透明度、版权、安全与安保三章，自愿签署。委员会与 AI Board 确认它是证明合规的“充分的自愿工具”，提供者可依第 53(4) 条据此证明合规；但 Omnibus 序言写明，实践准则法律效力有限，**不授予合规推定**
- 签署方（委员会名单，2026-10-07 更新）：Amazon、[[entities/anthropic|Anthropic]]、Google、IBM、[[entities/microsoft|Microsoft]]、[[entities/mistral-ai|Mistral AI]]、[[entities/openai|OpenAI]]、Aleph Alpha、Cohere、Black Forest Labs、ServiceNow 等 22 家
  - [[entities/xai|xAI]] 只签了安全与安保章，透明度与版权义务须用其他方式证明
  - 名单中没有 [[entities/meta-ai|Meta]]

## 应用

- 在欧盟提供模型或 AI 系统的公司都须遵守，包括美国和中国的模型厂商
- 开放权重发布者（如 [[entities/mistral-ai|Mistral AI]]、[[entities/deepseek|DeepSeek]]）可以用开源豁免减少文档义务，但训练算力超过 10^25 FLOP 的模型不豁免
- 图像、视频生成服务须在 2026-12-02 前满足新增禁止条款和标记义务

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 政策法规（欧盟）
- **对照**：
  - 美国[[concepts/california-sb-53|加州 SB 53]]以 10^26 次运算为门槛，侧重透明度和事件报告
  - 中国[[concepts/china-generative-ai-measures|生成式 AI 管理办法]]以上线前备案为核心

## 相关概念

- [[concepts/frontier-safety-frameworks|前沿模型安全框架]]
- [[concepts/california-sb-53|加州 SB 53]]
- [[concepts/china-generative-ai-measures|中国生成式 AI 管理办法与备案]]
- [[concepts/us-federal-ai-policy|美国联邦 AI 行政令]]
- [[concepts/scaling-laws|规模定律]]

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/openai|OpenAI]]
- [[entities/mistral-ai|Mistral AI]]
- [[entities/meta-ai|Meta AI]]
- [[entities/xai|xAI]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "This exception shall not apply to general-purpose AI models with systemic risks." — [[sources/ai-policy-survey-2026-11|AI 政策法规调研]]
- "The Commission may impose on providers of general-purpose AI models fines not exceeding 3 % of their annual total worldwide turnover in the preceding financial year or EUR 15 000 000, whichever is higher" — [[sources/ai-policy-survey-2026-11|AI 政策法规调研]]
- "Given that the codes of practice referred to in Article 50(7) and Article 56(6) have limited legal effect, and in particular do not grant a presumption of conformity, it is not strictly necessary for these codes to be approved by an implementing act." — [[sources/ai-policy-survey-2026-11|AI 政策法规调研]]
