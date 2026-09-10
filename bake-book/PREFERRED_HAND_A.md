# PreferredHand A — house pointer

Range Tech. **Landed** fulcrumRust [#168](https://github.com/initialvisuals/fulcrumRust/pull/168) (2026-09-10, merge `1849ce6b`). Hold-bone mirror + HAND L/R chrome.

**Canonical dial sheet:** fulcrumRust [`docs/PREFERRED_HAND_A_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/PREFERRED_HAND_A_DIAL_SHEET.md). Steal from that sheet — do **not** duplicate or invent numbers here. House seat: [`HOLD_POSE_SPINE.md`](HOLD_POSE_SPINE.md).

CREDITS + STEAL_MAP already claimed in-PR — house shelf only.

## Landed lock (stolen, not invented)

| Dial | Lock |
|------|------|
| **HAND chrome** | **`HAND R` / `HAND L`** from **live hold X**. Gun right of camera middle (+X) = **HAND R**. Midline counts R. **Not** inverted `Shoulder` enum. Axis invert? **No** |
| **Authored hip X** | **+0.2403** (camera-local +X = camera-right, `AXIS_LOCK`) |
| **Mirror A** | One right bank. Left = sagittal **−X / −yaw / −roll** (cant **0.785** → **−0.785**). Pitch / Y / Z stay. **No** `scale.x = −1` |
| **H** | Live HAND flip. PreferredHand onboard (#116) seats the home |
| **AIM TUNE** | Shows **HAND · kit · pose** (`HAND R  MP9-Z  HIP`). Left numbers are the mirror. WEAPON +X while HAND L writes authored −X so the gun still walks camera-right |
| **Crosshair** | 2D HUD plus hides when `ads_factor` **> 0.5** (`FeelState::ADS_COMMIT`). Hip + U-cycle canted keep it. Options **CROSSHAIR** toggle stays |

End PX **±0.50** held. Leftover `shoulder_cross_*` / `shoulder_x_min` stay DNA for End leftover-wall arith (~**+0.226**) — **not** applied to the live left hold.

## Still cooking (do not claim)

- fulcrumRust **#167** AIM TUNE live-save — **not** this cook
- Powder A/B/C. Do **not** claim Powder B landed
- READY HIP persist **#165** already landed (sibling — do **not** restamp here). #168 play U stays two poses (chosen hip ↔ canted)
- Hypha 3P lean boxes. Augury death / downed strip. Lab-Rat stamps

See `PEEK_FINDINGS.md` Closed by #168 + `FULCRUMRUST_LAST_PASS_LOCK.md`.
