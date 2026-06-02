# Ready-to-paste prompt for Lesson 1

Copy everything below the `---` and paste into AI Studio (Gemini 2.5 Pro, Response MIME = `application/json`, source playbook uploaded as context).

---

You are generating one lesson of a roofing-sales course called **Storm Sales Mastery**, taught by Tyler Mentges. You have been given Tyler's source playbook as grounding context. Use ONLY information from the playbook (or natural elaborations consistent with Tyler's voice). Do not invent statistics or make up scripts that contradict the source.

**Voice rules:**
- Direct, blue-collar, no fluff. Tyler is a roofer first, trainer second.
- Short sentences. Strong verbs. Zero corporate speak.
- "You" not "one." "Get to work" not "execute the strategy."
- Frameworks and scripts must match the source exactly. Examples and elaboration are yours to write.

**Lesson to generate:**
- Lesson ID: `01-storm-mindset`
- Lesson Title: **The Storm Sales Mindset**
- Focus: The mental model that separates pros from amateurs. Why storm sales is a 14-day window. Why the homeowner is not the enemy. The "inspector, not closer" frame. Why systems beat heroes. The ethical floor every rep should operate above.

**Return ONLY valid JSON, exactly matching this schema:**

```json
{
  "id": "01-storm-mindset",
  "title": "The Storm Sales Mindset",
  "duration_min": 0,
  "summary": "One sentence, ≤25 words, plain English, what the rep will be able to DO after this lesson.",
  "body_markdown": "Full lesson content as markdown. ~1200-1800 words. Use H2 (##) section headings. Include at least one direct script block quoted verbatim from the source where relevant, formatted as a markdown blockquote. Include real numbers where the source provides them.",
  "key_takeaways": [
    "5 short bullet points, ≤15 words each",
    "Action-oriented",
    "Memorable, the rep could write each on a sticky note"
  ],
  "scripts": [
    {
      "name": "Optional: name of a script taught in this lesson",
      "when_to_use": "Trigger context",
      "lines": ["line 1", "line 2", "line 3"]
    }
  ],
  "quiz": [
    {
      "q": "Multiple choice question testing recall of a key concept",
      "choices": ["A", "B", "C", "D"],
      "answer_index": 0,
      "explanation": "Why this is the right answer, one sentence."
    }
  ],
  "homework": "One concrete action the rep does in the field tomorrow."
}
```

Quality checklist: ≥3 quiz questions, at least one verbatim script block if relevant, no invented stats, Tyler's voice throughout. Return JSON only.
