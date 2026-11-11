---
title: 2026-11-12-Coding Agent 提示词合集
headline: 提示词合集 · 隐式状态机 · 做减法与去 AI 味
type: x-news-daily
date: 2026-11-12
tags: [x-daily, ai, coding-agents, prompts, state-machines, unslop, cleanup, home-repo]
source: x.com + github.com/dzhng/skills + github.com/heydamir/unslop + github.com/shadcn/improve
window: 2026-10-30 至 2026-11-11（专题合集，非常规日报窗口）
generated: 2026-11-12T06:01:00+08:00
coverage: special
---

# Coding Agent 提示词合集（2026-11-12）

本期是 AI每日精选的专题，不是常规日报。过去两周，X 上出现了一批可以直接丢给 Claude Code / Codex 的工作流和代码清理提示词：Home Repo、隐式状态机、用 `/goal` 做减法，以及去掉页面和代码里的 AI 味。下面按栏目收录**原帖全文或可复制提示词**，每条都带作者、原帖链接和抓取到的互动数据。提示词未作改写；若原文含链接缩短地址，会在文中另行给出还原后的完整 URL。

## 怎么用

- 需要复制的提示词都放在代码块里。
- 互动数据是本次抓取时的公开指标，不是转述来的约数。
- 提示词能否真的清出 bug、删对代码，一律标为 author-claim；原帖存在与否标为 verified。

## 1. Matt Pocock 的 Home Repo

