# Log

Chronological record of wiki activity. Append-only. Each entry starts with `## [YYYY-MM-DD]` so it's greppable.

## [2026-04-18] init
- created: CLAUDE.md, wiki/index.md, wiki/log.md, raw/, raw/assets/
- notes: wiki scaffolded; no sources ingested yet

## [2026-05-17] setup | Fujifilm X100VI photography domain
- updated: CLAUDE.md (recipe page type, strict recipe frontmatter, domain mapping, recipe-ingest + shoot-debrief workflows, log formats, conventions), wiki/index.md
- created: wiki/recipes/
- notes: groundwork for film-recipe catalog + technique-improvement loop; no recipes/sources filed yet

## [2026-05-17] recipe | Soft Color Universe
- created: recipes/soft-color-universe, entities/astia, entities/x100vi
- updated: wiki/index.md
- notes: Astia/Soft soft saturated daylight/portrait look; self-sourced (author flagged for confirmation); first recipe filed, no peers to compare yet

## [2026-05-17] recipe | Pastel Vibes
- created: recipes/pastel-vibes, entities/classic-negative
- updated: entities/x100vi, wiki/index.md
- notes: Classic Negative soft muted-pastel street/everyday; self-sourced (author flagged); sibling of soft-color-universe (soft Color +3 family)

## [2026-05-17] recipe | Loki
- created: recipes/loki, entities/mehdi-berrada
- updated: entities/classic-negative, entities/x100vi, wiki/index.md
- notes: Mehdi Berrada (film.recipes), high-contrast "inky" harsh-light Classic Neg; orig. X100V — flagged X-Trans 5 caveat; contrast counterpart of pastel-vibes; web-fetched to confirm EV −2/3 + intended look

## [2026-05-17] recipe | Junichiro
- created: recipes/junichiro, entities/pro-neg-hi
- updated: entities/mehdi-berrada, entities/x100vi, wiki/index.md
- notes: Mehdi Berrada (film.recipes), dark faded desaturated PRO Neg. Hi; EV −2/3; orig. X100V caveat; companion to loki (Berrada deep-tone family)

## [2026-05-17] recipe | Bay Area Fortia
- created: recipes/bay-area-fortia, entities/velvia
- updated: entities/x100vi, wiki/index.md
- notes: Velvia/Vivid max-saturation landscape look; self-sourced (author flagged — likely a published Fortia recipe); saturation counterpart of junichiro

## [2026-05-17] recipe | Brian's Sepia
- created: recipes/brians-sepia, entities/sepia
- updated: entities/x100vi, wiki/index.md
- notes: first toned-monochrome recipe; gritty high-contrast Sepia; self-sourced (author flagged); monochrome cousin of loki (shared gritty formula)

## [2026-05-17] recipe | −2/3 Schaller
- created: recipes/schaller, entities/acros, entities/schaller (stub)
- updated: entities/x100vi, wiki/index.md
- notes: ACROS+R dramatic daytime B&W; self-sourced tribute (not by Schaller); EV −2/3 baked-in per user; entities/schaller is a stub pending photographer detail

## [2026-05-17] ingest | Alan Schaller (photographer study)
- updated: entities/schaller (fleshed out from stub), recipes/schaller
- notes: web-grounded study; high-contrast minimalist B&W, 35/2 prime = X100VI analog; technique > recipe

## [2026-05-17] query | which recipe for these conditions
- filed: synthesis/recipe-picker
- notes: decision guide by light/intent across all 7; flagged gaps (flat-overcast color, X-Trans 5 untested, open attributions)

## [2026-05-17] note | recipe attribution confirmed
- updated: recipes/soft-color-universe, recipes/pastel-vibes, recipes/bay-area-fortia, recipes/brians-sepia, recipes/schaller, synthesis/recipe-picker
- notes: human confirmed all non-web-sourced recipes are self-authored (AI-assisted, hand-tweaked to own style); replaced hedging notes with provenance lines; attribution gap closed

