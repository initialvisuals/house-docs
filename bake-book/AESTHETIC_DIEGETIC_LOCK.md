# Aesthetics / diegetic lock (fulcrumRust)

Parked from Evan (2026-09-07).

## Diegetic labels — **Augury smart-glasses**

Analysis-knowledge-core in-world labels (interacts, extract points, section samplers):
- Thin white mono, fully embodied in world space
- **L-elbow / leader** to the world interact pin (door, loot, hatch, shaft, weapon, extract plots, Locus) — **landed #85** (`engine/src/labels.rs` `SmartLabel` / `CardPlan`)
- Tip mark + quiet angular junk; curl/Locus edge tints. EXTRACT stays white mono
- Not a centered HUD plate (old `-0.34, -0.268` retired for interact cards)
- Subtle glitches / digital artifacts around the overlays
- Spatially dynamic (not flat HUD chrome)

**Ammo is not glasses.** Glasses stay labels only — never a second ammo HUD.
Hold-**O** paints EXTRACT intent on the nearest in-front hatch/shaft — elbow card, **no popup** (Range #78 wired `Session::extract_checking`; Augury owns the glasses EXTRACT chrome — **landed #85**). Release clears. Full hatch popup (elevator / toggle / timed surface kill) still **~**.
Glasses status strip (PLACE / clock / INSPECT / …) unchanged. Hatches stay on the **yard pad** (`-24/-24`, `18/-28`, `-28/16` + shaft `18/-12`), not GRID_ORIGIN (19×19 rim).
Shipped label examples: stamp materials · `LOCUS  STANDARD|INKED  <brain>` · `INK HOTSPOT` · ToD/exposure · `HDRI` / `PROC` (Goegap plate #40) · `INSPECT` (hold-` #28) · `RELOAD` / `SWAP` (mag swap #32) · `BANDAGE` / `EMPTY` (bandage use #31) · `Z{n}  SIM` (HoB zero #33 / SIM-only #76) · `HEAT TUNE` (hold-J heat-tune #35) · `HOST` / `JOIN` / `PEER` (listen-server #34) · `DOWNED` · `DEAD` · `STIM` / `NO STIM` · `RALLY` · `NEED STAB` · `STAB STUB  NO NET` (down/death stub #36; #37 bind `I STIM`) · `DRY` / `YARD` / `OUT` (reverb volumes #56) · `EXTRACT` (hold-O #85) · `DOOR  F  DEPLOY` · lean/slide/speed/height peeks.
Goegap plate (fulcrumRust #40): glasses ToD strip may show `HDRI` / `PROC` — still labels only, never a second ammo HUD.
Bandage use (fulcrumRust #31): glasses may flash `BANDAGE` / `EMPTY` on use — still labels only, never a second ammo/health HUD. While downed unstabilized, `NEED STAB` (no consume) — still not a second health HUD (#36).
Live HoB zero / launch (fulcrumRust #33 / **#76** SIM-only): glasses status strip `Z{n}  SIM` (e.g. `Z100  SIM`); toast `ZERO  {n} M` — labels only, never a numeric ammo HUD. **P** unused; `LAUNCH  ARCADE` / `LAUNCH  SIM` gone.
Heat-tune dump (fulcrumRust #35): glasses may flash `HEAT TUNE` (amber-ish overlay) while J is down — still labels only, never a second ammo HUD; must not count mag rounds.
Listen-server (fulcrumRust #34): glasses may show `HOST  ip:port`, then `JOIN` / `PEER` after HELLO/WELCOME — still labels only, never a second ammo HUD.
Down / death stub (fulcrumRust #36 + #37 bind): glasses may flash `DOWNED` · `DEAD` · `STIM` / `NO STIM` · `RALLY` · `NEED STAB` · `STAB STUB  NO NET` (and related toasts / prompts like `HOLD F  SELF-STAB STUB` / `[F] PICK UP STIM` / `STABILIZED  T HEAL / I STIM / SLASH RALLY` / `DEAD  BAG STUB` / `CORPSE RECLAIM STUB`) — still labels only, never a second health HUD. #37 names I stim on the glasses prompt (was `Y STIM`); Y is host only.
Elbow smart-labels (fulcrumRust #85): interact cards sit off-center with an L-leader to the world pin — still labels only, never a second ammo HUD. Hold-**O** `EXTRACT` is that same chrome (no popup). Cite `FULCRUMRUST_LAST_PASS_LOCK.md`.

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
- Live HoB zero / launch (fulcrumRust #33 / **#76** SIM-only): glasses may show `Z{n}  SIM` (e.g. `Z100  SIM`) and toast `ZERO  {n} M` — still labels only, never a numeric ammo HUD. **P** unused; `LAUNCH  ARCADE` / `LAUNCH  SIM` gone
- Kit chrome taste (Initial Visuals Group Chat 2026-09-07): **gold paired with black** — **tech trim**, not gold-plate. Distinct from Locus **obsidian + gold crack veins** — **do not put Locus veins on gun kits**. Stamp side: `STAMP_FEEL_LOCK.md`. **#64** stub PBR applies that DNA on MP9-Z / SR-25 / M24 boxes (albedo mix + roughness/mask; TRIMSHEET_MICRO + MetalPanel/Corroded crops + scratch/print masks) — not gold-plate, not Locus veins. Store `dBXpg` still **open**
- **Crossover shoulder / left-corner peek** (travel landed #59; chest-cross tilt **landed #84**): **H** springs the **viewmodel** across the chest from authored hip +X ~**0.10** to a partial left (~**−0.041**, cap `shoulder_x_min` **−0.055**). ADS keeps **0.32**. Extra left probe `shoulder_viewmodel` **0.12**. Tilt pitch/yaw/roll **0.08 / 0.32 / 0.39** on existing ADS cant DNA. Not a body slide, not a mesh mirror / `scale.x = −1`, not infinite travel. Mag chrome travels with the kit. Existing H bind, not a new key. Quiet influence — no franchise name-drop. See `FULCRUMRUST_LAST_PASS_LOCK.md`

## Readable floor hotspots

Floor/wall aftermath (spills, barrel-choir embers, Lab-Rat stamps) stays readable without softlocking the path. Loud Inked void-spore scar under `YARD_INKED` is a floor leftover (curl remnants stay). Range Tech leftover feel-lab FX (fulcrumRust #47): punch vs scuff + stuck-slug plug stay floor/wall aftermath; hide-not-despawn via `casing_draw_m` **55** (brass + spent slugs). Mag chrome stays on the kit — no second ammo HUD. Locus hotspot FX language later — see `SULFUR_INFLUENCE.md`.

## Grimdark Locus terraforming (shipped Lab-Rat #20)

Aesthetic lock for Lab-Rat stamps + Range Tech FX contrast (wet-lab → main via fulcrumRust #20):
- **Hellish void spores** — Locus growth language, not cute mushrooms; yard reads webbing / fruiting body / spore tips + **loud Inked floor scar** (left of 2D webbing)
- **Locus technology / alien set dressing:** black **obsidian + gold crack veins** — loud-scar stamp material on Inked/Monk pads (Lab-Rat). Pairs with void-spore grit. Distinct from Range Tech kit chrome (gold+black tech trim) — veins stay off gun kits (Initial Visuals Group Chat 2026-09-07)
- Influence is **quiet** (BT black / chiral gold vibe) — **do not name-drop** franchises in shelf, READMEs, or public copy; no pastiche chase.
- **Cracks / edge-wear** driven by **2D mushroom density stamps** (`density_stamp_2d` → `WearStamp` on concrete)
- **Brutalist concrete** with procedural wear as the hard backdrop; glasses still labels only (`CONCRETE  STAMP`)
- **Grimdark material grade** — crushed luma on dirt / sand / rock / concrete / organic; organic bleed = void-spore takeover
- Range Tech: grimdark tracers / heat / muzzle on that concrete contrast; performant first. Hide-not-despawn XZ (`casing_draw_m` **55**, fulcrumRust #47) for brass + spent slugs; punch vs scuff impact marks — never a second ammo HUD
- Detail shelf: `STAMP_FEEL_LOCK.md` + fulcrumRust `docs/STAMPS.md`

## Grimdark extract host (shipped Hypha #16)

House `AESTHETIC_DIEGETIC_LOCK` on the Transvoxel host — terrain reads **grim/dense**, not a bright sandbox:
- **Ashen wash / slate sides / brutalist** vertex paint from Lab-Rat `VoxelMaterial::tint` (no second material story)
- Proc **edge-wear / hairline cracks** + denser mid-frequency rubble; void-spore stamp peek tints
- Extract clear is **dimmer** + dual colder lights + **cheap distance haze** (`fs_world`); hideout stays small / unfogged. Graphics dump defaults **#86**: extract fog **375 / 520** (hideout `haze_max` **0**) · cam **0.05 / 2000**
- Performant first — bake-once mesh, no live carve day-one
- **Texture density (2026-09-07):** yard reads **quiet grit + loud scars**. Lab-Rat **#58 landed** first vendored 256² bake-downs under loud scars (`sample_channels` quiet height + `grit::rough` wear). Greyscales bake down before density (8-bit / half-res / BC4-style) — not raw atelier **4k 48-bit PNG**. Hypha LOD-tied mips **landed #60** (near 256² / mid 64² / far 16² on Transvoxel distance rings so far grit does not shout). Atelier plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET) — Lab-Rat grit / slope / PBR cooking, **not** shipped. Range Tech kit metal/grit PBR stub **landed #64** (boxes only; not Lab-Rat terrain plugs)
- Detail: `TERRAIN_NORTHSTAR.md` + `STAMP_FEEL_LOCK.md` + fulcrumRust `docs/TERRAIN.md`

## Extract day/night sky (shipped Range Tech #24 + #40)

Feel-lab clock drives extract atmosphere — still grim/dense, not a bright sandbox:
- **One ToD sample** lights ambient / key / fill / fog + procedural dome together (**no XOR sky**). #40 Goegap plate rides the same sample.
- **`EXTRACT_SKY_LUMA` 0.20** crushes noon so day stays ashen; default clock **06:21**; Goegap plate shipped #40
- Night fades the day plate back to the procedural dome (stars stay); missing file stays procedural (honest)
- **/** toggles Goegap plate on/off — does **not** steal **M**. **#86:** `skyHdri` already default on; **/** still toggles
- Hideout stays authored interior / unfogged — ToD does not leak inside
- Glasses may show `06:21  DAWN  EXP 1.44  HDRI` (or `PROC` when plate off / missing) as labels only — never a second ammo HUD
- Graphics dump defaults **#86** on this same extract sky (not a second sky): fog **375 / 520** · light*Mul **0.11 / 0.41 / 0.61 / 2.11 / 1.65 / 1.06** · exp **1.44** · clouds **0.63** · sunPunch **0.51** · cam **0.05 / 2000**. Exposure keyboard still unbound after **#78**; **,** / **.** clouds still work
- Detail: `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/sky.rs` / `engine/src/hdri.rs`

## Digital / diegetic spatial audio (shipped Hypha + Augury #27 + #56)

Evan lock: binaural day-one so the world feels **digital/diegetic** — spatial is a render path on the #21 FX bus, not a second mixer:
- World-posed FX (muzzle / Locus slash / drops) with CE HRTF-ish pan; Voice centered; Music ambient bed (playlist **landed #64**)
- Authored CE reverb volumes (#56): glasses `DRY` / `YARD` / `OUT` — hideout interior / yard pad / open extract (wetter / longer tail). **FX wet send only.** Two-zone stub retired
- Complements Augury glasses + Range Tech diegetic gun chrome — ears place the world the way labels place interacts
- File-slot **wiring** shipped #54; day-one handmade vendor **landed #62** (small atelier set in `assets/sfx/`; missing → procedural). Remix first ±6% fire/foot/reload jitter **landed #64**; full remix minting still **open**. Shot propagation still later. Augury owns spatial + volumes + FX wet send; Range Tech owns mixer + file slots on the same bus. See Authored SFX vs spatial split below.
- Detail: `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `engine/src/audio.rs`

## Authored SFX vs spatial split (day-one FILE_SLOTS vendor landed #62)

File-slot **wiring** shipped #54. Day-one handmade atelier vendor **landed #62** — small set into FILE_SLOTS, not a full CE / aim-offset pack dump. #21 FX bus is **live**. Authored audio **comes over** that bus (rustles / rattles / slides). Mixer / Options Audio FX / Augury spatial+#56 reverb stay untouched. Controller feel-medium dials shipped #57 — that is not this row.

| Seat | Owns |
|------|------|
| **Range Tech** | Weapon / move SFX **file slots** off CE / FoW packs **into those buses** (#21 Voice / Music / FX). Not a fourth bus. Wiring shipped #54. Day-one handmade vendor landed #62. **SFX remix DNA** — pitch/speed/effects to mint new one-shots; indie underground; don’t overuse the same stem. First ±6% fire/foot/reload jitter **landed #64**; full remix minting still **open**. Music playlist beds **landed #64**. |
| **Augury (Chamber)** | Keeps spatial / reverb DNA (#27 CE FoW HRTF-ish pan + #56 DRY/YARD/OUT AABB volumes, FX wet send only). Does not take the file slots. |
| **Lab-Rat** | Stamps stay **quiet on audio** — no stamp SFX lane |

See `FULCRUMRUST_LAST_PASS_LOCK.md` + `EXTRACTION_AUDIO_LOCK.md`.

## FoW title mark / brand wordmark (shipped Augury #41)

Grim lowfi title — Evan’s Fulcrum of Will header is the wordmark on the #11 shell:
- Vendored CE `@4_15_26` `public/images/Fulcrum Of will Header.png` → `assets/brand/fulcrum-of-will-header.png` (2048-wide, aspect kept). Atelier `brand/` was README-only — **do not invent a replacement mark**; runtime does not clone atelier or CE
- Aspect-fit seat (`engine/src/brand.rs`): `MARK_MAX_W` **1.70** · `MARK_MAX_H` **0.40** · `MARK_CENTER_Y` **0.58** (clip-space y-up); `clip_aspect = image_aspect / window_aspect` so the header is not stretched junk; bottom of mark clears Deploy (`mark_clears_deploy`)
- Bitmap `FULCRUM OF WILL` text removed — PNG is the wordmark. **Logo seat #41 still stands.** Gold tick / gold hairline gone (#45) — analysis-knowledge-core chrome is thin white mono (not heat/ammo gold), tight white frames on Deploy/Host/Join/Continue/Options/Quit, white hairline, darker ground
- Still no second ammo HUD
- Detail: `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/brand.rs`

## Menus / settings (Augury shell shipped #45; Hypha guts shipped #46; GPU post #55; Graphics dump #86)

#45 shipped title + HOLD analysis-core polish + Options list shell. #46 filled the disabled `HYPHA` stub tabs — Graphics/Gameplay/Controls guts + window mode + persist. GPU post stack live **#55** (AO/AA/CA/grain/DoF; toggles change the image). HUD / glasses still draw after post. Graphics dump defaults **#86** (fog / cam / sky — not bloom / god-rays). Labels-only glasses lock unchanged. Logo/title mark #41 still stands.

| Seat | Owns |
|------|------|
| **Augury** | Title + HOLD chrome (#45): thin white mono, tight white frames, white hairline, darker ground. HOLD = **SYSTEM PAUSED** (CE pause language); Resume / Options / Quit to menu. Options list **Graphics / Audio / Gameplay / Controls**. Layout/colors/buttons remain Augury. Logo/title mark already #41 |
| **Hypha** | Tab guts **shipped #46**: borderless-fullscreen **default**; windowed 1280×720; exclusive (borderless fallback). Graphics / Gameplay / Controls guts + persist. GPU post **#55** — AO/AA/CA(+strength)/grain/DoF change the image; HUD/glasses still after post — **not** packed into ToD / Goegap / HDRI uniforms. Steal from CE/Mycelium. Does **not** dump atelier into Options Graphics. LOD-tied texture mips **landed #60** on Transvoxel distance rings — see `TERRAIN_NORTHSTAR.md`. Graphics dump **#86** — thin Options **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** + persist; do **not** invent bloom / god-ray / sunSize / brightness / gamma |
| **Range Tech** | Audio mixer stays #21 Voice/Music/FX (untouched by #46) |
| **Input** | FoW OG input manager also in scope (steal into fulcrumRust) — still cooking |

Esc Hypha pane / Audio → Options → title/pause. Still no second ammo HUD. See `FULCRUMRUST_LAST_PASS_LOCK.md`.

## Embodied feel (Range Tech — landed #57)

Evan lock. **Shipped** fulcrumRust #57. Range Tech owns the feel pass. Tune dials only; `AXIS_LOCK` stays; no materials / range geo.

Look inertia queue **26** · ADS look **0.86** / blend **6.4** · sprint high-ready **6.2** · slide carry **10.3 / 0.98 / 1.02** · jump land punch **0.052** rad overlay (does not write `pitch`). Medium sweet spot vs aim-offset × CE/FoW.

Day-one handmade SFX vendor **landed #62** — that is audio files, not these controller dials. #12 + #51 look/strafe/door stay. **#59** landed Q/E flip + CE hop + H crossover.

**Crossover shoulder / left-corner peek** (travel landed #59; chest-cross tilt **landed #84**): **H** springs the viewmodel across the chest from authored hip +X ~**0.10** to a partial left (~**−0.041**, cap `shoulder_x_min` **−0.055**). ADS keeps **0.32**. Tilt pitch/yaw/roll **0.08 / 0.32 / 0.39**. Not a body slide. Not a mesh mirror / `scale.x = −1`. Existing H bind, not a new key. Quiet influence — no franchise name-drop. See `FULCRUMRUST_LAST_PASS_LOCK.md`.

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
