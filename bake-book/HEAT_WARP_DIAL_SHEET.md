# Barrel heat warp — dial sheet

Canonical warp-visibility lock for Range Tech hold-**J** tip shimmer. Steal into fulcrumRust from this sheet + the in-repo source, not chat scroll.

**Source:** fulcrumRust [`docs/HEAT_WARP_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/HEAT_WARP_DIAL_SHEET.md)  
**Live fulcrumRust steal:** Range Tech **#155** (`d3d7848c`, 2026-09-10) — restore visible barrel heat warp at hold-J.  
**Sibling:** card geometry / CE tip **0.2.8** field stays [`../heat-card-dial-sheet.md`](../heat-card-dial-sheet.md) (**#129**). This sheet is the warp *range* + shader gate — not a card rewrite. Do **not** reopen orange cards.

1P viewmodel / Range feel only. Colorless Hypha post (`#66`) still receives the tip lattice as spatial input — no orange RGB card paste, no world-pipeline card draw.

Hold-**J** heat-tune cooks `barrel_energy` without recoil so the can stays still. This cook restores **visible** tip UV warp at that peek without bringing back the fog blob.

## Ownership

| Dial | Owner | What it does | What it is not |
|------|-------|--------------|----------------|
| `HeatDials.haze_strength` | Range | Barrel heat warp range. **0** = off. **0.01** = CE enable floor (warp on). **0.11** = stolen max. | Options Graphics **WARP** |
| Options Graphics **WARP** (`post.warp_strength`) | Hypha | Pixellation / floor-warp mix toward CE PIXEL SCALE 2. Default **0.01**, max **1.0**. | Heat lattice / barrel haze |
| Tip cards + lobe (`count` / `scale_*` / `lobe`) | Range | Author the **field**: UV center, radius, lattice energy. RGB stays zeroed in `heat_mesh`. | A drawn orange card |
| `post.heat` | Hypha consume | `[center_u, center_v, strength, radius]` — `heat_warp_uv` sample-only displace | Fog / ToD haze |
| Fog `fog_near` / `fog_far` | Hypha dump #86 | Extract distance haze **375 / 520**. Hideout unfogged. | Barrel heat |

Cranking Options **WARP** to 1.00 snaps the floor. It cannot sell barrel heat.

## Warp range

| Haze | Mul | Strength at visual 1 / lattice 0.60 | Peek |
|------|-----|-------------------------------------|------|
| **0** | 0 | 0 | Off |
| **0.005** | 0.50 | 0.405 | Fade onto the floor |
| **0.01** (CE live default) | **1.00** | **0.81** (`lattice × 1.35`) | Enable floor — hold-J tip warp |
| **0.11** (stolen / live-sheet max) | **1.20** | **0.972** | Max warp, still tip-local |

`post_heat_strength = visual × (lattice_emissive_mean × 1.35) × haze_warp_mul(haze)`.

`visual × haze` at the CE floor is **0.01**. The shader used to early-out below 0.01 and then scale leftover strength by **0.010** (~0.0001 UV). That is why max Options WARP + hold-J showed nothing.

## Field (anti-blob)

Cards stay the CE tip lock. Tall dump ribbons (`scale_y` 1.86) + `#71` lattice restore on a **0.18** radius were the fog blob. This cook does **not** reopen that field.

| Dial | Value | Note |
|------|-------|------|
| `haze_strength` | **0.01** | Enable floor (unchanged CE number) |
| `scale_x` / `scale_y` | **0.28 / 0.86** | Short thin tip cards |
| `count` / `segs` | **20 / 32** | Tip-weighted lattice |
| `lobe` | **0.40** | Tight muzzle |
| Radius scale / cap | **0.40 / 0.08** | Muzzle-adjacent only |
| Lattice gain | **1.35** | `#66` `energy/count * 1.35` |
| Max mul | **1.20** | Stolen 0.11 vs the floor |
| Shader gate | **0.001** | Was 0.01 (fought the enable floor) |
| Shader UV scale | **0.010** | `#66` steal — strength 0.81 → ~0.008 UV tip shimmer |

Fog 375 / 520 / enabled stay. No ToD / pass-lab retune.

## Left alone

Lab-Rat stamps / UV / STREAM / bounds. Beabim gun KIND. Augury chrome / Home. Hypha Options **WARP** pixellation numbers. `#89` projectile feel. AIM TUNE. Ground haze stays strength **0**.

See `FULCRUMRUST_LAST_PASS_LOCK.md` Visible barrel heat warp (#155) · `PEEK_FINDINGS.md` Closed by #155.
