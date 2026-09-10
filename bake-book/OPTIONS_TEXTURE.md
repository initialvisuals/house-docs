# Options TEXTURE + MIPMAP — house pointer

Lab-Rat. **Landed** fulcrumRust [#172](https://github.com/initialvisuals/fulcrumRust/pull/172) (2026-09-10, merge `3ca49f27`). Graphics pane **TEXTURE** / **MIPMAP** only (#114 seat).

**Canonical dial sheet:** fulcrumRust [`docs/OPTIONS_TEXTURE_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/OPTIONS_TEXTURE_DIAL_SHEET.md). Steal from that sheet — do **not** duplicate or invent numbers here. House seat: [`OPTIONS_SHELF.md`](OPTIONS_SHELF.md) Graphics.

CREDITS + STEAL_MAP already claimed in-PR — house shelf only.

## Landed lock (stolen, not invented)

Rows sit under **STREAM** on Options → GRAPHICS (title or HOLD). A/D or Enter cycles. Persist `project.json` on the existing Hypha save path. Maps onto tip-locked 256/64/16 thumbs — do not invent 4k atlases or new STREAM rings.

| Dial | Persist | Default | Steps | What it does |
|------|---------|---------|-------|--------------|
| **TEXTURE** | `texture_quality` | **HIGH** | LOW 16² · MED 64² · HIGH 256² · ULTRA 256² | Vendor COL / PBR shelf downsample of the existing thumb. Ultra === High — tip already ships 256² (`pbr=vendor`). Not atelier 3K |
| **MIPMAP** | `mipmap_quality` | **MED** | LOW +1 ring · MED identity · HIGH −1 · ULTRA −2 | How aggressive mid/far `lod_mips` packs get. Bias sits **after** `promote_for_uv` / `MATERIAL_HOLD_M`. High ≈ `FULCRUM_UV` scale 2; Ultra ≈ scale 4 (lod-2 bridge → near 256²; lod-3 horizon → mid 64²). Height / mesh lod / chunk metres **16** stay |

#152 crawl lock held: `STABLE_LOCUS_RES` **16** · `MATERIAL_HOLD_M` **2.5** · `LUMA_GRAIN` ±**0.08**. Height / DISP stay bilinear.

Building solids sample COL live (`grade_solid`). Terrain verts + desert skirt **regrade** on change (recolor in place — no remesh, no STREAM radius). Env peek: `FULCRUM_TEXTURE` / `FULCRUM_MIPMAP` override Options at boot (same pattern as `FULCRUM_STREAM`). Smoke prints `tex=high/256` on the `pbr=` tag and `mip=med` on `grit_mips=`.

## Still cooking (do not claim)

- Augury remap / Tab inventory press-toggle
- Hypha res / FOV / AA / AO / post / WARP / STREAM stay **#164** / STREAM Options — not this cook
- Range mouse V/H + hip/ADS **#163** · READY HIP **#165** · powder · AIM TUNE
- Bloom / godRays / brightness / gamma — still **no path** (#86)
- 4k atlases / new STREAM rings / atelier 3K

See `PEEK_FINDINGS.md` Closed by #172 + `FULCRUMRUST_LAST_PASS_LOCK.md`.
