# benjiaomodular — vendored subset

This repo includes a trimmed subset of the [benjiaomodular KiCad library](https://github.com/clacktronics/benjiaomodular) by [@benjiaomodular](https://instagram.com/benjiaomodular), licensed under [CC BY-SA 4.0](benjiaomodular-LICENSE.md).

## What's vendored here

Footprints (`benjiaomodular.pretty/`):
- `Potentiometer_RV09` — used by gio
- `Resistor_L6.3mm_D2.5mm_P7.62mm_Horizontal` — used by EurorackBusBoardJST

Symbols (`benjiaomodular.kicad_sym`):
- `PJ3001F` — used by gio

The library name `benjiaomodular` is preserved so existing project references (`benjiaomodular:PJ3001F`, etc.) resolve unchanged once the global `fp-lib-table` / `sym-lib-table` entries are repointed at this repo.

## Modifications

None. Files copied verbatim from upstream; the trimmed `.kicad_sym` is the upstream header + the `PJ3001F` symbol block + the closing paren (paren-balanced, no edits to the symbol itself).

## Upstream

- Source: https://github.com/clacktronics/benjiaomodular
- License: Creative Commons Attribution-ShareAlike 4.0 International
- Snapshot taken from local working copy on 2026-05-23
