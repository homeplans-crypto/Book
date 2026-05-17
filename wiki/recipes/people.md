---
type: recipe
created: 2026-05-17
updated: 2026-05-17
camera: X100VI
film_sim: Astia/Soft
author: self
sources: []
dynamic_range: DR200
grain: "Weak, Small"
color_chrome: Weak
color_chrome_fx_blue: Weak
white_balance: "Auto"
wb_shift: "R+0 B+0"
highlight: -1
shadow: +2
color: +1
sharpness: 0
clarity: +3
noise_reduction: -2
iso: "Auto"            # not captured from panel; set per scene
exposure_comp: "0 to +2/3, scene-dependent"  # +2/3 nominal portrait-flattery bias; ride per scene
best_for: [portrait, people, skin, faces]
tags: [recipe, astia]
---

A skin-tuned [[entities/astia]] portrait look — the same Astia base as [[recipes/soft-color-universe]] but every dial moved to serve a face. Vs SCU (Color +3 / Sharpness +1 / NR −4 / Shadow −1 / grain off): **Color +1** holds skin honest instead of saturated, **Sharpness 0** keeps it kind, **NR −2** smooths a touch more, **Shadow +2** adds gentle modeling, and a hint of Weak/Small grain warms the rendering. Reach for it on people in soft to mixed light. Caveats: Smooth Skin Effect deliberately **OFF** (character over plastic — texture controlled by exposure, not the smoothing dial); Adobe RGB color space (export sRGB for web); JPEG; DR200 needs ISO ≥ ~320.

> Self note 2026-05-17 (provenance / camera): committed to camera slot **CUSTOM 2**. Two panel readings differed only on push/pull (0 EV vs +2/3 EV); owner's call — **+2/3 is the nominal portrait bias, but it's a range set by the scene**, recorded as such. Not panel-verified for ISO.

> Self note 2026-05-17 (EV is the flattery dial): consistent with the [[recipes/brians-sepia]] two-EV debrief and [[concepts/portraits-and-skin-rendering]] — *brighter softens skin / de-emphasizes texture; slightly darker models with more character.* With Smooth Skin OFF, exposure is the primary flattery control for this recipe; the +2/3..0 range is exactly that lever.

> Self note 2026-05-17 ([[synthesis/photographer-profile]], [[synthesis/recipe-roster-review]]): **revealed preference — flagged contradiction.** The profile deprioritizes portrait ("people shot rarely → low priority"), but a *dedicated* People recipe is actively maintained on the camera. Keep both: the inference stands as written, but People is weighted as a **kept committed slot**, not a low-priority gap. This also partly closes the long-open smooth-skin/younger-subject thread — the skin-kind recipe it kept asking for now exists; the open item becomes a People-vs-SCU same-face A/B, not "uncovered."

Sibling to [[recipes/soft-color-universe]] (shared Astia parent, opposite tuning: SCU records the scene; People flatters the face). Provenance: self-authored — devised by the photographer (AI-assisted, hand-tuned), filed from camera slot CUSTOM 2. `author: self` (confirmed 2026-05-17).
