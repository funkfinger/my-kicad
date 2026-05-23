# my-kicad

Jay's personal KiCad library — footprints and symbols reused across projects.

## Layout

```
my_kicad_library.pretty/   KiCad footprint library (each .kicad_mod is one footprint)
my_kicad_library.kicad_sym KiCad symbol library
```

## Wiring it into a project (KiCad 9+)

Add these to your global `fp-lib-table` and `sym-lib-table` (in `~/Library/Preferences/kicad/<version>/`):

```
(lib (name "my_kicad_library") (type "KiCad") (uri "/Users/jayw/Git/Electronics/my-kicad/my_kicad_library.pretty") (options "") (descr ""))
(lib (name "my_kicad_library") (type "KiCad") (uri "/Users/jayw/Git/Electronics/my-kicad/my_kicad_library.kicad_sym") (options "") (descr ""))
```

Once registered, footprints can be referenced from any PCB as `my_kicad_library:<footprint-name>`.

## Current contents

Footprints:
- `funkfinger-logo`, `funkfinger-logo-9mm`, `funkfinger-logo-15mm` — funkfinger.com brand logo
- `gio-logo` — gio module silk
- `OSHW-Logo2_6mm` — Open Source Hardware mark
- `XIAO-RP2350-DIP_pins_only` — Seeed XIAO RP2350 with only the DIP pins exposed

Symbols:
- `XIAO-RP2350-DIP_pins_only`
