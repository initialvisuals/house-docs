# FoW palette — data scheme (`fow_palette/v1`)

File: `assets/trims_utility/fow_palette.json`. Human cheat: `docs/FOW_PALETTE.md`.

## Prefix lock

`FOW_` is reserved for palette colors. Never reuse for non-color identifiers.

## Naming

| Kind | Rule |
|------|------|
| Greys | `FOW_Black` / `FOW_White` at ends; mid `FOW_Grey_NN` by relative luminance (higher index = lighter). |
| Chromatics | Short taste tokens: `FOW_Blood`, `FOW_Foliage`, `FOW_Brass`, … |

## Shape

```
{
  "schema": "fow_palette/v1",
  "prefix": "FOW_",
  "plates": { "<id>": { "swatches": [{ "id", "hex", "rgb", "background" }] } },
  "house": { "swatches": [{ "id", "hex", "rgb", "kind", "plates", "lum", "grey_index?" }] }
}
```

## Steal rule

Artists sample the plate. Code / shaders / kits / agents steal `FOW_*` from this JSON — not chat scroll, not monitor eyedropper.
