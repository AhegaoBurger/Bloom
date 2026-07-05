---
name: learn-deep
description: The default deep-dive entry point whenever the user wants to learn any new concept, technology, or theory—it explains the concept thoroughly through five lenses in one pass and helps them choose where to go deeper: crossover leverages what they already know, occam frames how deep they should go, graph builds a knowledge map, prototype iterates on a minimal build, feynman stress-tests understanding. Triggers: I want to learn X, understand X, what is X, tell me about X, help me get X, teach me X, go deep on X, walk me through X. Unless the user explicitly wants just one lens (in which case switch to the corresponding single learn-* skill).
---

# Deep-diving a concept (learn-deep)

> Orchestrates the five lenses `learn-crossover` / `learn-occam` / `learn-graph` / `learn-prototype` / `learn-feynman` into a single panoramic pass, giving the user a "one full sweep + pick a direction" for learning any concept.

## When to use

When the user says "I want to learn / understand / get / tell me about a concept X"—**this is the default entry point**. Run all five lenses in one pass, then let the user choose where to go deeper.
**Exception**: if the user explicitly wants just one angle ("explain it by analogy," "help me build a knowledge map," "quiz me") → go straight to the corresponding single `learn-*` skill instead of running the whole thing.

## Before you start

**First, pin down the user's background**: which related fields they've studied, what they've built, which tools/theories they're comfortable with. crossover / occam / graph all depend on this later. Only count knowledge the user has explicitly confirmed they have.

## Execution order for the five lenses (this arc flows best: lower the barrier → set the depth → hand over a map → get hands dirty → check understanding)

### 1️⃣ crossover — start by showing "you already know half of this"
Grab the essential structure of X (strip the jargon) and work through the three conjectures: 🎁 you've already learned it / 🔗 structural isomorphism (a field-by-field mapping table) / 🧩 you can explain it with knowledge you already have, then name the meta-knowledge at play. **Build confidence first, then talk about going deeper.**

### 2️⃣ occam — frame "how deep should I go"
Locate the "given problem" (what does learning X solve), whether existing knowledge is enough, X's rate of depreciation and its ROI, and set a **depth boundary**: "good enough, stop here / just learn the smallest piece / worth a deep dive." This isn't discouragement—it's a guard against over-drilling right out of the gate.

### 3️⃣ graph — hand over a map so they know where X sits and when they've learned enough
The skeleton of X's place in the knowledge graph of its field (concepts/uses/parent and child nodes), flagging the highest-reuse nodes + the entry points reachable from common sense, and give a learning path. **Prompt the user to fill in nodes themselves** (you only learn by building the map yourself).

### 4️⃣ prototype — give a minimal-prototype starting point and pass the hands-on ball to the user
Give the starting point for "the crappiest thing that runs" + guiding questions (let the user spot the flaws themselves), and foreshadow the pitfalls they'll hit. **Don't do it for them.**

### 5️⃣ feynman — throw 2–4 questions that hit the blind spots to check understanding
Have the user answer in their own words; wherever the answer stumbles = a gap where they don't truly understand. Aim the last question at X's fundamental limitation if you can (the litmus test of real understanding).

### 6️⃣ Wrap-up: pick a direction
**Clearly recommend the 1–2 directions to go deeper** (combining occam's ROI call + the user's goals + which lens landed hardest for them), and point out which single skill to move to next (want to build → `learn-prototype`, want to be tested → `learn-feynman`).

## Notes

> ⚠️ **Ironclad rule · only use confirmed prior knowledge**: judge what the user "already knows" strictly from knowledge they've **confirmed they've studied** (stated directly or reliable background); it is **strictly forbidden** to treat "the material being explained / the article author's background / knowledge shown by others in the conversation" as the user's own. When unsure → just ask "⚠️ Have you studied ___?"—never assume it for them.

- **Each lens has its own focus—never overlap**: crossover leverages / occam only discusses how deep to go / graph only gives the map / prototype only gives the hands-on path / feynman only interrogates. Don't explain the same content five times.
- **Keep each lens tight**—this is a "single full sweep," and the deep dive is left for after the user picks. When in doubt, shorter, not more.
- Single-lens sub-entry points (use when the user wants just one): `learn-crossover` `learn-occam` `learn-graph` `learn-prototype` `learn-feynman`.
