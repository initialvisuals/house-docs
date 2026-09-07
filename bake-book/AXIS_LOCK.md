# AXIS_LOCK — three spaces (do not unify)

Parked from Range Tech / fulcrumRust #51 (2026-09-07). Source: fulcrumRust `docs/AXIS.md`. Steal the three spaces as written — do not invent a fourth, do not restyle into one frame.

Hypha / MyceliumEngine `FPS_RETROFIT` §4 + aim-offset.

Sideways impact / brass is almost always FX applying **camera/viewmodel −Z** to **sim barrel +Z** geo (or the reverse). Lab-Rat stamp **+Y** is a different content space — leave it.

## The three forwards

| Space | Forward | Used for | Local → world |
|-------|---------|----------|----------------|
| **Camera / viewmodel local** | **−Z** | Hold offsets, FP kit, `ejectionPort` | `origin + r*x + u*y + look*(-z)` |
| **CE FBX authoring** | **+X** | Stolen CE numbers | `rotY ≈ π/2` applied as **`rotY − π/2`** after FP is already −Z aligned. Do not rename rot axes. |
| **Sim barrel / mounts** | **+Z** | Projectiles, TP grip, **FX** (flash, tracers, impact, stuck-slug, brass, ricochet) | No negate. `axis::sim_barrel_basis(plus_z)` |

Pawn **world look** at yaw 0 is **+Z** (hideout door / extract yard). That is the same *vector* as arcade sim barrel when the bore matches look — it is **not** camera-local −Z. Camera local +Z is *back*.

Code: fulcrumRust `engine/src/axis.rs`.

## Feel-lab vs pawn look

Feel-lab Three.js looks **−Z** at yaw 0 and **subtracts** mouse X. We keep authored **+Z** spawn. Evan dizzy-play: **subtract** mouse X (invert horizontal) and **invert A/D** vs the #12 camera-right lock. Q/E lean signs stay +lean = left (#25). Do not invert lean — or unify the three forwards — to "fix" FX.

## FX contract (#47)

| Piece | Toss / sit | Long / thin axis |
|-------|------------|------------------|
| Muzzle flash | — | Sim barrel +Z (`shot.dir`) |
| Brass | Camera-right (feel-lab) | **Sim barrel +Z**, not toss, not camera −Z |
| Impact hole / chips / squat plug | Flush on surface | Thin along **world normal** via `sim_barrel_basis` (RH). Feel-lab Plane +Z → normal / squat cylinder +Y → normal |
| Spent slug | Reflect vel | Long along outgoing vel (sim +Z of the slug) |

#47 rebuilt FX with `forward × Y` (left-handed) and mixed camera local into barrel geo. Oriented boxes wound backwards; plugs/chips/brass read sideways.

## Lab-Rat (not this lock)

Stamp / mesh ingest is authored **+Y up**, CCW from outside (`CHANNELS.md`). Do not rotate stamps to fix sideways plugs.

## Regression watch

- #12 look/move/gun lock + tracers
- #25 Q/E lean clamp (sign stays +lean = left)
- Do not unify the three forwards
