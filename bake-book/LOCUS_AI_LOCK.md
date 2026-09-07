# Augury — Locus Standard + distance activation (fulcrumRust #18)

Durable dial / peek lock from The Augury yard slice. Steal state *shape* from CE/FoW — not a CE editor, not a full AI port.

## Ownership
- **The Augury** owns Locus brains, distance activation, yard spawn pad, hurtbox hitscan hook into Range Tech tracers
- **Range Tech** owns MP9-Z tracers / HoB / recoil (Augury only adds living hurtbox stop + damage)
- **Hypha** owns Transvoxel / window / load gate + shared `activation` gate for far chunk guts (`activation.rs`; same `ACTIVATE_M` / `SLEEP_M`)
- **Lab-Rat** owns stamps / growth plots (Locus pad sits **right of the creeper**, does not own stamp materials)

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

Fightable day-one pack: **one Locus Standard** on the extract yard. **Inked** is palette/silhouette stub only — **not spawned**. TODO: Inked / Sonderer / Monk / Oculus / crawler. Later: stamp spawn filters (prefer rock/concrete; avoid organic).

## Combat dials (day-one Standard)
| Dial | Value |
|------|-------|
| `MAX_HP` | **80** |
| `SMG_PELLET` | **14** (Range Tech hitscan via `apply_shot`) |
| `SLASH_DAMAGE` | **10** (Engage close; armor then HP on player side) |
| Chase / Engage speed | **2.65** / **1.15** |
| Yard pad `YARD_STANDARD` | **(5.15, 0, 7.85)** — player-right of creeper / mushroom |

## Glasses (labels only)
Near body: `LOCUS  STANDARD  IDLE|ALERT|CHASE|ENGAGE|RECOVER|DOWN` — Augury smart-glasses, never a second ammo HUD (`AESTHETIC_DIEGETIC_LOCK`).

## Morning peek
Title → Deploy → hideout door (**W** / **F**) → extract yard → look slightly **right** of mushroom / past creeper → ash/bone biped with orange eye slits → LMB MP9-Z wounds; far map guts stay cold.

Source: fulcrumRust `engine/src/locus.rs` + PR #18; shared gate `engine/src/activation.rs` + Hypha PR #23. Steal map Augury rows: Locus AI + distance activation → **partial** (numbers locked; Hypha far-guts reuse shipped).