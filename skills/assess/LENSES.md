# Assessment Lenses

The lenses `/assess` holds a prompt up to. **Apply with judgment** — weigh what's relevant to the prompt at hand, not all seven every time. These are lenses, not a scoring rubric.

Grounding: the question method. The core shift — the model is now a **senior partner**, not a junior teammate. You direct it by asking sharp questions, not by issuing fully-specified tasks. A senior partner explores, synthesizes across all inputs, and pushes back; a junior mirrors and waits.

## The seven lenses

1. **intent** — Is there a clear angle, a flashlight center? Or flat: just lists what's wanted, no point of view?
2. **edges** — Are bounds and exclusions stated? What's out of scope, what to ignore?
3. **breadth** — Does it invite engaging all the relevant inputs, or will it tunnel the model into one file/thread and miss the rest? Are the data artifacts named?
4. **pushback** — Does it invite the model to challenge and synthesize, or hand it an opinion to mirror back / a task to execute?
5. **form** — A senior-partner question-set, or a junior task-command?
6. **context** — Does the prompt supply, or point to, the inputs the model needs?
7. **success** — Is it clear what a good output looks like *for the user's task* — the acceptance test, distinct from the thesis/direction?

(Use these short names verbatim in the log's `lenses_missed`.)

## The three principles (source of lenses 1-5)

1. **Flashlight intent** — convey your thesis (center of the beam) AND the edges (what to exclude). Not too open, not too closed.
2. **Explore what good looks like** — for outputs hard to encode in an eval, pose multiple hard questions and let the model synthesize, rather than prescribing the weave.
3. **Wrestle with all inputs** — name the data artifacts; make the model engage the full breadth plus your implicit thesis; convey opinion as a thesis it can disagree with, not mirror.

## The five failure modes a weak prompt falls into

1. **Flat** — lists data/wants, conveys no intent.
2. **Rambling opinion** — states an opinion the model will just mirror, not stress-test.
3. **Over-open** — no center, no thesis.
4. **Over-closed** — no room to explore.
5. **Single-thread tunnel** — angles the model into one input, ignoring breadth.
