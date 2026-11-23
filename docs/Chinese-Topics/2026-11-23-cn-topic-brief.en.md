---
title: 2026-11-23-X Chinese Topics Brief
headline: Ant open-sources medical model · Beijing to meter tokens · DNI on chips
type: x-cn-topic-brief
date: 2026-11-23
tags: [x-cn-topic-brief, ai, ant-group, lingsante, medical-ai, token-factory, national-data-administration, nvidia, export-controls, kimi, semianalysis, rubin, muxi, hy4, zhipu, minimax, doubao]
source: x.com + huggingface.co / Yicai / The Next Web / Semafor / openai.com
window: 2026-11-22 08:00 to 2026-11-23 08:00 (Asia/Shanghai)
generated: 2026-11-23T08:30:00+08:00
coverage: partial
---
# X Chinese Topics Brief (2026-11-23)

No new Chinese model launches on Sunday. Chinese-language discussion centered on three things: Ant's open medical model, the National Data Administration's plan to standardize token billing, and the US intelligence chief confirming controlled chips reached China. Two leads suit technical pieces: SemiAnalysis benchmarking Nvidia Rubin with Kimi K3.1 Pro, and domestic GPU "Day 0" support.

## Today's must-reads

1. **Ant's inclusionAI open-sources LingSante-3.1-flash, a 560B / 25B-active medical model under MIT** (see Daily §2). China angle: a big Chinese lab open-sourcing a flagship-size vertical model under a looser license than most general models. Pair it with Chinese medical-AI rules: "downloadable" is not "clinically deployable." Status: ready to draft; weights and license verified, benchmark wins author-claim.

2. **National Data Administration: standards for token metering, billing and quality testing, and no "low-quality duplicate construction"** (see Daily §3). China angle: as token factories spread, a unified counting rule for reasoning and cached tokens will reshape the price war. English X mostly joked about "token bills"; a Chinese piece can explain the national standard project on counting rules. Status: ready; remarks verified, usage numbers author-claim.

3. **DNI Clayton: China "had access" to controlled Nvidia chips; Bessent defends sales** (see Daily §3). China angle: after last week's 879,868 approvals and the Jensen Huang affair, Washington is speaking with two voices. Write it as that, not as "US admits China broke the blockade." Status: ready; quotes verified, the "7,000–22,000 Blackwell" figure unverified.

4. **OpenAI publishes internal pretraining perplexity and proposes industry "common limits"** (see Daily §1). China angle: will Chinese labs publish comparable numbers? That decides whether they can be part of any future common-limit framework. Status: ready; verified.

## More topics

### 1. SemiAnalysis: Kimi K3.1 Pro on Vera Rubin NVL72 serves 1.82–6.67x the tokens per dollar of GB300

- Source & heat: [@AIQuanting breakdown](https://x.com/AIQuanting/status/2124641617093284150) | 96 views; [@ChuckBass8808 (zh)](https://x.com/ChuckBass8808/status/2124648515796381783) | 250 views, 7 likes
- What & why: The test replays real Claude Code sessions and counts tokens served per dollar of ownership cost. The breakdown notes GB300 does far better on vLLM, so most of the 6.67x comes from GB300's SGLang setup; at matched speed Rubin leads by about 2x.
- Angle: A 2.8T Chinese open model as the reference workload for Nvidia's new architecture is itself a signal.
- Timing & verification: relays only, original chart not read, unverified; very low heat.

### 2. MetaX says it has done "Day 0" support for 52 major models, Hy4 the latest

- Source & heat: [@ofrbkj](https://x.com/ofrbkj/status/2124419567304982964) | 407 views, 9 likes
- What & why: On Hy4's launch day MetaX announced its Xiyun C-series GPUs were ready; the post notes MetaX says it has adapted 52 models since Dec 2025.
- Angle: Next to Clayton's remarks, "how fast domestic compute adapts" is a more useful story than smuggling.
- Timing & verification: MetaX's own figure (relayed), author-claim.

### 3. Chinese AI app MAUs and listed-company losses: Doubao 419M; Zhipu and MiniMax each lost ~¥1.96B in H1

- Source & heat: [@YxzRainy MAU list](https://x.com/YxzRainy/status/2124307625362034935) | ~5.3K views, 72 likes; [@ileoyeye financials](https://x.com/ileoyeye/status/2124334765486821604) | ~17K views, 34 likes
- What & why: After Anthropic's IPO and the Riemann news, Chinese X compared the financial pressure on domestic model companies.
- Angle: A "burning cash while open-sourcing" feature, but find the filings first.
- Timing & verification: no sources given for MAU or financial figures, unverified; don't quote directly.

### 4. Doubao Work and Qwen Office add third-party models, closing WorkBuddy's multi-model edge

- Source & heat: [@WangNextDoor2](https://x.com/WangNextDoor2/status/2124458872454647819) | ~1.4K views, 5 likes
- What & why: Doubao Work opened Kimi, GLM and DeepSeek on Nov 12; days later Qwen Office added ten models. Some users report the same model runs slower inside Doubao Work.
- Angle: Chinese office-agent platforms are shifting from "our own model" to "model supermarket."
- Timing & verification: integrations need confirming on official pages, unverified this edition; UX reports are individual.
