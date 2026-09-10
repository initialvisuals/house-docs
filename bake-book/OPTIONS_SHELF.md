# Options shelf (FoW settings UI)

House contract for FoW Options / settings UI (2026-09-10). **Partial shipped #163** — Range Tech Controls mouse V/H + hip/ADS. Resolution / graphics quality / FOV slider / remaps / Tab press-toggle stay **holding / locked intent**. Steal from this sheet + fulcrumRust [`docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md), not chat. Do **not** invent numeric defaults unless already tip-locked elsewhere. No code. Clerk owns this sheet.

Flesh out Options with resolution, graphics quality, FOV, mouse/aim sens, remaps, Tab inventory press-toggle. Refer Concrete Echo for remap patterns.

Shipped Options shell stays: Augury list chrome **#45** · Hypha Graphics/Gameplay/Controls guts **#46** · GPU post **#55** · Graphics dump **#86** · WARP **#90** · Range Audio mixer **#21** + DEVICE **#82** · Range Controls mouse V/H + hip/ADS **#163**. This sheet is the **next** pane flesh-out — not a second overlay. Canonical mouse-sens dials live on fulcrumRust — house [`OPTIONS_MOUSE_SENS.md`](OPTIONS_MOUSE_SENS.md) is a pointer, not a second table.

## Resolution

Dropdown presets (hardware survey–minded). Hypha owns the list + window wiring.

| Preset | Lock |
|--------|------|
| **Native** | Desktop native. Do not invent a pixel pair |
| **1280×720** | Already tip-locked as #46 Windowed size |
| **1920×1080** | |
| **Ultrawide 2560×1080** | |
| **2560×1440** | |
| **3840×2160 (4K)** | |
| **Ultrawide 4K class** | 3840×1600 class. Do **not** invent an exact pixel pair if unsure — label **ultrawide 4K class** |
| **3440×1440** | Evan native curved UW |
| **Steam survey fill** | Other typical Steam survey resolutions when Hypha implements. Do **not** invent a long fake list — say **Steam survey fill when cooked** |

Window mode already live **#46**: Borderless default · Windowed decorated 1280×720 · Exclusive (borderless fallback). Resolution dropdown sits beside that — do not invent a second window story.

## Graphics

Quality / type rows. Do **not** invent Low / Med / High numbers or default strengths unless already tip-locked.

