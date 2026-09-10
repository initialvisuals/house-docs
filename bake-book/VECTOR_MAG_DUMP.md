# Vector mag dump (aim-offset / Vector feel)

Canonical artistic-auth frame for Range Tech muzzle / FX cooks. Steal into fulcrumRust from this sheet, not chat scroll.

**Source:** Evan aim-offset **Vector mag dump** (feel reference frame)  
**Parked:** 2026-09-09  
**Live fulcrumRust steal:** Range Tech **#89** (projectile feel) on existing `TracerField` — rect slab + debris + slug/wake + punch/scuff flash + fire-pulse glyphs. No new physics.  
**Sibling:** heat cards stay on [`../heat-card-dial-sheet.md`](../heat-card-dial-sheet.md) — this sheet is muzzle / FX, not heat. Warp *range* / shader gate → [`HEAT_WARP_DIAL_SHEET.md`](HEAT_WARP_DIAL_SHEET.md). Do **not** reopen orange cards. **#89** did **not** retune HeatDials. Live heat field is Range Tech **#129** CE tip **0.2.8** on Hypha `#66` (#71 blend is DNA). Visible hold-J tip warp **landed #155**.

House-docs does not vendor the PNG. The frame lives in the **InitialVisuals chat attachment** / Range cook context. Dials below are the lock.

## Locked dials

| Dial | Lock |
|------|------|
| **Muzzle flash** | Long **rect** yellow-white off the suppressor can. Not a round soft bloom |
| **Grit** | Orange sparks / grit around the flash periphery |
| **Receiver glyphs** | Sharp **emissive red** marks on the tan receiver, under the optic |
| **Local light** | Flash lights the can / front of the gun **and** the nearby floor — **reference-only** unless already on the feel sheet |
| **Optic** | Red-dot with orange triangular reticle marks — **reference only** unless already on the feel sheet |

Live spawn stays kit-tip (`kit_mesh::muzzle_tip_local`, #67). Flash long axis stays **sim barrel +Z** (`AXIS_LOCK`). Day-one kit stays MP9-Z — this is a steal look, not a Vector kit swap.

## Live dials (#89)

Range Tech **landed #89** on existing `TracerField` / AXIS_LOCK sim barrel **+Z** / #79 heightfield snap. SIM / HoB / gravity stay #76. Heat stays on the heat-card dial sheet.

| Dial | Now |
|------|-----|
| Muzzle flash | Long yellowish-white **rectangular slab** flush on the can tip (`half.z` ≫ `half.x`) + pale-yellow rim |
| Muzzle debris | 4–6 orange sparks, life 0.07–0.17 s |
| visualLength | floor **max(1.5, speed×0.035)** / cap **18** m |
| Core color | **2.85 / 2.25 / 0.95** |
| Slug head | **0.07** m (`TRACER_SLUG_LEN`) |
| Wake trail | 1–2 fading segments, tip-clamped |
| Hit flash | **0.15** s disc (grows 0.5→2.5, fade `1−√t`) |
| Punch sparks | **8–12**, 0.22–0.40 s, 35% white |
| Scuff sparks | **4–6**, 0.15–0.28 s, amber |
| Receiver glyphs | **fire pulse** red/orange on dump |

Local light / optic remain **reference-only** unless already on the feel sheet. Heat stays on `heat-card-dial-sheet.md` — Range Tech **#129** landed the CE tip **0.2.8** field; **#155** sells hold-J tip warp. Heat stays Range dials; vector mag dump stays **#89**.

## Not this shelf

Pixellation / dither walls and floor warp are **Hypha Graphics / Augury**. Do **not** claim them here. Do **not** invent bloom / godRays paths (`#86` parked those). Do **not** reopen heat orange cards (`#66` path / `#71` DNA / live `#129` CE tip / `#155` warp). **#89** did not ship a kit mesh rewrite, Aim-offset Home debugger, Beabim sync, or profile onboard.

## Ownership

| Seat | Owns |
|------|------|
| **Range Tech** | Muzzle flash / grit / local light / receiver glyph FX steal into fulcrumRust — **live #89** (rect slab + debris + slug/wake + punch/scuff + fire-pulse). Local light still reference-only |
| **Hypha / Augury** | Pixellation + floor warp — separately. Not this cook |
| **Lab-Rat** | Stamps — not this sheet |

## Steal notes

- Overnight muzzle / FX cooks steal from **this sheet**, not chat. Live #89 already took the rect slab / debris / slug / wake / punch-scuff / fire-pulse glyphs
- Local light is flash-as-light on the can / gun front / nearby floor — not a second heat system, not bloom — still **reference-only** unless already on the feel sheet
- Red receiver glyphs are diegetic kit chrome (sharp emissive), not glasses / not a second ammo HUD. Live #89 pulses them on fire
- Heat stay on `heat-card-dial-sheet.md` + Hypha `#66` colorless post. Live HeatDials field is **#129** CE tip 0.2.8. Visible hold-J warp **#155**. No orange card redraw
- Intact siblings: `#12` flash/spark/mark · `#19`/`#47` draw-distance · `#51` barrel +Z · `#67` kit-tip spawn · `#71` heat blend DNA · **`#129` CE tip field** · **`#155` hold-J warp** · `#76` SIM · `#79` heightfield snap · **`#89` live steal**

See `FULCRUMRUST_LAST_PASS_LOCK.md` Visible shot feedback + Projectile feel (#89) · `PEEK_FINDINGS.md` Closed by #89.
