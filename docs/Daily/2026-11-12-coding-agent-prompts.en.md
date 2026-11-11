---
title: 2026-11-12-Coding Agent Prompt Collection
headline: Agent prompt collection · implicit state machines · unslop
type: x-news-daily
date: 2026-11-12
tags: [x-daily, ai, coding-agents, prompts, state-machines, unslop, cleanup, home-repo]
source: x.com + github.com/dzhng/skills + github.com/heydamir/unslop + github.com/shadcn/improve
window: 2026-10-30 to 2026-11-11 (special collection, not the regular daily window)
generated: 2026-11-12T06:01:00+08:00
coverage: special
---

# Coding Agent Prompt Collection (2026-11-12)

This is a special issue of AI Daily Picks, not the regular daily brief. Over the past two weeks, a cluster of copy-paste workflows and cleanup prompts spread on X: the Home Repo, implicit state machines, subtracting dead weight with `/goal`, and stripping the AI look from pages and codebases. The entries below keep the **original post text or the copy-ready prompt**, with the author, a link to the source post, and the public metrics as fetched. Prompts are not paraphrased. Where a post used a shortened URL, the expanded address is noted in the surrounding text.

## How to use this issue

- Prompts meant for pasting sit in code blocks.
- Engagement figures are the public metrics at fetch time, not the rounded numbers from secondary write-ups.
- Whether a prompt actually finds bugs or deletes the right code is marked author-claim; that the original post exists is verified.

## 1. Matt Pocock's Home Repo

