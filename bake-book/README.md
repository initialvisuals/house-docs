# Bake book

House archive for **bakeable leftovers** from the Pycelium / mesocosm sim lab — visual and metric references MyceliumEngine and Concrete Echo can steal without keeping a live organic stew in the game runtime.

## Purpose

Park screenshots, param notes, and qualitative callouts next to the glyph legend so Engine / CE agents do not have to scroll chat for:

- Accidental boss / FX silhouettes
- Arena-graph and density-mask candidates
- Cord vs explorative growth looks
- Slice / cross-section anastomosis webs

This folder is a **reference shelf**, not a science claim. Numbers and shots are sim artifacts unless a row is marked measured.

fulcrumRust owns the port docs (`docs/STEAL_MAP.md`, `AXIS.md`, `TERRAIN.md`, `MILESTONE_01_PLAYABLE.md`, `CHANNELS.md`, `PVP_DIAL_SHEET.md`, `BIPED_3P_DIAL_SHEET.md`, `WOUND_FEEL_DIAL_SHEET.md`, `STAMP_PBR_DIAL_SHEET.md`, `HEAT_WARP_DIAL_SHEET.md`, `MP_WEAPON_DIAL_SHEET.md`, `SOFT_RIM_DIAL_SHEET.md`, `BALLISTICS_A_DIAL_SHEET.md`, `OPTIONS_MOUSE_SENS_DIAL_SHEET.md`, `AIM_TUNE_LIVE_SAVE.md`, `OPTIONS_GRAPHICS_DIAL_SHEET.md`, `PREFERRED_HAND_A_DIAL_SHEET.md`, `OPTIONS_DEFAULT_HIP_DIAL_SHEET.md`, plus stamps / growth). House-docs bake-book is the **dial shelf** — readable enough for seats without reading every `.rs`.

## What to drop here

| Kind | Examples | Intended reuse |
|------|----------|----------------|
| **Burj** | Tall column / mushroom-tower silhouettes from beast-mode tip plumes | Boss forms, landmark props, vertical FX |
| **Angel-hair** | Fine cord strands, wispy lattice between hubs | Enemy trails, goop FX, soft collision scatter |
| **Slice / webs** | Floor-network anastomosis, pockets, hubs from depth-slice views | Arena graphs, density masks, crimson/backrooms goop budgets |

Prefer filenames like `YYYY-MM-DD_preset_note.png` plus a one-line note in a sibling `.txt` or in the Pycelium experiment log when that lands.

## Related house notes

