# Options Graphics / RES / FOV — house pointer

Hypha. **Landed** fulcrumRust [#164](https://github.com/initialvisuals/fulcrumRust/pull/164) (2026-09-10, merge `159b3d11`). Graphics pane only. Augury **#45** chrome.

**Canonical dial sheet:** fulcrumRust [`docs/OPTIONS_GRAPHICS_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_GRAPHICS_DIAL_SHEET.md). Steal from that sheet — do **not** duplicate or invent numbers here. House seat: [`OPTIONS_SHELF.md`](OPTIONS_SHELF.md) Resolution / Graphics / FOV.

CREDITS + STEAL_MAP already claimed in-PR — house shelf only.

## Landed lock (stolen, not invented)

Hypha owns Options Graphics pane wiring. Persist `project.json`.

| Dial | Persist | Lock |
|------|---------|------|
| **RES** | `resolution` | Dropdown beside WINDOW. Default **NATIVE** (desktop native — no invented pair). Shelf presets + UW 4K CLASS (3840×1600 class) + Evan 3440×1440 + Steam survey fill **2560×1600 / 1920×1200 / 1366×768**. Borderless stays desktop-native |
| **FOV** | `fov_hip` | Hip **base**, default authored **90**. ADS still uses optic locks (iron/holo **60** · acog **25** · canted **60** CQC). Feel-sheet FOVs not overwritten. Pane 70–110 / step 1 is Hypha chrome — **not** tip-locked |
| **AA** | `aa_type` | Type **FXAA / OFF**. TAA later |
| **AA STR** | `aa_strength` | 0–1 on live #55 mix (**0.5** pass knob). Not CA **0.35** |
| **AO** | `ao_quality` | **OFF / LOW / HIGH**. Low = live 8-tap · r **0.55**. High = Mycelium 24-tap. No invented radius |
| **POST** | `post_quality` | **OFF / LOW / HIGH** master. Default **HIGH**. Off skips Options post. Low = AA only. Heat **#66** + wound **#143** stay. Bloom/godRays still no path |

Old `"ao"` / `"aa"` bools still load. New keys win when present.

## Still cooking (do not claim)

- Lab-Rat texture / mipmap quality (vendor COL / `lod_mips` / `FULCRUM_UV`)
- Augury remap / Tab inventory press-toggle
- TAA
- Bloom / godRays / brightness / gamma (**#86** no path)
- STREAM `StreamPolicy` (already Hypha TERRAIN / LAST_PASS — do not re-own)
- Range mouse V/H + hip/ADS (**#163** already shelved)
- Options default hip Chest vs Low + Powder B (Range — do **not** invent a #165 shelf here)

See `PEEK_FINDINGS.md` Closed by #164 + `FULCRUMRUST_LAST_PASS_LOCK.md`.
