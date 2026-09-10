# Options Graphics — house pointer

Hypha. **Landed** fulcrumRust [#164](https://github.com/initialvisuals/fulcrumRust/pull/164) (2026-09-10, merge `159b3d11`). Graphics pane only.

**Canonical dial sheet:** fulcrumRust [`docs/OPTIONS_GRAPHICS_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_GRAPHICS_DIAL_SHEET.md). Steal from that sheet — do **not** duplicate or invent numbers here. House seat: [`OPTIONS_SHELF.md`](OPTIONS_SHELF.md) Resolution / Graphics / FOV.

CREDITS + STEAL_MAP already claimed in-PR — house shelf only.

## Landed lock (stolen, not invented)

| Dial | Persist | Lock |
|------|---------|------|
| **RES** | `resolution` | Default **NATIVE** (desktop native — no invented pair). Presets: 1280×720 · 1920×1080 · UW 2560×1080 · 2560×1440 · 3840×2160 4K · **UW 4K CLASS** (3840×1600 class) · **3440×1440** (Evan) · Steam survey fill **2560×1600 / 1920×1200 / 1366×768** (July 2026 primary display). Borderless stays desktop-native |
| **FOV** | `fov_hip` | Hip **base** **90**. ADS still uses optic locks (iron/holo **60** · acog **25** · canted **60** CQC · scope **10**). Feel-sheet FOVs are not overwritten. Pane 70–110 / step 1 is Hypha chrome — **not** tip-locked |
| **AA** | `aa_type` | **FXAA / OFF**. Default FXAA. TAA later |
| **AA STR** | `aa_strength` | **0–1** on the live #55 mix. Default **0.5** = pass knob (not CA **0.35**) |
| **AO** | `ao_quality` | **OFF / LOW / HIGH**. Default Off. Low = live #55 8-tap · r **0.55**. High = Mycelium **24**-tap, same 0.55 radius. No invented radius |
| **POST** | `post_quality` | **OFF / LOW / HIGH**. Default **HIGH**. Off skips Options post. Low = AA only. Heat #66 + wound #143 stay |

WINDOW / CA / GRAIN / DOF / FOG / CAM / WARP / STREAM unchanged. Old `"ao"` / `"aa"` bools still load. Lab-Rat texture / mipmap **later landed #172** — see [`OPTIONS_TEXTURE.md`](OPTIONS_TEXTURE.md).

## Still cooking (do not claim)

- Lab-Rat texture / mipmap quality **later landed #172** — see [`OPTIONS_TEXTURE.md`](OPTIONS_TEXTURE.md)
- Augury remap / Tab inventory press-toggle
- Options READY HIP **#165** already landed (sibling). Powder B — do **not** claim landed
- fulcrumRust **#167** AIM TUNE live-save — **not** this cook
- Bloom / godRays / brightness / gamma — still **no path** (#86)

See `PEEK_FINDINGS.md` Closed by #164 + `FULCRUMRUST_LAST_PASS_LOCK.md`.
