---
title: 2026-11-10-X Chinese Topics Brief
headline: Meituan opens LongCat-2.5 · China merges AI filings · CN takes on Fable 5.2
type: x-cn-topic-brief
date: 2026-11-10
tags: [x-cn-topic-brief, ai, meituan, longcat-2-5, cac, ai-filing, anthropic, claude-fable-5-2, seedream-5-5, deepseek-harness]
source: x.com + huggingface.co/meituan-longcat/LongCat-2.5 / beian.cac.gov.cn (via multiple reposts)
window: 2026-11-09 08:00 to 2026-11-10 08:00 Asia/Shanghai
generated: 2026-11-10T08:30:00+08:00
coverage: partial
---
# X Chinese Topics Brief (2026-11-10)

Topics for Chinese-language writers. Two home-grown stories led the Chinese timeline today: Meituan open-sourced LongCat-2.5, and the Cyberspace Administration of China (CAC) launched a unified filing system. Most other heat was reposting Anthropic's Fable 5.2. Nov 9 items (DeepSeek Harness, the Menlo report, Arete) are not reopened.

## Today's must-reads

1. **Meituan opens LongCat-2.5 weights** (see Daily item 2). 1.6T total / ~48B active, MIT license, trained on domestic accelerators, W4A4 quantization. Angle: how a trillion-parameter open model runs on Chinese chips. Status: ready to draft; weights verified, benchmarks self-reported.

2. **CAC launches a unified "new technology and new application" filing system.** From Nov 9, generative AI, algorithm, deep-synthesis and blockchain filings share one portal; the old algorithm and blockchain filing systems are retired, and filings are searchable by entity name or filing number. The accompanying FAQ says blockchain service names may not contain "virtual currency," "exchange" or "ICO." Angle: a practical explainer for teams shipping AI products in China. Status: ready to draft; consistent across many accounts, but the official page was not opened directly this issue.

3. **Chinese reaction to Claude Fable 5.2** (see Daily item 1). Chinese reposts focus on the 20% price cut and "1,000 agents formalized Fermat's Last Theorem in 30 hours." Angle: "are mathematicians becoming supervisors?" commentary, attributing the results to Anthropic. Status: ready to draft.

## More topics

### 1. LongCat-2.5 open weights

- Source & heat: [Meituan_LongCat](https://x.com/Meituan_LongCat/status/2119793531393040462), ~35K views, 954 likes; Chinese reposts [NFT_Chen](https://x.com/NFT_Chen/status/2119810010415018299), ~3K; [bobolv235824](https://x.com/bobolv235824/status/2119721972921700786)
- What it covers: MIT license; model card reports ~43% higher decode throughput for W4A4 vs W8A8; NPU deployment via SGLang-FluentLLM
- Angle: put it in one table with GLM-5.3, kimi-k3 and DeepSeek-V4.1-Flash to map the Chinese open-model top tier
- Timing & verification: weights verified; the model page shows 1.8T stored parameters vs the advertised 1.6T

### 2. CAC unified filing system

- Source & heat: [Foresight_News](https://x.com/Foresight_News/status/2119766565877170438), ~4.8K; [xiaoanlab](https://x.com/xiaoanlab/status/2119725432199057870); [cryptowang4423](https://x.com/cryptowang4423/status/2119704842654671185), ~14K
- What it covers: four filing types in one place; five situations that block blockchain filings (virtual-currency activity, servers abroad, no ICP filing, and others)
- Angle: "one portal doesn't mean looser rules," for teams serving both China and overseas
- Timing & verification: consistent across sources; official text still to be checked

### 3. Seedream 5.5 goes global

- Source & heat: [dreamina_ai](https://x.com/dreamina_ai/status/2119751497282125949), ~90K views, 337 likes
- What it covers: portrait realism, ~95% text accuracy, drift-free local edits, transparent assets; limited-time free use
- Angle: hands-on comparisons for posters and e-commerce images
- Timing & verification: official, verified; text accuracy is self-reported

### 4. DeepSeek Harness at "60M tokens per user per day"

- Source & heat: [tsuan167186](https://x.com/tsuan167186/status/2119747278210523499), ~80; [GodanLeeX](https://x.com/GodanLeeX/status/2119604768847069656), ~300
- What it covers: a back-of-envelope from the official Nov 8 data puts each daily user at ~60M tokens a day, implying mostly background agent runs; one developer reports loops and context overflow after installing 15+ plugins
- Angle: a practical "more plugins isn't better" follow-up to the Nov 9 topic
- Timing & verification: per-user figure is a user estimate; plugin issues are anecdotal, unverified

### 5. Qwen Office 2.0 multi-user agents

- Source & heat: only a digest account repost, [SUPARLUXI](https://x.com/SUPARLUXI/status/2119933248159850731), very low heat
- What it covers: reportedly launched multi-user agent collaboration on Nov 9
- Angle: revisit once there is official information
- Timing & verification: unverified, no official post found; backup only
