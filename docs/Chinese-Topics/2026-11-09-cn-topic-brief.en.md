---
title: 2026-11-09-X Chinese Topics Brief
headline: DeepSeek Harness 1.54M DAU · 89% of open spend to Chinese models · Arete
type: x-cn-topic-brief
date: 2026-11-09
tags: [x-cn-topic-brief, ai, deepseek-harness, menlo-ventures, kimi, arete-27b, qwen, harness-leaderboard, bla]
source: x.com + menlovc.com/perspective/2026-the-state-of-enterprise-ai / nousresearch.com/arete / huggingface.co/spaces/joelniklaus/harness-leaderboard
window: 2026-11-07 08:00 to 2026-11-09 08:00 Asia/Shanghai
generated: 2026-11-09T08:30:00+08:00
coverage: partial
---
# X Chinese Topics Brief (2026-11-09)

Topic list for Chinese-language writers. Weekend conversation in the Chinese AI community centered on how big domestic agent platforms have become and how the West uses, and modifies, Chinese open models. Nov 8 items (Qwen 4 teaser, Qoduck, MaxxBench, Claude memory) are not reopened.

## Today's must-reads

1. **DeepSeek Harness hits 1.54M DAU** (Daily #2). The official article gives DAU, daily tokens, plugin counts and a plugin-author program. Good for an "agent OS where everything is a plugin" piece. Status: draftable; verified, DAU limited to official-API users.

2. **89% of US enterprise open-model spend goes to Chinese models.** Menlo Ventures' Nov 3 report went viral in Chinese circles this weekend: Kimi 61%, DeepSeek 15%, GLM 11%, Qwen 3%, Llama 7%. But open source is only ~4% of model spend and ~19% of tokens. Angle: "winning usage, not yet the money." Status: draftable; report verified, shares are survey estimates.

3. **Arete-27B fine-tunes the party line out of Qwen** (Daily #3). Pair with #2: Chinese models became the West's open base, and also a thing to be reworked. Status: draftable; Nous-built eval, attribute clearly and keep the tone neutral.

## More topics

### 1. DeepSeek Harness plugin ecosystem

- Source & heat: [DeepSeekHarness](https://x.com/DeepSeekHarness/status/2119431663642153128), ~314K views, 3,892 likes, 1,709 bookmarks; early Chinese recap [leo114119](https://x.com/leo114119/status/2118353985317032366), ~5.6K
- What and why: v0.1 Aug 13, desktop Sep 29; 1.54M DAU, ~92T tokens/day; 35K plugins, ~60% of active users use them; official marketplace in progress
- Angle: Profile the Chinese plugin authors the article names (creator workbench, design, context viewer, paper reading)
- Timing & verification: verified; support-program terms not yet published

### 2. Menlo report: open-model spend

- Source & heat: recaps by [Frontier_Now_26](https://x.com/Frontier_Now_26/status/2119336437888008365), [meishengsimon](https://x.com/meishengsimon/status/2119429761764081728) and others, low per-post heat but widely repeated; original at [menlovc.com](https://menlovc.com/perspective/2026-the-state-of-enterprise-ai/)
- What and why: survey of ~400 US enterprise decision-makers (Sep 8–26); Anthropic holds 55% of enterprise LLM API spend
- Angle: the pricing logic behind "19% of tokens, 4% of spend"
- Timing & verification: verified (report); per-model shares are estimates, not audited; Menlo discloses it invests in Anthropic

### 3. Picking a harness: Niklaus leaderboard + Garry Tan

- Source & heat: [joelniklaus](https://x.com/joelniklaus/status/2118373808692437403), ~315K; Chinese recap [heitieya](https://x.com/heitieya/status/2119295228830248976), ~735; [garrytan](https://x.com/garrytan/status/2119492448200405110), ~55K
- What and why: on open models the wrapper gap is 24 points (mini-swe-agent 51.4% vs OpenClaw 27.3%); Hermes Agent is best on DeepSeek-V4.1-Flash, Kimi Code on Flint; on frontier closed models all 7 setups land at 71–79%
- Angle: a practical "which harness for Chinese open models" post
- Timing & verification: author-claim

### 4. BLA: anti-AI reverse-engineering tool from a Chinese developer

- Source & heat: [xteam3301](https://x.com/xteam3301/status/2119409257628246441); [xqliu](https://x.com/xqliu/status/2119394753355895093), ~450
- What and why: decoy keys and resource traps make reverse-engineering agents waste tokens; CLI and MCP
- Angle: indie developer plus AI offense/defense tool write-up
- Timing & verification: author-claim; effect numbers self-reported

### 5. "IP, PLEASE": a Claude-made game about catching people using Claude from China

- Source & heat: [feishutoday](https://x.com/feishutoday/status/2119545717572391286), ~380
- What and why: a *Papers, Please* parody satirizing Anthropic's restrictions on Chinese users
- Angle: light weekend item
- Timing & verification: unverified (author and link not independently checked); low heat, backup only