Author [@mattpocockuk](https://x.com/mattpocockuk/status/2120260969750540327) (Matt Pocock), 2026-11-11 05:03 (Taipei time).

- What happened: He keeps skills, steering files, and a wiki in one "Home Repo," starts agents only there, and puts pointers in `AGENTS.md` so the agent can clone or edit other repos when needed.
- Source & engagement: [original post](https://x.com/mattpocockuk/status/2120260969750540327), 4,190 bookmarks, 2,883 likes, 154 reposts, 270 replies, 61 quotes, 211,546 impressions.
- Verification: full text verified. Effectiveness is author-claim.

Original text (including the `AGENTS.md` example pointers):

~~~~text
A lot of folks ask me "how do you work with agents in multiple repos at once?"

I have a very simple solution - the Home Repo

I have a single repo (the home) where all of my skills, steering files, wiki etc live.

I run my agent in the home repo, and then inside AGENTS.md I have pointers to the other repos:

```
For skills, clone mattpocock/skills to ~/repos/skills.
For Sandcastle, clone mattpocock/sandcastle to ~/repos/sandcastle
```

This is extremely simple and incredibly effective. The home repo lets you:

1. Put all your steering files and tooling in one place
2. Have a single spot to run all your agents in
3. Make sweeping changes over multiple repos

Talked about this in the course yesterday and folks are loving it (see below).

I'm sure you will too. Enjoy!
~~~~

The `AGENTS.md` snippet on its own:

```text
For skills, clone mattpocock/skills to ~/repos/skills.
For Sandcastle, clone mattpocock/sandcastle to ~/repos/sandcastle
```

## 2. Implicit state machines

The thread starts with [@steveruizok](https://x.com/steveruizok/status/2116552016218710389) on 2026-10-31. Later posts added UX/DX/AX constraints, a longer version that documents machines and fixes illegal states with regression tests, an explanation of why tests can still pass, and a variant that hunts implicit design-system components.

### Source: @steveruizok

Author [@steveruizok](https://x.com/steveruizok/status/2116552016218710389) (Steve Ruiz), 2026-10-31 23:24 (Taipei time).

- Source & engagement: [original post](https://x.com/steveruizok/status/2116552016218710389), 15,806 bookmarks, 8,480 likes, 398 reposts, 167 replies, 291 quotes, 2,170,348 impressions.
- Verification: original text verified.

```text
good prompt "find all of the implicit state machines in my app"
```

Copy-ready prompt:

```text
find all of the implicit state machines in my app
```

### @Voxyz_ai: UX / DX / AX constraints

Author [@Voxyz_ai](https://x.com/Voxyz_ai/status/2119444845890617507) (Vox), 2026-11-08 23:00 (Taipei time). The highest-engagement post in this series.

- Source & engagement: [original post](https://x.com/Voxyz_ai/status/2119444845890617507), 22,913 bookmarks, 9,515 likes, 443 reposts, 237 replies, 63 quotes, 1,229,664 impressions.
- Verification: original text verified. Results are author-claim.

```text
Vibecoders, 𝗜'𝗺 𝗯𝗲𝗴𝗴𝗶𝗻𝗴 𝘆𝗼𝘂, open your messiest project and paste this into Claude Code or Codex:

"Find all of the implicit state machines in my app. Make the best decision that will elevate all three: the user experience (UX), developer experience (DX), and agent experience (AX) always, without breaking anything."
```

Copy-ready prompt:

```text
Find all of the implicit state machines in my app. Make the best decision that will elevate all three: the user experience (UX), developer experience (DX), and agent experience (AX) always, without breaking anything.
```

### @trevin: document machines, find illegal states, fix them, add regression tests

Author [@trevin](https://x.com/trevin/status/2118690987153186845) (Trevin Chow), 2026-11-06 21:04 (Taipei time). Quotes Steve's original post.

- Source & engagement: [original post](https://x.com/trevin/status/2118690987153186845), 4,469 bookmarks, 2,654 likes, 100 reposts, 32 replies, 11 quotes, 111,378 impressions.
- Verification: original text verified. "Helps find a ton of bugs for me" is author-claim.

```text
This is an amazing prompt that helps find a ton of bugs for me. 

“Find the app’s explicit and implicit state machines and document their states, invariants, and transition tables in one file. Identify invalid states or transitions the code can actually reach, with evidence, including through retries and concurrency. Prioritize confirmed bugs by impact, group related fixes into issues, then fix them with regression tests and keep the document updated.”
```

Copy-ready prompt:

```text
Find the app’s explicit and implicit state machines and document their states, invariants, and transition tables in one file. Identify invalid states or transitions the code can actually reach, with evidence, including through retries and concurrency. Prioritize confirmed bugs by impact, group related fixes into issues, then fix them with regression tests and keep the document updated.
```

### @DavidKPiano: why tests can pass and bugs remain

Author [@DavidKPiano](https://x.com/DavidKPiano/status/2119788094434038264) (David K), 2026-11-09 21:44 (Taipei time). This is an explanation, not a paste-ready prompt: when the logic is scattered, illegal states can still be reachable, and both tests and code-review agents can still say LGTM.

- Source & engagement: [original post](https://x.com/DavidKPiano/status/2119788094434038264), 1,094 bookmarks, 1,331 likes, 82 reposts, 54 replies, 20 quotes, 118,375 impressions.
- Verification: original text verified. The FaceTime reference and the claim that "very bad bugs" can remain are author-claim.

```text
What is an implicit state machine? 

Your apps are full of state machines, which is the logic that says "when we're in this state, and this event happens, now we're in this state" (given, when, then).

Sometimes those state machines are clearly mapped out (switch statements, reducers, tables/maps, libraries like XState for the more complex ones, etc.) and the logic is explicitly enumerable.

And sometimes it's not. The ad-hoc logic is spread all over the place. That's how developers typically code, and that's how agents typically vibe-code (they learned from you). Those are implicit state machines.

What's wrong with implicit state machines? It's not clear what state transitions are possible, so you might have "allowed" states that should have been impossible without knowing it. Agents make the same mistakes. 

You can get all tests passing and your code review agents (even the well-funded ones) can say "LGTM" and you can *still* have very bad bugs because an implicit state machine allowed unexpected or illegal behavior. (Remember the Apple FaceTime bug?)

So yeah, making your app logic explicit is important.
```

### @rodydavis: implicit design-system components

Author [@rodydavis](https://x.com/rodydavis/status/2120402273029201934) (Rody Davis), 2026-11-11 14:24 (Taipei time). Quotes Steve's post and swaps "state machines" for "design system components."

- Source & engagement: [original post](https://x.com/rodydavis/status/2120402273029201934), 247 bookmarks, 268 likes, 7 reposts, 7 replies, 1 quote, 10,814 impressions.
- Verification: original text verified.

```text
good prompt “find all of the implicit design system components in my app”
```

Copy-ready prompt:

```text
find all of the implicit design system components in my app
```

## 3. Subtract / delete dead code

### @Voxyz_ai: a five-prompt /goal cleanup thread

Author [@Voxyz_ai](https://x.com/Voxyz_ai/status/2118357672106029272) (Vox), 2026-11-05 23:00 (Taipei time). The parent post argues that leftover quota at reset is wasted Astra and Sol time, and that `/goal` can clear dead code, duplicated logic, unused dependencies, idle scheduled tasks, and old sessions or worktrees. The five replies below are the full original texts. Each one says to work on a new branch and not to push or merge.

- Source & engagement: [parent post](https://x.com/Voxyz_ai/status/2118357672106029272), 3,882 bookmarks, 1,672 likes, 92 reposts, 62 replies, 8 quotes, 259,449 impressions. Reply-level metrics are listed with each prompt.
- Verification: all five full texts verified. Cleanup results are author-claim.

**Parent post:**

```text
𝗖𝗼𝗱𝗲𝘅 𝘁𝗶𝗽: if you still have half your quota left when it resets, you’re throwing away days of Astra and Sol.

Use `/goal` to squeeze every last bit out of it and clean out what months of vibe coding piled up: dead code nothing calls, the same logic written several times over, dependencies you don’t need, old sessions and worktrees hogging your disk, or even scheduled tasks that have been running for nothing.

Here are 5 prompts and goals you can copy-paste directly. ↓
```

**1/5 Delete dead code** ([post](https://x.com/Voxyz_ai/status/2118357672550683020), 138 bookmarks, 82 likes, 21,461 impressions):

```text
1/5 Delete dead code

/goal Find the code in this repo that nothing uses anymore, and prove it's really unused before you delete it.

→ Functions, classes, components and exports that nothing calls
→ Files and directories that no entry point references
→ Branches that can never run, feature flags hard-coded off, and whole blocks of commented-out code

For each one, show the evidence first: the repo-wide search results, whether it's reachable from an entry point, and whether any test uses it. Anything you're unsure about (dynamic imports, calls by string name, public APIs) goes on a separate list and stays.

Delete on a new branch. Run the tests and the build after each batch, and if anything breaks, restore that batch. Don't push, and don't merge the branch.

At the end, give me:
→ How many files and lines you deleted
→ What you kept, and why
→ The test and build results
```

**2/5 Merge duplicate implementations** ([post](https://x.com/Voxyz_ai/status/2118357673070776644), 60 bookmarks, 41 likes, 18,141 impressions):

```text
2/5 Merge duplicate implementations

/goal Find the places in this repo where the same thing is written several times, and merge each into one.

→ Functions and helpers with different names that do the same job
→ Near-identical components, request wrappers and validation logic
→ Code that was copy-pasted and then tweaked a little in each place

For each group, say which version you're keeping and why, then point every other call site at it. Only merge code that behaves exactly the same. List anything with small differences and show it to me at the end.

Work on a new branch and run the tests after each group. Don't push, and don't merge the branch.

At the end, give me:
→ How many groups you merged, and how many lines that saved
→ The ones with differences that you didn't merge
→ The test results
```

**3/5 Remove dependencies you don't need** ([post](https://x.com/Voxyz_ai/status/2118357673632797142), 53 bookmarks, 31 likes, 15,968 impressions):

```text
3/5 Remove dependencies you don't need

/goal Check every dependency this project installs and remove the ones it doesn't need.

→ Installed but never used in the code
→ Used for one or two small features you could write yourself in a few dozen lines
→ Two libraries doing the same job

Delete the unused ones outright. For the ones you can write yourself, write the replacement and add tests first, then remove the dependency. Where two do the same job, keep one and move every call over to it. List any big dependency you're unsure about and let me decide at the end.

Work on a new branch and run the tests and the build after each change. Don't push, and don't merge the branch.

At the end, give me:
→ Which dependencies you removed, and how much smaller the install got
→ What you wrote yourself, and how many lines each
→ What you kept, and why
```

**4/5 Shut off scheduled tasks that run for nothing** ([post](https://x.com/Voxyz_ai/status/2118357674106700164), 42 bookmarks, 28 likes, 14,151 impressions). This one is read-only and says not to change any settings:

```text
4/5 Shut off scheduled tasks that run for nothing

/goal List every scheduled task I've set up: cron and launchd jobs on this machine, scheduled workflows in CI, and scripts in the project that run on a timer.

For each one, write down:
→ What it does and how often it runs
→ How many times it ran in the last month, and how many times it failed
→ Whether anyone actually uses what it produces
→ Whether it overlaps with another task

Sort them into "keep", "change how often" and "turn off". Don't change any settings. At the end, give me the list and how to turn each one off.
```

**5/5 Clear out old sessions and worktrees** ([post](https://x.com/Voxyz_ai/status/2118357674677166497), 110 bookmarks, 47 likes, 12,567 impressions). Also tells the agent not to delete anything, only to write a script for review:

```text
5/5 Clear out old sessions and worktrees

On Claude Code desktop, /storage shows how much disk it's using and lets you clear out inactive tasks and unused worktrees. For Codex, use this:

/goal Do a read-only scan of ~/.codex and this project's worktrees. Look at sizes only and don't open any file contents.

→ Old session logs, with sizes totaled by month
→ Worktrees that are already merged or no longer in use, and whether their branches have unpushed changes
→ Build output and caches that regenerate on their own after you delete them

Sort them into "safe to remove" and "let me review first". Any worktree with unpushed changes always goes under "let me review first". Don't delete anything. Write a cleanup script for the "safe to remove" group only, and I'll review it before I run it. In the script, remove worktrees with git worktree remove.

At the end, tell me how much space this would free up in total.
```

### @Voxyz_ai: "Fewer, deeper modules, smaller interfaces"

Author [@Voxyz_ai](https://x.com/Voxyz_ai/status/2119777023845417175) (Vox), 2026-11-09 21:00 (Taipei time). Quotes the UX/DX/AX post, then offers a five-word cleanup prompt and a longer block to paste after a feature works.

- Source & engagement: [original post](https://x.com/Voxyz_ai/status/2119777023845417175), 1,263 bookmarks, 691 likes, 19 reposts, 37 replies, 4 quotes, 49,753 impressions.
- Verification: original text verified. "Strongest cleanup prompt," falling line counts, and smarter abstractions are author-claim.

```text
One more thing.

Highly recommend trying the 𝘀𝘁𝗿𝗼𝗻𝗴𝗲𝘀𝘁 𝗰𝗼𝗱𝗲 𝗰𝗹𝗲𝗮𝗻𝘂𝗽 𝗽𝗿𝗼𝗺𝗽𝘁 out there right now. It's only 5 words: "fewer, deeper modules, smaller interfaces"

The best part is 𝘄𝗮𝘁𝗰𝗵𝗶𝗻𝗴 𝘁𝗵𝗲 𝗹𝗶𝗻𝗲 𝗰𝗼𝘂𝗻𝘁 𝗱𝗿𝗼𝗽 as all the duplicate code gets wiped out and the core logic lands in one place. The AI comes up with way smarter abstractions, fixes a pile of bugs along the way, and the whole codebase ends up fully consistent.

Every time you get a feature working, drop this whole block into Claude Code or Codex 👇

"Fewer, deeper modules, smaller interfaces. Check data once where it comes in, then just use it. Write one-off logic right where it's used instead of splitting it into a function ahead of time. Skip try/catch wherever you can."
```

Five-word version:

```text
fewer, deeper modules, smaller interfaces
```

Longer block:

```text
Fewer, deeper modules, smaller interfaces. Check data once where it comes in, then just use it. Write one-off logic right where it's used instead of splitting it into a function ahead of time. Skip try/catch wherever you can.
```

### @chenchengpro's five-prompt roundup, plus the originals

Author [@chenchengpro](https://x.com/chenchengpro/status/2120040764243894547) (陈成), 2026-11-10 14:28 (Taipei time). A five-prompt set with named sources. The roundup is quoted first, then the source posts we found. Wording and punctuation sometimes differ from the roundup; **prefer the original authors' posts when copying**.

- Source & engagement: [original post](https://x.com/chenchengpro/status/2120040764243894547), 1,810 bookmarks, 1,117 likes, 61 reposts, 17 replies, 2 quotes, 66,647 impressions.
- Verification: the roundup text is verified. Source-level checks follow.

**Roundup text** (the shortened link in item 5 is expanded to https://github.com/shadcn/improve):

```text
Prompts to use with Fable 5.2 to improve your codebase.

1/ Full health check. from Alex Albert，Anthropic

Read this entire project and find everything that's broken, inconsistent, inefficient, or no longer needed. Fix what you're sure about and list the rest for me to review.

2/ Simplify by cutting the superfluous. from Anthony Riera

I want you to audit our codebase, is anything here unnecessary, overly complicated in our
current setup, or based on weak assumptions? Challenge them. #1 What can be deleted entirely? #2 What can be simplified now that unnecessary pieces are gone? Then make the changes. Prefer deleting over simplifying, simplifying over optimizing, and optimizing over automating. This product is being used by thousands of customers, do not cut any corners.

3/ Find the implicit state machine. from Steve Ruiz and Kun Chen and RicardoSawir

audit and find implicit state machines in this <codebase/directory/module> that would drive
concrete improvements if made explicit. fewer words, big visuals

or with consider for UX/DX/AX.

Find all of the implicit state machines in my app (there are probably a ton). Make the best decision that will elevate all three: the user experience (UX), developer experience (DX), and agent experience (AX) always, without breaking anything. Also, make state machines explicit.

4/ Review agent configuration. from WquGuru & Vox

Review my entire agent setup: AGENTS.md, CLAUDE.md, skills, commands, subagents, hooks, settings/permissions, and MCP servers. Check for gaps in guardrails and whether it follows current best practices for Fable 5.2.

5/ shadcn/improve

run https://github.com/shadcn/improve for my codebase.
```

**1/ Original: [@alexalbert__](https://x.com/alexalbert__/status/2119884951550386671)** (Alex Albert, Anthropic), 2026-11-10 04:08 (Taipei time). 18,675 bookmarks, 9,888 likes, 518 reposts, 342 replies, 214 quotes, 1,118,848 impressions. The API returned no extended note; the visible text ends at the ~280-character limit with "highly recommend trying." The quoted prompt itself is complete. The original uses typographic apostrophes (that’s / you’re), unlike the straight quotes in the roundup.

```text
Every time we have a new model, I run the same simple prompt on all my projects:

"Read this entire project and find everything that’s broken, inconsistent, inefficient, or no longer needed. Fix what you’re sure about and list the rest for me to review."

highly recommend trying
```

**2/ Original: [@anthonyriera](https://x.com/anthonyriera/status/2119870644514893997)** (Anthony Riera), 2026-11-10 03:12 (Taipei time). 2,576 bookmarks, 1,398 likes, 45 reposts, 24 replies, 2 quotes, 100,828 impressions. The source uses two dashed questions, not the roundup's "#1 / #2."

```text
I want you to audit our codebase, is anything here unnecessary, overly complicated in our current setup, or based on weak assumptions? Challenge them. 

- What can be deleted entirely?
- What can be simplified now that unnecessary pieces are gone?

Then make the changes. Prefer deleting over simplifying, simplifying over optimizing, and optimizing over automating.

This product is being used by thousands of customers, do not cut any corners.
```

**3/ Further originals.** Steve's source is in section 2. [@kunchenguid](https://x.com/kunchenguid/status/2119924895060795492) (Kun Chen), 2026-11-10 06:47 (Taipei time), posted the "fewer words, big visuals" wording: 1,962 bookmarks, 918 likes, 40 reposts, 17 replies, 9 quotes, 64,809 impressions; he also mentions optional [lavish-axi](https://github.com/kunchenguid/lavish-axi). [@RicardoSawir](https://x.com/RicardoSawir/status/2119891925671305268) (Ricardo Sawir), 2026-11-10 04:36 (Taipei time), replied to Alex Albert with the UX/DX/AX version plus "Also, make state machines explicit" (5 bookmarks, 4 likes, 1,937 impressions). Vox's earlier UX/DX/AX post is in section 2; Ricardo's reply adds the "make explicit" clause after it.

Kun Chen's prompt:

```text
audit and find implicit state machines in this <codebase/directory/module> that would drive concrete improvements if made explicit. explain before/after of each one and discuss with me in lavish-axi. fewer words, big visuals
```

Ricardo Sawir's prompt:

```text
Find all of the implicit state machines in my app (there are probably a ton). Make the best decision that will elevate all three: the user experience (UX), developer experience (DX), and agent experience (AX) always, without breaking anything. Also, make state machines explicit.
```

**4/ Original: [@wquguru](https://x.com/wquguru/status/2119962410056642797)** (WquGuru), 2026-11-10 09:16 (Taipei time). 45 bookmarks, 48 likes, 6 reposts, 6 replies, 5,469 impressions. The roundup also credits "WquGuru & Vox." WquGuru's wording matches; we did not find a @Voxyz_ai post with this same prompt, so Vox as a co-source is unverified.

```text
Review my entire agent setup: AGENTS.md, CLAUDE.md, skills, commands, subagents, hooks, settings/permissions, and MCP servers.

Check for gaps in guardrails and whether it follows current best practices for Fable 5.2.
```

**5/ [shadcn/improve](https://github.com/shadcn/improve)** (MIT © shadcn; about 10,782 stars at fetch). The roundup's usage line is:

```text
run https://github.com/shadcn/improve for my codebase.
```

The repo's idea: use a stronger model to audit and write plans, and hand execution to cheaper models. The skill itself does not change application code; plans land in `plans/`. Install with `npx skills add shadcn/improve`. Common entry points are `/improve`, `/improve quick`, and `/improve deep`. See the README for the full documentation; this page does not reproduce it in full.

## 4. Strip the AI look

### @alex_prompter's structured unslop prompt

Author [@alex_prompter](https://x.com/alex_prompter/status/2119010352272998434) (Alex Prompter), 2026-11-07 18:13 (Taipei time).

- What happened: He adapted Damir Sokolovsky's open-source unslop skill into a prompt you can paste into Claude Code, aimed at pages that already have features and users. It changes craft only (styling and approved copy), then runs two fresh subagents as judge and guard.
- Source & engagement: [original post](https://x.com/alex_prompter/status/2119010352272998434), 534 bookmarks, 198 likes, 19 reposts, 23 replies, 28,661 impressions.
- Verification: full prompt verified. The 1.9 million views and "5,500 GitHub stars" figures are the author's claims at the time of writing. Separately, Damir's repo [heydamir/unslop](https://github.com/heydamir/unslop) is licensed CC BY 4.0 and had about 14,481 stars at fetch.
- License: the post ends with this attribution, kept verbatim as requested — **Adapted from unslop by Damir Sokolovsky, CC BY 4.0.** Damir's skill post: [heydamir, 2026-10-30 21:20 (Taipei time)](https://x.com/heydamir/status/2116158176336970008), 9,778 bookmarks, 5,221 likes, 240 reposts, 139 replies, 69 quotes, 642,663 impressions. Repo: https://github.com/heydamir/unslop.

Prompt text (replace `[PAGE: local dev URL]` with your local preview URL):

```text
<task>
Strip the AI look from [PAGE: local dev URL]. Change the craft only: features, behavior, facts and section order stay. No new sections or components.
</task>

<before>
Read-only until I approve. Use Chrome DevTools MCP. Leave any login to me and never read credentials.
- Save before shots outside the repo, emulating 1440x900 and 390x844, in screen-height pieces.
- Record the build and test results and lighthouse_audit accessibility failures on desktop and mobile.
</before>

<plan>
1. Slop list: number every sign of AI slop and where it shows: purple gradients, glows, gradient text, emoji labels, sparkle badges, wide-tracked caps, endless loops, drifting spacing. If the page is mostly fine, say so and fix only these.
2. Direction, three lines.
World: its setting or material.
Focus: 1-2 spots get rich color and detail, the rest stays quiet.
Signature: one small detail only this product would have.
Real brand colors, logos and fonts stay (a purple gradient isn't one).
3. Copy table, current vs proposed, tone only: exclamation marks, "Welcome back" greetings, hype words. No claim, number, price, name or legal line changes.
Show me all three, then stop and wait for my OK.
</plan>

<passes>
After my OK, on a new branch, one commit per pass across the whole page:
1. Spacing: 4px grid, same things same size
2. Color: one neutral scale tinted toward World, three text levels, one accent saved for Focus spots, no hue gradients or glows
3. Icons: the project's line icons replace emoji, one size and stroke
4. Copy: approved rows only
5. Type: weights 400 and 500, sentence case, the project's font
6. Layout: alignment and proportions inside sections only
7. Details: consistent radii, quiet badges, the Signature
8. Visuals: remove decorative filler, generate nothing
9. Motion: remove loops, transition-all, hover scale-ups
</passes>

<rules>
- Only styling and approved copy change. Anything else (logic, data, config, a new package or font) goes on an approval list, unbuilt.
- Theme files count as styling; name any other pages a change reaches.
- Keep every id, data- and aria- attribute. Never edit a test to pass it: copy-only breaks go on the approval list.
- Text stays at WCAG AA: 4.5:1, or 3:1 for large text. Every control keeps a visible focus state.
- Never push or merge.
</rules>

<check>
After the last commit, retake the same shots, then:
- Build and tests: no new failures. No tests? Click only the controls that can't write, send, delete or pay, and call that weaker proof.
- Rerun lighthouse_audit: no new failures. It can't score text over images or gradients, so list those as unchecked. Tab through to see focus states. Grep for motion items stills can't show.
- Judge, a fresh subagent, not a fork: gets only the before and after shots and slop list, edits nothing. Marks each item gone, still there or can't tell, citing the screenshot. Flags anything broken at phone width. Swap test: would this page still make sense with another company's name?
- Guard, same terms: gets only the rules above, approved copy rows and full branch diff. Lists every change that isn't styling or approved copy.
</check>

<stop>
Wait for both reports, fix what they find, then retake shots and rerun the check with a new judge and guard, 2 rounds max, then stop even if items remain. Failed swap test: push World and Signature, styling only. If frozen copy causes it, just report it.
</stop>

<output>
Final slop marks, test and Lighthouse results, approval list. End with what you need from me: merge, revert, or a call on each approval.
</output>

Adapted from unslop by Damir Sokolovsky, CC BY 4.0.
```

His [first reply](https://x.com/alex_prompter/status/2119010364436471877) adds browser-tool setup and points back to Damir's skill. t.co links below are expanded to full URLs:

```text
Add the browser tool before you start the session:

claude mcp add chrome-devtools --scope user npx chrome-devtools-mcp@latest

Google collects usage statistics from that tool by default and its README shows the flag to opt out, and Claude can see everything in the browser it opens, so keep it on dev data.

Commit your work first so the branch starts clean, then replace [PAGE] with your local dev URL, because the branch never gets pushed and a preview wouldn't show the edits. If you want source edits blocked until you approve, launch with claude --permission-mode plan. The two subagents may surface permission prompts in your main session.

Want the full rule set and the before and after video? Install Damir's skill, which goes further on design than this prompt. It adds one skill folder with instructions, reference files and two Node scripts and no hooks, the scripts only run for live-site snapshots and videos (they need Playwright and ffmpeg), and it asks before any paid image generation. Read it first, like any third-party install. The author's route is a plain clone and copy, which skips the Node 22.20 requirement and the telemetry:

git clone https://github.com/heydamir/unslop
mkdir -p ~/.claude/skills && cp -r unslop/skills/unslop ~/.claude/skills/

Or use the skills CLI, which needs Node 22.20 or later and sends anonymous telemetry unless you set DISABLE_TELEMETRY=1:

npx skills add heydamir/unslop -g -a claude-code

Sources:
https://github.com/heydamir/unslop
https://x.com/heydamir/status/2115063463063998736
https://x.com/heydamir/status/2116158176336970008
https://github.com/ChromeDevTools/chrome-devtools-mcp
https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html
```

### @dzhng: a de-slop skill distilled from sessions, meant to run overnight with /goal

Author [@dzhng](https://x.com/dzhng/status/2120297879046865279) (David Zhang), 2026-11-11 07:29 (Taipei time).

- What happened: He asked Fable 5.2 to read his session transcripts and distill principles for a refactor skill that de-slops a codebase, then suggested running it with `/goal` overnight. "One run a day keeps the slop away." The post links to https://github.com/dzhng/skills (about 1,500 stars at fetch). The matching file is [`skills/review/refactor-codebase/SKILL.md`](https://github.com/dzhng/skills/blob/main/skills/review/refactor-codebase/SKILL.md), added at 2026-11-11 05:13 (Taipei time), close to the post. The commit message says it was trimmed from Caldo's untangle-codebase (also MIT). There is no skill literally named `de-slop`.
- Source & engagement: [original post](https://x.com/dzhng/status/2120297879046865279), 196 bookmarks, 124 likes, 6 reposts, 18 replies, 8,440 impressions.
- Verification: the post and skill file are verified. Overnight results are author-claim.
- License: the repo is MIT License, Copyright (c) 2026 David Zhang. The skill is quoted in full below with the copyright and permission notice, as the license requires for substantial portions.

Original post:

```text
Asked Fable-5.2 to read through all my session transcripts and distill a set of principles for a refactor skill to de-slop any codebase

Use with /goal to work with large codebases and leave on overnight

One run a day keeps the slop away
```

Full `refactor-codebase` skill (MIT License, Copyright (c) 2026 David Zhang; Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files, to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, subject to the condition that the above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software. THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.):

~~~~markdown
---
name: refactor-codebase
description: Refactor a whole codebase in one run, tuned to clear the layered debt AI-written code piles up, so a typical change lands in one place. Worth running regularly.
disable-model-invocation: true
---

# Refactor Codebase

Refactor this whole codebase until a typical change lands in one place. Treat
this as a goal and run it to the end. If I named an area, start there.

Ask one question of everything: **should these pieces change together?** The
code gets the answer wrong in three ways:

- **Hidden links** — pieces that must change together, where nothing shows it:
 copied logic or values, a module reading state another module sets, one
 feature spread across folders by layer, a call order callers just have to
 know.
- **Needless links** — pieces tied together that change for different reasons:
 callers reaching into internals, stable code importing volatile code, a
 general function with a parameter only one caller understands, a shallow
 module whose interface changes whenever its internals do.
- **Surplus** — pieces with no reason of their own to change: pass-through
 wrappers, extension points and config for things that never vary, dead code.

## Workflow

1. **List every problem before changing anything.** Go through the whole
 codebase and write down each place it gets the question wrong. List every
 **special case** too: an `if` for one value, a parameter for one caller, a
 swallowed exception, a retry or sleep, a disabled test. Each one is a
 requirement the design never accounted for. Have subagents run the
 specialist hunts and add what they report, changing nothing yet:
 [find-state-machines](../find-state-machines/SKILL.md) for one lifecycle
 spread across flags, effects and callbacks,
 [find-overengineering](../find-overengineering/SKILL.md) for guards and
 fallbacks nothing needs, and [ratchet-files](../ratchet-files/SKILL.md)
 for files too big to read whole. To reason across all of it at
 once, script a skeleton with the function bodies stripped and a graph of
 what imports what, and use git history as evidence of what really changes
 together. Keep the list in a file so it survives compaction.
2. **Redesign from the list.** Work out the system as if it had known today's
 requirements from the start. Look for the one fix behind several problems;
 it often looks nothing like them. Never patch special cases one by one.
 Write each fix above the problems it removes:

   ```md
   - Make `Dialog` give focus back to whatever had it before it opened.
     - `LogoutDialog` waits 100ms after closing and hopes the input can take focus.
     - `SettingsDialog` sets a global `skipRefocus` flag to stop that refocus.
   - Make every user action one command with a name, a handler and an undo.
     - Toolbar and menu call the same actions, each with its own disabled check.
     - The keymap has a switch with one case per action.
     - The command palette keeps its own action list, missing the newer ones.
     - Undo has a special case for every action.
   ```

 Each fix is one mechanism that lands as one commit. Land nothing until the
 list is only fixes: every problem and special case sits under the fix that
 removes it, or under Kept with the reason the system still needs it.
3. **Land one fix at a time,** each time the one that removes the most of what
 is left; it often makes smaller ones moot. Follow
 [refactor-change](../refactor-change/SKILL.md) for each, then audit its
 diff with [code-review](../code-review/SKILL.md) and fix what it finds.
 Commit each fix on its own with the project's checks passing, and name any
 behavior it changes in the commit message, so a behavior change traces to
 one fix. Tests are the safety net here, so leave them alone until step 5.
4. **Search again.** Have fresh subagents hunt for hidden links, needless
 links, surplus and special cases, rerun the specialist hunts, and return to
 step 1 with what they find.
5. **Audit the tests.** Once the search comes back empty, run
 [audit-tests](../audit-tests/SKILL.md) over the suites the refactor
 touched, and land what it finds the same way.

Done when subagents find nothing worth fixing, a typical change lands in one
place, nothing imports anything more volatile than itself, every test earns
its keep, and behavior is the same as when you started, apart from bugs the
refactor fixed. The number of
special cases left is the best measure of how close you are.
~~~~

## Verification and licenses

- All 11 featured items (including every reply in Vox's five-part `/goal` thread) plus the source posts by Alex Albert, Anthony Riera, Kun Chen, Ricardo Sawir, WquGuru, and Damir Sokolovsky were retrieved from the X API and are marked verified.
- Whether the prompts find bugs, delete the right code, or remove the AI look, and the view/star counts stated in the original posts, are author-claim.
- Alex Albert's post came back with no extended note; the visible text ends at the ~280-character limit ("highly recommend trying"). The quoted prompt is complete.
- 陈成 credited item 4 to "WquGuru & Vox." WquGuru's text matches. No @Voxyz_ai post with the same "Review my entire agent setup…" wording was found, so Vox as a co-source is unverified.
- Licenses: the [@alex_prompter](https://x.com/alex_prompter/status/2119010352272998434) prompt is adapted from Damir Sokolovsky's unslop, CC BY 4.0; the line "Adapted from unslop by Damir Sokolovsky, CC BY 4.0." is kept verbatim. The source repo [heydamir/unslop](https://github.com/heydamir/unslop) is also CC BY 4.0. [dzhng/skills](https://github.com/dzhng/skills) and `refactor-codebase` are MIT, Copyright (c) 2026 David Zhang; the copyright and permission notice are included above. The commit message also credits Caldo's untangle-codebase (MIT). [shadcn/improve](https://github.com/shadcn/improve) is MIT © shadcn; this page quotes the usage line and license, not the full README.