| Dial | Intent | Already tip-locked (do not invent past this) |
|------|--------|---------------------------------------------|
| **AA Type** | Dropdown | Live AA is luma-edge FXAA (**#55** Mycelium `fxaa.rs`). TAA later. Do not invent a longer type list |
| **AA strength** | Strength on the chosen AA | CA strength already **0.35** / step **0.05** / range **0–1** (**#46**). That is CA, not AA. Do not invent an AA-strength default |
| **Texture quality** | Lab-Rat vendor COL lane | Near grit vendor **256²** (**#58** / **#144** `pbr=vendor`). Not an Options default invented here |
| **Mipmap quality** | Lab-Rat `lod_mips` / `FULCRUM_UV` | Hypha LOD rings near **256²** / mid **64²** / far **16²** (**#60**). Rings stay STREAM/LOD — not an Options default invented here |
| **AO quality** | Quality on the #55 SSAO pass | AO is a live toggle today. Do not invent tap counts or radius |
| **Post-processing quality** | Overall post quality | Live stack **#55**: AO / AA / CA / grain / DoF (+ **#66** heat warp / **#90** WARP / **#68** ADS DoF / **#143** wound consume). Bloom / godRays / brightness / gamma **no path** (**#86**). Do not invent an overall-quality number |

Graphics pane wiring (rows + persist on `project.json`) is Hypha. Texture / mipmap *authority* is Lab-Rat (vendor COL / `lod_mips` / `FULCRUM_UV`). Do not dump atelier into Options Graphics.

## Camera / feel

| Dial | Intent | Already tip-locked (do not invent past this) |
|------|--------|---------------------------------------------|
| **FOV** | Slider | Authored kit/optic FOV stays LAST_PASS: hip **90** · iron ADS **60** · holo ADS **60** · acog ADS **25** · canted ADS **60** CQC (**#14** / **#22** / **#100**). Those are optic locks, **not** an Options slider default. Do not invent slider min / max / step |
| **MOUSE V** | Separate V | **Landed #163.** Controls **MOUSE V** (`look_mul_v`) **1.00** on the existing `LOOK_MUL` lock **0.25–2.00** / step **0.05** (**#46**). Invert Y stays a toggle. #51 dizzy-play invert X stays LAST_PASS. Do not invent new V numbers |
| **MOUSE H** | Separate H | **Landed #163.** Controls **MOUSE H** (`look_mul_h`) **1.00** on the same `LOOK_MUL` lock. Old single `look_mul` seeds both axes when the split keys are absent |
| **HIP** | Non-ADS look | **Landed #163.** Controls **HIP** (`hip_look_mul`) **1.00**. Separate from ADS. Same lock |
| **ADS** | Aim look, **separate** from hip | **Landed #163.** Controls **ADS** (`ads_look_mul`) **1.00**. Feel-sheet ADS weight **0.86** / blend **6.4** stay DNA (**#57** / **#113** scales blend by kit ergo) — Options ADS is a user mul on top, default **1.00**. Do not invent a new ADS multiplier |

Range Tech owns V/H + hip vs ADS — **shipped #163**. Hypha owns the FOV slider + Graphics pane seat. AIM TUNE PX-wall cook is Range **parallel** (`shoulder_x_max` **±0.50** already **#138**) — not this sheet’s implementation.

## Landed #163 — Controls mouse V/H + hip/ADS

Steal from fulcrumRust [`docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md) (merge `96e4410e`). Do **not** invent numbers.

| Row | Persist | Lock |
|-----|---------|------|
| **MOUSE H** | `look_mul_h` | **1.00** · `LOOK_MUL` **0.25–2.00** / step **0.05** |
| **MOUSE V** | `look_mul_v` | **1.00** · same lock |
| **HIP** | `hip_look_mul` | **1.00** · same lock |
| **ADS** | `ads_look_mul` | **1.00** · same lock. **Not** feel `AdsHipDials.ads_look_mul` **0.86** |

Feel-lab `MoveDials.look_sens` **0.0022** + FOV-matched ADS weight stay DNA — these are user muls on top. Persist `project.json` on the existing Hypha save path. Default all-1.00 Options ⇒ same look as the old single LOOK **1.00**. Invert Y stays.

## Holding — Options default hip (Chest vs Low) — not shipped

Evan lock. Options default hip **Chest (default)** vs **Low** toggle. In-play two poses only (chosen hip + canted). Shotgun may force Low later. Range still cooking this tip + Powder B separately. Do **not** claim the hip toggle or Powder B landed. Do **not** invent implementation.

## Input

| Dial | Intent |
|------|--------|
| **Input remapping** | **Missing.** Steal Concrete Echo remap patterns (Augury). LAST_PASS already parks FoW OG input manager as still cooking; binds stay README today (`LOOK SITS ON FEEL-LAB SENS · BINDS IN README`). Do not invent a bind table or default keys here |
| **Tab → inventory** | Press to open, press again to close. **No hold-flash** while bouncing Tab. LAST_PASS already seats **Tab** = inventory / status (includes health). This sheet locks **press-toggle**, not hold-to-peek. Do not invent flash timings |

Augury owns remaps + Tab press-toggle. Do not flash INV/STATUS on Tab-down while the key bounces.

## Related tip — STREAM Options (do not re-own)

STREAM Options (`StreamPolicy` window / wide / resident) already **Hypha**. Link [`TERRAIN_NORTHSTAR.md`](TERRAIN_NORTHSTAR.md) + [`FULCRUMRUST_LAST_PASS_LOCK.md`](FULCRUMRUST_LAST_PASS_LOCK.md) + fulcrumRust [`docs/TERRAIN.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/TERRAIN.md). Live walk: **#137** 11×11 (`STREAM_RINGS` 5 · prefetch=5+heading · hold=2/12) · **#142** pend coalesce `2/2`. Do **not** re-own STREAM / hitch / hold on this sheet.

## Seat map

| Seat | Owns |
|------|------|
| **Hypha** | Resolution, FOV, AA type/strength, AO, post quality, Graphics pane wiring |
| **Lab-Rat** | Texture quality, mipmap quality (vendor COL / `lod_mips` / `FULCRUM_UV`) |
| **Range Tech** | Mouse V/H + hip/ADS **landed #163**; AIM TUNE PX-wall cook parallel (**#138** / **#159** already landed — not this sheet). Options default hip Chest vs Low + Powder B still cooking — do **not** claim landed |
| **Augury** | Input remapping (CE), Tab inventory press-toggle no hold-flash |
| **Beabim** | Off unless net-related |
| **Clerk** | This sheet |

## Explicitly parked

- **Invented default numbers.** Do not invent slider mins / maxes / steps, quality-tier ints, AA-strength defaults, or Steam-survey pixel pairs beyond the table above. Mouse V/H / hip / ADS steal **#163** only.
- **Powder A/B/C** until Evan locks. Range is still cooking Powder B separately from #163. Do not invent powder ids or dials. Do **not** claim Powder B landed.
- **Options default hip Chest vs Low toggle.** Evan locked intent. In-play two poses only (chosen hip + canted); shotgun may force Low later. Range still cooking. Do **not** claim the hip toggle landed. Do **not** invent implementation.
- **PX clamp fix** is Range cook (**#138** `shoulder_x_max` **±0.50** · **#159** `TUNE_POS_X_ABS` **0.50**), not this sheet’s implementation.
- Bloom / godRays / brightness / gamma — still **no path** (**#86**).
- Scope glass / LPVO — still holding until LPVO (Hypha Graphics when it lands).
- STREAM / `StreamPolicy` window / wide / resident — Hypha TERRAIN / LAST_PASS. Not this shelf.

See `PEEK_FINDINGS.md` Holding / locked intent — Options shelf. Overnight cooks steal from this sheet.
