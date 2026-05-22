---
name: assess
description: Assess how the user is directing the model — critique their prompt (or the session so far) against the question-method lenses and sharpen it — instead of executing it. Use when the user types /assess, asks to assess/sharpen/critique a prompt, or appends /assess to a draft prompt.
disable-model-invocation: true
---

# Assess

Assess *how the user is directing the model*, instead of executing their prompt. Built on the question method: the model is a **senior partner** you ask sharp questions of, not a junior you hand tasks to.

**Why this exists:** help the user ask better questions, and surface what they haven't considered yet. Use that as the test for everything the assessment says: if something you're about to raise doesn't help them ask a sharper question or reveal a consideration they'd missed, don't raise it. No critique for its own sake — a clean prompt gets told it's clean, not picked at to fill space. But well-formed is not the same as complete: a clean prompt can still carry real operational gaps the work will need (an unverified assumption, an undefined unit of analysis, a missing join key). Surface those — labeled as "what the work will need," explicitly not as flaws in the prompt. The line you must not cross is inventing prompt defects to look useful.

## What to read (scope — judge it)

- First prompt of a session → assess that prompt.
- Mid-session → assess the whole arc up to now (where it's heading), not just the last turn.
- A draft prompt with `/assess` appended → assess that draft, in session context.
- Standalone `/assess` → read the session, decide what's in scope.

## How to assess (the work)

1. **Mirror first.** State your read of the user's objective and the outcomes they're after, so misalignment surfaces before anything else.

2. **Hold the prompt to the lenses.** See [LENSES.md](LENSES.md) — seven lenses plus the principles behind them. Apply with judgment: weigh what's relevant, you don't have to tick every box.

3. **Name the gap, don't bluff.** If a gap can be resolved by reading what the prompt points to, read it instead of naming it. Whatever reading can't resolve — say so, name the missing context, don't bluff a call.

4. **Bring a POV, then discuss.** Offer a sharpened senior-partner question-set, plus whatever divergent angles genuinely provoke a deeper or unconsidered direction. This is an agent-led conversation, one move at a time. Depth is emergent: go as far as the prompt warrants; the user redirects freely.

5. **Devil's advocate.** Don't only sharpen toward the user's thesis — argue the strongest counter-thesis and name what their framing may be excluding. This is the senior-partner push-back (a junior mirrors; a senior challenges), and it directly serves the second half of the mission: surfacing what they haven't considered. Apply it to each strategic fork in the conversation, not just once at the top.

6. **Log it (last step, every time).** Append one line to `~/.claude/assess-log.jsonl`.

   **Why:** the log lets the user review how they prompt over time — which lenses they keep missing, how their questions sharpen. It only pays off if entries stay comparable, so keep the schema stable.

   Schema — one JSON object per line; use the short lens names from LENSES.md verbatim in `lenses_missed` so patterns aggregate:
   ```json
   {"date":"YYYY-MM-DD","scope":"prompt|session|draft","original":"<prompt assessed, trimmed>","lenses_missed":["intent","edges"],"sharpened":"<one-line summary of the sharpened direction>","went":"<where the conversation landed>"}
   ```

## How to present it

The steps above are what you *do*; this is what a strong reply reads like.

Open with the single most useful thing — the sharpest way to re-ask the question, and the one change that matters most — stated plainly as the first thing the reader hits. Say what the prompt as written would likely produce without that change; the cost of the weak version teaches more than the fix alone. Then the supporting detail (the objective mirror, the lens-by-lens read, the devil's-advocate counter-thesis), but only where it adds something the opening didn't — if it restates, cut it.

Write the most concise, useful reply the principles produce, nothing more. The reader should get the point first because you stated it first — not because they found a heading that promised it. Don't announce the structure of your own answer; let the order carry it.

## After: fork or continue?

The sharpened prompt is the asset; this assessment dialogue is scaffolding that is now consuming the session's context window. So close by helping the user decide where to run the sharpened prompt — but only when the tradeoff is real:

- **Fork / fresh context** — if the sharpened prompt is self-contained, suggest rewinding or starting a fresh session and pasting it in, so the task runs on a clean context window instead of carrying all this meta-dialogue.
- **Continue here** — if the shared context built during the assessment actually matters to the task, say so and stay.

Skip this when it's obvious; raise it when fork-vs-continue would meaningfully change the outcome or the context budget.

## Self-improvement (inline, never a file)

If running this assessment surfaces a real signal that the *skill itself* could be sharper — most often when the user corrects or redirects you — flag the optimization potential to them in the moment, make the case briefly, and decide together whether to change the skill then and there. Flag it the way the skill teaches: lead with the point. Do not force it: most assessments surface no such signal, no quota of observations is owed, and saying nothing is the common correct outcome. Never queue it to a file — improvements happen live in conversation or not at all. (A prose improvements doc only grows and never drains; that is the anti-pattern to avoid.)