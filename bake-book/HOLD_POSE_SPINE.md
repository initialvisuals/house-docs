# Hold pose spine (grip-invariant PreferredHand A)

House contract for PreferredHand / AIM TUNE pose architecture. **Partial shipped #168** — Range Tech one right bank + sagittal HAND L/R mirror + HAND chrome + AIM TUNE HAND·kit·pose + ADS crosshair hide. Steal from this sheet + fulcrumRust [`docs/PREFERRED_HAND_A_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/PREFERRED_HAND_A_DIAL_SHEET.md), not chat. Do **not** invent dial numbers. No code. Clerk owns this sheet. House pointer: [`PREFERRED_HAND_A.md`](PREFERRED_HAND_A.md).

## Spine

Poses sit on the **hold/grip bone**. Guns hang from attach sockets relative to that hold. One pose bank + HAND L/R mirror (PreferredHand **A**).

## Locked

| Lock | Detail |
|------|--------|
| **Hold is the pose home** | Cant / hip / low-hip / etc. reference the **hold/grip bone**, not each gun mesh |
| **Guns hang** | Kits attach from sockets relative to that hold |
| **Optic class** | Iron sights classified as an **optic class** — one class offset; ADS transitions to the active glass of the selected weapon |
| **PreferredHand A** | **Landed #168.** One right bank + sagittal **−X / −yaw / −roll** for left — not full L+R authored pairs per gun×optic |
| **HAND chrome** | **Landed #168.** **`HAND R` / `HAND L`** from **live hold X** (gun right of camera middle = **HAND R**). Midline counts R. **Not** inverted `Shoulder` enum. Axis invert? **No** |
| **L/R shoulder** | HAND flip + lean hinge (Hypha tip). Not a second per-gun bank. Leftover H dest ~**−0.041** is **not** the live left pose |
| **Grip invariant** | **Hold/grip socket** is the spatial invariant across kits. Muzzle / suppressor / optic / grips are **child sockets** — attachment swaps move barrel tip, not the hold bank |
| **Ballistics loft** | Uses **muzzle child**, not hold bone |
| **AIM TUNE** | **Landed #168.** Panel shows **HAND · kit · pose**. Left numbers are the mirror. Live-save schema **landed #167** (sibling persist — not this spine) |
| **ADS crosshair** | **Landed #168.** 2D plus hides when `ads_factor` **> 0.5**. Hip + U-cycle canted keep it |
| **L/R overrides** | Explicit L/R overrides only where asymmetric (cant/inspect) later if A fails — **not week wrap** |

Do **not** author a second pose bank per gun. Do **not** move the hold bank when a can / optic / grip swaps. Do **not** loft ballistics from the hold bone. **No** `scale.x = −1`.

## Landed #168 — HAND chrome + sagittal mirror

Steal from fulcrumRust [`docs/PREFERRED_HAND_A_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/PREFERRED_HAND_A_DIAL_SHEET.md) (merge `1849ce6b`). Do **not** invent numbers.

| Component | Right (authored) | Left (mirror) |
|-----------|------------------|---------------|
| pos.x | +X (hip **+0.2403**) | −X |
| pos.y / pos.z | stay | stay |
| rot.x (pitch) | stay | stay |
| rot.y (yaw) | + | − |
| rot.z (roll) | + (cant **0.785**) | − (cant **−0.785**) |

**H** is the live HAND flip. PreferredHand onboard (#116) seats the home (`shoulder_t` 0 or 1). Leftover `shoulder_cross_*` / `shoulder_x_min` stay DNA for End PX leftover-wall arith (`−cross_x + x_min` ≈ **+0.226**) — **not** applied to the live left hold. End PX box stays **±0.50**. WEAPON Fine/Coarse **+X** while HAND L writes authored −X so the gun still walks toward camera-right on screen. ATTACH stays socket-local.

Play U stays two poses (chosen hip ↔ canted). Do **not** add READY HIP persist rows on this spine.

## Already shipped (siblings — do not restamp)

These stay facts. This sheet does **not** claim they already implemented grip-invariant A.

- PreferredHand enum + NEW PROFILE onboard **landed #116** (Hypha). Right default · `project.json` permanent vs live · death clears live · extract→stash stub. `shoulder_t` seats Range H. **#168** consumes the enum for home seat + live HAND chrome. **No** `scale.x = −1`
- AIM TUNE End sheet **#97** / live-save **#103** / per-kit pull **#167** / PX **#138** / **#159**. Poses **#94 / #98 / #99 / #100** · hold springs **#109**. Canted optic ATTACH **#150**
- Hypha 3P lean hinge **#145**. Beabim held 3P kit clone **#153**. House lock **1P ≠ 3P** held

#116 stays the onboard enum. #168 is the pose-bank mirror + chrome.

## Seat map

| Seat | Owns |
|------|------|
| **Range Tech** | AIM TUNE / PreferredHand A cook — **landed #168** (pose bank on hold/grip · optic class · HAND L/R mirror A · HAND chrome · ADS crosshair hide) |
| **Hypha** | Lean hinge (tip). PreferredHand enum / profile **#116** already landed |
| **Beabim** | 3P attach honesty — remote kit hangs from the same hold invariant (1P ≠ 3P held) |
| **Clerk** | This sheet |

## Explicitly parked

- **Full per-gun L+R banks.** A is the path. Do not author gun×optic L+R pairs this wrap
- **Glasses N / numpad.** Not this sheet
- **Ballistics #161 rebase.** Separate. Loft still uses **muzzle child**, not hold bone — do not fold that rebase into this cook
- **fulcrumRust #167** AIM TUNE live-save — **landed** (sibling persist cook — not this spine)
- **Powder A/B/C.** Do **not** claim Powder B landed
- **READY HIP persist / Chest vs Low Options row.** Do **not** add READY HIP dials here. #168 play U stays two poses without restamping that seat. See `OPTIONS_SHELF.md`
- Explicit L/R overrides for asymmetric cant/inspect — later if A fails. **Not week wrap**

See `PEEK_FINDINGS.md` Closed by #167 + Closed by #168. Overnight cooks steal from this sheet.
