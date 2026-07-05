---
name: learn-crossover
description: Use when the user is learning or bumping into a new concept / technology / algorithm / domain (especially when it feels unfamiliar or a bit hard). Applies the "crossover principle" to leverage what the user already knows to unlock the new material fast — pointing out the thing they've secretly already learned (just under a different name), old knowledge that is structurally isomorphic, existing knowledge that explains the new material, and the cross-domain meta-pattern the new concept embodies. Turns "learning something new" into "discovering you already know half of it." Triggers: learning X, running into X, this is hard, what is X, help me understand X.
---

# The Crossover Principle (learn-crossover)

> Core creed: **The real way to learn fast is to realize "you've already learned this."** A crossover matches **structure**, not names.

## When to use

When the user is learning / running into a new concept X (a new technology, algorithm, theory, domain…), especially when it feels "unfamiliar / a bit hard." Difficulty is usually not an IQ problem — it's that X still has some "old knowledge that hasn't been connected up yet" relative to the user.

## Process

### Step 1: Grab the essential structure of X (no term-piling)

Say in a sentence or two what X actually does — what its core mechanism / structure is. Strip off the terminology shell and leave "at its core it's a ___." **Only once you have the structure can you match it against what the user has already learned.**

### Step 2: Figure out what the user already knows

**Ask proactively** and build a list of the user's "already-mastered knowledge":

- Ask about the user's background: which related fields they've studied, what projects they've done, which tools / theories they're familiar with
- Only count knowledge the user has **confirmed in their own words** during the conversation
- Goal: find old knowledge that is structurally isomorphic to X, or that can explain X

When in doubt, just ask "Have you studied ___?" **Never infer what the user knows from the material being taught or from the background of the article's author.**

### Step 3: Organize the output around the "three crossover conjectures" (core)

1. **🎁 You've actually already learned it (just renamed)** — highest priority. Is X simply a Y the user already knows, wearing a different field's name? (e.g., derivative = gradient = rate of change). On a hit, just say "you already know this — it's only been renamed to X."
2. **🔗 Structurally isomorphic (very similar)** — give a **field-level correspondence table** between some Z the user has learned and X (A↔a, B↔b…), and **clearly mark what's the same and what's different**. Ironclad rule: keep the differences as differences, but the similar parts are your learning lever — don't refuse to use it just because it's "strictly not identical."
3. **🧩 Explainable (explained via existing knowledge)** — use some W the user has already mastered to make X click.

### Step 4: Point out the meta-knowledge

Which **recurring underlying pattern** does X embody? (divide and conquer, self-bootstrapping / bootstrap, damping–negative feedback, exploration vs. exploitation, quantitative-to-qualitative change, controlled variables, state machines…). Tell the user "you've seen this pattern before in ___ and ___," and hang X onto their meta-knowledge network.

### Step 5: Land it

Close with one sentence that lowers the fear of learning + names the smallest remaining piece that's genuinely new:

> "So with X you already know the ___ part; the only truly new thing you have to learn from scratch is ___."

## Notes

> ⚠️ **Ironclad rule · use only confirmed known knowledge**: to judge "what the user already knows," you may only use knowledge they've **confirmed learning** (stated themselves or from a reliable background). It is **strictly forbidden** to treat "the material being taught / the article author's background / someone else's knowledge in the conversation" as things the user knows. When in doubt → just ask "⚠️ Have you studied ___?" Never assume on their behalf. (The most common way this crashes: mistakenly pinning the material author's background onto the learner, which voids the entire crossover.)

- **Err on the side of more concrete examples** (case-driven); don't hand over abstract frameworks.
- Structural correspondences should go down to a **field-level mapping table** — don't vaguely say "they're similar."
- When you're unsure whether a crossover connection holds, **flag it as "an analogy still to be verified"** — propose it as a hypothesis, and allow it to be overturned.
- Sibling skills: for "should I even learn this" use `learn-occam`, for "map out the system" use `learn-graph`, for "learn by doing and iterating" use `learn-prototype`, and for "check whether I really get it" use `learn-feynman`.
