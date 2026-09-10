# Options shelf (FoW settings UI)

House contract for FoW Options / settings UI (2026-09-10). **Partial shipped #163 + #164** — Range Tech Controls mouse V/H + hip/ADS · Hypha Graphics **RES / FOV / AA / AA STR / AO / POST**. Remaps / Tab press-toggle stay **holding / locked intent**. Steal from this sheet + fulcrumRust [`docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md) + [`docs/OPTIONS_GRAPHICS_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_GRAPHICS_DIAL_SHEET.md), not chat. Do **not** invent numeric defaults unless already tip-locked elsewhere. No code. Clerk owns this sheet.

Flesh out Options with resolution, graphics quality, FOV, mouse/aim sens, remaps, Tab inventory press-toggle. Refer Concrete Echo for remap patterns.

Shipped Options shell stays: Augury list chrome **#45** · Hypha Graphics/Gameplay/Controls guts **#46** · GPU post **#55** · Graphics dump **#86** · WARP **#90** · Range Audio mixer **#21** + DEVICE **#82** · Range Controls mouse V/H + hip/ADS **#163** · Hypha Graphics shelf **#164**. This sheet is the **next** pane flesh-out — not a second overlay. Canonical mouse-sens + Graphics dials live on fulcrumRust — house [`OPTIONS_MOUSE_SENS.md`](OPTIONS_MOUSE_SENS.md) + [`OPTIONS_GRAPHICS.md`](OPTIONS_GRAPHICS.md) are pointers, not second tables.

## Resolution

Dropdown presets beside WINDOW. Hypha owns the list + window wiring. **Landed #164.**

| Preset | Lock |
|--------|------|
| **NATIVE** | Desktop native. Default. Do not invent a pixel pair |
| **1280×720** | Already tip-locked as #46 Windowed size |
| **1920×1080** | |
| **Ultrawide 2560×1080** | |
| **2560×1440** | |
| **3840×2160 (4K)** | |
| **UW 4K CLASS** | Applies **3840×1600** class |
| **3440×1440** | Evan native curved UW |
| **Steam survey fill** | **2560×1600 / 1920×1200 / 1366×768** (July 2026 primary display; next-most-common pairs not already on the shelf) |

Window mode already live **#46**: Borderless default · Windowed decorated 1280×720 · Exclusive (borderless fallback). Borderless stays desktop-native (no second borderless-at-res story). Windowed uses the preset (Native → monitor size). Exclusive picks the closest video mode.

## Graphics

Quality / type rows. Hypha Graphics pane **landed #164**. Texture / mipmap stay Lab-Rat.

