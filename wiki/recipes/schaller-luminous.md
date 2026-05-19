---
type: recipe
created: 2026-05-17
updated: 2026-05-17
camera: X100VI
film_sim: ACROS+Ye
author: self
sources: []
dynamic_range: DR200
grain: off
color_chrome: off
color_chrome_fx_blue: off
white_balance: "Auto"
wb_shift: "R+0 B+0"
highlight: -1
shadow: -1
color: n/a            # ACROS is monochrome — no color control
sharpness: 0
clarity: +1
noise_reduction: -3
iso: "Auto"           # not captured from panel; set per scene
exposure_comp: "+2/3" # committed camera value; spec was meter-for-highlights ~0
best_for: [architecture, monochrome, light-on-form, sculptural, luminous, retained-detail, night, texture]
tags: [recipe, acros, monochrome]
---

The **dimensional / sculptural** [[entities/acros]] mode — the opposite tonal philosophy from [[recipes/schaller|Schaller Dark]]. Where Dark crushes for graphic drama, Luminous keeps it **deep but luminous**: Highlight −1 / Shadow −1 retain shadow detail and protect highlights, Clarity +1 gives definition without harshness, ACROS+Ye + Monochromatic Color WC 0 MG 0 keeps it neutral and clean. Full tonal separation, strong-not-harsh, light revealing form. Targets the [Ann Demeulemeester](https://www.alanschaller.com/ann-demeulemeester) mode of [[entities/schaller|Alan Schaller]] and **absorbs the [[entities/helene-binet|Binet]] tonal register** (luminous deep tone, retained gradation, the zoomed-in fragment) — there is no separate architectural-color recipe; this is it. Caveats: Adobe RGB (export sRGB for web); JPEG; DR200 needs ISO ≥ ~320.

> Self note 2026-05-17 (look — the Metropolis case): for a *luminous subject suspended in a scene-given dark frame* (e.g. Schaller's London-Underground "Metropolis" frame), **this is the right base, not Schaller Dark** — the defining feature is the fully-rendered, gradated subject; the black frame comes from the scene's light differential + f/2 + shooting through a gap, not from a shadow-crush dial. The recipe is ~30% of that look; composition and exposure-for-the-subject do the rest. Localized dodge/burn + a hard black point (Schaller's Lightroom/Silver Efex move) is the unreachable last part of a global JPEG recipe.

> Self note 2026-05-17 (provenance / camera + spec deltas): NEW recipe, committed to camera slot **CUSTOM 7** ahead of validation by owner choice. Camera is canonical (no prior earned evidence). Two deltas vs the roster-review proposed spec, recorded as committed: **DR200** (spec wanted DR400 for highlight headroom) and **EV +2/3** (spec said meter-for-highlights ~0, no baked-in). Neither breaks identity — +2/3 supports "luminous" — but flag for the retroactive A/B. ACROS+Ye resolves the spec's +Ye-vs-plain-ACROS question (Ye committed).

> Self note 2026-05-17 ([[synthesis/recipe-roster-review]]): retroactive validation = **A/B #4** — Schaller Luminous vs [[recipes/schaller|Schaller Dark]] on one sculptural light-on-form subject, same frame, both modes — confirms the two modes are genuinely distinct and both earn a slot. Until shot and filed as a debrief this recipe is unproven in the field.

> Source note 2026-05-17 ([[sources/schaller-bw-street-tips]], [[entities/ansel-adams]], [[synthesis/schaller-technique]]): **this recipe's philosophy is Schaller's own stated default.** His tonality tip is the [[entities/ansel-adams|Adams]] Zone System — *every tone represented, black→white + greys between; you don't need extreme contrast/negative space.* That is exactly Luminous (deep-but-luminous, retained detail, full separation). Frames the two-mode split: Luminous = Schaller's full-range default; [[recipes/schaller|Schaller Dark]]'s crush is the *deliberate exception*, not the norm. Independent support for keeping both as distinct slots (A/B #4).

> Proposed change 2026-05-18 — A/B-GATED, NOT committed ([[synthesis/recipe-roster-review]] decisions log 2026-05-18, [[synthesis/schaller-technique]]): the Schaller videos independently justify **reverting both committed deltas to the original spec.** (1) **DR200 → DR400** — full tonal range needs highlight headroom, and the [[entities/ansel-adams|Zone-System]] full range `[BW]` *is* this recipe's identity. (2) **EV +2/3 → ~0, metered for highlights** — Schaller *protects* highlights / underexposes `[NS]`; +2/3 brightens toward the clipping he avoids, and at DR200 there is no headroom (DR200+EV+2/3 is the least Schaller-consistent pairing). The JPEG no-post constraint ("editing is varnish" `[BW]`; no RAW shadow-boost) *strengthens* the in-camera-latitude case. **Guardrail: do not change the camera** — this is settled by the sharpened 3-way A/B #4 (Luminous DR400/EV~0 vs Luminous committed DR200/EV+2/3 vs Dark, same frame), then filed as a `debrief`.

> Shooting discipline 2026-05-18 ([[synthesis/schaller-technique]]): expose to **protect the highlights** and hold the full tonal range (the Adams default, not crush); find light that *reveals form*; subframe; shoot with intention. The recipe is the small part — the seeing is the work.

> Self note 2026-05-18 (FIRST FIELD EVIDENCE — frame 5204, [[synthesis/debriefs]]): rainy gray scene (flag + power-line web), shot in the **committed form** (DR200, EV +2/3). **Recipe delivered on its stated identity:** full tonal range from near-black to white, sky a smooth mid-gray with gradation (not blown), flag stripes preserved as alternating values, wires razor-crisp via Clarity +1, tattered-edge texture intact. Evidence 1 → 3.
>
> **Bigger finding — Luminous is portable, not condition-dependent like [[recipes/schaller|Dark]].** Dark collapses in flat light (fern-shade 5159: needs hard light + EV −2/3); **Luminous held in flat-light rain** because its philosophy is to *preserve* what's there, not manufacture drama from it. The two Schaller modes have **different reliability profiles** ([[concepts/condition-dependent-recipes]] updated).
>
> **A/B #4 proposal reframed.** Committed DR200/EV+2/3 is not failing here — so the DR400/EV~0 reversion isn't *refuted* but isn't *urgent*. Its value would be in a **high-DR scene** (hard sun + deep shade; bright night point sources) where headroom matters. **Run A/B #4 in a high-DR scene**, not rain.

Pairs with [[recipes/schaller|Schaller Dark]] as the wiki's two-mode Schaller B&W set (Dark = crushed/graphic street; Luminous = deep-but-luminous form). Provenance: self-authored tribute — devised by the photographer (AI-assisted, hand-tuned), filed from camera slot CUSTOM 7. A homage to [[entities/schaller|Alan Schaller]]'s dimensional mode, not authored by him. `author: self` (confirmed 2026-05-17).
