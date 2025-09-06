# [[Zettacasting]] Workflow in Obsidian

> A compact, actionable step‑by‑step guide for turning inputs into outputs using Zettacasting (aka zerocasting) inside Obsidian.

---

## Quick summary
This note captures a simple, repeatable 5‑step cycle for taking things you consume (books, tweets, conversations) and turning them into connected, reusable ideas and outputs. The goal: capture quickly, process thoughtfully, connect laterally, produce reliably, and record reactions.

---

## The 5‑step Zettacasting Cycle (short)
1. **Capture** — fleeting notes & literature notes (get it down).
2. **Process** — make notes atomic + searchable.
3. **Connect** — link laterally using the Idea Compass.
4. **Produce** — turn notes into newsletter posts, tweets, drafts.
5. **Track reactions** — save responses, replies and new sparks.

> Each step below contains explicit, *do this now* actions you can paste into Obsidian templates.

---

## Step 1 — Capture (practical)

- **What to capture:** anything that *interests you* — [[fleeting thoughts]], [[literature]] - book insights, quotes, examples, questions. Don't self‑censor.
- **Where to capture:** root folder (no folders needed), a Capture quick note, or mobile quick capture plugin.
- **Template to use (quick capture):**

```
#capture/{{date:YYYY-MM-DD}} - {{time}}
---
type: fleeting / literature
source: [[source]] / URL
short: One-line summary
text: |
  Paste / type verbatim idea or quote
tags: #capture
---
```

- **Rules:**
  - Keep capture frictionless — prioritize getting the thought down over perfect structure.
  - Mark `type:` so you can later filter (fleeting / literature).

---

## Step 2 — Process (make atomic + searchable)
**Goal:** turn messy captures into small, reusable building blocks.

No need to have folders - 
Easy to be searched
Make Notes Atomic
Make it more Search Friendly

Actions (do these when you have ~10 minutes):
1. Open captured notes and **split** them into at most one idea per note. Use three atomic categories: `Question`, `Idea`, `Supplement` (anecdote/quote/study).
2. For each new atomic note, add a short, searchable title and 3–5 keywords in the frontmatter or top.
3. Add **status tags** for workflow: `#build`, `#check`, `#toread`, `#newsletter`, `#tweet`.
4. Add content metadata (source, page, URL, date).

**Atomic note template (paste when processing):**

```
# Idea: Sampling period — Range
keywords: sampling period, specialization, breadth
type: idea
status: #build  #newsletter
source: Range — David Epstein
summary: One-line summary of the core idea.
note:
  - Short paragraph explaining the idea in your own words.
links: [[Sampling period — example 1]]
---
```

**Supplement (anecdote/study) template:**

```
# Study: Youth sports sampling study
type: supplement
keywords: youth sports, sampling
source: [Author, Year] / URL
summary: Short summary of method & finding
link-to-idea: [[Idea: Sampling period — Range]]
status: #reference
```

**Tips:**
- When splitting, err on the side of smaller notes. A good rule: could this fit on an index card? If yes, it’s atomic.
- Use the quick switcher (`Ctrl+O`) to check for existing titles before creating new notes — avoids accidental duplication and encourages linking.

---

## Step 3 — Connect (Idea Compass + lateral linking)
**Goal:** force lateral thinking and create serendipitous links.

**Idea Compass (practical):** For a central note, create four sub‑questions on the note: **West (similar), East (opposite), North (theme/question), South (leads to / consequences)**.

**Compass block (paste inside an idea note):**

```
## Idea Compass
- **West (Similar / supporting):** [[T-shaped person]]; [[Polymath]]
- **East (Opposite / counterpoint):** 10,000 hour rule; specialization argument
- **North (Theme / question):** How does sampling period affect career trajectories?
- **South (Leads to):** Personal monopoly vs. niche; long-term creativity
```

**Connecting actions:**
1. Open the note's compass and create double‑bracket links for each concept you think of — even if the target note doesn't exist yet (create placeholders).
2. For each link you add, write 1–2 lines explaining the relationship (why similar / why opposite).
3. Tag the central note with `#build` if you want to elaborate later; `#check` if you need to verify sources.

