# Options mouse / hip / ADS sensitivity — house pointer

Range Tech. **Landed** fulcrumRust [#163](https://github.com/initialvisuals/fulcrumRust/pull/163) (2026-09-10, merge `96e4410e`). Controls pane only.

**Canonical dial sheet:** fulcrumRust [`docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_MOUSE_SENS_DIAL_SHEET.md). Steal from that sheet — do **not** duplicate or invent numbers here. House seat: [`OPTIONS_SHELF.md`](OPTIONS_SHELF.md) Camera / feel.

CREDITS + STEAL_MAP already claimed in-PR — house shelf only.

## Landed lock (stolen, not invented)

All four Controls rows sit on the existing #46 `LOOK_MUL` lock (**1.00** / **0.25–2.00** / step **0.05**). Persist `project.json`.

| Row | Persist | Default |
|-----|---------|---------|
| **MOUSE H** | `look_mul_h` | **1.00** |
| **MOUSE V** | `look_mul_v` | **1.00** |
| **HIP** | `hip_look_mul` | **1.00** |
| **ADS** | `ads_look_mul` | **1.00** |

Feel-lab `MoveDials.look_sens` **0.0022** + feel ADS weight **0.86** / blend **6.4** stay DNA. Options ADS is a user mul on top. Old `"look_mul"` seeds both mouse axes when the split keys are absent. Invert Y stays.

## Still cooking (do not claim)

- Options READY HIP **#165** already landed (sibling — CHEST / LOW HIP, persist `default_hip`). Do **not** restamp those rows here. Do **not** claim Powder B landed
- Hypha Graphics **RES / FOV / AA / AA STR / AO / POST** later landed **#164** — see [`OPTIONS_GRAPHICS.md`](OPTIONS_GRAPHICS.md)
- Augury remap / Tab inventory press-toggle
- PreferredHand A later landed **#168** — see [`PREFERRED_HAND_A.md`](PREFERRED_HAND_A.md)
- fulcrumRust **#167** AIM TUNE LIVE per-kit persist — **landed** (Range parallel — not this sheet)

See `PEEK_FINDINGS.md` Closed by #163 + `FULCRUMRUST_LAST_PASS_LOCK.md`.
