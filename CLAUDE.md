# CLAUDE.md — Wiki Schema

This repo is an LLM-maintained wiki. You (Claude) are the maintainer. The human curates sources and asks questions; you do the reading, writing, cross-referencing, and bookkeeping. See `llm-wiki-pattern.md` for the underlying pattern.

## Layout

- `raw/` — immutable source documents (articles, papers, transcripts, notes). **Never edit files here.** Only read.
- `raw/assets/` — images and binary attachments for raw sources.
- `wiki/` — all LLM-generated markdown pages. You own this directory.
- `wiki/index.md` — content catalog. Update on every ingest.
- `wiki/log.md` — chronological activity log. Append on every ingest, query-filed-back, or lint.
- `CLAUDE.md` — this file. The schema. Co-evolve it with the human as workflows mature.

## Page types

Put every wiki page in `wiki/` and choose a type:

- **Source pages** (`wiki/sources/<slug>.md`): one per ingested raw document. Summary, key claims, entities mentioned, links to related pages.
- **Entity pages** (`wiki/entities/<slug>.md`): people, orgs, places, products — anything that can be named.
- **Concept pages** (`wiki/concepts/<slug>.md`): ideas, theories, techniques, recurring themes.
- **Synthesis pages** (`wiki/synthesis/<slug>.md`): comparisons, analyses, timelines, filed-back answers to queries.

Slugs are lowercase, kebab-case. Use Obsidian-style `[[wiki links]]` (e.g. `[[entities/ada-lovelace]]`) so the graph view works.

## Frontmatter

Every page starts with YAML frontmatter so Dataview can query it:

```yaml
---
type: source | entity | concept | synthesis
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: [sources/foo, sources/bar]   # for entity/concept/synthesis pages
tags: [tag1, tag2]
---
```

## Workflows

### Ingest

When the human drops a file into `raw/` and asks to ingest:

1. Read the source end-to-end. If it references images in `raw/assets/`, view the relevant ones.
2. Discuss key takeaways with the human before writing. Confirm emphasis and scope.
3. Create `wiki/sources/<slug>.md` with: one-paragraph summary, key claims (bulleted, each citable back to the source), entities/concepts mentioned.
4. For each entity and concept the source touches, either create a new page or update the existing one. Add the new source to its `sources:` frontmatter. Note any contradictions with existing claims inline (e.g. `> Contradicts [[sources/other-doc]] which claims X.`).
5. Update `wiki/index.md` — add the new source and any new entity/concept pages.
6. Append to `wiki/log.md` using the format below.
7. Report back: which pages created, which updated, any contradictions flagged.

A single ingest typically touches 10–15 files. That's expected.

### Query

When the human asks a question:

1. Read `wiki/index.md` first to identify relevant pages.
2. Read those pages. Follow `[[links]]` as needed.
3. Answer with citations to wiki pages (and transitively to sources).
4. If the answer is substantive — a comparison, timeline, analysis, new connection — offer to file it as `wiki/synthesis/<slug>.md` and append to `log.md`. Don't let good synthesis vanish into chat.

### Lint

When the human asks for a health check:

- Contradictions across pages
- Stale claims newer sources have superseded
- Orphan pages (no inbound `[[links]]`)
- Concepts/entities mentioned but lacking their own page
- Missing cross-references where two pages clearly relate
- Data gaps worth filling with a web search or new source
- Suggest follow-up questions and sources to look for

Report findings; don't auto-fix structural issues without confirmation.

## Log format

Append to `wiki/log.md`. Consistent prefix so `grep "^## \[" wiki/log.md` works:

```
## [YYYY-MM-DD] ingest | <source title>
- created: sources/foo, entities/bar
- updated: concepts/baz, entities/qux
- notes: <one line, optional>

## [YYYY-MM-DD] query | <short question>
- filed: synthesis/<slug>  (if filed back)

## [YYYY-MM-DD] lint
- <short summary of findings>
```

## Conventions

- Default to writing no filler. Wiki pages should be terse and dense — claims, links, citations. Not essays.
- Every non-trivial claim on an entity/concept/synthesis page should cite at least one `[[sources/...]]` page.
- When a new source contradicts an existing claim, keep both. Flag the contradiction inline and in the log. Don't silently overwrite.
- Prefer editing existing pages over creating new ones. Only create a new entity/concept page when it's referenced in two or more sources, or when the human asks.
- Never touch `raw/`. If a source is wrong, note it on the source page — don't edit the raw file.
