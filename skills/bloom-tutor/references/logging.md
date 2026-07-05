# Learning Log and Progressive Loading

`learning-log.jsonl` lives in the working root directory; it is append-only and existing entries must never be overwritten or modified.

## `/organize learning` — Record Incremental Learning to the Log

**Trigger words:** `/organize learning`, "log what I've learned recently", "record a learning-log entry"

**Steps:**

1. **Read the log baseline**: read the root-level `learning-log.jsonl` and take the `date` and `courses` from the last entry (which article each topic was last read up to)
2. **Scan all topic folders**: list every subfolder under the root directory (excluding hidden directories and `.templates`), and for each topic:
   - List all `XX.md` files (excluding `syllabus.md` and `summary.md`)
   - Compare against the baseline to find the **newly added documents** (those completed since the last entry)
   - Read these new documents and distill 3-5 core concepts / key points
3. **Generate a log entry**: build the following single-line JSON and **append** it to `learning-log.jsonl`:

```json
{
  "date": "YYYY-MM-DD",
  "courses": [
    {
      "name": "topic name (folder name)",
      "new_docs": ["02.md", "03.md"],
      "key_concepts": ["concept 1", "concept 2", "concept 3"],
      "progress": "X of Y articles completed"
    }
  ],
  "summary": "one-sentence summary of this learning increment",
  "total_new_docs": 0
}
```

4. **Show the user a summary**: in the user's language, concisely present which new content was added to which topics, without repeating the raw JSON

**Rules:**
- Append only; never overwrite or modify existing entries
- Even when there are no new documents, still append an entry with `total_new_docs` set to 0 and `summary` set to "No new learning content this period"
- On the first run (empty log), scan all existing documents to establish the initial baseline and set `summary` to "Initialize learning log"

## `/view learning log` — Review History

**Trigger words:** `/view learning log`, "what have I learned recently", "review my learning history"

**Steps:**
1. Read all entries from the root-level `learning-log.jsonl`
2. In reverse chronological order (newest first), format and present, in the user's language: date, topic, number of new documents, and core concepts

## Progressive-Loading Principle

`learning-log.jsonl` is the **first entry point** for understanding the learning state. Whenever the user asks "what have I learned recently," "how's my progress," or anything else that requires knowing the learning state:

1. **Read `learning-log.jsonl` first** — it records the latest progress of every topic, the completed documents, and a summary of core concepts
2. **When the log is enough, don't proactively open specific documents** — answer directly from the log
3. **Only drill down into specific documents when**:
   - The user has a question about a concept and you need the original detail
   - The user explicitly asks "help me look at article N of topic XX"
   - The log alone can't answer, and you've told the user you need to look deeper

> Start from the lightest summary layer (the log), and drill down into specific documents only when needed, rather than loading all topic content at once.
