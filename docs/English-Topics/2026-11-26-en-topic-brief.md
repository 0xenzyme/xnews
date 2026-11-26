---
title: 2026-11-26-X 英文热点简报
headline: ω=9/4 刷屏 · Rust 迁移实录 · 分解传言与 AGI 时间表
type: x-en-topic-brief
date: 2026-11-26
tags: [x-en-topic-brief, ai, ai-math, matrix-multiplication, riemann, factoring-rumor, anthropic, rust, private-inference, perplexity, metr, agi-timelines, shane-legg, anthropic-ipo, gemini-api-cli, interpretability, telos, every]
source: x.com（官方帖 @SebastienBubeck、@AnthropicAI、@sama、@ShaneLegg、@OfficialLoganK；METR；anthropic.com、github.com/openai/math）
window: 2026-11-25 08:00 至 2026-11-26 08:00（Asia/Shanghai；补收前一窗口漏掉的 11-25 凌晨发布）
generated: 2026-11-26T08:30:00+08:00
coverage: partial
---
# X 英文热点简报（2026-11-26）

英文 X 今天被数学刷屏：OpenAI 的 ω=9/4 预印本、黎曼证明之后 agent 批量出结果、以及 Scott Aaronson 被转述的「多项式时间分解」传言，三者被很多人串成「实验室在藏最强模型」的叙事。工程圈则在转 Anthropic 的 Rust 迁移博客。观点层面，Shane Legg 17 年来首次上调 AGI 概率，METR 解读 OpenAI 困惑度曲线「约快 7 倍」。

## 今日必读

1. **ω 恰好 9/4**（见 Daily 第 1 节）。英文 X 反应两极：一边是 Greg Brockman 转引「一生没想到能看到的结果」，一边是复杂度圈等着细读 111 页。热度：Bubeck 帖约 67 万曝光、gdb 帖约 33 万曝光。状态：可起草；预印本 verified，正确性 author-claim。

2. **数学「连锁反应」与分解传言**（见 Daily 第 1 节）。角度：把「论文 / 团队自述 / 传言」三层分开写。热度：[@kimmonismus](https://x.com/kimmonismus/status/2125602411540566221) 约 160 万曝光、7,467 赞——传言比论文传得更远。状态：可起草，但分解部分只能写成 unverified 传言；Google 6 篇论文未找到原始出处。

3. **Anthropic：用线上服务验证 Rust 迁移**（见 Daily 第 2 节）。角度：「agent 写 + agent 验」的完整案例，以及差异指纹这一可复用方法。热度：约 180 万曝光、3,730 收藏（收藏率高，说明工程师在存档）。状态：可起草；方法 verified，性能数字 author-claim。

## 更多话题

- **OpenAI Private Inference 小范围测试**（[@sama](https://x.com/sama/status/2125638790593274259)，6,629 赞）。角度：机密计算 + 前沿模型能否打开受监管行业。核验：verified；细节未公开。
- **困惑度曲线 7 倍加速**（[@METR_Evals](https://x.com/METR_Evals/status/2125372372039741753)，2,022 赞）。角度：首次公开的完整预训练损失序列；数据集未开放，外部无法复算。核验：METR 计算 author-claim。
- **Shane Legg：2028 年前 Minimal AGI 概率超过 50%**（[@ShaneLegg](https://x.com/ShaneLegg/status/2125665607840346357)，985 赞）。角度：长期最稳定的预测者首次调整。核验：verified（本人帖）。
- **$ANT 收复 83 美元发行价**（[@KobeissiLetter](https://x.com/KobeissiLetter/status/2125645220524286373)）。角度：零售资金托底，创始人套现近 20 亿美元的讨论仍在。核验：行情转述，author-claim。
- **Gemini API CLI 进入别家编码 agent**（[@OfficialLoganK](https://x.com/OfficialLoganK/status/2125681386388422775)，579 收藏）。角度：Google 的「做别家 agent 的子能力」策略。核验：verified。
- **Anthropic Fellows 回到「单个神经元」做可解释性**：二手帖称，按神经元对输出的贡献来衡量，开源模型里的单神经元就能检测有害内容、引导行为（[@0x0SojalSec](https://x.com/0x0SojalSec/status/2125386525093560745)）。热度：低。核验：本期未读到 Anthropic 原帖或论文链接，unverified。
- **Every 融资 1,750 万美元 A 轮**（[@danshipper](https://x.com/danshipper/status/2125615579964833827)）。角度：AI 媒体 + 工具 + 咨询的组合模式。核验：verified。
