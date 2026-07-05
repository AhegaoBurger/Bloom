---
name: learn-graph
description: Use when the user wants to systematically learn a new field, doesn't know where to start, or worries their learning "isn't systematic enough." Together with the user, build a knowledge graph of the field's concepts/uses/parent-child nodes using the "knowledge-graph learning method" (the act of building the graph yourself IS the learning), flag the nodes with the highest reuse value and the "points you can enter from common sense alone," lay out an effective learning path, and answer "how much is enough." Triggers: learn field X systematically, where do I start, my learning feels unsystematic, I want the full picture of X, plan a learning path, how big is this field.
---

# Knowledge-Graph Learning Method (learn-graph)

> Core creed: **The process of building the graph yourself, step by step, IS the most effective learning—don't just adopt someone else's ready-made graph.** For almost any body of knowledge, there's a point where common sense alone is enough to get you in the door.

## When to use

The user wants to systematically break into a new field, or is anxious about "not learning systematically enough / not knowing when they've done enough."

## Process (the key: build it *with* the user, don't just hand over one finished graph)

### Step 1: Pin down the target field X and the goal

Why is the user learning X? (Picks up from the "established problem" in `learn-occam`.) The goal decides how fine-grained the graph needs to be.

### Step 2: Build the graph—capture just three things

**Concept/name · use · contextual relationships (parent-child nodes)**:

- Child node = what X rests on / is built upon; parent node = what goal X serves.
- **Fill it in together by asking questions** (you only learn by building the graph yourself)—don't dump it all at once. Give the skeleton first, and leave nodes for the user to fill in.

### Step 3: Mark the two key things

- **Reuse value**: which nodes have many parents (like Python) → learn these first, the payoff is highest.
- **Entry point**: which node "can be entered from common sense alone" → the starting point of the learning path.

### Step 4: Output the learning path + granularity

Starting from the entry point, lay out one effective path along the parent-child relationships. Switch granularity freely as needed (field-level graph → sub-discipline graph). "How much is enough" = it's enough to cover the nodes that solve the goal from Step 1; you don't have to learn all of it.

### Step 5: Handoff

- Not sure whether a node is missing prerequisite knowledge → this is exactly the graph's strength, and it's already marked on the graph.
- Found the entry point and it's time to get hands-on → switch to `learn-prototype` (find the "crappiest prototype" starting point on the graph).

## Notes

> ⚠️ **Ironclad rule · Only use confirmed, already-known knowledge**: To judge what the user "already knows," you may only use knowledge they've **confirmably learned** (either stated in their own words or a reliable background); it is **strictly forbidden** to treat "the material currently being taught / the article author's background / someone else's knowledge in the conversation" as something the user knows. Not sure → just ask "⚠️ Have you learned ___?"—never assume on their behalf.

- Emphasize "build it yourself": use questions to keep the user involved, don't show off one perfect graph.
- Sibling skills: `learn-occam` (should you learn it) `learn-crossover` (what you already know) `learn-prototype` (get hands-on) `learn-feynman` (self-check).