**Daily practice:** when processing new notes, spend 5 minutes adding at least *one* compass connection.

---

## Step 4 — Produce (turn notes into output)
**Goal:** reliable output without reinventing the wheel.

**Workflow:**
1. Create a `Writing Idea Tracker` dataview to surface notes tagged `#newsletter` or `#tweet`.
2. Use those notes as building blocks — each atomic idea becomes a paragraph, anecdote, or tweet.
3. Draft quickly: assemble 3–5 linked notes into an outline, then write.

**Dataview example (paste into a note page):**

```dataview
table status, file.cday as created
from ""
where contains(tags, "#newsletter")
sort file.cday desc
```

**Production checklist:**
- [ ] Pick 1 `#newsletter` note
- [ ] Gather 1–2 `supplement` notes (quotes, studies)
- [ ] Build a 3‑point outline using linked notes
- [ ] Draft and publish (or queue)
- [ ] Tag published note with `#published` and add the output link (tweet URL / newsletter id)

---

## Step 5 — Capture reactions & serendipity
**Goal:** fold conversations & feedback back into the vault so output + reaction become new input.

**What to save:** replies, DMs, comments, new ideas that came from sharing.

**Reaction note template:**

```
# Reaction: Tweet about friendship measured in likes
source-output: Tweet YYYY-MM-DD
summary: Short summary of responses and notable replies
notable-comments:
  - @user: "ship idea" — link [[Ship concept]]
follow-ups:
  - create note [[Ship as verb]] #toread
```

**Actions:**
- Tag reactions with `#reaction` and link to the source note(s) that inspired the output.
- If a reply surfaces a new idea, capture it as a fleeting note and process it later.

---

## Practical systems and conventions (recommended)
- **Vault structure:** flat root (no folders necessary). Use tags + dataview to retrieve.
- **Tag system (recommended):**
  - `#idea`, `#question`, `#supplement`
  - status tags: `#build`, `#check`, `#toread`, `#published`
  - output tags: `#newsletter`, `#tweet`, `#draft`
- **Title style:** `Type: Short keyword — Source` (e.g., `Idea: Sampling period — Range`). This makes quick switcher discovery obvious.
- **Keywords:** add 2–4 keywords per note to improve full‑text search hits (treat like SEO for your brain).
- **Quick processing routine:** Every 2–3 days, allocate 10–15 minutes to process captured notes.

---

## Short worked example (Sampling period)
1. **Captured (fleeting):** raw quote + idea in `#capture`.
2. **Processed:** created `Idea: Sampling period — Range` and three `Supplement` notes (anecdote A, study B, quote C). Tags: `#idea #build #newsletter`.
3. **Connected:** used Idea Compass linking to `[[T-shaped person]]`, `[[Polymath]]`, and `[[10k-hour rule]]` (added text explaining the relation).
4. **Produced:** assembled 2 supplements + idea into a short newsletter draft. Tag draft with `#newsletter` and final note with `#published` after sending.
5. **Tracked reactions:** saved replies in `Reaction: Sampling period — newsletter — 2025-09-XX` and linked follow up ideas.

---

## Useful snippets (copy into a snippets file)
- Quick capture command: `Template: Capture` (see template above).
- Atomic note template: `Template: Idea` (see above).
- Compass snippet: copy the `## Idea Compass` block.
- Dataview: writing idea tracker (see above)

---

## Daily habit micro‑prompts
- *Today’s 5‑minute capture:* open phone and write one fleeting thought.
- *Processing sprint (10 minutes):* split 3 captured items into atomic notes.
- *Connecting minute (5 minutes):* add one compass link to an idea.

---

## Final notes (philosophy & sanity)
- Write everything that interests you — don't judge. Time + connection will reveal value.
- Favor linking over strict folders. Tags + search scale better.
- Treat Zettacasting as training your attention, not a game of perfect organization.

---

*If you want, I can also create ready-to‑paste Obsidian templates for the Capture, Idea, Supplement and Reaction notes (YAML frontmatter versions + community plugin friendly).*

