---
title: 2026-11-24-X Chinese Topics Brief
headline: Jensen reinstated · GLM-5.4 loop architecture · Claude proves VP≠VNP
type: x-cn-topic-brief
date: 2026-11-24
tags: [x-cn-topic-brief, ai, nvidia, jensen-huang, megaspeed, zhipu, glm-5.4, loop-transformer, claude, vp-vnp, deepmind, quantum, qoder, hungerg, memos, claude-ship]
source: x.com + nvidianews.nvidia.com / CNBC / Semafor / z.ai / github.com/anthropics/formal-math / deepmind.google
window: 2026-11-23 08:00 to 2026-11-24 08:00 (Asia/Shanghai)
generated: 2026-11-24T08:40:00+08:00
coverage: partial
---
# X Chinese Topics Brief (2026-11-24)

Chinese-language X ran on three threads today: Jensen Huang's reinstatement and the market surge (lots of "TV-drama plot" jokes), Zhipu's GLM-5.4 loop architecture and hands-on tests, and Claude's VP ≠ VNP proof three days after Riemann. Qoder's anonymous "stealth model" HungerG is a good short piece.

## Today's must-reads

1. **Nvidia reinstates Jensen Huang, stock closes up 31%; Megaspeed blacklisted the same day** (see Daily §1). Chinese angle: the board cites "input from senior levels of the US government," Trump says he got involved, and the Southeast Asian transshipper is blacklisted the same day. Frame it as "the man is back, the channel is closed" — the effect on Chinese access to GPUs matters more than the stock. Status: ready; reinstatement, move and listing verified.

2. **Zhipu GLM-5.4: a 750B Loop Transformer running 28 layers twice** (see Daily §3). Chinese angle: a Chinese lab takes looped transformers to flagship scale by retrofitting an existing base; the KV design (one extra sliding window per loop) is the technical highlight. Chinese hands-on posts say "strong but slow" — voxel scenes and the pelican test take over an hour. Coding Plan only; no API or weights. Status: ready; architecture verified, benchmarks author-claim.

3. **Claude-authored VP ≠ VNP proof lands in Anthropic's official repo** (see Daily §2). Chinese angle: explain "algebraic P vs NP," why it does not solve P vs NP, and what "passes Lean but no human review" means. Chinese reposts already say "47-year mystery cracked"; keep it measured. Status: ready; repo contents verified, theorem author-claim.

4. **DeepMind agent teams optimize quantum algorithms** (see Daily §2). Chinese angle: most Chinese posts use the correct "nearly 10×" framing, but some treat arcsin's 290× as the headline. Pair with the Claude proof for an "AI + Lean science" piece. Status: ready; verified.

## More topics

### 1. Qoder launches anonymous "stealth model" HungerG, free Nov 23–30

- Source & heat: [@qoder_ai_ide](https://x.com/qoder_ai_ide/status/2124899980632822148) | ~1.22M views, 623 likes; [@aitrackerbot pelican / black-hole tests](https://x.com/aitrackerbot/status/2124954200119631970) | 31 likes
- What and why: Qoder (Alibaba's AI IDE) added a model codenamed HungerG with undisclosed identity, free for 7 days on Qoder and Qoder IDE, inviting users to guess who built it.
- Angle: Stealth models are often pre-launch tests; track the guesses, but do not name a vendor without evidence.
- Timing & verification: Launch verified (official post); identity unknown — any guess is unverified.

### 2. MemOS ships 554B memory-native MemT-1.0-Pro

- Source & heat: [@MemOS_dev](https://x.com/MemOS_dev/status/2124623963087126562) | ~1.25M views, 2,838 likes, 3,126 bookmarks
- What and why: Built with Nvidia on Nemotron 3 Ultra; memory written into fixed-size parameter blocks.
- Angle: "Memory inside the model" vs RAG vs long context is a live question for agent builders.
- Timing & verification: Launch verified; weights and scores not checked against the model card — author-claim.

### 3. Worry that Qwen core staff left and Qwen4 may not be open-weight

- Source & heat: [@MiaoHype](https://x.com/MiaoHype/status/2125017050128994498) | 61 views, 2 likes
- What and why: A Chinese user fears Qwen4 will not ship open weights after core staff departures.
- Angle: Would be big for China's open-source ecosystem if officially sourced.
- Timing & verification: No reliable source found — unverified; very low heat, not drafting.

### 4. Claude Ship and Claude Plugins

- Source & heat: [@ClaudeDevs](https://x.com/ClaudeDevs/status/2124959436640858475) | ~1.19M views, 13.8K likes; [@claudeai Plugins](https://x.com/claudeai/status/2124970294523945328) | 4,480 likes
- What and why: Automated PR review, fixes and policy-based approval; connectors and skills merged into plugins.
- Angle: Chinese developers who point Claude Code at domestic models (e.g. GLM-5.4) will want to know whether /ship works with third-party models — worth a hands-on test.
- Timing & verification: Verified (official article).
