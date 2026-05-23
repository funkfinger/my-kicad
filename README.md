# my-kicad

Jay's personal KiCad library — footprints and symbols reused across projects, plus trimmed vendored copies of third-party libraries also used here.

## Layout

```
my_kicad_library.pretty/        Jay's own footprints
my_kicad_library.kicad_sym      Jay's own symbols

benjiaomodular.pretty/          Vendored subset (CC BY-SA 4.0) — see benjiaomodular-ATTRIBUTION.md
benjiaomodular.kicad_sym
benjiaomodular-LICENSE.md
benjiaomodular-ATTRIBUTION.md
```

## Wiring it into a project (KiCad 9+)

Add these to your global `fp-lib-table` and `sym-lib-table` (in `~/Library/Preferences/kicad/<version>/`):

```
(lib (name "my_kicad_library") (type "KiCad") (uri "/Users/jayw/Git/Electronics/my-kicad/my_kicad_library.pretty") (options "") (descr ""))
(lib (name "my_kicad_library") (type "KiCad") (uri "/Users/jayw/Git/Electronics/my-kicad/my_kicad_library.kicad_sym") (options "") (descr ""))
(lib (name "benjiaomodular")   (type "KiCad") (uri "/Users/jayw/Git/Electronics/my-kicad/benjiaomodular.pretty")   (options "") (descr ""))
(lib (name "benjiaomodular")   (type "KiCad") (uri "/Users/jayw/Git/Electronics/my-kicad/benjiaomodular.kicad_sym") (options "") (descr ""))
```

Once registered, parts can be referenced as `<libname>:<part-name>`.

## Current contents

### `my_kicad_library` (Jay's own)

Footprints:
- `funkfinger-logo`, `funkfinger-logo-9mm`, `funkfinger-logo-15mm` — funkfinger.com brand logo
- `gio-logo` — gio module silk
- `OSHW-Logo2_6mm` — Open Source Hardware mark
- `XIAO-RP2350-DIP_pins_only` — Seeed XIAO RP2350 with only the DIP pins exposed

Symbols:
- `XIAO-RP2350-DIP_pins_only`

### `benjiaomodular` (vendored subset — CC BY-SA 4.0)

Trimmed from [github.com/clacktronics/benjiaomodular](https://github.com/clacktronics/benjiaomodular). Full details in [benjiaomodular-ATTRIBUTION.md](benjiaomodular-ATTRIBUTION.md).

Footprints:
- `Potentiometer_RV09` — used by gio
- `Resistor_L6.3mm_D2.5mm_P7.62mm_Horizontal` — used by EurorackBusBoardJST

Symbols:
- `PJ3001F` — used by gio
