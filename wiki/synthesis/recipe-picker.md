---
type: synthesis
created: 2026-05-17
updated: 2026-05-17
sources: [recipes/soft-color-universe, recipes/pastel-vibes, recipes/bay-area-fortia, recipes/loki, recipes/junichiro, recipes/brians-sepia, recipes/schaller]
tags: [synthesis, recipe-picker, decision-guide]
---

# Which recipe for these conditions?

Decision guide across the 7 custom slots on the [[entities/x100vi]]. Pick by **light first**, then intent. All recipes are JPEG / Adobe RGB (export sRGB for web). Partially field-tested (see [[synthesis/debriefs]]) — Soft Color Universe, Pastel Vibes, and Loki are now experience-based; the rest are still by formula.

## By light

| Light | Color | Black & white |
|---|---|---|
| **Hard / directional light, texture** (not only midday sun) | [[recipes/loki]] — warm, inky, near-mono; EV −2/3 | [[recipes/schaller]] — ACROS+R drama, EV −2/3 · [[recipes/brians-sepia]] — warm-toned, harder |
| **Bright sun + bold color** (landscape/nature) | [[recipes/bay-area-fortia]] — max saturation | — |
| **Soft / directional daylight, golden hour, blue hour** (portraits, warm) | [[recipes/soft-color-universe]] — soft, saturated, rich sky | [[recipes/schaller]] if going mono |
| **Soft light *with structure*, want restraint** | [[recipes/pastel-vibes]] — muted, cool (needs texture/point light; deprioritized by taste) | — |
| **Flat / featureless overcast** | [[recipes/soft-color-universe]] — Pastel Vibes over-softens here | (mono recipes go flat — see gap) |
| **Low / moody, shadow-led** | [[recipes/junichiro]] — dark, faded, EV −2/3 | [[recipes/junichiro]] reads near-mono |

## By intent

- **Unsure / default color** → [[recipes/soft-color-universe]]. Field-tested to hold up in *most* lighting (2026-05-17 cross-test); the safe everyday choice. Pick a specialized recipe when you want a specific *look*, not because this one fails.
- **Punchy & graphic, color** → Loki (hard light) / Bay Area Fortia (saturated subjects).
- **Soft & flattering, skin** → Soft Color Universe (warm; preferred). Pastel Vibes (cool, muted) also skin-safe but deprioritized by taste. Avoid Velvia/Loki on faces.
- **Dark, cinematic, restrained** → Junichiro.
- **Dramatic B&W, geometry & negative space** → Schaller (the [[entities/schaller|Alan Schaller]] approach — see that page; the seeing matters more than the recipe).
- **Toned, gritty B&W** → Brian's Sepia.

## Rules of thumb

- **EV −2/3** is baked into Loki, Junichiro, Schaller — underexpose or the look collapses.
- **High-contrast recipes need real shadows.** Loki, Junichiro, Brian's Sepia, Schaller all fail in flat overcast.
- **Berrada family** (Loki, Junichiro) share a deep-toned, EV −2/3 signature — see [[entities/mehdi-berrada]].
- **Classic Neg spans the range:** Pastel Vibes (soft) ↔ Loki (hard) — same sim, opposite dials.
- **Soft/low-contrast recipes need scene structure.** Pastel Vibes (and soft looks generally) read well only with directional/point light or texture to grip; in genuinely flat light they go mushy. Match recipe softness to the light's structure, not just the time of day.
- **Film sim sets blue-hour sky impact.** Astia + Color Chrome Strong (SCU) > Classic Neg + Weak (Pastel Vibes) for a vivid sky.
- **Loki is a tonal recipe, not a color one.** Color 0 + deep curve + warm WB makes it behave like warm B&W — it *erases* the blue-hour palette. Treat it (and Junichiro) as part of the dark/tonal cluster; never the blue-hour pick.
- **Loki's domain is contrast + texture + directional light**, broader than "harsh sun." Raking light on texture is its sweet spot; bare point sources blow out hard on DR100.

## Gaps (worth filling)

- **No color recipe purpose-built for flat overcast.** Confirmed 2026-05-17 that Pastel Vibes is *not* the answer (it over-softens in flat light). [[recipes/soft-color-universe]] is the field-proven practical default. A dedicated flat-light recipe (brighter, lifted-shadow, more local contrast) is still worth building. Gap softened, not closed.
- **X-Trans 5 transfer — Loki RESOLVED** (2026-05-17): transfers cleanly, look intact. By extension the X-Trans 5 concern for [[recipes/junichiro]] is now low-priority (still formally unverified). Remaining untested recipes: Bay Area Fortia, Junichiro, Brian's Sepia, Schaller.

Attribution resolved 2026-05-17: Loki & Junichiro are Mehdi Berrada (film.recipes); the other five are self-authored (AI-assisted, hand-tweaked to the photographer's style).