作者 [@mattpocockuk](https://x.com/mattpocockuk/status/2120260969750540327)（Matt Pocock），2026-11-11 05:03（台北时间）。

- 发生了什么：他用一个「Home Repo」集中放 skills、steering 文件和 wiki，agent 只在这个仓库里启动；其他项目的位置写在 `AGENTS.md` 里，需要时再让 agent 自己去改。
- 原帖与互动：[原帖](https://x.com/mattpocockuk/status/2120260969750540327)，4,190 收藏、2,883 赞、154 转发、270 回复、61 引用、211,546 次曝光。
- 核验：原帖全文 verified。有效性为 author-claim。

原文（含他写在 `AGENTS.md` 里的示例指针）：

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

可单独复制的 `AGENTS.md` 示例：

```text
For skills, clone mattpocock/skills to ~/repos/skills.
For Sandcastle, clone mattpocock/sandcastle to ~/repos/sandcastle
```

## 2. 隐式状态机系列

源头是 [@steveruizok](https://x.com/steveruizok/status/2116552016218710389) 2026-10-31 那句短提示。之后一周里出现了加 UX/DX/AX 约束的版本、把状态写成文档并修 bug 的扩写，以及为什么「测试都过了还会出 bug」的解释；也有人把它改成找隐式设计系统组件。

### 源头：@steveruizok

作者 [@steveruizok](https://x.com/steveruizok/status/2116552016218710389)（Steve Ruiz），2026-10-31 23:24（台北时间）。

- 原帖与互动：[原帖](https://x.com/steveruizok/status/2116552016218710389)，15,806 收藏、8,480 赞、398 转发、167 回复、291 引用、2,170,348 次曝光。
- 核验：原文 verified。

```text
good prompt "find all of the implicit state machines in my app"
```

可复制提示词：

```text
find all of the implicit state machines in my app
```

### @Voxyz_ai：加上 UX / DX / AX 约束

作者 [@Voxyz_ai](https://x.com/Voxyz_ai/status/2119444845890617507)（Vox），2026-11-08 23:00（台北时间）。本系列里互动最高的一条。

- 原帖与互动：[原帖](https://x.com/Voxyz_ai/status/2119444845890617507)，22,913 收藏、9,515 赞、443 转发、237 回复、63 引用、1,229,664 次曝光。
- 核验：原文 verified。效果为 author-claim。

原文：

```text
Vibecoders, 𝗜'𝗺 𝗯𝗲𝗴𝗴𝗶𝗻𝗴 𝘆𝗼𝘂, open your messiest project and paste this into Claude Code or Codex:

"Find all of the implicit state machines in my app. Make the best decision that will elevate all three: the user experience (UX), developer experience (DX), and agent experience (AX) always, without breaking anything."
```

可复制提示词：

```text
Find all of the implicit state machines in my app. Make the best decision that will elevate all three: the user experience (UX), developer experience (DX), and agent experience (AX) always, without breaking anything.
```

### @trevin：写成文档、找出非法状态、修复并补回归测试

作者 [@trevin](https://x.com/trevin/status/2118690987153186845)（Trevin Chow），2026-11-06 21:04（台北时间）。引用了 Steve 的源头帖。

- 原帖与互动：[原帖](https://x.com/trevin/status/2118690987153186845)，4,469 收藏、2,654 赞、100 转发、32 回复、11 引用、111,378 次曝光。
- 核验：原文 verified。他写「helps find a ton of bugs for me」为 author-claim。

```text
This is an amazing prompt that helps find a ton of bugs for me. 

“Find the app’s explicit and implicit state machines and document their states, invariants, and transition tables in one file. Identify invalid states or transitions the code can actually reach, with evidence, including through retries and concurrency. Prioritize confirmed bugs by impact, group related fixes into issues, then fix them with regression tests and keep the document updated.”
```

可复制提示词：

```text
Find the app’s explicit and implicit state machines and document their states, invariants, and transition tables in one file. Identify invalid states or transitions the code can actually reach, with evidence, including through retries and concurrency. Prioritize confirmed bugs by impact, group related fixes into issues, then fix them with regression tests and keep the document updated.
```

### @DavidKPiano：为什么测试都过了还会出 bug

作者 [@DavidKPiano](https://x.com/DavidKPiano/status/2119788094434038264)（David K），2026-11-09 21:44（台北时间）。这不是一条可粘贴的提示词，而是对「隐式状态机」的解释：逻辑散落各处时，非法状态仍然可达，测试和 code review agent 都可能放行。

- 原帖与互动：[原帖](https://x.com/DavidKPiano/status/2119788094434038264)，1,094 收藏、1,331 赞、82 转发、54 回复、20 引用、118,375 次曝光。
- 核验：原文 verified。对 FaceTime 等案例的引用以及「仍然会有很糟的 bug」为 author-claim。

```text
What is an implicit state machine? 

Your apps are full of state machines, which is the logic that says "when we're in this state, and this event happens, now we're in this state" (given, when, then).

Sometimes those state machines are clearly mapped out (switch statements, reducers, tables/maps, libraries like XState for the more complex ones, etc.) and the logic is explicitly enumerable.

And sometimes it's not. The ad-hoc logic is spread all over the place. That's how developers typically code, and that's how agents typically vibe-code (they learned from you). Those are implicit state machines.

What's wrong with implicit state machines? It's not clear what state transitions are possible, so you might have "allowed" states that should have been impossible without knowing it. Agents make the same mistakes. 

You can get all tests passing and your code review agents (even the well-funded ones) can say "LGTM" and you can *still* have very bad bugs because an implicit state machine allowed unexpected or illegal behavior. (Remember the Apple FaceTime bug?)

So yeah, making your app logic explicit is important.
```

### @rodydavis：找隐式的设计系统组件

作者 [@rodydavis](https://x.com/rodydavis/status/2120402273029201934)（Rody Davis），2026-11-11 14:24（台北时间）。引用 Steve 的源头帖，把「state machines」换成了「design system components」。

- 原帖与互动：[原帖](https://x.com/rodydavis/status/2120402273029201934)，247 收藏、268 赞、7 转发、7 回复、1 引用、10,814 次曝光。
- 核验：原文 verified。

```text
good prompt “find all of the implicit design system components in my app”
```

可复制提示词：

```text
find all of the implicit design system components in my app
```

## 3. 做减法 / 删死代码

### @Voxyz_ai：用 /goal 清理的 5 条串

作者 [@Voxyz_ai](https://x.com/Voxyz_ai/status/2118357672106029272)（Vox），2026-11-05 23:00（台北时间）。主帖建议：如果额度重置时还剩一半，不如用 `/goal` 清掉 vibe coding 堆下来的死代码、重复实现、多余依赖、空转定时任务，以及旧 session / worktree。下面 5 条是同一条串里的完整原文，均要求在新分支上工作、不要 push / merge。

- 原帖与互动： [主帖](https://x.com/Voxyz_ai/status/2118357672106029272) 3,882 收藏、1,672 赞、92 转发、62 回复、8 引用、259,449 次曝光。各条回复的互动单独标注。
- 核验：五条全文 verified。清理效果为 author-claim。

**主帖原文：**

```text
𝗖𝗼𝗱𝗲𝘅 𝘁𝗶𝗽: if you still have half your quota left when it resets, you’re throwing away days of Astra and Sol.

Use `/goal` to squeeze every last bit out of it and clean out what months of vibe coding piled up: dead code nothing calls, the same logic written several times over, dependencies you don’t need, old sessions and worktrees hogging your disk, or even scheduled tasks that have been running for nothing.

Here are 5 prompts and goals you can copy-paste directly. ↓
```

**1/5 Delete dead code**（[原帖](https://x.com/Voxyz_ai/status/2118357672550683020)，138 收藏、82 赞、21,461 次曝光）：

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

**2/5 Merge duplicate implementations**（[原帖](https://x.com/Voxyz_ai/status/2118357673070776644)，60 收藏、41 赞、18,141 次曝光）：

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

**3/5 Remove dependencies you don't need**（[原帖](https://x.com/Voxyz_ai/status/2118357673632797142)，53 收藏、31 赞、15,968 次曝光）：

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

**4/5 Shut off scheduled tasks that run for nothing**（[原帖](https://x.com/Voxyz_ai/status/2118357674106700164)，42 收藏、28 赞、14,151 次曝光）。这一条是只读清单，要求不要改任何设置：

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

**5/5 Clear out old sessions and worktrees**（[原帖](https://x.com/Voxyz_ai/status/2118357674677166497)，110 收藏、47 赞、12,567 次曝光）。同样要求不要直接删除，只写脚本等你审：

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

### @Voxyz_ai：「Fewer, deeper modules, smaller interfaces」

作者 [@Voxyz_ai](https://x.com/Voxyz_ai/status/2119777023845417175)（Vox），2026-11-09 21:00（台北时间）。引用了上面那条 UX/DX/AX 帖，并给出一个 5 词清理提示，以及一段可整段粘贴的加长版。

- 原帖与互动：[原帖](https://x.com/Voxyz_ai/status/2119777023845417175)，1,263 收藏、691 赞、19 转发、37 回复、4 引用、49,753 次曝光。
- 核验：原文 verified。「最强清理提示」「行数会下降、抽象会更好」为 author-claim。

```text
One more thing.

Highly recommend trying the 𝘀𝘁𝗿𝗼𝗻𝗴𝗲𝘀𝘁 𝗰𝗼𝗱𝗲 𝗰𝗹𝗲𝗮𝗻𝘂𝗽 𝗽𝗿𝗼𝗺𝗽𝘁 out there right now. It's only 5 words: "fewer, deeper modules, smaller interfaces"

The best part is 𝘄𝗮𝘁𝗰𝗵𝗶𝗻𝗴 𝘁𝗵𝗲 𝗹𝗶𝗻𝗲 𝗰𝗼𝘂𝗻𝘁 𝗱𝗿𝗼𝗽 as all the duplicate code gets wiped out and the core logic lands in one place. The AI comes up with way smarter abstractions, fixes a pile of bugs along the way, and the whole codebase ends up fully consistent.

Every time you get a feature working, drop this whole block into Claude Code or Codex 👇

"Fewer, deeper modules, smaller interfaces. Check data once where it comes in, then just use it. Write one-off logic right where it's used instead of splitting it into a function ahead of time. Skip try/catch wherever you can."
```

五词版：

```text
fewer, deeper modules, smaller interfaces
```

加长版：

```text
Fewer, deeper modules, smaller interfaces. Check data once where it comes in, then just use it. Write one-off logic right where it's used instead of splitting it into a function ahead of time. Skip try/catch wherever you can.
```

### @chenchengpro 五条合集，以及原作者原文

作者 [@chenchengpro](https://x.com/chenchengpro/status/2120040764243894547)（陈成），2026-11-10 14:28（台北时间）。他把五条提示词收在一起，并点名了来源。下面先放合集原文，再分别给出我们找到的原作者帖；个别用词、标点和陈成转写并不完全相同，**复制时建议以原作者帖为准**。

- 原帖与互动：[原帖](https://x.com/chenchengpro/status/2120040764243894547)，1,810 收藏、1,117 赞、61 转发、17 回复、2 引用、66,647 次曝光。
- 核验：合集原文 verified。各条来源的核验见下。

**合集原文**（第 5 条里的缩短链接已还原为 https://github.com/shadcn/improve）：

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

**1/ 原作者 [@alexalbert__](https://x.com/alexalbert__/status/2119884951550386671)**（Alex Albert，Anthropic），2026-11-10 04:08（台北时间）。18,675 收藏、9,888 赞、518 转发、342 回复、214 引用、1,118,848 次曝光。接口返回的正文在约 280 字处结束，末尾是「highly recommend trying」，没有更长的 note；引号里的提示词本身是完整的。请注意原帖用的是弯引号 that’s / you’re，与合集里的直引号不同。

```text
Every time we have a new model, I run the same simple prompt on all my projects:

"Read this entire project and find everything that’s broken, inconsistent, inefficient, or no longer needed. Fix what you’re sure about and list the rest for me to review."

highly recommend trying
```

**2/ 原作者 [@anthonyriera](https://x.com/anthonyriera/status/2119870644514893997)**（Anthony Riera），2026-11-10 03:12（台北时间）。2,576 收藏、1,398 赞、45 转发、24 回复、2 引用、100,828 次曝光。结构是两条破折号问题，不是合集里的「#1 / #2」。

```text
I want you to audit our codebase, is anything here unnecessary, overly complicated in our current setup, or based on weak assumptions? Challenge them. 

- What can be deleted entirely?
- What can be simplified now that unnecessary pieces are gone?

Then make the changes. Prefer deleting over simplifying, simplifying over optimizing, and optimizing over automating.

This product is being used by thousands of customers, do not cut any corners.
```

**3/ 原作者补遗。** Steve 的源头见第 2 节。[@kunchenguid](https://x.com/kunchenguid/status/2119924895060795492)（Kun Chen）2026-11-10 06:47（台北时间）给出「fewer words, big visuals」版，1,962 收藏、918 赞、40 转发、17 回复、9 引用、64,809 次曝光；他还提到可选工具 [lavish-axi](https://github.com/kunchenguid/lavish-axi)。[@RicardoSawir](https://x.com/RicardoSawir/status/2119891925671305268)（Ricardo Sawir）2026-11-10 04:36（台北时间）在 Alex Albert 帖下回复了带「Also, make state machines explicit」的 UX/DX/AX 版（5 收藏、4 赞、1,937 次曝光）。Vox 更早的 UX/DX/AX 版见第 2 节，Ricardo 这条是在其后补充「make explicit」。

Kun Chen 提示词：

```text
audit and find implicit state machines in this <codebase/directory/module> that would drive concrete improvements if made explicit. explain before/after of each one and discuss with me in lavish-axi. fewer words, big visuals
```

Ricardo Sawir 提示词：

```text
Find all of the implicit state machines in my app (there are probably a ton). Make the best decision that will elevate all three: the user experience (UX), developer experience (DX), and agent experience (AX) always, without breaking anything. Also, make state machines explicit.
```

**4/ 原作者 [@wquguru](https://x.com/wquguru/status/2119962410056642797)**（WquGuru），2026-11-10 09:16（台北时间）。45 收藏、48 赞、6 转发、6 回复、5,469 次曝光。合集同时署名「WquGuru & Vox」；我们找到了 WquGuru 这条原文，但没有找到 @Voxyz_ai 发出过同一段提示词的帖子，Vox 作为共同来源暂标 unverified。

```text
Review my entire agent setup: AGENTS.md, CLAUDE.md, skills, commands, subagents, hooks, settings/permissions, and MCP servers.

Check for gaps in guardrails and whether it follows current best practices for Fable 5.2.
```

**5/ [shadcn/improve](https://github.com/shadcn/improve)**（MIT © shadcn；抓取时约 10,782 star）。合集里的用法是一句：

```text
run https://github.com/shadcn/improve for my codebase.
```

仓库说明：用更强的模型做审计和写计划，执行交给更便宜的模型；skill 本身不改业务代码，计划写进 `plans/`。安装：`npx skills add shadcn/improve`。常用入口是 `/improve`、`/improve quick`、`/improve deep`。完整说明见仓库 README，此处不整篇转载。

## 4. 去掉 AI 味

### @alex_prompter 的 unslop 结构化提示词

作者 [@alex_prompter](https://x.com/alex_prompter/status/2119010352272998434)（Alex Prompter），2026-11-07 18:13（台北时间）。

- 发生了什么：他改写了 Damir Sokolovsky 的开源 unslop skill，做成一段可直接粘进 Claude Code 的提示词，用来去掉已有页面上的「AI 味」（只改样式和已批准文案，功能与事实不动），并用两个新的 subagent 分别当 judge 和 guard。
- 原帖与互动：[原帖](https://x.com/alex_prompter/status/2119010352272998434)，534 收藏、198 赞、19 转发、23 回复、28,661 次曝光。
- 核验：提示词全文 verified。关于 190 万播放、5,500 GitHub star 等数字是原帖撰写时的自述，author-claim；我们另查到 Damir 的仓库 [heydamir/unslop](https://github.com/heydamir/unslop) 目前为 CC BY 4.0，抓取时约 14,481 star。
- 许可：原帖结尾的署名与许可声明如下，按要求原文保留——**Adapted from unslop by Damir Sokolovsky, CC BY 4.0.** Damir 原 skill 帖：[heydamir，2026-10-30 21:20（台北时间）](https://x.com/heydamir/status/2116158176336970008)，9,778 收藏、5,221 赞、240 转发、139 回复、69 引用、642,663 次曝光。仓库：https://github.com/heydamir/unslop。

提示词原文（把 `[PAGE: local dev URL]` 换成你的本地预览地址）：

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

他在[第一条回复](https://x.com/alex_prompter/status/2119010364436471877)里补充了浏览器工具安装方式，并再次指向 Damir 的 skill。下面正文里的 t.co 已还原为完整地址：

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

### @dzhng：从 session 里提炼的 de-slop skill，配合 /goal 过夜跑

作者 [@dzhng](https://x.com/dzhng/status/2120297879046865279)（David Zhang），2026-11-11 07:29（台北时间）。

- 发生了什么：他让 Fable 5.2 读过往 session 记录，提炼出一套给整个代码库做重构、去掉 slop 的原则，写成 skill，并建议配 `/goal` 隔夜跑。「One run a day keeps the slop away。」帖内链接指向仓库 https://github.com/dzhng/skills（抓取时约 1,500 star）。仓库里对应的是 [`skills/review/refactor-codebase/SKILL.md`](https://github.com/dzhng/skills/blob/main/skills/review/refactor-codebase/SKILL.md)：该文件在 2026-11-11 05:13（台北时间）加入，时间与发帖接近；提交说明写明它改编自 Caldo 的 untangle-codebase（同样是 MIT）。仓库没有名为 `de-slop` 的 skill。
- 原帖与互动：[原帖](https://x.com/dzhng/status/2120297879046865279)，196 收藏、124 赞、6 转发、18 回复、8,440 次曝光。
- 核验：原帖与 skill 文件 verified。隔夜跑的效果为 author-claim。
- 许可：仓库为 MIT License，Copyright (c) 2026 David Zhang。按许可条件，下面转载 skill 全文，并保留版权与许可声明。

原帖全文：

```text
Asked Fable-5.2 to read through all my session transcripts and distill a set of principles for a refactor skill to de-slop any codebase

Use with /goal to work with large codebases and leave on overnight

One run a day keeps the slop away
```

`refactor-codebase` skill 全文（MIT License，Copyright (c) 2026 David Zhang；Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files, to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, subject to the condition that the above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software. THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.）：

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

## 核验与授权

- 专题列出的 11 组原帖（含 Vox 五条 `/goal` 串的全部回复）以及陈成点名的 Alex Albert、Anthony Riera、Kun Chen、Ricardo Sawir、WquGuru、Damir Sokolovsky 原帖，全文均已从 X 接口取回，标 verified。
- 提示词能否找到 bug、删对代码、去掉 AI 味，以及原帖里的播放量 / star 自述，标 author-claim。
- Alex Albert 原帖接口返回的正文在约 280 字处结束（「highly recommend trying」），未取到更长 note；引号内提示词完整。
- 陈成把第 4 条同时归给 WquGuru 与 Vox：WquGuru 原文已核对；未找到 @Voxyz_ai 发出同一段「Review my entire agent setup…」的帖子，Vox 共同来源暂标 unverified。
- 授权：[@alex_prompter](https://x.com/alex_prompter/status/2119010352272998434) 提示词改编自 Damir Sokolovsky 的 unslop，CC BY 4.0，文中已保留「Adapted from unslop by Damir Sokolovsky, CC BY 4.0.」；原仓库 [heydamir/unslop](https://github.com/heydamir/unslop) 同样是 CC BY 4.0。[dzhng/skills](https://github.com/dzhng/skills) 与其中的 `refactor-codebase` 为 MIT，Copyright (c) 2026 David Zhang，上文已附版权与许可声明；提交说明还提到改编自 Caldo 的 untangle-codebase（MIT）。[shadcn/improve](https://github.com/shadcn/improve) 为 MIT © shadcn，本文只摘了用法和许可，未整篇转载 README。
