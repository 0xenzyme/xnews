---
title: 2026-11-23-X English Topics Brief
headline: OpenAI perplexity curve · open medical model · DNI on chips
type: x-en-topic-brief
date: 2026-11-23
tags: [x-en-topic-brief, ai, openai, pachocki, perplexity, lingsante, sarvam, riemann-hypothesis, nielsen, nvidia, clayton, chatgpt, tesla, sweeney, lecun]
source: x.com + openai.com / huggingface.co / riemannhypothesisclaude.org / Semafor
window: 2026-11-22 08:00 to 2026-11-23 08:00 (Asia/Shanghai)
generated: 2026-11-23T08:30:00+08:00
coverage: partial
---
# X English Topics Brief (2026-11-23)

English-language discussion on Sunday ran on safety and policy: Altman called Pachocki's perplexity essay "the most important thing OpenAI has published in awhile," and Clayton said controlled chips reached China. Open-source news was Ant's medical model and India's new 105B checkpoint. The Lean certification of the Riemann proof was not moved by Nielsen's paper; the factoring rumor should not be followed.

## Today's must-reads

1. **Pachocki's "Perplexity and Intelligence": internal log-perplexity published, industry "common limits" proposed** (see Daily §1). English X treated this as a safety-policy signal, not a research note. Key figures: GPT-3.5 ~0.99, GPT-4 ~0.91, recent models below 0.8, math breakthroughs at ~0.76, a 0.68–0.7 window ahead, and a possible pretraining-research "avalanche" as soon as 2027. Angle: without a shared dataset, how do you compare a limit? Status: ready; verified.

2. **DNI Clayton confirms China "had access" to export-controlled Nvidia chips** (see Daily §3). English discussion got noisy ("most expensive sex since Helen of Troy"); a piece should go back to the quote: "based on the facts alleged in the indictment." The same day Bessent recast "sales to the Chinese military" as "companies that do business with the Chinese military." Status: ready; quotes verified, Blackwell counts unverified.

3. **LingSante-3.1-flash and Sarvam-105B-1711 ship the same day** (see Daily §2). English builders will care about licenses, self-host cost, and whether official benches reproduce. One is a 560B MIT medical model; the other is a 105B Flash-Lite that fits one workstation GPU. Status: ready; weights verified, scores author-claim.

4. **Riemann follow-ups: reconstructions appear; Nielsen's "invalid" paper and a factoring rumor** (see Daily §1). English X mixed Nielsen's paper with P=NP talk. Keep them apart: the Lean certification still stands; the reconstructions are unfinished; the factoring claim was posted with "an entire shaker of salt." Yann LeCun's comment is a useful line: math is a domain where proofs can be checked automatically, which is not "general superintelligence." Status: ready; reconstructions verified, Nielsen and the rumor unverified.

## More topics

### 1. ChatGPT desktop lands 500+ performance PRs in a week

- Source & heat: [@feedthejim](https://x.com/feedthejim/status/2124603578019086484) | ~70K views, 727 likes
- What & why: Cold threads open 80% faster and downloads shrink; the author credits Astra for the speedup.
- Angle: A case of coding agents doing perf engineering, not a product launch.
- Timing & verification: employee's personal post, author-claim.

### 2. Tim Sweeney on Tesla's real-time AI video: first practical case of a world model "running circles around" engines

- Source & heat: Elon's original post was in the prior window (Nov 21 22:35 UTC); [@TimSweeneyEpic's reply](https://x.com/TimSweeneyEpic/status/2124550082943197455) is in this one | ~182K views, 3,689 likes
- What & why: Sweeney calls it the first real-world (not demo) case of a world model outrunning engines, and predicts the two will keep leapfrogging.
- Angle: How game engines and world models will share the work; not "engines are dead."
- Timing & verification: Sweeney's personal judgment, author-claim.

### 3. Anthropic's tool-use patterns keep spreading: one user cut MCP upfront tokens from 118K to 2,400

- Source & heat: [@0xwhrrari](https://x.com/0xwhrrari/status/2124493122549715437) | ~28K views, 283 likes, 445 bookmarks; [@0xKiyoro](https://x.com/0xKiyoro/status/2124479300241952781) | 4,856 views, 49 likes
- What & why: Not a new paper; a second wave of "tool search / deferred loading / write code in a sandbox." Users report a 98% token cut on the same tasks.
- Angle: A practice checklist, after checking the original paper's date so this is not written as "released today."
- Timing & verification: individual results unverified; the patterns themselves come from Anthropic's published engineering notes.
