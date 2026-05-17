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
white_balance: "Auto (White Priority)"
wb_shift: "R+0 B+0"
highlight: +1
shadow: +4
color: n/a            # ACROS is monochrome — no color control
sharpness: 0
clarity: +3
noise_reduction: -3
iso: "Auto"           # not shown in source; set per scene
exposure_comp: "-2/3" # baked-in intent: underexpose 2/3 in daytime
best_for: [architecture, geometry, monochrome, high-contrast, negative-space, night, texture, street]
tags: [recipe, acros, monochrome]
---

**Schaller Dark.** A dramatic [[entities/acros]] black-and-white with a yellow filter — the crushed/graphic *street* mode, the wiki's premium hard-light B&W. The +Ye filter darkens skies and deepens tonal separation **without lightening the orange-heavy local environment the way +R did** (the resolved taste fix); Shadow +4 crushes blacks while Highlight +1 keeps a slight roll-off; Clarity +3 adds grit; grain off keeps it clean (the museum-quality stance); Monochromatic Color WC−1 MG−1 cools the tone very slightly. A tribute recipe to the photographer [[entities/schaller]] — not authored by him. Built to be shot at **EV −2/3 in daytime** (the owner's stated intent, load-bearing — not optional), in strong light with sky and structure. Avoid flat overcast — Shadow +4 needs real contrast to read. Caveat: Adobe RGB, JPEG. Slug `recipes/schaller` retained for inbound-link stability; the recipe's name is **Schaller Dark**. Pairs with [[recipes/schaller-luminous]] as the two-mode Schaller set.

> User note 2026-05-17: −2/3 EV is the suggested daytime exposure for this recipe — treat it as part of the recipe, not optional.

> Self note 2026-05-17 (usage model): **primary use is architectural photography** — geometry, structure, hard light. Other uses (street, texture, negative-space studies) are secondary. A specialty tool around the primary [[recipes/soft-color-universe]], not a general alternative.

> Self note 2026-05-17 (shot — completes the 7-recipe matrix, [[synthesis/debriefs]]): **delivers the [[entities/schaller|Alan Schaller]] aesthetic.** The Kicker Soundstage frame (lit geometry, pure-black sky/void, negative space) is the clearest proof — recipe + the *seeing* both landed. Works at **night**, not just harsh daytime: Shadow +4 + ACROS+R turns artificial-lit structure into stark geometry; X-Trans 5 fine (deep but not destroyed when there's light/contrast). `best_for` widened (architecture, night, texture, negative-space).

> Self note 2026-05-17 (technical): renders fine texture **cleanly at Sharpness 0** — ACROS acuity + Clarity +3 give crisp detail without the over-crunch of the Sharpness +3 recipes. On the shared grass subject it gave the best isolation of the three tonal takes (vs [[recipes/loki]] gritty-warm, [[recipes/junichiro]] soft-faded).

> Self note 2026-05-17 (vs [[recipes/bay-area-fortia]], same McKnight facade): where Fortia over-saturated/clipped the warm artificial light, Schaller **sidesteps the problem entirely** and turns the mullion grid into the subject. Rule: when night artificial color is problematic, go mono and let geometry carry it.

> Self note 2026-05-17 (fern-shade matrix, frame 5159, [[synthesis/debriefs]]): in flat porch shade at normal exposure it rendered **soft, high-key, low-contrast** — pleasant but *not the Schaller look at all*. Same failure mode as the "overexposed Loki" (5155): Shadow +4 needs hard light + the EV −2/3 underexposure to produce drama; without them it collapses to a generic bright mono. **Condition-dependent tool, not a portable filter** — the EV −2/3 + hard light is load-bearing. See [[concepts/condition-dependent-recipes]].

Pairs with [[recipes/brians-sepia]] as part of the wiki's monochrome set: Schaller Dark is clean (grain-off) ACROS + yellow-filter drama; Brian's Sepia is warm-toned and harder-edged; [[recipes/schaller-luminous]] is the deep-but-luminous counterpart. All share the gritty Clarity +3 / deep-shadow formula seen in [[recipes/loki]].

The look chases [[entities/schaller|Alan Schaller]]'s high-contrast minimalist B&W. Key for actually getting there: the recipe is the small part. Shoot it in hard directional light, expose for the highlights (the EV −2/3 helps), and compose for negative space and geometry, not just a subject. The X100VI's 35mm-equiv f/2 lens matches his Leica setup — the constraint is deliberate, lean into it.

> Self note 2026-05-17 ([[synthesis/photographer-profile]], [[synthesis/recipe-roster-review]]): **strongly aligned, not peripheral.** The photographer has an architectural background and sees structurally — Schaller's geometry/negative-space approach is *native*, and clean ACROS at Sharpness 0 fits the museum/exhibition target. Roster KEEP (strong). One precise UPDATE probe queued: the **+R** filter *lightens* the area's abundant OSU-orange brick/material and flattens its tonal separation — test **+Ye / +G** on an orange-dominant local scene and pick the variant that holds orange separation best. Recipe tweak, not a slot swap.

> Self note 2026-05-17 (this recipe = **Schaller Dark**, [Ann Demeulemeester](https://www.alanschaller.com/ann-demeulemeester) clarified two modes): the human keeps **both** Schaller modes as separate recipes. **This page is the *Dark* (crushed/graphic street) mode** — kept, validated (Soundstage); the only changes queued are taste fixes: **grain off** and filter off **+R** (orange palette) — Shadow +4 / EV −2/3 / inky character retained. The *Luminous* mode (deep-but-luminous, retained detail, clean) is a **separate new recipe** (*Schaller Luminous*), not a retarget of this one. Both A/B-gated; see [[synthesis/recipe-roster-review]].

> Self note 2026-05-17 (camera reconciliation — committed roster): the full 7-slot roster was committed to the camera ahead of validation by owner choice; **Schaller Dark = CUSTOM 6** (not 7). Two *intentional, roster-queued taste fixes are now applied and canon:* film sim **+R → +Ye** (the +Ye/+G probe is resolved — +Ye committed) and **grain → off**. Separately, the CUSTOM 6 panel was found **deviating from the designed recipe on four dials: EV +2/3, Sharpness +3, Monochromatic Color WC+2, NR −4** — a **missed input**, not an intended change. **Resolved 2026-05-17: the owner corrected the camera to match the designed recipe** (EV **−2/3**, Sharpness **0**, WC **−1** MG **−1**, NR **−3**). Camera and wiki now agree; the designed constants above are authoritative. The grass-3way "Sharpness 0 is cleaner than +3" finding (self note above) stands intact and is *reinforced* by this. Retroactive **A/B #3** (Schaller Dark +Ye, grain-off, designed dials vs the prior +R version on an orange-material scene) still confirms the intentional taste fixes held. See [[synthesis/recipe-roster-review]].

Provenance: self-authored tribute — devised by the photographer (AI-assisted, then hand-tweaked to their own style), filed from camera slot **CUSTOM 6**. A homage to [[entities/schaller|Alan Schaller]]'s look, not authored by him. `author: self` (confirmed 2026-05-17).
