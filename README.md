# assess

Get sharper answers from AI by fixing the question, not the answer. `/assess` reads
how you're directing the model and shows you a stronger way to ask, so it explores
and pushes back instead of just running a mediocre prompt.

It's a Claude Code plugin from Family IT Guy, built on the question method: treat the
model as a senior partner you ask sharp questions of, not a junior you hand tasks to.

## What it does

When you give AI a quick, vague prompt, you get a quick, vague answer. `/assess`
doesn't answer the prompt. It plays back what you're actually after, points out what
the question is missing (your real angle, who or what it's for, what a good result
looks like), and hands you a sharper version to run. Most of the quality of an AI
answer comes from the question, and that's the part `/assess` fixes.

## When to reach for it

Use `/assess` when you're the one asking the model to build, learn, or figure
something out, especially on work that matters. Skip it when you're just answering a
question the model asked you, like saying yes to a plan it proposed. The tell: are you
initiating, or responding?

Three ways to run it:
- Type `/assess` to assess your last prompt or the session so far.
- Append `/assess` to a draft prompt to sharpen it before you send it.
- Run it mid-session to check where a line of work is heading.

## Install

```
/plugin marketplace add Family-IT-Guy/plugins
/plugin install assess@familyitguy
```

To update later: `/plugin marketplace update familyitguy` then `/plugin install
assess@familyitguy`. (Or turn on auto-update in the `/plugin` menu under Marketplaces.)
