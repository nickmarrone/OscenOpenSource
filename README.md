# Oscen Open Source

Open source hardware designs for **Oscen Eurorack Modules**.

This repository contains the KiCad design files (schematics, PCB layouts, panels)
and manufacturing outputs (Gerbers, BOMs, pick-and-place files) for a selection of
Oscen's Eurorack modules, released for the community to study, build, and remix.

## Modules

| Module | Format | Description |
| --- | --- | --- |
| [Quad Passive Switch](QuadPassiveSwitch/) | 4HP, 3U | Four independent SPDT passive switches for manually routing signals — no power required. |

### Quad Passive Switch

A 4HP utility module with four independent **SPDT (single-pole, double-throw)**
toggle switches. Each section takes one input and routes it to one of two outputs
(or, run in reverse, selects between two inputs feeding a single output). The
signal path is entirely passive, so the module needs no power and adds no coloration
— useful for routing audio, CV, gates, clocks, or triggers.

See the [module README](QuadPassiveSwitch/README.md) for full details.

## Repository layout

Each module lives in its own directory and contains:

- `*.kicad_sch` — schematic
- `*.kicad_pcb` — main PCB layout
- `*_faceplate.kicad_pcb` — panel / faceplate layout
- `*.kicad_pro` / `*.kicad_prl` — KiCad project files
- `*.pdf` — rendered schematic
- `production/` — Gerbers, drill files, BOM, and pick-and-place outputs ready for fabrication

## Building these modules

1. Open the module's `.kicad_pro` in [KiCad](https://www.kicad.org/) (8.0 or newer) to view or edit the design.
2. To fabricate, send the Gerber `.zip` files in the module's `production/` directory
   to a PCB manufacturer, along with the BOM (`*_bom.csv`) and position
   (`*_positions.csv`) files if you want assembly.

## License

These designs are released as open source hardware. Unless otherwise noted in a
module's directory, you are free to build, modify, and share them. Please credit
**Oscen Modules**.