| Dial | Intent | Tip lock (stolen #164 — do not invent past this) |
|------|--------|--------------------------------------------------|
| **AA Type** | Dropdown | **FXAA / OFF**. Default FXAA. Live AA is luma-edge FXAA (**#55** Mycelium `fxaa.rs`). TAA later. Do not invent a longer type list |
| **AA STR** | Strength on the chosen AA | **0–1** on the live #55 mix. Default **0.5** = pass knob. **Not** CA strength **0.35** / step **0.05** (**#46**) |
| **Texture quality** | Lab-Rat vendor COL lane | Near grit vendor **256²** (**#58** / **#144** `pbr=vendor`). Not an Options default invented here. **Not** #164 |
| **Mipmap quality** | Lab-Rat `lod_mips` / `FULCRUM_UV` | Hypha LOD rings near **256²** / mid **64²** / far **16²** (**#60**). Rings stay STREAM/LOD — not an Options default invented here. **Not** #164 |
| **AO** | Quality on the #55 SSAO pass | **OFF / LOW / HIGH**. Default Off. Low = live #55 8-tap · r **0.55**. High = Mycelium **24**-tap, same 0.55 radius. No invented radius |
| **POST** | Overall post quality | **OFF / LOW / HIGH**. Default **HIGH**. Off skips Options post (AO/AA/CA/grain/DoF/WARP). Low = AA only (if FXAA). High honors individual flags. Heat #66 + wound #143 stay. Bloom / godRays / brightness / gamma **no path** (**#86**) |

Graphics pane wiring (rows + persist on `project.json`) is Hypha. Texture / mipmap *authority* is Lab-Rat (vendor COL / `lod_mips` / `FULCRUM_UV`). Do not dump atelier into Options Graphics.

## Camera / feel

| Dial | Intent | Already tip-locked (do not invent past this) |
|------|--------|---------------------------------------------|
| **FOV** | Hip **base** | **Landed #164.** Options hip base default **90**. ADS still lerps to authored optic FOVs: iron/holo **60** · acog **25** · canted **60** CQC · scope **10** (**#14** / **#22** / **#100**). Feel-sheet locks are **not** overwritten. Pane min/max/step **70 / 110 / 1** are Hypha chrome — **not** tip-locked |
| **MOUSE V** | Separate V | **Landed #163.** Controls **MOUSE V** (`look_mul_v`) **1.00** on the existing `LOOK_MUL` lock **0.25–2.00** / step **0.05** (**#46**). Invert Y stays a toggle. #51 dizzy-play invert X stays LAST_PASS. Do not invent new V numbers |
| **MOUSE H** | Separate H | **Landed #163.** Controls **MOUSE H** (`look_mul_h`) **1.00** on the same `LOOK_MUL` lock. Old single `look_mul` seeds both axes when the split keys are absent |
| **HIP** | Non-ADS look | **Landed #163.** Controls **HIP** (`hip_look_mul`) **1.00**. Separate from ADS. Same lock |
| **ADS** | Aim look, **separate** from hip | **Landed #163.** Controls **ADS** (`ads_look_mul`) **1.00**. Feel-sheet ADS weight **0.86** / blend **6.4** stay DNA (**#57** / **#113** scales blend by kit ergo) — Options ADS is a user mul on top, default **1.00**. Do not invent a new ADS multiplier |

Range Tech owns V/H + hip vs ADS — **shipped #163**. Hypha owns FOV + Graphics pane — **shipped #164**. AIM TUNE PX-wall cook is Range **parallel** (`shoulder_x_max` **±0.50** already **#138**) — not this sheet’s implementation. AIM TUNE LIVE per-kit pull **#167** is also Range parallel (`aim_live` + `aim_tune.*`; no new keys) — not this sheet.

## Landed #164 — Graphics RES / FOV / AA / AO / POST

Steal from fulcrumRust [`docs/OPTIONS_GRAPHICS_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_GRAPHICS_DIAL_SHEET.md) (merge `159b3d11`). Do **not** invent numbers.

| Row | Persist | Lock |
|-----|---------|------|
| **RES** | `resolution` | Default **NATIVE**. Shelf presets + UW 4K CLASS (3840×1600) + Evan **3440×1440** + Steam survey fill **2560×1600 / 1920×1200 / 1366×768** |
| **FOV** | `fov_hip` | Hip **base** **90**. ADS optic locks still win |
| **AA** | `aa_type` | **FXAA / OFF**. Default FXAA |
| **AA STR** | `aa_strength` | **0.50** = live #55 mix. Not CA 0.35 |
| **AO** | `ao_quality` | **OFF / LOW / HIGH**. Default Off. Low 8-tap · r **0.55**. High **24**-tap, same radius |
| **POST** | `post_quality` | **OFF / LOW / HIGH**. Default **HIGH** |

Compat: old `"ao"` / `"aa"` bools still load (true → AO Low / AA FXAA). New keys win when present. WINDOW / CA / GRAIN / DOF / FOG / CAM / WARP / STREAM unchanged.

## Landed #163 — Controls mouse V/H + hip/ADS

Steal from fulcrumRust [`docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md) (merge `96e4410e`). Do **not** invent numbers.

| Row | Persist | Lock |
|-----|---------|------|
| **MOUSE H** | `look_mul_h` | **1.00** · `LOOK_MUL` **0.25–2.00** / step **0.05** |
| **MOUSE V** | `look_mul_v` | **1.00** · same lock |
| **HIP** | `hip_look_mul` | **1.00** · same lock |
| **ADS** | `ads_look_mul` | **1.00** · same lock. **Not** feel `AdsHipDials.ads_look_mul` **0.86** |

Feel-lab `MoveDials.look_sens` **0.0022** + FOV-matched ADS weight stay DNA — these are user muls on top. Persist `project.json` on the existing Hypha save path. Default all-1.00 Options ⇒ same look as the old single LOOK **1.00**. Invert Y stays.

## Holding — Options default hip (Chest vs Low) — not this shelf

Evan lock. Options default hip **Chest (default)** vs **Low** toggle. In-play two poses only (chosen hip + canted). Shotgun may force Low later. Do **not** add READY HIP persist rows here. Do **not** claim the hip toggle or Powder B landed. Do **not** invent implementation. #168 play U stays two poses without restamping this seat.

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
| **Hypha** | Resolution, FOV, AA type/strength, AO, post quality, Graphics pane wiring — **landed #164** |
| **Lab-Rat** | Texture quality, mipmap quality (vendor COL / `lod_mips` / `FULCRUM_UV`) |
| **Range Tech** | Mouse V/H + hip/ADS **landed #163**; AIM TUNE PX-wall cook parallel (**#138** / **#159** already landed — not this sheet); AIM TUNE LIVE per-kit pull **#167** parallel (not this sheet). Options default hip Chest vs Low + Powder B still cooking — do **not** claim landed |
| **Augury** | Input remapping (CE), Tab inventory press-toggle no hold-flash |
| **Beabim** | Off unless net-related |
| **Clerk** | This sheet |

## Explicitly parked

- **Invented default numbers.** Do not invent slider mins / maxes / steps beyond stolen #164 chrome honesty (FOV 70–110 / step 1 is **not** tip-locked). Mouse V/H / hip / ADS steal **#163** only. Graphics steal **#164** only.
- **Powder A/B/C** until Evan locks. Do not invent powder ids or dials. Do **not** claim Powder B landed.
- **Options default hip Chest vs Low toggle.** Do **not** add READY HIP rows on this shelf. Do **not** claim the hip toggle landed.
- **fulcrumRust #167** AIM TUNE live-save — **landed** (Range parallel persist cook — not this sheet).
- **PX clamp fix** is Range cook (**#138** `shoulder_x_max` **±0.50** · **#159** `TUNE_POS_X_ABS` **0.50**), not this sheet’s implementation.
- Bloom / godRays / brightness / gamma — still **no path** (**#86**).
- Scope glass / LPVO — still holding until LPVO (Hypha Graphics when it lands).
- STREAM / `StreamPolicy` window / wide / resident — Hypha TERRAIN / LAST_PASS. Not this shelf.

See `PEEK_FINDINGS.md` Holding / locked intent — Options shelf. Overnight cooks steal from this sheet.
