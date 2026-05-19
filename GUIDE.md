# Your Architecture Knowledge Bank — A Plain-English Guide

This is a personal research library that grows with you. Every article you read, every lecture you attend, every book chapter you annotate — you can add it here, and Claude will read it, summarize it, connect it to everything else you've collected, and help you find the ideas inside it.

---

## What Is This, Exactly?

Think of it as a Wikipedia you build yourself, about the things *you* care about.

- **You collect sources** — articles, PDFs, transcripts, your own notes
- **Claude reads and files them** — writing a summary, tagging the people and ideas inside, linking everything together
- **You ask questions** — and Claude answers using only what's in your library, citing its sources

The more you add, the smarter it gets. After a few months, you have a searchable record of everything you've learned.

---

## What You Need

1. **Claude** — either:
   - [claude.ai](https://claude.ai) with a Pro subscription (easiest), or
   - Claude Code (the desktop/terminal app) with an API key
2. **This folder** — open it as your working directory in Claude
3. **Obsidian** *(optional but recommended)* — a free app that lets you browse your wiki visually, follow links between pages, and see a graph of how everything connects. Download at [obsidian.md](https://obsidian.md). Open this folder as a vault.

---

## First Time Setup

1. Open this folder in Claude (or point Claude Code at it)
2. Say: **"Read CLAUDE.md and index.md to get started"**
3. Claude will read its instructions and the existing content catalog
4. You're ready

That's it. Claude handles everything else.

---

## How to Add a Source

There are three ways:

### Option A — Paste text directly
Copy the text of an article, transcript, or your own notes. Then say:

> "Ingest this: [paste the text]"

### Option B — Drop a PDF into the `raw/` folder
Save the file to the `raw/` folder in this directory. Then say:

> "Ingest raw/the-filename.pdf"

### Option C — Give Claude a URL
> "Ingest this article: https://..."

Claude will then:
- Tell you the 3–5 most important takeaways
- Ask if there's anything specific you want to emphasize
- Write a summary page, create pages for the people and ideas mentioned, and update the catalog

---

## How to Ask Questions

Just ask naturally. Examples:

- *"What did Zaha Hadid say about the relationship between software and form?"*
- *"Compare brutalism and parametric design — what do they share?"*
- *"Summarize everything I know about Tadao Ando"*
- *"What are the recurring criticisms of deconstructivism across my sources?"*
- *"I'm writing about sustainable materials — what's relevant in my library?"*

Claude will read the relevant pages and synthesize an answer. If the answer is particularly rich, it will offer to save it as a new page so you can find it again later.

---

## How to Browse Your Wiki

If you have Obsidian installed:

1. Open Obsidian → **Open folder as vault** → select this folder
2. Click any page in `wiki/` to open it
3. Click any `[[linked term]]` to jump to that page
4. Open the **Graph view** (left sidebar icon) to see how everything connects visually

You can also just read the files — they're plain markdown, readable in any text editor.

---

## How to Check the Health of Your Wiki

Occasionally say:

> "Lint" or "Health check"

Claude will scan all your pages and tell you:
- Any pages that nothing links to (orphans)
- Any people or concepts mentioned in text but not properly linked
- Any contradictions between sources
- Gaps worth filling — questions your library can't yet answer

---

## Tips for Architects

**Good things to add:**
- Magazine articles (Dezeen, Architectural Review, El Croquis interviews)
- Book chapters or essays (Venturi, Koolhaas, Frampton, Zumthor)
- Lecture transcripts or talk notes
- Project briefs or competition programmes you've studied
- Your own site visit notes ("I visited the Therme Vals today — here's what I observed")
- Building reviews or critic essays

**Good questions to ask over time:**
- *"What materials keep appearing across the projects I've studied?"*
- *"Which architects have written about light and how do their views differ?"*
- *"Build me a timeline of the key moments in brutalism based on my sources"*

**One habit that makes a big difference:**
After any lecture, talk, or site visit — even just 5 minutes of notes — add them as a source. The library compounds: one note is nothing, fifty notes is a research asset.

---

## The Worked Example

The `wiki/` folder already contains one complete example — an ingested profile of **Zaha Hadid**. It shows:

- `wiki/sources/2026-05-16-zaha-hadid-guardian-profile.md` — what a source page looks like
- `wiki/entities/Zaha-Hadid.md` — what a person page looks like
- `wiki/entities/Zaha-Hadid-Architects.md` — what a firm page looks like
- `wiki/concepts/parametric-design.md` — what a concept page looks like

Read these before you start adding your own content to get a feel for the format.

---

## Quick Reference

| What you want to do | What to say to Claude |
|--------------------|-----------------------|
| Add a source | "Ingest this: [text or URL or filename]" |
| Ask a question | Just ask it |
| See a summary of a person/building | "What do I know about [name]?" |
| Compare two things | "Compare [X] and [Y]" |
| Find connections | "What connects [X] and [Y] in my library?" |
| Check wiki health | "Lint" |
| Save a good answer | "Save this as a synthesis page" |
| Start a session | "Read CLAUDE.md and index.md" |
