# CLAUDE.md — Wiki Schema

This repo is an LLM-maintained wiki. You (Claude) are the maintainer. The human curates sources and asks questions; you do the reading, writing, cross-referencing, and bookkeeping. See `llm-wiki-pattern.md` for the underlying pattern.

**Domain:** Fujifilm X100VI film recipes and amateur photography practice. The goal is not just to catalog recipes but to **improve the human's technique and skill over time** — the wiki closes a feedback loop between what's read, what's shot, and what's learned. See "Domain mapping" below for how the generic page types specialize to this domain.

## Layout

- `raw/` — immutable source documents (articles, papers, transcripts, notes). **Never edit files here.** Only read.
- `raw/assets/` — images and binary attachments for raw sources.
- `wiki/` — all LLM-generated markdown pages. You own this directory.
- `wiki/recipes/` — one page per Fujifilm film recipe (structured settings + intended look). See "Recipe pages".
- `wiki/index.md` — content catalog. Update on every ingest.
- `wiki/log.md` — chronological activity log. Append on every ingest, query-filed-back, or lint.
- `CLAUDE.md` — this file. The schema. Co-evolve it with the human as workflows mature.

## Page types

Put every wiki page in `wiki/` and choose a type:

- **Source pages** (`wiki/sources/<slug>.md`): one per ingested raw document. Summary, key claims, entities mentioned, links to related pages.
- **Recipe pages** (`wiki/recipes/<slug>.md`): one per Fujifilm film recipe. Strict frontmatter (every dial setting as a field) + a short prose note on the look and when to use it. See "Recipe frontmatter".
- **Entity pages** (`wiki/entities/<slug>.md`): people, orgs, places, products — anything that can be named.
- **Concept pages** (`wiki/concepts/<slug>.md`): ideas, theories, techniques, recurring themes.
- **Synthesis pages** (`wiki/synthesis/<slug>.md`): comparisons, analyses, timelines, filed-back answers to queries.

Slugs are lowercase, kebab-case. Use Obsidian-style `[[wiki links]]` (e.g. `[[entities/ada-lovelace]]`) so the graph view works.

### Domain mapping

How the generic types specialize to Fujifilm photography:

- **recipes/** — each film recipe (e.g. `recipes/kodak-portra-400`). The structured core of the wiki.
- **concepts/** — photography technique: composition, exposure, focus modes, reading light, dynamic range, white balance theory, street etiquette, when to shoot JPEG vs RAW.
- **entities/** — the `entities/x100vi` body; each film simulation (`entities/classic-chrome`, `entities/classic-neg`, etc.); diffusion/ND filters; recipe authors (`entities/fuji-x-weekly`, `entities/ritchie-roesch`); photographers the human studies.
- **sources/** — recipe articles, technique articles, YouTube transcripts, and the human's own shoot notes / debriefs.
- **synthesis/** — "best recipe for harsh sun", recipe comparison tables, technique progressions, and **shoot debriefs** that close the skill-improvement loop (see Workflows).

## Frontmatter

Every page starts with YAML frontmatter so Dataview can query it:

```yaml
---
type: source | recipe | entity | concept | synthesis
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: [sources/foo, sources/bar]   # for recipe/entity/concept/synthesis pages
tags: [tag1, tag2]
---
```

### Recipe frontmatter

Recipe pages use a strict, fixed schema so Dataview can filter and compare them. Every recipe page starts with:

```yaml
---
type: recipe
created: YYYY-MM-DD
updated: YYYY-MM-DD
camera: X100VI
film_sim: Classic Negative          # the Fujifilm film simulation, full name
author: Fuji X Weekly               # creator/source of the recipe, or "self"
sources: [sources/foo]              # where it came from
dynamic_range: DR400                # DR100 | DR200 | DR400 | DRAUTO
grain: "Strong, Large"              # off | "Weak/Strong, Small/Large"
color_chrome: Strong                # off | Weak | Strong
color_chrome_fx_blue: Weak          # off | Weak | Strong
white_balance: "Auto"               # e.g. Auto | "5500K" | "Daylight"
wb_shift: "R+2 B-5"                 # red/blue shift
highlight: -1                       # tone curve, -2..+4
shadow: +1                          # tone curve, -2..+4
color: +2                           # -4..+4
sharpness: -2                       # -4..+4
clarity: 0                          # -5..+5
noise_reduction: -4                 # -4..+4
iso: "Auto, max 6400"               # ISO or Auto-ISO ceiling
exposure_comp: "+1/3 to +2/3"       # typical EV bias
best_for: [overcast, street, portrait]   # conditions/subjects this look suits
tags: [recipe, classic-neg]
---
```

Below the frontmatter, keep it terse: a 2–4 sentence note on the look (what it does to color/contrast), when to reach for it, and any caveats. Link the film sim (`[[entities/classic-negative]]`), the author (`[[entities/fuji-x-weekly]]`), and the source page. If a field doesn't apply to a given camera/recipe, set it to `n/a` rather than omitting it — keep the schema stable.

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

### Recipe ingest

When the human pastes or drops in a film recipe (from Fuji X Weekly, another creator, or their own dialed-in settings):

1. Parse it into the strict **Recipe frontmatter** schema. Map every dial setting to a field. If the source omits a setting, infer the camera default and mark it (e.g. `clarity: 0  # default, not specified`).
2. Create `wiki/recipes/<slug>.md`. Slug after the recipe's common name (e.g. `recipes/kodak-tri-x-400`).
3. Add/update the film-sim entity page (`entities/<film-sim>`) and the author entity page; add this recipe to their pages and `sources:` frontmatter.
4. If a raw article was the source, also create the `sources/` page per normal Ingest. If the human just pasted dial settings with no article, the recipe page is self-sourced — set `author: self` or cite the creator inline, no `sources/` page needed.
5. Update `wiki/index.md` (Recipes section) and append to `wiki/log.md`.
6. Report: recipe filed, what look it's for, and which existing recipes it's most similar to.

### Query

When the human asks a question:

When the human asks a question:

1. Read `wiki/index.md` first to identify relevant pages.
2. Read those pages. Follow `[[links]]` as needed.
3. Answer with citations to wiki pages (and transitively to sources).
4. If the answer is substantive — a comparison, timeline, analysis, new connection — offer to file it as `wiki/synthesis/<slug>.md` and append to `log.md`. Don't let good synthesis vanish into chat.

### Shoot debrief

This is the skill-improvement loop. When the human shares notes/reflections from a shoot (what they tried, which recipe, what worked, what failed, sample-image observations):

1. File the raw notes as a `sources/` page if dropped into `raw/`, or capture them directly in the debrief.
2. Create or append to `wiki/synthesis/debriefs.md` (a running, reverse-chronological log) — or a dated `wiki/synthesis/debrief-YYYY-MM-DD.md` if the shoot is substantial. Capture: conditions, recipe used (`[[recipes/...]]`), what went well, what to fix, one concrete thing to practice next.
3. Update the relevant technique **concept pages** with what was learned — add a dated observation, flag it if it contradicts an earlier claim (keep both). This is where skill compounds: concept pages accrete the human's own hard-won lessons, not just article claims.
4. If a recipe under- or over-performed in given conditions, note it on that `recipes/` page (e.g. `> Self note 2026-05-17: too contrasty in flat overcast light.`) and adjust its `best_for:` if warranted.
5. Append to `wiki/log.md` as a `debrief` entry. End with a short, specific suggestion for the next shoot or a technique to drill.

The point: every shoot should leave the wiki — and the human's technique — measurably sharper than before.

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

### Roster review

Decides which of the 7 X100VI camera custom slots to **keep, update, or swap**. Run on request, and suggest it after every ~3 new debriefs or the first debrief of a new shooting condition. The living scorecard is `wiki/synthesis/recipe-roster-review.md`.

1. Read the inputs: `synthesis/photographer-profile`, `synthesis/reference-matrix`, `synthesis/recipe-picker`, `synthesis/debriefs`, `concepts/condition-dependent-recipes`, and each `recipes/*.md` (`best_for` + dated self-notes).
2. Score each slot 1–5 on: **practice alignment**, **earned evidence**, **distinctiveness**, **reliability** (portable, or condition-dependent with a precondition that actually occurs in practice), **aesthetic fit**. Every score must trace to a citable wiki line — no unsupported claims.
3. Assign each slot a disposition:
   - **KEEP** — high practice alignment + distinct earned strength + (portable OR precondition reliably occurs).
   - **UPDATE** — right role, fixable known limit or `best_for`/notes need retuning.
   - **SWAP** — redundant with a kept recipe, and/or taste-rejected, and/or precondition rarely occurs; a practice-aligned candidate would serve better.
4. Maintain the swap-candidate backlog (practice-aligned recipes to trial for any freed slot).
5. **Hard guardrail:** never update or swap a camera slot on theory. Every UPDATE/SWAP must first be validated by a controlled comparison (reference-location matrix or single-subject A/B vs. the incumbent), filed as a normal `debrief`, *then* committed to the camera. The review only *proposes* and queues the A/B.
6. Rewrite `wiki/synthesis/recipe-roster-review.md` (it is living synthesis, not append-only): updated scorecard, dispositions, backlog, and a dated decisions subsection. Append a `roster` entry to `wiki/log.md`.

## Log format

Append to `wiki/log.md`. Consistent prefix so `grep "^## \[" wiki/log.md` works:

```
## [YYYY-MM-DD] ingest | <source title>
- created: sources/foo, entities/bar
- updated: concepts/baz, entities/qux
- notes: <one line, optional>

## [YYYY-MM-DD] recipe | <recipe name>
- created: recipes/<slug>
- updated: entities/<film-sim>, entities/<author>
- notes: <look / best-for, one line>

## [YYYY-MM-DD] debrief | <shoot, one line>
- updated: synthesis/debriefs, concepts/<technique>
- next: <one concrete thing to practice>

## [YYYY-MM-DD] query | <short question>
- filed: synthesis/<slug>  (if filed back)

## [YYYY-MM-DD] roster | <one-line disposition summary>
- updated: synthesis/recipe-roster-review
- swap: <slot/recipe → candidate, if any> | queued A/B: <test>
- notes: <keep/update/swap counts, one line>

## [YYYY-MM-DD] lint
- <short summary of findings>
```

## Conventions

- Default to writing no filler. Wiki pages should be terse and dense — claims, links, citations. Not essays.
- Every non-trivial claim on an entity/concept/synthesis page should cite at least one `[[sources/...]]` page.
- When a new source contradicts an existing claim, keep both. Flag the contradiction inline and in the log. Don't silently overwrite.
- Prefer editing existing pages over creating new ones. Only create a new entity/concept page when it's referenced in two or more sources, or when the human asks.
- Recipe pages are the exception to the "two sources" rule: create one per recipe, always. They are inherently structured data and the wiki's most-queried objects.
- Keep the recipe frontmatter schema **stable**. Don't add/rename fields ad hoc — if the schema needs to change, change it here in CLAUDE.md and migrate existing recipe pages in one pass.
- The human's own shoot observations are first-class claims. Cite them as `> Self note YYYY-MM-DD: ...` on the relevant page. They can contradict and override article claims (keep both, flag it).
- Never touch `raw/`. If a source is wrong, note it on the source page — don't edit the raw file.