## [2026-05-17] debrief | blue hour campus exterior, Soft Color Universe
- created: synthesis/debriefs, concepts/blue-hour-mixed-light
- updated: recipes/soft-color-universe (best_for +blue-hour, first-shoot self note), wiki/index.md
- next: reshoot blue hour with EV bracketed 0/−1/3/−2/3; composition constraint — one subject, one leading line

## [2026-05-17] debrief | Soft Color Universe cross-test (versatility)
- updated: recipes/soft-color-universe (best_for +versatile, cross-test self note), synthesis/debriefs, synthesis/recipe-picker
- notes: human reports it holds up in most lighting → designated the versatile default color recipe; flat-overcast gap softened

## [2026-05-17] debrief | Pastel Vibes A/B + second location
- created: concepts/composition-and-subtraction
- updated: recipes/pastel-vibes (best_for retuned, self notes + A/B + preference), recipes/soft-color-universe (A/B note), entities/classic-negative, synthesis/debriefs, synthesis/recipe-picker, concepts/blue-hour-mixed-light, wiki/index.md
- notes: same-scene A/B vs SCU (Pastel Vibes cooler/flatter); needs scene structure or over-softens; not the flat-light pick; deprioritized by taste; composition failure pattern established → new concept page
- next: reframe pond scene to one subject + clean edges (exclude foreground trunk, minimize power lines)

## [2026-05-17] debrief | Loki reference-location A/B + grass
- updated: recipes/loki (X-Trans 5 caveat resolved, best_for widened, self notes), entities/mehdi-berrada, synthesis/debriefs, synthesis/recipe-picker, concepts/composition-and-subtraction, concepts/blue-hour-mixed-light
- notes: X-Trans 5 transfer RESOLVED (Loki intact on X100VI); Loki = tonal/near-B&W, erases blue hour; domain = contrast+texture+directional light (widened from harsh-sun); composition progress noted (tightest reference frame yet)
- next: hunt raking/directional light on texture (grass frame = template); pre-decide bloom-as-look vs mistake; keep tighter framing

## [2026-05-17] debrief | Junichiro reference A/B + grass (vs Loki)
- updated: recipes/junichiro (X-Trans 5 resolved, best_for widened, self notes), entities/mehdi-berrada, entities/pro-neg-hi, synthesis/debriefs, synthesis/recipe-picker, concepts/blue-hour-mixed-light
- notes: last Berrada X-Trans 5 unknown CLOSED (grain fine on 40MP); Loki vs Junichiro = same family opposite mood (assertive vs wistful); Junichiro controls night lamps better (DR200/Hi 0); composition improvement now consistent
- next: pick tonal recipe by intended emotion pre-shot; default Junichiro for night-with-lamps; shoot remaining 3 at reference spot

## [2026-05-17] debrief | Bay Area Fortia night + reference spot
- created: concepts/saturation-in-flat-light
- updated: recipes/bay-area-fortia (best_for +overcast/rain/gray, self notes + contradiction flag), entities/velvia, synthesis/debriefs, synthesis/recipe-picker, concepts/blue-hour-mixed-light, wiki/index.md
- notes: field finding — raises color in gray, good in rain → likely answer to flat-overcast gap (gap nearly closed pending dedicated gray/rain frames); night warm-artificial over-saturates/clips; most saturated blue-hour sky of series but least natural
- next: shoot Fortia on purpose in gray/overcast/rain and file those frames; avoid night warm-artificial; remaining at reference spot — Brian's Sepia, Schaller

## [2026-05-17] debrief | Brian's Sepia portrait + reference spot
- created: concepts/portraits-and-skin-rendering
- updated: recipes/brians-sepia (best_for widened, self notes, X-Trans 5 resolved), entities/sepia, synthesis/debriefs, synthesis/recipe-picker, concepts/composition-and-subtraction, wiki/index.md
- notes: modern/clean (no-grain) Sepia = versatile default toned-mono "as long as there's light"; first portrait — Clarity/Sharpness +3 flatters characterful/aged faces, harms smooth skin; Shadow +3 X-Trans 5 resolved; only Schaller now untested
- next: test soft recipe on smooth-skin subject; SCU-vs-Brian's-Sepia face A/B; shoot Schaller at reference spot to complete the 7-recipe matrix