- Axis lock (cam −Z / CE +X / barrel +Z) → [`AXIS_LOCK.md`](AXIS_LOCK.md)
- Progression spine (FoW SP climb inside PvPvE + factions — **holding / locked intent**, not shipped) → [`PROGRESSION_SPINE.md`](PROGRESSION_SPINE.md)
- Options shelf (FoW settings UI — **READY HIP landed #165** Chest/Low + two-pose U; remaps / Tab press-toggle still **holding**; Range mouse V/H + hip/ADS **landed #163**; Hypha Graphics **RES / FOV / AA / AA STR / AO / POST landed #164**) → [`OPTIONS_SHELF.md`](OPTIONS_SHELF.md) + house pointers [`OPTIONS_MOUSE_SENS.md`](OPTIONS_MOUSE_SENS.md) + [`OPTIONS_GRAPHICS.md`](OPTIONS_GRAPHICS.md) → fulcrumRust [`docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md) + [`docs/OPTIONS_GRAPHICS_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_GRAPHICS_DIAL_SHEET.md) + [`docs/OPTIONS_DEFAULT_HIP_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_DEFAULT_HIP_DIAL_SHEET.md)
- Terrain tune iterator (FoW live dials + **Refresh** / partial remesh — **holding / locked intent**, not shipped; peek default **underfoot + Refresh**) → [`TERRAIN_TUNE.md`](TERRAIN_TUNE.md)
- Ballistics spine (arc **A** leftover — Beabim leftover/net **landed #160**; Range loft DNA + AIM TUNE **MODEL** stash **landed #161**; Powder **B** slightly hot service **landed #166** SR-25 **785 → 810** steal M24 · gravity **9.8** / zero **100 m** held · **A** restoreable · **C** arcade parked; `hitscan` / `ballistic_A` stash) → [`BALLISTICS_SPINE.md`](BALLISTICS_SPINE.md) + fulcrumRust [`docs/BALLISTICS_A_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/BALLISTICS_A_DIAL_SHEET.md)
- Hold pose spine (grip-invariant PreferredHand **A** / AIM TUNE — **landed #168** one right bank + sagittal HAND L/R mirror + HAND chrome + ADS crosshair hide; Options READY HIP **#165** intersects the pose home without inventing HAND chrome) → [`HOLD_POSE_SPINE.md`](HOLD_POSE_SPINE.md) + house pointer [`PREFERRED_HAND_A.md`](PREFERRED_HAND_A.md) → fulcrumRust [`docs/PREFERRED_HAND_A_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/PREFERRED_HAND_A_DIAL_SHEET.md)
- Glyph HUD decode → [`../glyph-legend.md`](../glyph-legend.md)
- Heat dials (Range Tech **#129** CE tip 0.2.8 field · **#155** visible hold-J warp) → [`../heat-card-dial-sheet.md`](../heat-card-dial-sheet.md) + [`HEAT_WARP_DIAL_SHEET.md`](HEAT_WARP_DIAL_SHEET.md)
- Vector mag dump (muzzle rect flash / grit / glyphs — live steal **landed #89**) → [`VECTOR_MAG_DUMP.md`](VECTOR_MAG_DUMP.md)
- AIM TUNE Pos X travel (Range Tech **#138** ±0.50 · **#159** `TUNE_POS_X_ABS` **0.50** floor · End home snap `hold_blend` · leftover +0.226 ≠ End box) → fulcrumRust [`docs/AIM_TUNE_X_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/AIM_TUNE_X_DIAL_SHEET.md)
- AIM TUNE LIVE per-kit persist (Range Tech **#167** + two-exe **#169** — `aim_live` + `aim_tune.*` unchanged; per-kit pull must not clobber other guns with authored defaults; apply snaps `hold_blend`; absolute `FULCRUM_SETTINGS` / cwd path · flush absorb undirty · `project.json.lock`; two-instance is **not** a soft follow) → house pointer [`AIM_TUNE_LIVE_SAVE.md`](AIM_TUNE_LIVE_SAVE.md) → fulcrumRust [`docs/AIM_TUNE_LIVE_SAVE.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/AIM_TUNE_LIVE_SAVE.md)
- PVP leftover (Beabim **#133** KIND_PVP default off · hide names · KIND_BRASS · eye 1.60/1.62 · rim respawn · **#139** HOST session board / no-127 invite · **#141** PVP honesty / PeerBody leftover / HP-AR Sync / unique pads · **#147** leftover ray **500 m** was 80 · flat `SMG_PELLET` **14** · Locus yard keeps own 80 · **#160** `KIND_SHOT` loft + `ballistic_A` leftover / hitscan stash · **#161** Range loft DNA + AIM TUNE **MODEL** stash · **#166** Range Powder **B** slightly hot service (SR-25 **785 → 810** steal M24) · **#153** hub no-loot / `HUB_PROTECT_SECS` **15** / `protect_ms`) → fulcrumRust [`docs/PVP_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/PVP_DIAL_SHEET.md) + [`docs/BALLISTICS_A_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/BALLISTICS_A_DIAL_SHEET.md)
- MP weapon honesty + hideout hub PeerBodies (Beabim **#153** — `KIND_LOOT_WORLD` **15** · mag/reserves/attach persist no magic · held 3P kit on PeerBody lean · hideout PeerBodies · hub no-loot downs · `HUB_PROTECT_SECS` **15**) → fulcrumRust [`docs/MP_WEAPON_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/MP_WEAPON_DIAL_SHEET.md) + house [`HIDEOUT_HUB.md`](HIDEOUT_HUB.md) (soft leftover landed; floorplan metres **pending**)
- Wound feel / 1P screen-react (Range Tech **#143** — suppress-near soft short blur · armour jostle + soft blur no red · HP stronger jostle + blur + red fade · envelope `--===--------` · never full-strength blur · 1P local; Hypha `post.wound` [blur, red]; hooks Beabim KIND_PVP Hit not Sync; Death/Slain stays Augury) → fulcrumRust [`docs/WOUND_FEEL_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/WOUND_FEEL_DIAL_SHEET.md)
- 4× world + pend coalesce (Hypha **#142** — 37×37 / 592 m / ~350k · STREAM held 11×11 · `coalesce=2/2` · rim 288 m) → fulcrumRust [`docs/TERRAIN.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/TERRAIN.md) + [`docs/SPAWNS.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/SPAWNS.md)
- Landmark AABB ride (Hypha **#136** — `RIDE_STEP` 0.50 · `RIDE_SKIN` 0.06 · `SUPPORT_STEP` 0.25) → fulcrumRust [`docs/LANDMARK_RIDE.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/LANDMARK_RIDE.md)
- 3P biped / PeerBody (Hypha **#131** — eye 1.60 · head 1.62 centered · left-offset killed) → fulcrumRust [`docs/BIPED_3P_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/BIPED_3P_DIAL_SHEET.md)
- Stamp / building / terrain PBR polish (Lab-Rat **#144** — rocks 3-lobe shade/face/chip · buildings Concrete grade + face UVs · default `pbr=vendor` 256² COL · five thumbs + concrete NRM; texture+UV only; chunk 16 m held) → fulcrumRust [`docs/STAMP_PBR_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/STAMP_PBR_DIAL_SHEET.md)
- Visible barrel heat warp (Range Tech **#155** — `haze_strength` **0** off / **0.01** CE enable floor / **0.11** stolen max; post `visual × lattice × 1.35` at the floor; shader gate **0.001**; tip cards `scale_x/y` **0.28/0.86**; Options **WARP** is Hypha pixellation) → [`HEAT_WARP_DIAL_SHEET.md`](HEAT_WARP_DIAL_SHEET.md) + fulcrumRust [`docs/HEAT_WARP_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/HEAT_WARP_DIAL_SHEET.md)
- Hideout hub (FoW pre-raid friend hub — Beabim leftover **landed #153**; floorplan metres **pending Evan tip**) → [`HIDEOUT_HUB.md`](HIDEOUT_HUB.md)
- Soft rim leftover (Augury **#156** — glasses `SIGNAL  THINS` / `CARRIER  LOST` + death-DNA glitch + FX `Slot::Crackle`; Hypha `RimHook` physics read-only `RIM_SOFT_M` **24** / world rim ~**422**; approach **0.08** → peak **0.28** · block **0.36** · chroma **0.012**; no Slain plate; thin hold **#158** spring-stop `approaching && t >= 0.995` stays BLOCK / `CARRIER  LOST` / glitch **0.36** + crackle — Hypha `blocked` is crossing-frame only) → fulcrumRust [`docs/SOFT_RIM_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/SOFT_RIM_DIAL_SHEET.md) + house `PEEK_FINDINGS.md` Closed by #156
- FoW palette / `FOW_*` color kit (`fow_palette/v1`) → [`../FOW_PALETTE.md`](../FOW_PALETTE.md)
- Pycelium experiment-log PR (when merged) → `docs/EXPERIMENT_LOG.md` in `initialvisuals/pycelium`
- Bake metric targets: fusion rate, cord vs explorative tips, C:N hunting paths
- Atelier public-portfolio steal (store `W3np6` / `dBXpg` + seat ownership) → [`ATELIER_PORTFOLIO_STEAL.md`](ATELIER_PORTFOLIO_STEAL.md)
- Holocron file-base viewer (Evan gift; slope/PBR plugs landed #80; Lab-Rat rust rewrite still waits on SVG / density-mask) → [`TOOLS.md`](TOOLS.md)

## Brand DNA

Presentation can nod to the distressed creature mark (**claw first, face second**). Do not invent logo assets here — this shelf is for sim bake refs only.

---

**Initial Visuals** — tools, sims, games, and experiments.
