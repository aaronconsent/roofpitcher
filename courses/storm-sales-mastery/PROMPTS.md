# How to generate Storm Sales Mastery using your Google account

**Time required:** ~45 minutes. No coding. No API keys. All browser, free tier.

You will use two Google products:
- **NotebookLM** ([notebooklm.google.com](https://notebooklm.google.com)) — for grounded RAG + audio
- **AI Studio** ([aistudio.google.com](https://aistudio.google.com)) — for the lesson-content generation (Gemini 2.5 Pro free tier)

---

## Step 1 — Set up the NotebookLM notebook (~5 min)

1. Go to [notebooklm.google.com](https://notebooklm.google.com), sign in with your Google account.
2. Click **+ New notebook**. Name it `Roof Pitcher — Storm Sales Mastery`.
3. Click **Add source → Upload** and upload `courses/storm-sales-mastery/source/tyler-playbook.md` from this repo.
4. Wait 10 seconds for NotebookLM to index it. You'll see it appear in the left sidebar.

That's the knowledge base.

---

## Step 2 — Generate the 6 lesson contents (~25 min)

You have two options here. Both work. Pick one.

### Option A — Use NotebookLM directly (slightly higher quality, slightly slower)

For each of the 6 lessons, in NotebookLM's chat box, paste the prompt from **`prompts/lesson-prompt.md`** in this directory, replacing `{{LESSON_ID}}`, `{{LESSON_TITLE}}`, and `{{LESSON_FOCUS}}` with the values from `course.json`.

NotebookLM will return JSON grounded in Tyler's playbook. Copy the JSON output into `lessons/{{LESSON_ID}}.json`.

### Option B — Use AI Studio (faster, you control the model)

1. Go to [aistudio.google.com](https://aistudio.google.com), sign in.
2. New prompt → select **Gemini 2.5 Pro**.
3. Click **Insert** → upload `source/tyler-playbook.md` as context (or paste it inline).
4. Set **Response MIME type** to `application/json` (in the right panel under Advanced Settings).
5. For each lesson, paste the prompt from `prompts/lesson-prompt.md` with the placeholders filled in.
6. Save each output as `lessons/{{LESSON_ID}}.json`.

A filled-in example for Lesson 1 is in `prompts/example-lesson-01-prompt.md` — copy that exact text into AI Studio to get a real working lesson.

---

## Step 3 — Generate Audio Overviews (~10 min, NotebookLM only)

1. Back in NotebookLM, in the right panel click **Audio Overview**.
2. Click **Customize** and paste this prompt (per lesson):

   > Generate an audio overview focused exclusively on the section titled **"{{LESSON_TITLE}}"** in the source document. Two-host conversational style. ~10 minutes. Target audience: roofing sales reps. Quote specific scripts and frameworks from the source. Avoid generic sales advice — stay grounded.

3. Click **Generate**. Takes 3–5 min.
4. Download the MP3.
5. Rename to `{{LESSON_ID}}.mp3` and drop in `/public/audio/storm-sales-mastery/`.

Repeat for all 6 lessons (or do the 1 or 2 you want to demo first).

---

## Step 4 — Tell me you're done

Paste back into the chat:
- "Lessons done" → I'll wire up the Astro player routes pointing at the JSON + MP3 files
- Or, share one lesson JSON inline and I'll preview-render it immediately

---

## Cost so far

| Item | Cost |
|---|---|
| NotebookLM (free tier, ≤50 notebooks) | $0 |
| AI Studio Gemini 2.5 Pro (free tier, ≤2 RPM, plenty for one course) | $0 |
| Your time | ~45 min |
| **Total** | **$0** |
