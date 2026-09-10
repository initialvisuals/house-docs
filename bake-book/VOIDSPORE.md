# Locus Voidspore yard leftover — house pointer

Lab-Rat. **Landed** fulcrumRust [#171](https://github.com/initialvisuals/fulcrumRust/pull/171) (2026-09-10, merge `ce4162a5`). Cheap looping **growth leftover** on the extract yard — dark / inked webbing with purple tips. Start of a Locus Mycelium Voidspore entity. **Not** a fourth named plot. **Not** pycelium GPU mesocosm.

**Canonical dial sheet:** fulcrumRust [`docs/VOIDSPORE_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/VOIDSPORE_DIAL_SHEET.md) (merge tip `ce4162a5`). Steal from that sheet — do **not** invent numbers here. House seat: [`STAMP_FEEL_LOCK.md`](STAMP_FEEL_LOCK.md) leftover consumers + [`FULCRUMRUST_LAST_PASS_LOCK.md`](FULCRUMRUST_LAST_PASS_LOCK.md).

CREDITS + STEAL_MAP + VOIDSPORE_DIAL_SHEET already claimed in-PR — house shelf only.

## Landed lock (stolen, not invented)

Sit-on-surface colony **left of extract spawn**. Peek: Title → Deploy → extract, look **left**. Dark inked webbing on the dirt; tips read purple; fruiting nodes stack like rock lobes. Home **COLL**: purple pad wire + projected points (steal probe_mark). Not a glasses card.

| Dial | Value | Notes |
|------|-------|-------|
| Matrix | **10 × 4 × 10** | Sit-on-surface. Occupancy is a fixed `u8` grid. |
| Max live | **48** cells | Fixed `[Cell; 48]`. No per-frame alloc. |
| Max tips | **8** | Agents walk / curl / die. Branch is rare. |
| Max solids | **152** | 3-lobe fruit + tip chip worst case. Growth leftover GPU **768 / 192** KiB (was 640 / 160). |
| Update Hz | **10** | Frame tick only accumulates. |
| Cell min / max | **0.016 / 0.034** m half-span | Low-poly leftover boxes. Size rides 0..1 growth then wilt. |
| Pitch | **0.085** m | Cell spacing. Footprint ~0.85 × 0.34 m. |
| Life | **36** steps | Body can wilt early (hash). Tips last until the agent dies. |
| Density gate | **0.12** | `density_stamp_2d` — webbing silhouette, not a filled cube. |
| Lobe density | **0.42** | Rock-lobe 3-box stack (shade / face / chip) on field peaks. |
| Tip purple | `[0.68, 0.20, 0.86]` | Steal HOLO. Body ink `[0.10, 0.04, 0.12]` / void `[0.16, 0.05, 0.14]`. |
| Brightness | **0.16 → 0.78** × grit rough | Quiet `grit::rough` modulates emit. Height `grit::height_delta` lifts Y. |
| Cycle | **11.0** s or starve (`<3` live / `0` tips) | Soft restart. Generation increments. Seed xor gen. |
| Warm | **18** steps on `new` | Deploy already reads a colony (HOLO mid-grow DNA). |
| Origin XZ | **−3.55, 2.35** | Left-forward of extract spawn `(0, −1.4)`. Off plots / Inked / lean / pedon. |
| Floor | `terrain.height_at` read | Sit-on-surface. Not a remesh. |
| Env | `FULCRUM_VOIDSPORE=0` / `off` | Kill switch. Default on. |
| Smoke | `voidspore=gen=N cells=M tips=T` | Extract `stream_rev` / terrain tris / CHANNELS layers must not move. |

Draw path is existing extract `upload_growth` leftover slot. Hideout HOLO_MYCELIUM keeps the pedon slot. Quiet grit thumbs stay.

## Parked (do not claim)

- Living growth-enemy / sprint-grow / AI / combat
- CHANNELS compile of the leftover (Hypha remesh)
- Hideout plant (HOLO owns the pedon slot)
- Glasses elbow (Augury)
- Net / PeerBody
- Options texture / mipmap (Lab-Rat vendor COL / `lod_mips` / `FULCRUM_UV` — still cooking)
- A fourth named plot

See `PEEK_FINDINGS.md` Closed by #171 + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `docs/VOIDSPORE_DIAL_SHEET.md`.
