---
title: 2026-11-19-X Chinese Topics Brief
headline: Hy4 flash weights drop · Neon’s quiet CN start · ANT prices
type: x-cn-topic-brief
date: 2026-11-19
tags: [x-cn-topic-brief, ai, hy4-flash, hunyuan, tencent, gemini-4-neon, google, anthropic, ipo, ant, opencode, qwen4-max]
source: x.com (also checked huggingface.co/tencent/Hy4-flash, blog.google, anthropic.com pricing release, CNBC)
window: 2026-11-18 08:00 to 2026-11-19 08:00 (Asia/Shanghai)
generated: 2026-11-19T08:25:00+08:00
coverage: partial
---
# X Chinese Topics Brief (2026-11-19)

The global headlines are Gemini 4 Neon and Anthropic’s first trade, but the Chinese-language thread that actually circulated is Tencent Hunyuan’s Hy4 flash weight drop. Native Chinese discussion of Neon and the ANT pricing is still thin, and some recaps still use the pre-upsized share count. Chinese posts are mostly in the thousands to tens of thousands of impressions; official English posts are in the mid- to high-six figures.

## Today's must-reads

1. **Hy4 flash open weights** (see Daily §3). This is the cleanest product story in the Chinese circle today: instruct, FP8, and Base dropped together; the model card lists ~220B total / ~12B active per token, a 1M context, and the Tencent Hy License. OpenCode says it stays exclusively free there for 10 more days. Worth writing as “read the license, then compare FP8 local runs with the OpenCode window on the same everyday tasks,” not as another “open source wins” recap. Status: ready to draft; the weight drop is verified, speed and cost multiples are author-claim.

2. **Gemini 4 Neon is live, but Chinese discussion barely started** (see Daily §1). Official English posts cleared ~400k impressions; native Chinese posts before the announcement were mostly “which element ships tonight” and pricing-table leaks, and post-launch heat is still in the tens to thousands. Worth spelling out the slot: between Carbon and Hydrogen, $3 input / $15 output, not a new Carbon, and not an official statement that older client models have been pulled. Status: ready to draft; launch and pricing are verified.

3. **Anthropic prices at $83, ANT trades today** (see Daily §2). The official offer was upsized to 980 million shares; CNBC pegs proceeds at about $81.3 billion. Chinese recaps can still sit on the old 825 million share count or the $70–$78 range. Worth writing what listing day means for domestic buyers and rivals, and flagging that private-placement amounts were not checked against the company release. Status: ready to draft; price and first-trade date are verified, proceeds and valuation are media math.

## More topics

### 1. OpenCode extends a 10-day free window for Hy4 flash

- Source & heat: [opencode](https://x.com/opencode/status/2123106127030210786)｜~41k impressions, 1,198 likes
- What’s in it: Official post calls Hy4 flash “an unexpected hit” and says it remains exclusively free on OpenCode for the next 10 days
- Angle: Pair with last issue’s GLM 5.3 discount and write how to run the same repo through back-to-back cheap windows, instead of hopping models
- Timing & verification: Official wording is verified; region limits and whether it stacks with the earlier promo are unverified

### 2. Qwen4-Max aftershock: more platform listings, but the launch itself is outside this window

- Source & heat: [Alibaba_Qwen](https://x.com/Alibaba_Qwen/status/2122888191950901534)｜~42k impressions; [Alibaba_Qwen](https://x.com/Alibaba_Qwen/status/2122958542982508901)｜~24k impressions
- What’s in it: Qwen4-Max formally launched on Nov 16; this window is mostly distribution posts (Runware, TokenHarbor). Some Chinese recaps still mix the preview sunset date with GA pricing
- Angle: Don’t treat it as today’s launch; it can be a short note on how a Chinese flagship lands on third-party agent platforms
- Timing & verification: Official account quote-posts verify the platform listings; specs and cost-cut figures are official author-claim from Nov 16 and were not re-checked this issue

### 3. Scattered talk of Qwen3.8-27B coding-agent adapters

- Source & heat: English-language recap threads on RL + adapters for Qwen3.8-27B as a coding agent; some Chinese posts use that to contrast closed Qwen4-Max with smaller open builds. Heat is fragmented
- What’s in it: Keep the mid-size open models and the closed flagship on separate lines, instead of one “Alibaba shipped another model” headline
- Angle: Useful color, not a lead, unless you can point to a specific repo and eval setup
- Timing & verification: Mostly second-hand roundups, unverified until the original repos are checked
