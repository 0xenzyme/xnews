---
title: 2026-11-22-X Chinese Topics Brief
headline: Riemann proof certified · MiniMax requests exposed · House targets Chinese open models
type: x-cn-topic-brief
date: 2026-11-22
tags: [x-cn-topic-brief, ai, riemann-hypothesis, claude, lean, openrouter, minimax, novita, privacy, house-report, open-weights, cursor, kimi, tencent, hy4, nvidia, h200, export-controls, inkling, qwen]
source: x.com + alpo.ge / Lean community blog / Scientific American / Novita notice / Privacy Affairs / House committee sites / CNBC / huggingface.co / California DOJ / Bloomberg
window: 2026-11-21 08:00 to 2026-11-22 08:00 (Asia/Shanghai), with Nov 20 catch-ups
generated: 2026-11-22T08:40:00+08:00
coverage: partial
---
# X Chinese Topics Brief (2026-11-22)

Saturday's Chinese-language conversation centered on three things: whether the AI-assisted Riemann proof is "really done," OpenRouter's notice that MiniMax-bound requests may have been read by a third party, and a House report urging a federal ban on Chinese open-weight models. Tencent's full Hy4 weights, missed last edition, are caught up here.

## Today's must-reads

1. **Riemann Hypothesis: the Lean and Mathlib communities certify the proof** (see Daily section 1). The common Chinese reply, "wait for peer review," is half out of date: the formal statement and proof have been independently rechecked. Still open: a human-readable paper, and what Claude actually contributed, which rests on the author's account. Treat the same-day Navier–Stokes paper separately; its key numerical certificate is not public. Status: ready to draft; formal result verified, division of labor author-claim, Navier–Stokes unverified.

2. **OpenRouter: requests forwarded to MiniMax via three hosts may have been read by a third party** (see Daily section 3). The Chinese angle: trust in Chinese model vendors among overseas developers, and how much a "zero data retention" label means on an aggregator. Novita has an official notice admitting the forwarding and giving a date range; MiniMax has not responded publicly. Keep three layers apart: the researcher's test, the hosts' admissions, and MiniMax's explanation (relayed via StreamLake). Status: ready to draft; Novita verified, OpenRouter email author-claim, MiniMax explanation unverified.

3. **House committees urge banning Chinese open-weight models in federal systems, contracts, and high-risk critical infrastructure** (see Daily section 4). CNBC reports Cursor will explore phasing them out, and notes its Composer 2 was built on Kimi K2.5. Angle: the more the US uses Chinese open models, the more compliance pressure follows; pair it with Raschka's point that US and Chinese open models pushed each other forward. Status: ready to draft; report verified, Cursor position author-claim.

4. **Tencent Hunyuan releases full Hy4 weights: 770B / 49B active, 1M context, with a system card** (see Daily section 2). A counterpoint to item 3: the US talks restrictions while a Chinese lab keeps open-sourcing flagships with safety evals. Status: ready to draft; weights verified, system-card findings author-claim.

## More topics

### 1. 879K H200 / MI325X chips approved for China, ~272K to Alibaba, Tencent, Baidu, and BYD

- Source & heat: [@GOP__Ls](https://x.com/GOP__Ls/status/2124246547059679334) — about 19K impressions, 1,453 likes (partisan framing); primary: [CNBC](https://www.cnbc.com/2026/11/19/nvidia-amd-china-chip-sales-congress.html)
- What's in it: Congressional disclosure of Commerce data shows 879,868 approvals as of May 11, 2026; the four firms on the Pentagon's Chinese-military-companies list got about 272,000. Bloomberg separately reports California's Nvidia probe covers possible criminal violations.
- Angle: From Chinese clouds' view, will approved shipments actually arrive? Keep it apart from the smuggling allegations.
- Timing & verification: The figures are verified as consistently reported; the X claim of a "25% cut" is unverified and not used.

### 2. Inkling 2 Mini vs Qwen 3.8 27B, run locally

- Source & heat: [@bebuu_ai](https://x.com/bebuu_ai/status/2124067425113329707) — about 26K impressions, 310 likes; [@pratikg on a Mac mini](https://x.com/pratikg/status/2123942773594427629) — about 27K impressions, 195 likes
- What's in it: Hands-on tests of two ~26–27B models on 32GB and 64GB Macs; Inkling 2 Mini activates only 3.4B parameters per token.
- Angle: "What runs on a laptop" is a perennial Chinese-dev question; works as a comparison piece.
- Timing & verification: Model specs verified (official page); test results are personal: unverified.

### 3. Chainalysis: China-linked wallet payments jump 55% after frontier model launches

- Source & heat: [@Cointelegraph](https://x.com/Cointelegraph/status/2124163503086858461) — about 38K impressions, 98 likes
- What's in it: Reportedly Chinese users pay proxy services in stablecoins to reach ChatGPT, Claude, and Gemini, with payments 55% above normal in the three days after new model releases.
- Angle: Side evidence of demand under export controls, but second-hand only.
- Timing & verification: We did not find the Chainalysis original: author-claim.
