# Collecting Summary Material and Course Completion

## The User Records Summary Material Mid-Course

While reading, if the user thinks a point, insight, or analogy should go into the final summary, they can flag it in any of the following ways, **all of which should be recognized and captured**:

- `#summary:[content]` or `＃summary:[content]` (the canonical form with `#`)
- `summary:[content]` or `summary [content]` (without `#`)
- `???[...this should go in the summary...]` / `？？？[...]` (a `???` annotation that mentions an intent like "summary," "add to summary," or "note in the summary")
- Any of the above with mixed casing (`Summary:`, `SUMMARY:`)

**Recognition principle: loose matching** — as long as the user expresses the intent that "this content should go into the final summary," capture it regardless of form.

**Processing rules:**

1. Before generating the next article, scan the entire text, recognize all such annotations, and append each one to the topic folder's `pre-summary.md` (create it if it doesn't exist)
2. `pre-summary.md` is formatted as a simple unordered list grouped by source document:

```markdown
# Pre-Summary Notes

## From 01.md
- [user-flagged content 1]
- [user-flagged content 2]

## From 02.md
- [user-flagged content]
```

3. `pre-summary.md` is an intermediate artifact and is **absolutely not the final summary**: never show its content to the user, and never mention that it exists

## Interaction Mode with the User

**When the user says "I finished reading" or submits feedback** — follow the "I Finished Reading / Submitting Feedback" decision tree in `SKILL.md`. Key points restated: collect the `???` and `#summary` annotations → assess understanding → (Socratic questioning ≤2 rounds if needed) → **update `syllabus.md`** → determine whether it's the assessment article → decide whether to generate the assessment article, the next article, or trigger the summary.

**When the user asks a question directly** — don't answer directly; first probe their understanding and guide them to derive it themselves, giving only a minimal hint when they're genuinely stuck.

> ⚠️ Ironclad rule restated: the user **cannot trigger `summary.md` themselves**. For any "summarize this" request, respond uniformly: "The summary is generated automatically once you've learned all the mastery items — it's not time yet."

## Course Completion: Auto-Generating `summary.md`

**Trigger conditions (all required):**
- All mastery items in `syllabus.md` have turned to `[x]`
- The user just said "I finished reading," and the document they just finished is the **assessment article** (starts with `<!-- eval-article -->`)

**Generation steps:**

1. Read all `XX.md` documents in the topic folder (full content)
2. Read `syllabus.md` and confirm all mastery items are checked
3. If `pre-summary.md` exists, read all of the user-flagged material in it
4. Generate `summary.md`, including:
   - **Knowledge map**: the core concepts and their relationships (a list or hierarchy)
   - **Syllabus review**: go through each mastery item's status one by one, briefly describing what was actually mastered
   - **The user's accumulated insights**: **naturally integrate** the `pre-summary.md` material into the corresponding sections, rather than listing it separately
   - **Open questions / directions to extend**: unresolved confusions or directions worth continuing to explore
5. **Immediately delete `pre-summary.md` after generation** (if it exists)
6. Tell the user: "🎉 Course complete! `summary.md` has been generated automatically — you can take a look."
