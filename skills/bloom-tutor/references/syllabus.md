# Course Syllabus `syllabus.md` Rules

**Core philosophy: fixed learning objectives, flexible learning path.**

- The syllabus specifies **what you'll be able to do once you finish this course**, not "what article 01 covers, what article 02 covers"
- There's no limit on the number of documents — some people finish in 4 articles, others need 10; it depends entirely on their starting point and pace
- Every learning outcome in the syllabus is a specific, verifiable ability, not a vague "know about / understand"
- The syllabus supports three learning depths: **simple**, **standard**, **deep**. When the user doesn't specify one, default to **standard**.

## Format

```markdown
# [Topic Name] · Course Syllabus

> This syllabus defines all the abilities you'll master after completing this topic.
> Learning depth: [simple / standard / deep]
> The number of documents varies from person to person, but the mastery content is not compromised.

## Core Mastery Items

After completing this topic, you will be able to:

### [Module One Name]
- [ ] [specific ability description, phrased as "be able to …", verifiable]
- [ ] [specific ability description]

### [Module Two Name]
- [ ] [specific ability description]
- [ ] [specific ability description]

(grouped by knowledge module, each item a checkbox to be checked off after learning)

## Not in Scope for This Topic

- [explicitly list which related topics this course does not cover, to avoid mismatched expectations]

## Learning Progress

| Document | Mastery Items Covered | Date Generated |
|------|-----------|---------|
| (a row is appended automatically after each new document is generated) |
```

## Requirements for Generating the Syllabus

1. Every mastery item must be a **verifiable behavior** (can explain, can derive, can apply, can judge); banned are unverifiable phrasings like "know about X" or "be familiar with Y"
2. The learning depth determines how far the syllabus expands:
   - **Simple**: 2-3 modules, 8-10 mastery items; focus on the main thread, the minimum necessary concepts, and high-frequency applications
   - **Standard**: 3-4 modules, 10-12 mastery items; cover the core concepts, key reasoning, typical applications, and common pitfalls
   - **Deep**: 4-5 modules, 12-15 mastery items; add first principles, underlying mechanisms, boundary conditions, counterexamples, and transfer judgment
3. Modules must be organized by the knowledge's inherent logic, and number no more than 5
4. **"Not in Scope for This Topic" must be filled in**, to help the user form a clear sense of the boundaries

## Linkage Between the Syllabus and the Documents

- **Before** generating each new document, check which mastery items in the syllabus aren't yet covered, to keep overall progress on course; each article's content should map to at least one mastery item in the syllabus, and don't generate content unrelated to the syllabus
- **After** generating each new document, you must immediately update this file:
  1. Change the `[ ]` for the mastery items this article covers to `[x]`
  2. Append a row to the "## Learning Progress" table: document number, mastery items covered (a short list), and date generated
- When all mastery items have turned to `[x]`, **do not generate `summary.md` directly**; instead generate the "assessment article" first (see `articles.md`)
