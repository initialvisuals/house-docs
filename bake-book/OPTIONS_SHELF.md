# Options shelf (FoW settings UI)

House contract for FoW Options / settings UI (2026-09-10). **Holding / locked intent — not shipped.** Steal from this sheet, not chat. Do **not** invent numeric defaults unless already tip-locked elsewhere. No code. Clerk owns this sheet.

Flesh out Options with resolution, graphics quality, FOV, mouse/aim sens, remaps, Tab inventory press-toggle. Refer Concrete Echo for remap patterns.

Shipped Options shell stays: Augury list chrome **#45** · Hypha Graphics/Gameplay/Controls guts **#46** · GPU post **#55** · Graphics dump **#86** · WARP **#90** · Range Audio mixer **#21** + DEVICE **#82**. This sheet is the **next** pane flesh-out — not a second overlay.

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
| **Mouse vertical sensitivity** | Separate V | Existing Controls look scale is a **single** `LOOK_MUL` (**1.0** / min **0.25** / max **2.0** / step **0.05** — **#46**). Split V/H is this sheet. Do not invent new V numbers |
| **Mouse horizontal sensitivity** | Separate H | Same `LOOK_MUL` lock. Invert Y already a toggle. #51 dizzy-play invert horizontal stays LAST_PASS. Do not invent new H numbers |
| **Aim / ADS sensitivity** | **Separate** from hip / normal look sens | ADS look **0.86** / blend **6.4** already Range feel (**#57** / **#113** scales blend by kit ergo). That is feel-sheet ADS weight — **not** an Options ADS-sens default. Hip vs ADS must stay **two dials**. Do not invent a new ADS multiplier |

Range Tech owns V/H + hip vs ADS. Hypha owns the FOV slider + Graphics pane seat. AIM TUNE PX-wall cook is Range **parallel** (`shoulder_x_max` **±0.50** already **#138**) — not this sheet’s implementation.

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
| **Range Tech** | Mouse V/H sens, hip vs ADS aim sens; AIM TUNE PX-wall cook parallel (**#138** already landed — not this sheet) |
| **Augury** | Input remapping (CE), Tab inventory press-toggle no hold-flash |
| **Beabim** | Off unless net-related |
| **Clerk** | This sheet |

## Explicitly parked

- **Invented default numbers.** Do not invent slider mins / maxes / steps, quality-tier ints, AA-strength defaults, or Steam-survey pixel pairs beyond the table above.
- **Powder A/B/C** until Evan locks. Do not invent powder ids or dials.
- **PX clamp fix** is Range cook (**#138** `shoulder_x_max` **±0.50**), not this sheet’s implementation.
- Bloom / godRays / brightness / gamma — still **no path** (**#86**).
- Scope glass / LPVO — still holding until LPVO (Hypha Graphics when it lands).
- STREAM / `StreamPolicy` window / wide / resident — Hypha TERRAIN / LAST_PASS. Not this shelf.

See `PEEK_FINDINGS.md` Holding / locked intent — Options shelf. Overnight cooks steal from this sheet.
