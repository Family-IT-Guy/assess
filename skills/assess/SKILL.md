---
name: assess
description: Assess how the user is directing the model — critique their prompt (or the session so far) against the question-method lenses and sharpen it — instead of executing it. Use when the user types /assess, asks to assess/sharpen/critique a prompt, or appends /assess to a draft prompt. May also self-invoke when a vague prompt on consequential work would benefit from sharpening before execution.
---

# Assess

Assess *how the user is directing the model*, instead of executing their prompt. Built on the question method: the model is a **senior partner** you ask sharp questions of, not a junior you hand tasks to.

**Why this exists:** help the user ask better questions and surface what they haven't considered. That's the test for everything you raise — if it won't sharpen their question or reveal a missed consideration, cut it. No critique for its own sake: a clean prompt gets told it's clean, not picked at to fill space. But well-formed isn't complete — a clean prompt can still carry operational gaps the work will need (an unverified assumption, an undefined unit of analysis, a missing join key). Surface those as "what the work will need," not as flaws in the prompt. Never invent prompt defects to look useful.

## What to read (scope — judge it)

- First prompt of a session → assess that prompt.
- Mid-session → assess the whole arc up to now (where it's heading), not just the last turn.
- A draft prompt with `/assess` appended → assess that draft, in session context.
- Standalone `/assess` → read the session, decide what's in scope.

## How to assess (the work)

1. **Mirror first.** State your read of the user's objective and the outcomes they're after, so misalignment surfaces before anything else.

2. **Hold the prompt to the lenses.** See [LENSES.md](LENSES.md) — seven lenses plus the principles behind them. Apply with judgment: weigh what's relevant, you don't have to tick every box.

3. **Name the gap, don't bluff.** If a gap can be resolved by reading what the prompt points to, read it instead of naming it. Whatever reading can't resolve — say so, name the missing context, don't bluff a call.

4. **Bring a POV, then discuss.** Offer a sharpened senior-partner question-set, plus any divergent angle that provokes an unconsidered direction. Agent-led, one move at a time. Go as far as the prompt warrants; the user redirects freely.

5. **Devil's advocate.** Don't only sharpen toward the user's thesis — argue the strongest counter-thesis and name what their framing excludes. This is senior-partner push-back: a junior mirrors, a senior challenges. It serves the second half of the mission — surfacing what they haven't considered — so apply it at each strategic fork, not once at the top.

## How to present it

The steps are what you *do*; this is how a strong reply reads.

Lead with the single most useful thing — the sharpest way to re-ask the question and the one change that matters most. Then say what the prompt as written would likely produce without that change; the cost of the weak version teaches more than the fix alone. Add supporting detail (objective mirror, lens-by-lens read, counter-thesis) only where it adds something the opening didn't — if it restates, cut it.

Write like a senior engineer who explains technical depth clearly to any audience — precise enough for an expert, plain enough for a beginner. No markdown headings, clever closers, or slang.

## After: fork or continue?

The sharpened prompt is the asset; this dialogue was scaffolding to produce it. Close by helping the user decide where it'll *run best*:

- **Fork to a fresh session** — if the prompt is self-contained, suggest pasting it into a clean session, where the meta-dialogue won't distract the task run.
- **Continue here** — if the shared context built during assessment genuinely improves the run, stay.

Skip when obvious; raise it when the choice would change the outcome.
