# Aesthetics / diegetic lock (fulcrumRust)

Parked from Evan (2026-09-07).

## Diegetic labels — **Augury smart-glasses**

Analysis-knowledge-core in-world labels (interacts, extract points, section samplers):
- Thin white mono, fully embodied in world space
- Lead lines + angular digital junk
- Subtle glitches / digital artifacts around the overlays
- Spatially dynamic (not flat HUD chrome)

**Ammo is not glasses.** Glasses stay labels only — never a second ammo HUD.
Shipped label examples: stamp materials · `LOCUS  STANDARD|INKED  <brain>` · `INK HOTSPOT` · ToD/exposure · `HDRI` / `PROC` (Goegap plate #40) · `INSPECT` (hold-` #28) · `RELOAD` / `SWAP` (mag swap #32) · `BANDAGE` / `EMPTY` (bandage use #31) · `Z{n}  SIM|ARCADE` (live HoB zero #33) · `HEAT TUNE` (hold-J heat-tune #35) · `HOST` / `JOIN` / `PEER` (listen-server #34) · `DOWNED` · `DEAD` · `STIM` / `NO STIM` · `RALLY` · `NEED STAB` · `STAB STUB  NO NET` (down/death stub #36; #37 bind `I STIM`) · lean/slide/speed/height peeks.
Goegap plate (fulcrumRust #40): glasses ToD strip may show `HDRI` / `PROC` — still labels only, never a second ammo HUD.
Bandage use (fulcrumRust #31): glasses may flash `BANDAGE` / `EMPTY` on use — still labels only, never a second ammo/health HUD. While downed unstabilized, `NEED STAB` (no consume) — still not a second health HUD (#36).
Live HoB zero / launch (fulcrumRust #33): glasses status strip `Z{n}  SIM|ARCADE` (e.g. `Z100  SIM`); toasts `ZERO  {n} M` / `LAUNCH  ARCADE` / `LAUNCH  SIM` — labels only, never a numeric ammo HUD.
Heat-tune dump (fulcrumRust #35): glasses may flash `HEAT TUNE` (amber-ish overlay) while J is down — still labels only, never a second ammo HUD; must not count mag rounds.
Listen-server (fulcrumRust #34): glasses may show `HOST  ip:port`, then `JOIN` / `PEER` after HELLO/WELCOME — still labels only, never a second ammo HUD.
Down / death stub (fulcrumRust #36 + #37 bind): glasses may flash `DOWNED` · `DEAD` · `STIM` / `NO STIM` · `RALLY` · `NEED STAB` · `STAB STUB  NO NET` (and related toasts / prompts like `HOLD F  SELF-STAB STUB` / `[F] PICK UP STIM` / `STABILIZED  T HEAL / I STIM / SLASH RALLY` / `DEAD  BAG STUB` / `CORPSE RECLAIM STUB`) — still labels only, never a second health HUD. #37 names I stim on the glasses prompt (was `Y STIM`); Y is host only.

## Diegetic gun chrome — **Range Tech** (Sulfur frame)

Ammo lives on the weapon:
- Mag dots / diegetic ammo chrome on the seated feel-lab kit (receiver rail LEDs + plaque; fulcrumRust #14 + #22)
- Well count **is** mag size — MP9-Z **20** / SR-25 **20** / M24 **5**; Hold-R peek becomes that chrome, not a second counter
- Glasses may flash `RELOAD` / `SWAP` during mag swap (fulcrumRust #32) — still no numeric ammo HUD; Hold-R remains peek chrome on the gun. Dials: `RELOAD_PEEK_HOLD_SEC` **0.20** · `RELOAD_DOUBLE_TAP_SEC` **0.30** · `RELOAD_BASIC_SEC` **1.10** · `RELOAD_EMERGENCY_SEC` **0.46**
- Barrel heat stays diegetic on the gun unless a separate heat-tell says otherwise
- Heat-tune dump (fulcrumRust #35): hold **J** still cooks diegetic barrel energy / tip cards + lobe on the same path; glasses `HEAT TUNE` only (amber-ish overlay) — never a numeric ammo HUD; must not count mag rounds
- Optic hoods + .45 can are Range Tech attachments (**V** / **N**, kit allow-list); glasses still labels only
- World drop/pickup (fulcrumRust #19): chrome travels with the loose kit UUID; empty hands hide viewmodel / heat — still no HUD ammo counter
- Hold-` inspect (fulcrumRust #28): reload-lift look-over overlay so the receiver faces the lens; glasses may flash `INSPECT` — still no numeric ammo HUD
- Live HoB zero / launch (fulcrumRust #33): glasses may show `Z{n}  SIM|ARCADE` (e.g. `Z100  SIM`) and toast `ZERO  {n} M` / `LAUNCH  ARCADE` / `LAUNCH  SIM` — still labels only, never a numeric ammo HUD

## Readable floor hotspots

Floor/wall aftermath (spills, barrel-choir embers, Lab-Rat stamps) stays readable without softlocking the path. Loud Inked void-spore scar under `YARD_INKED` is a floor leftover (curl remnants stay). Range Tech leftover feel-lab FX (fulcrumRust #47): punch vs scuff + stuck-slug plug stay floor/wall aftermath; hide-not-despawn via `casing_draw_m` **55** (brass + spent slugs). Mag chrome stays on the kit — no second ammo HUD. Locus hotspot FX language later — see `SULFUR_INFLUENCE.md`.

## Grimdark Locus terraforming (shipped Lab-Rat #20)

Aesthetic lock for Lab-Rat stamps + Range Tech FX contrast (wet-lab → main via fulcrumRust #20):
- **Hellish void spores** — Locus growth language, not cute mushrooms; yard reads webbing / fruiting body / spore tips + **loud Inked floor scar** (left of 2D webbing)
- **Cracks / edge-wear** driven by **2D mushroom density stamps** (`density_stamp_2d` → `WearStamp` on concrete)
- **Brutalist concrete** with procedural wear as the hard backdrop; glasses still labels only (`CONCRETE  STAMP`)
- **Grimdark material grade** — crushed luma on dirt / sand / rock / concrete / organic; organic bleed = void-spore takeover
- Range Tech: grimdark tracers / heat / muzzle on that concrete contrast; performant first. Hide-not-despawn XZ (`casing_draw_m` **55**, fulcrumRust #47) for brass + spent slugs; punch vs scuff impact marks — never a second ammo HUD
- Detail shelf: `STAMP_FEEL_LOCK.md` + fulcrumRust `docs/STAMPS.md`

## Grimdark extract host (shipped Hypha #16)

House `AESTHETIC_DIEGETIC_LOCK` on the Transvoxel host — terrain reads **grim/dense**, not a bright sandbox:
- **Ashen wash / slate sides / brutalist** vertex paint from Lab-Rat `VoxelMaterial::tint` (no second material story)
- Proc **edge-wear / hairline cracks** + denser mid-frequency rubble; void-spore stamp peek tints
- Extract clear is **dimmer** + dual colder lights + **cheap distance haze** (`fs_world`); hideout stays small / unfogged
- Performant first — bake-once mesh, no live carve day-one
- Detail: `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/TERRAIN.md`

## Extract day/night sky (shipped Range Tech #24 + #40)

Feel-lab clock drives extract atmosphere — still grim/dense, not a bright sandbox:
- **One ToD sample** lights ambient / key / fill / fog + procedural dome together (**no XOR sky**). #40 Goegap plate rides the same sample.
- **`EXTRACT_SKY_LUMA` 0.20** crushes noon so day stays ashen; default clock **06:21**; Goegap plate shipped #40
- Night fades the day plate back to the procedural dome (stars stay); missing file stays procedural (honest)
- **/** toggles Goegap plate on/off — does **not** steal **M**
- Hideout stays authored interior / unfogged — ToD does not leak inside
- Glasses may show `06:21  DAWN  EXP 1.44  HDRI` (or `PROC` when plate off / missing) as labels only — never a second ammo HUD
- Detail: `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/sky.rs` / `engine/src/hdri.rs`

## Digital / diegetic spatial audio (shipped Hypha + Augury #27)

Evan lock: binaural day-one so the world feels **digital/diegetic** — spatial is a render path on the #21 FX bus, not a second mixer:
- World-posed FX (muzzle / Locus slash / drops) with CE HRTF-ish pan; Voice centered; Music ambient bed
- Hideout (tight) vs extract (industrial yard) reverb zone stub
- Complements Augury glasses + Range Tech diegetic gun chrome — ears place the world the way labels place interacts
- Seat split of later file slots is **cooking** — do **not** claim SFX file slots shipped. See Authored SFX vs spatial split below.
- Detail: `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `engine/src/audio.rs`

## Authored SFX vs spatial split (Evan dump 2026-09-07 — cooking, not shipped)

**Not done.** Do **not** claim SFX file slots as shipped. #21 FX bus is **live** (procedural tones today). Authored audio is meant to **come over** that bus (rustles / rattles / slides).

| Seat | Owns |
|------|------|
| **Range Tech** | Weapon / move SFX **file slots** off CE / FoW packs **into those buses** (#21 Voice / Music / FX). Not a fourth bus. |
| **Augury (Chamber)** | Keeps spatial / reverb DNA (#27 CE FoW HRTF-ish pan + hideout/extract zone stub). Does not take the file slots. |
| **Lab-Rat** | Stamps stay **quiet on audio** — no stamp SFX lane |

See `FULCRUMRUST_LAST_PASS_LOCK.md` + `EXTRACTION_AUDIO_LOCK.md`.

## FoW title mark / brand wordmark (shipped Augury #41)

Grim lowfi title — Evan’s Fulcrum of Will header is the wordmark on the #11 shell:
- Vendored CE `@4_15_26` `public/images/Fulcrum Of will Header.png` → `assets/brand/fulcrum-of-will-header.png` (2048-wide, aspect kept). Atelier `brand/` was README-only — **do not invent a replacement mark**; runtime does not clone atelier or CE
- Aspect-fit seat (`engine/src/brand.rs`): `MARK_MAX_W` **1.70** · `MARK_MAX_H` **0.40** · `MARK_CENTER_Y` **0.58** (clip-space y-up); `clip_aspect = image_aspect / window_aspect` so the header is not stretched junk; bottom of mark clears Deploy (`mark_clears_deploy`)
- Bitmap `FULCRUM OF WILL` text removed — PNG is the wordmark. **Logo seat #41 still stands.** Gold tick / gold hairline gone (#45) — analysis-knowledge-core chrome is thin white mono (not heat/ammo gold), tight white frames on Deploy/Host/Join/Continue/Options/Quit, white hairline, darker ground
- Still no second ammo HUD
- Detail: `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/brand.rs`

## Menus / settings (Augury shell shipped #45; Hypha guts shipped #46)

#45 shipped title + HOLD analysis-core polish + Options list shell. #46 filled the disabled `HYPHA` stub tabs — Graphics/Gameplay/Controls guts + window mode + post stubs + persist. **Do not claim GPU post passes (SSAO/FXAA/CA/grain/DoF shaders) shipped** — toggles persist as stubs and no-op safely. Logo/title mark #41 still stands.

| Seat | Owns |
|------|------|
| **Augury** | Title + HOLD chrome (#45): thin white mono, tight white frames, white hairline, darker ground. HOLD = **SYSTEM PAUSED** (CE pause language); Resume / Options / Quit to menu. Options list **Graphics / Audio / Gameplay / Controls**. Layout/colors/buttons remain Augury. Logo/title mark already #41 |
| **Hypha** | Tab guts **shipped #46**: borderless-fullscreen **default**; windowed 1280×720; exclusive (borderless fallback). Graphics / Gameplay / Controls guts; post AO/AA/CA(+strength)/grain/DoF persist as live-read stubs until GPU passes — **not** packed into ToD / Goegap / HDRI uniforms. Steal from CE/Mycelium. **No atelier push** |
| **Range Tech** | Audio mixer stays #21 Voice/Music/FX (untouched by #46) |
| **Input** | FoW OG input manager also in scope (steal into fulcrumRust) — still cooking |

Esc Hypha pane / Audio → Options → title/pause. Still no second ammo HUD. See `FULCRUMRUST_LAST_PASS_LOCK.md`.

## Embodied feel (Range Tech — cooking, not shipped)

Evan 2026-09-07. **Not done.** Range Tech owns the feel pass. Do **not** claim it shipped.

Aim-offset **looks/feels correct** for guns, attachments, controller — **transpose** that work into fulcrumRust (**outside materials and range geometry**). Concrete Echo / FoW OG has a great controller too + **action audio cues**. Find a **sweet medium** between aim-offset and CE/FoW for embodied feel.

Weapon / move SFX file slots (rustles / rattles / slides) are the authored-audio split above — **not shipped**. #12 bind lock (Q/E lean, Ctrl+mouse height, wheel speed) stays. See `FULCRUMRUST_LAST_PASS_LOCK.md`.

## Influence north-stars (shortcut aesthetics)

| Influence | Steal |
|-----------|-------|
| **Forever Winter** | Scale-sized maps; smaller level instances connected by tunnels on a world map (connectors, not deep guts) |
| **Beta Decay** | Lowfi graphic energy (FoW-adjacent) |
| **Devil Daggers** / similar Steam indies | Tight lethal feel, readable silhouettes |
| **NaissanceE** | World structure + scale |
| **Akira** | Layered tech / city-decay energy |
| **Zdzisław Beksiński** | Mushroom / bio-growth nightmare — loud-scar stamp lane |
| **Nivanh Chanthara** / **Mortal Shell** artists / **Maciej Kuciara** | Gritty, detailed, believable-yet-unbelievable; layered technique |
| **Sulfur** | Diegetic mag dots + readable floor hotspots (language only) |

Also: FoW lowfi skin; Lab-Rat stamps as bake north-stars (not live stew).

Source of truth: https://github.com/initialvisuals/fulcrumRust/blob/main/docs/STEAL_MAP.md
