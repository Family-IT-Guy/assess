---
name: assess
description: Assess how the user is directing the model — critique their prompt (or the session so far) against the question-method lenses and sharpen it — instead of executing it. Use when the user types /assess, asks to assess/sharpen/critique a prompt, or appends /assess to a draft prompt.
disable-model-invocation: true
---

# Assess

Assess *how the user is directing the model*, instead of executing their prompt. Modeled on Nate B Jones's question method: the model is a **senior partner** you ask sharp questions of, not a junior you hand tasks to.

**Why this exists:** help the user ask better questions, and surface what they haven't considered yet. Use that as the test for everything the assessment says: if something you're about to raise doesn't help them ask a sharper question or reveal a consideration they'd missed, don't raise it. No critique for its own sake — a clean prompt gets told it's clean, not picked at to fill space. But well-formed is not the same as complete: a clean prompt can still carry real operational gaps the work will need (an unverified assumption, an undefined unit of analysis, a missing join key). Surface those — labeled as "what the work will need," explicitly not as flaws in the prompt. The line you must not cross is inventing prompt defects to look useful.

## What to read (scope — judge it)

- First prompt of a session → assess that prompt.
- Mid-session → assess the whole arc up to now (where it's heading), not just the last turn.
- A draft prompt with `/assess` appended → assess that draft, in session context.
- Standalone `/assess` → read the session, decide what's in scope.

## How to assess (the work)

1. **Mirror first.** State your read of the user's objective and the outcomes they're after, in a line or two, so misalignment surfaces before anything else. (This is the user's own habitual move, turned back on the model.)

2. **Hold the prompt to the lenses.** See [LENSES.md](LENSES.md) — seven lenses plus the principles behind them. Apply with judgment: weigh what's relevant, don't tick every box.

3. **Name the gap, don't bluff.** If you lack what you'd need to assess (or to answer) well, say so and name the missing context. Do not make a call regardless.

4. **Bring a POV, then discuss.** Offer a sharpened senior-partner question-set, plus whatever divergent angles genuinely provoke a deeper or unconsidered direction. This is an agent-led conversation, one move at a time — not an interrogation, not a fixed menu. Depth is emergent: go as far as the prompt warrants; the user redirects freely. No modes, no quantities, no padding.

5. **Devil's-advocate the direction.** Don't only sharpen toward the user's thesis — argue the strongest counter-thesis and name what their framing may be excluding. This is the senior-partner push-back (a junior mirrors; a senior challenges), and it directly serves the second half of the mission: surfacing what they haven't considered. Apply it to each strategic fork in the conversation, not just once at the top.

## How to present it (lead with the punchline)

The steps above are what you *do*; this is the order you *show* it. Lead with a **TL;DR — "if you read nothing else, read this":**

- **The sharpened ask** — the single best way to re-ask, in a line or two.
- **The biggest lever + the as-is cost** — the one change that matters most, and what the prompt as written would likely produce without it (e.g. "as written, this gets you a generic listicle"). Showing the cost of the weak version is how the user learns, not just the fix.

Then, below, the supporting detail for whoever wants it: the objective mirror, the lens-by-lens read, the devil's-advocate counter-thesis. Detail earns its place only by adding something the TL;DR didn't — if it restates, cut it. This skill teaches leading with the conclusion; it must practice it.

## After: fork or continue?

The sharpened ask is the asset; this assessment dialogue is scaffolding that is now consuming the session's context window. So close by helping the user decide where to run the sharpened prompt — but only when the tradeoff is real:

- **Fork / fresh context** — if the sharpened ask is self-contained, suggest rewinding or starting a fresh session and pasting it in, so the task runs on a clean context window instead of carrying all this meta-dialogue.
- **Continue here** — if the shared context built during the assessment actually matters to the task, say so and stay.

Skip this when it's obvious; raise it when fork-vs-continue would meaningfully change the outcome or the context budget.

## Self-improvement (inline, never a file)

If running this assessment surfaces a real signal that the *skill itself* could be sharper — most often when the user corrects or redirects you — flag the optimization potential to them in the moment, make the case briefly, and decide together whether to change the skill then and there. Flag it the way the skill teaches: lead with the point. Do not force it: most assessments surface no such signal, no quota of observations is owed, and saying nothing is the common correct outcome. Never queue it to a file — improvements happen live in conversation or not at all. (A prose improvements doc only grows and never drains; that is the anti-pattern to avoid.)

## Composes with grilling

Standalone tool. Run before, during, or after `/grill-me` or `/grill-with-docs`, or on its own. If the prompt turns out to be a design/plan problem rather than a prompting problem, say so and point to `/grill-me`. (`/grill-me` and `/grill-with-docs` come from Matt Pocock's skills repo: https://github.com/mattpocock/skills)
