---
type: synthesis
created: 2026-05-17
updated: 2026-05-17
sources: [recipes/soft-color-universe, recipes/pastel-vibes, recipes/bay-area-fortia, recipes/loki, recipes/junichiro, recipes/brians-sepia, recipes/schaller]
tags: [synthesis, recipe-picker, decision-guide]
---

# Which recipe for these conditions?

Decision guide across the 7 custom slots on the [[entities/x100vi]]. Pick by **light first**, then intent. All recipes are JPEG / Adobe RGB (export sRGB for web). Partially field-tested (see [[synthesis/debriefs]]) — Soft Color Universe, Pastel Vibes, Loki, Junichiro, and Bay Area Fortia are now experience-based (Fortia's gray/rain strength asserted from experience, dedicated sample frames pending); Brian's Sepia and Schaller still by formula.

## By light

| Light | Color | Black & white |
|---|---|---|
| **Hard / directional light, texture** (not only midday sun) | [[recipes/loki]] — warm, inky, near-mono; EV −2/3 | [[recipes/schaller]] — ACROS+R drama, EV −2/3 · [[recipes/brians-sepia]] — warm-toned, harder |
| **Bright sun + bold color** (landscape/nature) | [[recipes/bay-area-fortia]] — max saturation | — |
| **Gray / overcast / rain** (color-poor light) | [[recipes/bay-area-fortia]] — saturation *rescues* dull light (field finding) | — |
| **Soft / directional daylight, golden hour, blue hour** (portraits, warm) | [[recipes/soft-color-universe]] — soft, saturated, rich sky | [[recipes/schaller]] if going mono |
| **Soft light *with structure*, want restraint** | [[recipes/pastel-vibes]] — muted, cool (needs texture/point light; deprioritized by taste) | — |
| **Flat / featureless overcast** | Neutral default: [[recipes/soft-color-universe]]. Color-rescue: [[recipes/bay-area-fortia]] (bold, lifts gray) | (mono recipes go flat — see gap) |
| **Low / moody, shadow-led** | [[recipes/loki]] (assertive, warm, crushed) or [[recipes/junichiro]] (wistful, soft, faded) — choose by mood; Junichiro safer with lamps | both read near-mono |

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
- **Film sim sets blue-hour sky impact.** Astia + Color Chrome Strong (SCU) > Classic Neg + Weak (Pastel Vibes) for a vivid sky. Bay Area Fortia (Velvia) beats both for raw sky saturation but looks the least natural.
- **Velvia amplifies the color already there.** Match it to the *deficit* (gray/rain — it rescues) not the *abundance* (warm artificial/neon — it clips). See [[concepts/saturation-in-flat-light]].
- **Loki & Junichiro are tonal recipes, not color ones.** Both erase color/blue-hour palette; never the blue-hour pick. Split by mood: **Loki = assertive (hard/warm/crushed/crisp); Junichiro = wistful (soft/cool/faded/grainy).** Junichiro handles night point sources better (DR200 + Highlight 0 vs Loki DR100 + Highlight +4).
- **Loki's domain is contrast + texture + directional light**, broader than "harsh sun." Raking light on texture is its sweet spot; bare point sources blow out hard on DR100.

## Gaps (worth filling)

- **Flat-overcast gap — likely answered.** [[recipes/bay-area-fortia]] is the field-asserted color-rescue for gray/rain (saturation compensates for color-poor light); [[recipes/soft-color-universe]] remains the *neutral* default; Pastel Vibes is *not* the answer (over-softens). To fully close: file dedicated gray/rain Fortia frames. Gap nearly closed pending those.
- **X-Trans 5 transfer — both Berrada recipes RESOLVED** (2026-05-17): Loki and Junichiro transfer cleanly, grain fine on 40MP. Remaining untested recipes: Bay Area Fortia, Brian's Sepia, Schaller.

Attribution resolved 2026-05-17: Loki & Junichiro are Mehdi Berrada (film.recipes); the other five are self-authored (AI-assisted, hand-tweaked to the photographer's style).
