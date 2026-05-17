---
type: synthesis
created: 2026-05-17
updated: 2026-05-17
sources: [recipes/soft-color-universe]
tags: [synthesis, debrief, running-log]
---

# Shoot debriefs

Reverse-chronological. Each entry: conditions, recipe, what worked, what to fix, one thing to drill next. The skill loop — see `CLAUDE.md` → Shoot debrief.

---

## 2026-05-17 — Blue hour, campus exterior · [[recipes/soft-color-universe]]

**Conditions:** Deep twilight / blue hour. Mixed light: cool ambient sky vs. warm artificial streetlamps and facade lighting. Static architectural subject (campus building, tower, lamp-lit trees). Appears low-ISO / stable (clean shadows). Image reviewed from chat — *not filed to `raw/assets/`* (no file on disk; drop the JPEG there to make it permanently citable).

**What worked — recipe over-performed outside its `best_for`:**
- **Warm/cool color separation is excellent.** Color +3 + Color Chrome Strong + FX Blue Weak render a rich cobalt sky against amber lamplight without going garish — the palette is the photo's strength.
- **Auto WB held mixed light well.** It preserved the blue of twilight (didn't neutralize the mood) while letting tungsten/warm lamps stay warm. No muddy cross-contamination.
- **Soft tone curve suited the scene.** Highlight −1 / Shadow −1 + DR200 protected the lit facade (texture retained, not clipped) and kept shadows deep but readable — no harsh blowouts despite high scene dynamic range.
- **Clarity +3 / Sharpness +1 / NR −4 clean.** Crisp brick and foliage detail, no objectionable noise → confirms NR −4 is fine at low ISO.

**What to fix / limits to find:**
- **Bare lamp globes clip to white with bloom.** Acceptable for night, but the recipe doesn't (can't) save bare point sources — capture-side EV is the lever, not the recipe.
- **Composition is the weak link, not the recipe.** Three competing structures (tree / tower / right-hand wall); the large flat building wall is dead space. The sidewalk+railing leading line toward the tower is the strongest idea — it isn't committed to.
- **NR −4 untested at high ISO.** This frame was clean but low-ISO; the real night limit is unknown.

**Verdict:** Soft Color Universe is a strong blue-hour / mixed-light recipe, not just a daylight one. `best_for` updated.

**Drill next:** Reshoot a blue-hour scene with **EV bracketed 0 / −1/3 / −2/3**, watching the lamp globes and sky depth — learn exactly where DR200 + Highlight −1 stops protecting highlights. Composition constraint: **one subject, one leading line** — no frames with three buildings.
