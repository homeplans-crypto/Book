# Book

An LLM-maintained wiki. The pattern is described in [`llm-wiki-pattern.md`](./llm-wiki-pattern.md); the operational schema lives in [`CLAUDE.md`](./CLAUDE.md).

## Structure

```
raw/                immutable source documents (articles, papers, notes)
raw/assets/         images and attachments for raw sources
wiki/               LLM-generated markdown pages
wiki/index.md       content catalog, updated on every ingest
wiki/log.md         chronological activity log
wiki/sources/       one page per ingested raw document
wiki/entities/      people, orgs, places, products
wiki/concepts/      ideas, theories, techniques, themes
wiki/synthesis/     comparisons, analyses, filed-back queries
CLAUDE.md           schema and workflows for the LLM maintainer
```

## Workflow

1. **Ingest**: drop a source into `raw/`, ask Claude to ingest it.
2. **Query**: ask questions; Claude reads `wiki/index.md` first, then drills in.
3. **Lint**: periodically ask Claude to health-check the wiki.

Open this repo in Obsidian to browse with graph view and `[[wiki links]]`.
