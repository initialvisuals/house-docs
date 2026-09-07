# Augury — Locus Standard + Inked + distance activation (fulcrumRust #18 + #26)

Durable dial / peek lock from The Augury yard slice. Steal state *shape* from CE/FoW — not a CE editor, not a full AI port.

## Ownership
- **The Augury** owns Locus brains, distance activation, yard spawn pads, hurtbox hitscan hook into Range Tech tracers
- **Range Tech** owns kit tracers / HoB / recoil (Augury only adds living hurtbox stop + damage)
- **Hypha** owns Transvoxel / window / load gate + shared `activation` gate for far chunk guts (`activation.rs`; same `ACTIVATE_M` / `SLEEP_M`)
- **Lab-Rat** owns stamps / growth plots (Standard pad **right of creeper**; Inked pad **left of 2D webbing**); Lab-Rat #30 owns the **loud growth stamp** under the Inked pad; ink disc remains Augury chrome

## Distance activation (far guts stay cold)
| Dial | Value | Note |
|------|-------|------|
| `ACTIVATE_M` | **24** | Wake when player enters; cold bodies skip path/hunt; **Hypha #23** also gates far stamp guts / growth+Locus upload |
| `SLEEP_M` | **32** | Hysteresis — warm body cools past this; shared with Hypha chunk activation |
| `HEAR_M` | **18** | Shot crack can wake Idle without LOS |
| `ALERT_M` | **14** | Idle → Alert when close |
| `ENGAGE_M` | **2.15** | Chase ↔ Engage melee band |
| `LOSE_M` | **20** | Chase → Recover when player slips away |

## Brain (CE shape, thin)
`Idle → Alert → Chase / Engage → Recover` · `Dead` = ragdoll flop stub (`DOWN` on glasses).

Fightable day-one pack: **Locus Standard + Locus Inked** on the extract yard (same brain + shared Hypha wake meters). TODO family: Sonderer / Monk / Oculus / crawler. Later: stamp spawn filters (prefer rock/concrete; avoid organic).

## Combat dials (day-one Standard + Inked)
| Dial | Value |
|------|-------|
| `MAX_HP` | **80** |
| `SMG_PELLET` | **14** (Range Tech hitscan via `apply_shot`; kits follow seated fire sheet) |
| `SLASH_DAMAGE` | **10** (Engage close; armor then HP on player side) |
| Chase / Engage speed | **2.65** / **1.15** |
| Yard pad `YARD_STANDARD` | **(5.15, 0, 7.85)** — player-right of creeper / mushroom; ash/bone + rust-orange eyes |
| Yard pad `YARD_INKED` | **(−5.10, 0, 8.20)** — player-left of 2D webbing; darker/hooded/thinner + cyan eyes + cheap ink-zone disc (Augury chrome); Lab-Rat loud stamp under pad |

## Glasses (labels only)
Near body: `LOCUS  STANDARD  IDLE|ALERT|…` or `LOCUS  INKED  IDLE|ALERT|…`. Off the Locus prompt on the scar: `INK HOTSPOT` (Lab-Rat). Augury still owns Locus labels — never a second ammo HUD (`AESTHETIC_DIEGETIC_LOCK`).

## Morning peek
Title → Deploy → hideout door (**W** / **F**) → extract yard:
- **Standard:** look slightly **right** of mushroom / past creeper → ash/bone biped, rust-orange eyes
- **Inked:** look slightly **left** of 2D webbing → dark hood, cyan eyes, standing on the loud ink / void-spore hotspot (ink disc still Augury chrome)
LMB (or seated kit) wounds either; far map guts stay cold — only these two yard bodies warm.

Source: fulcrumRust `engine/src/locus.rs` + PR #18 + PR #26; Lab-Rat stamp under Inked pad = PR #30 (`growth::INKED_HOTSPOT`); shared gate `engine/src/activation.rs` + Hypha PR #23. Steal map Augury Locus row → **partial** (Standard + Inked shipped; family TODO remains).
