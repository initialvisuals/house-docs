# Hold pose spine (grip-invariant PreferredHand A)

House contract for PreferredHand / AIM TUNE pose architecture. **Holding / locked intent — parked until Evan refresh.** Steal from this sheet, not chat. Do **not** invent dial numbers. No code. Clerk owns this sheet.

## Spine

Poses sit on the **hold/grip bone**. Guns hang from attach sockets relative to that hold. One pose bank + HAND L/R mirror (PreferredHand **A**).

## Locked

| Lock | Detail |
|------|--------|
| **Hold is the pose home** | Cant / hip / low-hip / etc. reference the **hold/grip bone**, not each gun mesh |
| **Guns hang** | Kits attach from sockets relative to that hold |
| **Optic class** | Iron sights classified as an **optic class** — one class offset; ADS transitions to the active glass of the selected weapon |
| **PreferredHand A** | One pose bank + **HAND L/R mirror** — not full L+R authored pairs per gun×optic |
| **L/R shoulder** | HAND flip + lean hinge (Hypha tip). Not a second per-gun bank |
| **Grip invariant** | **Hold/grip socket** is the spatial invariant across kits. Muzzle / suppressor / optic / grips are **child sockets** — attachment swaps move barrel tip, not the hold bank |
| **Ballistics loft** | Uses **muzzle child**, not hold bone |
| **L/R overrides** | Explicit L/R overrides only where asymmetric (cant/inspect) later if A fails — **not week wrap** |

Do **not** author a second pose bank per gun. Do **not** move the hold bank when a can / optic / grip swaps. Do **not** loft ballistics from the hold bone.

## Already shipped (siblings — do not restamp)

These stay facts. This sheet does **not** claim they already implemented grip-invariant A.

- PreferredHand enum + NEW PROFILE onboard **landed #116** (Hypha). Right default · `project.json` permanent vs live · death clears live · extract→stash stub. `shoulder_t` seats Range H. **No** `scale.x = −1`
- AIM TUNE End sheet **#97** / live-save **#103** / PX **#138**. Poses **#94 / #98 / #99 / #100** · hold springs **#109**. Canted optic ATTACH **#150**
- Hypha 3P lean hinge **#145**. Beabim held 3P kit clone **#153**. House lock **1P ≠ 3P** held

Range Tech owns the AIM TUNE / PreferredHand **cook after refresh**. #116 stays the onboard enum. This spine is the pose bank after Evan refresh.

## Seat map (ownership — cook after refresh)

| Seat | Owns |
|------|------|
| **Range Tech** | AIM TUNE / PreferredHand cook after refresh (pose bank on hold/grip · optic class · HAND L/R mirror A) |
| **Hypha** | Lean hinge (tip). PreferredHand enum / profile **#116** already landed |
| **Beabim** | 3P attach honesty — remote kit hangs from the same hold invariant (1P ≠ 3P held) |
| **Clerk** | This sheet |

## Explicitly parked

- **Full per-gun L+R banks.** A is the path. Do not author gun×optic L+R pairs this wrap
- **Glasses N / numpad.** Not this sheet
- **Ballistics #161 rebase.** Separate. Loft still uses **muzzle child**, not hold bone — do not fold that rebase into this cook
- **Options default hip Chest vs Low toggle.** Evan locked intent (Chest default). In-play two poses only (chosen hip + canted); shotgun may force Low later. Range still cooking this tip + Powder B separately — not this spine’s implementation. Do **not** claim the hip toggle or Powder B landed. See `OPTIONS_SHELF.md`
- Explicit L/R overrides for asymmetric cant/inspect — later if A fails. **Not week wrap**

See `PEEK_FINDINGS.md` Holding / locked intent — hold pose spine. Overnight cooks steal from this sheet.
