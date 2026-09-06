# Glyph legend — Pycelium HUD decode

Parked house decode for the **pycelium-win** mesocosm telemetry HUD (cryptic 3×5 bitmap digits). Keep the glyphs as flavor; English rides **analysis-knowledge-core** (fade-in white mono labels, thin frames, elbow callouts) on hover / pick with a density dial.

## Top numbers (top → bottom)

| Slot | Meaning |
|------|---------|
| 1 | **FPS** — frame rate |
| 2 | **Live tips** — active growth tips |
| 3 | **Fusions** — anastomosis events (HUD: per-step, not career totals) |
| 4 | **Branches** — branch events (same caveat as fusions) |
| 5 | **C:N** — soluble carbon / nitrogen ratio |

## Mid bars (teal → brown)

| Bar | Meaning |
|-----|---------|
| 1 | **Biomass / hypha** |
| 2 | **Internal C (cord)** |
| 3 | **Soluble C (food)** |
| 4 | **Soluble N** |
| 5 | **Enzyme** |
| 6 | **Organic / soil** |

## Lower block

| Region | Fields |
|--------|--------|
| **Slice** | Z / thickness / zoom |
| **Tip** | selected tip id / lineage / age / reserve |
| **Param** | slot + value (live tune readout) |

## UI pattern note

- Cryptic digits stay on-screen as house DNA.
- Hover / pick → analysis-knowledge-core English fade-in (not permanent chrome).
- SuperSim-style density dial: quiet idle → rich on sample → telemetry on bench/drift.
- Do not force this pattern into unrelated public READMEs; use where a live HUD exists.

## Sibling shelf

Bake shots (Burj / angel-hair / slice webs) → [`bake-book/README.md`](bake-book/README.md)

When Pycelium #4 merges, prefer `pycelium/docs/HUD_LEGEND.md` as the live source of truth and sync this file.

---

**Initial Visuals** — tools, sims, games, and experiments.
