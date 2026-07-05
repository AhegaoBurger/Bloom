---
name: learn-occam
description: Use when the user is torn over whether to learn something, how deeply to learn it, or how to trade off time, energy, and projects. Applies the "keep-it-simple strategy": first press for the concrete problem to be solved, test whether existing knowledge already handles it, weigh how fast the knowledge depreciates against its ROI, use "explore vs. apply" to decide whether to learn something new or use what's on hand, and land on a verdict of "learn it / skip it / learn just the minimum that's enough" — so you don't hoard knowledge that's about to depreciate. Triggers: should I learn X, is it worth going deep, how much is enough to learn, what should I learn when time is short, dig deeper or good-enough is fine.
---

# Keep-It-Simple Strategy (learn-occam)

> Core creed: **the most valuable thing in this world isn't knowledge, it's your time.** If existing knowledge can solve it, don't learn something new; what you'll need later, learn later.

## When to use

The user is agonizing over "should I learn X / how deep should I go / where should my energy go." This is the **brake** on a breadth-first tendency with an over-long queue of interests.

## Flow

### Step 1: Find the "given problem" first

Press with one question: **what is the specific problem you're trying to solve?** No concrete problem, purely "feels like I should learn it / everyone else is" → straight into the "learn later" queue, no claim on present energy. Understanding what knowledge is *for* matters more than the knowledge itself.

### Step 2: Can existing knowledge handle it?

**Ask exactly what the user already knows** — if it can solve the problem, **don't learn anything new**. When you're unsure whether they "might already know it," pair this with `learn-crossover`.

### Step 3: Depreciation rate + ROI

How soon will this knowledge depreciate? (Tech stacks and tools often turn over noticeably in 6–12 months.) Is it worth the relatively limited time? **Depreciates fast + can be outsourced to AI / looked up anytime → you only need to "know it exists and what it's for," no need to actually learn it.**

### Step 4: Explore vs. apply (N-armed bandit)

Right now, should you "explore" (learn new) or "apply" (use what you have)? The higher the cost of exploring → the more you should lean toward applying. Only when the goal is hard enough and existing knowledge genuinely can't reach it does the keep-it-simple strategy **push** you to learn.

### Step 5: Give the verdict

Pick one of three, clearly: **① Learn it** (worth it, and existing knowledge can't do the job) / **② Skip it** (into the "learn later" queue) / **③ Learn just the minimum that's enough** (name exactly which small piece). If they want to dig deep, hand off to `learn-graph` to build a path.

## Notes

> ⚠️ **Ironclad rule · only use confirmed known knowledge**: judge what the user "already knows" only from knowledge they've **confirmed learning** (stated in their own words or a reliable background); it is **strictly forbidden** to treat "the material being discussed / an article author's background / someone else's knowledge in the conversation" as things the user knows. When unsure → just ask "⚠️ Have you learned ___?" Never assume it for them.

- The keep-it-simple strategy isn't about "learning less," it's about "letting the problem decide what you learn."
- Its weakness is falling into a local optimum — when you're unsure whether "prerequisite knowledge is missing," hand off to `learn-graph`.
- Sibling skills: `learn-crossover` (what you already know) `learn-graph` (systematic mapping) `learn-prototype` (hands-on iteration) `learn-feynman` (self-check).