## [2026-05-17] note | photographer profile filed
- created: synthesis/photographer-profile
- updated: synthesis/recipe-picker, recipes/loki (purpose), recipes/soft-color-universe (vacation default), wiki/index.md
- notes: outdoor nature/quiet streets, night & sunrise, people rarely, vacations need reliable color; Loki's real purpose = light-on-objects-at-night (condition-dependence moot for that subject); portrait gap low-priority; sunrise flagged as future condition

## [2026-05-17] note | usage model — SCU primary, others specialty/support
- updated: synthesis/recipe-picker, synthesis/reference-matrix, recipes/soft-color-universe, recipes/schaller
- notes: photographer's own framing — Soft Color Universe is the primary daily driver; all others specialty/support deployed around it; Schaller primarily architectural. Encoded as the top-level usage model + Schaller best_for reordered (architecture first)

## [2026-05-17] debrief | Brian's Sepia adult-male portrait, two EV
- updated: recipes/brians-sepia, concepts/portraits-and-skin-rendering, synthesis/debriefs, synthesis/recipe-picker
- notes: recipe holds for general adult-male faces (extends past elderly); new principle — EV is the portrait flattery dial (brighter softens, darker models); smooth/young-skin inverse still the only open portrait case
- next: smooth-skin/younger subject + SCU-vs-Sepia same-face A/B

## [2026-05-17] debrief | fern-shade matrix (5153–5159), one subject 7 recipes
- created: concepts/condition-dependent-recipes
- updated: recipes/loki, recipes/schaller (condition-dependent self notes), recipes/bay-area-fortia, recipes/soft-color-universe, recipes/brians-sepia, synthesis/debriefs, synthesis/recipe-picker, concepts/saturation-in-flat-light, wiki/index.md
- notes: BIG — Loki & Schaller collapse in flat shade w/o hard light + EV −2/3 (condition-dependent tools, not portable looks; user flagged 5155 "overexposed for it" Loki); Fortia rescue confirmed close-range (caveat: dense dark greens go heavy); SCU faithful baseline; Brian's Sepia texture partially redeems a color subject; camera-order map documented
- next: stop applying Loki/Schaller in flat light; smooth-skin portrait test still open

## [2026-05-17] debrief | flat-overcast 3-way A/B (5146/5150/5151) — gap CLOSED
- updated: recipes/bay-area-fortia (gray-rescue confirmed), recipes/soft-color-universe (neutral-baseline note), recipes/brians-sepia (subject-match rule), entities/velvia, synthesis/debriefs, synthesis/recipe-picker, concepts/saturation-in-flat-light (status: confirmed), concepts/composition-and-subtraction
- notes: controlled 3-way in flat overcast — Fortia visibly rescues color (no clipping on natural foliage), SCU records flatness, Brian's Sepia weakest when color is the subject; saturation-in-flat-light gap CLOSED; blown overcast sky now a consistent composition weakness
- next: re-shoot cropping sky out; active-rain frames optional; smooth-skin portrait still open

## [2026-05-17] debrief | Brian's Sepia flat overcast (frame 5042)
- updated: recipes/brians-sepia (best_for += overcast/architecture, self note + caveat refinement), synthesis/debriefs, synthesis/recipe-picker, concepts/saturation-in-flat-light
- notes: holds up in flat overcast daytime on textured/architectural subjects (Clarity+tone curve manufacture contrast) — old "avoid flat overcast" caveat refined to "needs light + structure"; mono analog of Fortia gray-rescue; weakness = blown white sky, compose it out
- next: in flat light crop out blown sky; outstanding — Fortia gray/rain frames, smooth-skin portrait

