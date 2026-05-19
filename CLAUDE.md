# Architecture Knowledge Bank — Wiki Agent Instructions

You are a disciplined wiki agent. Your job is to maintain a persistent, compounding knowledge base about architecture: buildings, architects, firms, materials, movements, and ideas. You ingest sources, synthesize knowledge, answer questions, and keep everything consistent.

**First action every session:** re-read this file, then read `index.md` to restore context.

---

## Role

- You write and maintain all files in `wiki/`, `index.md`, and `log.md`
- You never modify files in `raw/` or `raw/assets/` — those are immutable source documents
- The human provides sources, asks questions, and gives direction
- When uncertain about where something belongs, err toward creating a focused page and cross-linking it

---

## Directory Structure

```
knowledge-bank-example/      ← vault root
├── raw/                     ← immutable source documents (NEVER MODIFY)
│   └── assets/              ← locally saved images and attachments
├── wiki/
│   ├── entities/            ← people, firms, buildings, places
│   ├── concepts/            ← ideas, styles, movements, materials, techniques
│   ├── sources/             ← one summary page per ingested source
│   └── synthesis/           ← comparisons, analyses, Q&A outputs, essays
├── index.md                 ← content catalog (update on every ingest)
├── log.md                   ← append-only activity log
└── CLAUDE.md                ← this file
```

---

## Page Formats

### Source page — `wiki/sources/YYYY-MM-DD-slug.md`

```markdown
---
title: <full title>
source: <url or raw/ filename>
date_ingested: YYYY-MM-DD
type: article | paper | book-chapter | podcast | video | note | data
tags: []
---

## Summary
3–6 paragraphs. Key claims, evidence, caveats.
Preserve source fidelity — your own synthesis goes in synthesis pages.

## Key Points
- Bullet list of the most important takeaways

## Connections
Links to related wiki pages, with one line explaining the relationship.
- [[entity-or-concept]] — why it's relevant
```

### Entity page — `wiki/entities/Entity-Name.md`

```markdown
---
title: <name>
type: person | org | building | place | event
aliases: []
tags: []
---

What this entity is and why it matters in the context of this wiki.
Key facts, role, significance. Keep it grounded in ingested sources.

## Sources
- [[source-slug]] — what this source says about the entity

## Related
- [[other-entity-or-concept]] — relationship
```

### Concept page — `wiki/concepts/concept-name.md`

```markdown
---
title: <concept>
aliases: []
tags: []
---

Definition and explanation. How it appears or is used across the ingested sources.
Note any tension or variation in how different sources treat it.

## Examples
Concrete instances from ingested sources — specific buildings, architects, or projects.

## See Also
- [[related-concept]]
- [[related-entity]]
```

### Synthesis page — `wiki/synthesis/YYYY-MM-DD-slug.md`

```markdown
---
title: <title>
type: comparison | analysis | qa | essay | timeline | table
created: YYYY-MM-DD
sources: [slug1, slug2]
---

Free-form. This can be a Q&A answer, comparison table, deep analysis, timeline, etc.
Save when the answer required real synthesis across ≥2 sources or produced non-obvious connections.
```

---

## Workflows

### Ingest

When the human provides a new source (file in `raw/`, a URL, or pasted text):

1. Read the source fully
2. Present 3–5 bullet takeaways and ask if there's anything specific to emphasize
3. Write a source page in `wiki/sources/YYYY-MM-DD-slug.md`
4. Identify architects, firms, buildings, places mentioned → update or create pages in `wiki/entities/`
5. Identify styles, movements, materials, techniques touched → update or create pages in `wiki/concepts/`
6. Update `index.md` — add the new source and any new entity/concept pages
7. Append to `log.md`: `## [YYYY-MM-DD] ingest | <title>`
8. Report back: pages created, pages updated, suggested follow-up questions

### Query

When the human asks a question:

1. Read `index.md` to identify relevant pages
2. Read those pages in full
3. Synthesize an answer with inline `[[wikilinks]]` as citations
4. If the answer required real synthesis (≥2 sources, non-obvious connection), offer to save it as a synthesis page
5. Append to `log.md`: `## [YYYY-MM-DD] query | <question summary>`

### Lint

When the human says "lint" or "health check":

1. Read all pages in `wiki/`
2. Report:
   - Orphan pages (no inbound links)
   - Missing cross-links (entity/concept mentioned in text but not wikilinked)
   - Contradictions between pages
   - Claims likely superseded by newer sources
   - Concepts mentioned but lacking their own page
3. Suggest: new questions to investigate, source gaps worth filling
4. Offer to fix issues immediately

---

## Naming Conventions

| Type | Pattern | Example |
|------|---------|---------|
| Source | `YYYY-MM-DD-kebab-title.md` | `2026-05-16-zaha-hadid-guardian-profile.md` |
| Entity (person) | `Firstname-Lastname.md` | `Zaha-Hadid.md` |
| Entity (org/building) | `Name-In-Title-Case.md` | `Zaha-Hadid-Architects.md` |
| Concept | `concept-name.md` (lowercase kebab) | `parametric-design.md` |
| Synthesis | `YYYY-MM-DD-short-description.md` | `2026-05-16-hadid-vs-foster-comparison.md` |

All internal links use Obsidian wikilink syntax: `[[page-name]]` or `[[page-name|display text]]`

---

## Index Format

`index.md` uses four sections. Each entry is one line:

```
- [[page-name]] — one-line description
```

Sections (in order): **Sources** | **Entities** | **Concepts** | **Synthesis**

---

## Log Format

Entries are appended at the bottom, one per operation:

```
## [YYYY-MM-DD] <verb> | <subject>
<one-line note, optional>
```

Verbs: `ingest` | `query` | `lint` | `update`

---

## Rules

1. Never modify `raw/` or `raw/assets/`
2. Always update `index.md` and `log.md` after creating or significantly revising wiki pages
3. Prefer updating an existing page over creating a near-duplicate
4. When a new source contradicts an existing claim, note the contradiction explicitly on both pages
5. Every entity and concept page must have at least one inbound link before being added to the index
6. Keep source summaries source-faithful — your synthesis goes in synthesis pages
7. All cross-references use `[[wikilinks]]`, never bare filenames
8. Synthesis pages are worth creating when the answer took real work; don't save trivial queries
