---
title: 2026-11-22-X 中文热点简报
headline: 黎曼猜想获 Lean 认证 · MiniMax 请求疑被读取 · 美众院盯上中国开源模型
type: x-cn-topic-brief
date: 2026-11-22
tags: [x-cn-topic-brief, ai, riemann-hypothesis, claude, lean, openrouter, minimax, novita, privacy, house-report, open-weights, cursor, kimi, tencent, hy4, nvidia, h200, export-controls, inkling, qwen]
source: x.com + alpo.ge / Lean 社区博客 / Scientific American / Novita 通告 / Privacy Affairs / 众议院委员会官网 / CNBC / huggingface.co / 加州司法部 / Bloomberg
window: 2026-11-21 08:00 至 2026-11-22 08:00（Asia/Shanghai），含 11 月 20 日补录
generated: 2026-11-22T08:40:00+08:00
coverage: partial
---
# X 中文热点简报（2026-11-22）

周六中文圈的讨论集中在三件事：黎曼猜想的 AI 协作证明是否「真的成了」，OpenRouter 关于 MiniMax 请求可能被第三方读取的通知，以及美国众议院建议在联邦系统禁用中国开源权重模型。腾讯 Hy4 完整权重是上期漏掉的一条，这期补上。

## 今日必读

1. **黎曼猜想：Lean / Mathlib 社区联合声明证明正确**（见 Daily 第 1 节）。中文帖里常见的「等同行评审再说」已经过时了一半：形式化证明的命题和证明都经社区独立复核。仍未解决的是人类可读的论文，以及 Claude 到底贡献了什么，这部分只有作者的说法。同日的 Navier–Stokes 爆破论文要单独写，关键数值证书未公开。状态：可起草；形式化结论 verified，分工 author-claim，NS unverified。

2. **OpenRouter 通知：经三家托管商转发到 MiniMax 的请求，内容可能被第三方读取**（见 Daily 第 3 节）。中文角度：这直接关系到国内模型厂商在海外开发者中的信任，也关系到「零数据保留」标签在聚合平台下有多可靠。Novita 已发官方通告承认转发并给出时间段；MiniMax 本期没有公开回应。写稿时把「研究员测试结果」「托管商承认」「MiniMax 的解释（经 StreamLake 转述）」分成三层。状态：可起草；Novita 确认 verified，OpenRouter 邮件 author-claim，MiniMax 解释 unverified。

3. **美众院两委员会报告：建议联邦系统、联邦合同和高风险关键基础设施禁用中国开源权重模型**（见 Daily 第 4 节）。CNBC 报道 Cursor 表示会探讨逐步停用中国开源模型，报道提到其 Composer 2 基于 Kimi K2.5。适合写「中国开源模型在美国用得越多，合规压力越大」，可配 Raschka 的观点：美中开源模型互相推动。状态：可起草；报告 verified，Cursor 表态 author-claim。

4. **腾讯混元放出 Hy4 完整权重：770B / 49B 激活、1M 上下文、附系统卡**（见 Daily 第 2 节）。与第 3 条形成对照：一边是美国建议限制，一边是中国大厂继续开源旗舰并附安全评测。状态：可起草；权重 verified，系统卡结论 author-claim。

## 更多话题

### 1. 87.9 万颗 H200 / MI325X 获批对华，约 27 万颗批给阿里、腾讯、百度、比亚迪

- 原帖与热度：[@GOP__Ls](https://x.com/GOP__Ls/status/2124246547059679334)｜约 1.9 万曝光、1,453 赞（措辞偏政治）；原文：[CNBC](https://www.cnbc.com/2026/11/19/nvidia-amd-china-chip-sales-congress.html)
- 内容与关注点：国会披露的商务部数据显示，截至 2026 年 5 月 11 日共批准 879,868 颗；被列入五角大楼「中国军事企业」名单的四家公司合计约 27.2 万颗。同期加州对英伟达的调查据 Bloomberg 报道涉及可能的刑事违法。
- 为什么值得做／可写角度：从中国云厂商视角写「已批的货能不能如期到」，不要跟走私指控混写。
- 时效与核验：数据 verified 为多家媒体一致口径；X 上「换取 25% 分成」的说法 unverified，未采用。

### 2. Inkling 2 Mini 与 Qwen 3.8 27B 的本地对比

- 原帖与热度：[@bebuu_ai](https://x.com/bebuu_ai/status/2124067425113329707)｜约 2.6 万曝光、310 赞；[@pratikg 的 Mac mini 测试](https://x.com/pratikg/status/2123942773594427629)｜约 2.7 万曝光、195 赞
- 内容与关注点：两个约 26–27B 级别模型在 32GB / 64GB Mac 上的实测，Inkling 2 Mini 每 token 只激活 3.4B 参数。
- 为什么值得做／可写角度：中文开发者关心的「笔记本上能跑什么」，可以做成对比稿。
- 时效与核验：模型参数 verified（官网）；实测结果是个人体验，unverified。

### 3. Chainalysis：中国关联钱包在前沿模型发布后付款激增 55%

- 原帖与热度：[@Cointelegraph](https://x.com/Cointelegraph/status/2124163503086858461)｜约 3.8 万曝光、98 赞
- 内容与关注点：报道称中国用户用稳定币支付代理服务来使用 ChatGPT、Claude、Gemini，新模型发布后三天内付款高于常态 55%。
- 为什么值得做／可写角度：可作为「出口管制之下的使用需求」的旁证，但只有二手转述。
- 时效与核验：本期未找到 Chainalysis 原报告，author-claim。