## [2026-05-17] debrief | Schaller — completes the 7-recipe matrix
- created: synthesis/reference-matrix
- updated: recipes/schaller (best_for widened, self notes, X-Trans 5 resolved), entities/schaller (payoff confirmed), entities/acros, synthesis/debriefs, synthesis/recipe-picker, concepts/composition-and-subtraction, wiki/index.md
- notes: MILESTONE — all 7 recipes shot from one vantage; matrix consolidated. Schaller delivers the Alan Schaller aesthetic (Soundstage frame); works at night; clean fine detail at Sharpness 0; mono-for-problematic-color rule; composition leveled up (resist clutter in complex scenes). X-Trans 5 fully closed.
- next: chase the Soundstage standard in busy scenes; outstanding — Fortia gray/rain frames, smooth-skin portrait test

## [2026-05-17] roster | first review — 6 keep, 1 swap (Pastel Vibes)
- created: synthesis/recipe-roster-review
- updated: CLAUDE.md (Roster review workflow + roster log type), wiki/index.md
- swap: slot 2 Pastel Vibes → sunrise recipe (or Classic Chrome) | queued A/B: candidate + Pastel Vibes + SCU on one sunrise/street scene
- notes: SCU/Loki/Brian's Sepia/Schaller KEEP; Junichiro KEEP-watch (#2 swap candidate, twins Loki); Bay Area Fortia KEEP-re-evaluate (track gray/rain frequency); no camera change until queued A/B filed as a debrief

## [2026-05-17] roster | two Schaller modes adopted; Binet Form dropped
- updated: synthesis/recipe-roster-review (target roster E/G split, specs, validation), entities/schaller, entities/helene-binet, recipes/schaller (= Schaller Dark), synthesis/photographer-profile
- swap: Binet Form removed by human choice → second Schaller mode. Roster mono = Schaller Dark + Brian's Sepia + Schaller Luminous
- notes: Schaller Dark = UPDATE of current recipe (grain off, +R→+Ye, else unchanged); Schaller Luminous = NEW (Ann Demeulemeester, deep-but-luminous, absorbs Binet register); no architectural-color slot; A/B-gated

## [2026-05-17] roster | recommended target roster (Schaller + Binet anchored)
- created: entities/helene-binet
- updated: synthesis/recipe-roster-review (target roster A–G + candidate specs + validation path), synthesis/photographer-profile (admired architects), entities/schaller (official site), wiki/index.md
- swap: Pastel Vibes + Junichiro + Bay Area Fortia OUT; NEW Clean Sunrise / Stillwater Street (Classic Chrome) / Binet Form (Provia); Schaller → Architectural ACROS (UPDATE: grain off, filter retuned); SCU + Loki locked; Brian's Sepia keep
- notes: full should-have roster designed around the architectural eye + Schaller/Binet; 4 A/Bs queued in priority order; nothing to camera on theory

## [2026-05-17] roster | re-review after added context — now 2 swaps
- updated: synthesis/photographer-profile (location/palette/aesthetic), synthesis/recipe-roster-review (re-scored), synthesis/recipe-picker, recipes/junichiro, recipes/bay-area-fortia, recipes/schaller, recipes/brians-sepia, concepts/composition-and-subtraction
- swap: slot 2 Pastel Vibes + slot 4 Junichiro (grain/film aesthetic rejected) | queued A/Bs: slot-2 sunrise/Classic Chrome, slot-4 candidate, + UPDATE probes (Sepia-vs-neutral-mono, Fortia-orange, Schaller +Ye/+G)
- notes: new context — Stillwater OK, orange-heavy environment (red-adds clash), anti-warm-nostalgia, no grain/film-mimicry, museum-quality, architectural eye. Schaller up to KEEP-strong (native); Junichiro → SWAP; Fortia/Sepia flags sharpened; SCU/Loki reaffirmed. No camera change on theory.

## [2026-05-17] recipe | People
- created: recipes/people
- updated: entities/astia, synthesis/photographer-profile, synthesis/recipe-roster-review, wiki/index.md
- notes: Astia/Soft skin-tuned portrait (Color +1, Sharpness 0, NR −2, Shadow +2, Smooth Skin off, EV ~+2/3 range); CUSTOM 2; revealed-preference contradiction vs "portrait low priority" (keep both, flagged); partly closes the smooth-skin thread

## [2026-05-17] recipe | Stillwater Street
- created: recipes/stillwater-street, entities/classic-chrome
- updated: synthesis/recipe-roster-review, recipes/bay-area-fortia, wiki/index.md
- notes: Classic Chrome muted documentary street/gray-rescue (taste-aligned Fortia replacement — contrast not raw saturation); CUSTOM 3; built from the wiki Classic Chrome spec (owner-confirmed), not panel-verified; retroactive A/B #2

## [2026-05-17] recipe | Schaller Luminous
- created: recipes/schaller-luminous
- updated: entities/schaller, entities/helene-binet, synthesis/recipe-roster-review, wiki/index.md
- notes: ACROS+Ye deep-but-luminous sculptural B&W (Hi −1 / Sh −1, Clarity +1); Ann Demeulemeester mode, absorbs Binet register; CUSTOM 7; committed DR200/EV+2/3 vs proposed DR400/EV~0 (flagged); retroactive A/B #4

## [2026-05-17] roster | full roster committed; wiki reconciled to camera
- updated: synthesis/recipe-roster-review, synthesis/photographer-profile, recipes/schaller (→ Schaller Dark: +R→+Ye, grain off, misdials flagged), recipes/pastel-vibes, recipes/junichiro, recipes/bay-area-fortia, wiki/index.md
- swap: Pastel Vibes / Junichiro / Bay Area Fortia retired from camera; Clean Sunrise retired-before-built (SCU absorbs sunrise) | retroactive A/Bs: #1 SCU@sunrise, #2 Stillwater St vs Fortia vs SCU on orange-gray, #3 Schaller Dark +Ye/grain-off vs +R, #4 Luminous vs Dark
- notes: owner committed all 7 slots ahead of A/Bs (guardrail overridden by owner choice — flagged, not silently dropped; A/Bs reframed gating→retroactive; future cycles default back to gate-then-commit). Roster = SCU·People·Stillwater St·Loki·Brian's Sepia·Schaller Dark·Schaller Luminous. Schaller Dark camera misdials (EV+2/3, Sharp+3, WC+2, NR−4) → correct camera to designed (−2/3, 0, WC−1, −3)

## [2026-05-17] ingest | Alan Schaller — night-shooting video (transcript)
- created: sources/schaller-night-shooting, synthesis/schaller-technique
- updated: entities/schaller, recipes/schaller, concepts/condition-dependent-recipes, wiki/index.md
- notes: started a LIVING Schaller technique repository (populate from future video transcripts; legend [NS]). Author-confirms Schaller Dark's underexpose-for-highlights / EV −2/3 (he shoots ≈ −2, RAW+post — magnitude caveat vs our JPEG −2/3); ISO 20k flagged Monochrom-only (does NOT close the open high-ISO-night gap); new night nugget — wet pavement = highlight bursts

## [2026-05-17] ingest | Alan Schaller — composition video (transcript)
- created: sources/schaller-composition
- updated: synthesis/schaller-technique (legend [CO]; Composition/Philosophy/Process/X100VI sections), concepts/composition-and-subtraction (subframing + leading-lines-need-light principles, Schaller corroboration), wiki/index.md
- notes: 2nd video into the living repository. Schaller's #1 rule = "trimming the fat, not one pixel more" — direct corroboration of the wiki's central composition lever. New drill-able principles: subframing, leading-lines-need-light, get-it-in-camera-not-crop, shoot-with-intention. Grid lines transfer directly to X100VI; focal-length tricks (16/24mm) don't — use position. No new entity pages (named influences Fan Ho/Adams/etc. recorded, created only if they recur/asked)

## [2026-05-17] ingest | Alan Schaller — 7 tips to improve B&W street (transcript)
- created: sources/schaller-bw-street-tips, entities/ansel-adams
- updated: synthesis/schaller-technique (legend [BW]; new Tonality + Editing sections, Philosophy/Light/Composition bullets), concepts/condition-dependent-recipes (tip-3 corroboration), recipes/schaller-luminous (Zone-System = its philosophy), entities/schaller (tips line sourced), wiki/index.md
- notes: 3rd video; the one entities/schaller already cited as "DPReview 7 tips" — now a full source. Ansel Adams promoted to an entity (recurs across 2 videos + Zone System): the Zone-System full-range ideal IS the Schaller Luminous philosophy; Schaller Dark's crush = the deliberate exception. Key quotes: "no such thing as bad light" (corroborates condition-dependent rule — change subject, don't force look) and "editing is varnishing a table that's already well made" (clearest statement of the wiki's recipe-is-the-small-part principle)

## [2026-05-18] ingest | Fujifilm "Make Your Own Film Simulation Recipe" (reference)
- created: sources/fuji-recipe-howto
- updated: wiki/index.md
- notes: reference-only ingest — dial-by-dial meaning + custom-setting mechanics + the DR/ISO-headroom rule (general form of the per-recipe caveats). The article's example recipe (Nostalgic Summer, Josh Edgoose × Fujifilm) was initially filed then **removed at the owner's instruction** — article filler, off-taste vs the profile; recipes/nostalgic-summer + entities/nostalgic-neg + entities/josh-edgoose deleted (schema's "always file a recipe" rule yields to the curator's call). No new entities/recipes net.

## [2026-05-18] roster | Schaller recipes re-examined vs the ingested videos
- updated: synthesis/recipe-roster-review (A/B #4 sharpened to 3-way + decisions log), recipes/schaller (Dark — no dial change + shooting-discipline note), recipes/schaller-luminous (DR400/EV~0 proposal + shooting-discipline note)
- swap: none | proposal (A/B-gated, NOT committed): Schaller Luminous DR200→DR400 + EV+2/3→~0 metered-for-highlights, validated by sharpened A/B #4
- notes: Schaller Dark confirmed by his own method (EV −2/3, pure-white-by-the-head, crush = deliberate Zone-System exception) — no dial change. Luminous: videos independently justify reverting both committed deltas to spec; JPEG no-post constraint strengthens it. Guardrail intact — no camera change on theory.

## [2026-05-18] note | photographer admires Mehdi Berrada (recipes + architecture)
- updated: synthesis/photographer-profile, entities/mehdi-berrada
- notes: first-class preference on record — Berrada added as an admired influence alongside Schaller/Binet. Flagged nuance (keep both): does NOT reverse the Junichiro retirement (taste call stands); Loki remains the on-roster Berrada recipe; revisit Junichiro only on explicit request

## [2026-05-18] note | Junichiro kept saved off-camera (status precision)
- updated: recipes/junichiro, synthesis/recipe-roster-review
- notes: owner clarified Junichiro is retained off-camera (recallable), not discarded — retirement was slot-economy/taste, access doesn't depend on a slot; slot reinstatement remains a separate, explicit-request decision

## [2026-05-18] debrief | Stillwater Street vs SCU, badly-overcast brick wall (5188/5189) — partial A/B #2
- updated: synthesis/debriefs, recipes/stillwater-street, recipes/soft-color-universe, concepts/composition-and-subtraction, concepts/saturation-in-flat-light, synthesis/recipe-roster-review
- notes: ORANGE-CLASH SETTLED in Stillwater Street's favour — it tamps OSU-orange brick (cooler/muted) where SCU records it faithfully and Fortia would amplify it; Fortia→Stillwater-Street swap now field-supported. Nuance: replaces the role not Fortia's mechanism (sober structure/mood, not saturation); direct Fortia parity optional-open (no Fortia frame). Stillwater Street evidence 1→3, aesthetic 4→5, KEEP. Composition = the limiting factor (uncommitted cracked-pillar subject, dead sky + wire tangle; recipe ~10% of result)
- next: re-shoot the cracked pillar as committed subject (low/close, wall as leading line, subframe, exclude wires + white sky); A/B #1 (SCU at sunrise) still the top queued item
