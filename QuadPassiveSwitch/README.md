# Quad Passive Switch

A 4HP, 3U Eurorack utility module with four independent **SPDT** (single-pole,
double-throw) passive switches. Each section manually routes one signal between two
destinations using a sub-mini toggle switch. The whole module is passive — it needs
**no power** and adds no buffering or coloration to the signal.

## Specifications

| | |
| --- | --- |
| Format | Eurorack, 3U |
| Width | 4HP (20 mm) |
| Panel height | 128.5 mm |
| Depth | Shallow (passive, no power header) |
| Power | None required |
| Switches | 4 × SPDT sub-mini toggle |
| Jacks | 12 × 3.5 mm mono switched |

## How it works

The module is divided into four identical sections, arranged top-left (TL),
top-right (TR), bottom-left (BL), and bottom-right (BR). Each section has:

- **IN** — signal input
- **OUT 1** — output selected when the toggle is in position 1
- **OUT 2** — output selected when the toggle is in position 2

The toggle switch connects **IN** to either **OUT 1** or **OUT 2**. Because the
path is just a mechanical contact, it works with any signal: audio, CV, gates,
clocks, or triggers.

### Reverse use (2-to-1)

Since the switch is passive and symmetrical, each section can be used in reverse:
patch two sources into **OUT 1** and **OUT 2**, and the toggle selects which one
appears at **IN**. In this mode **IN** becomes the output and the OUTs become inputs.

> Note: as with any passive multiple/switch, only patch a signal into one side of a
> given section at a time when using it in reverse, to avoid summing or back-feeding
> sources.

## Bill of materials

| Designators | Qty | Part | Footprint |
| --- | --- | --- | --- |
| J1–J12 | 12 | 3.5 mm mono switched jack (PJ398SM) | `EighthInch_PJ398SM` |
| SW1–SW4 | 4 | SPDT sub-mini toggle | `Switch_Toggle_SPDT_SubMini` |

See [`production/quad_passive_switch_gerbers_v1.0_bom.csv`](production/quad_passive_switch_gerbers_v1.0_bom.csv)
for the fabrication BOM.

## Files

- `quad_passive_switch.kicad_sch` — schematic
- `quad_passive_switch.kicad_pcb` — main PCB layout
- `quad_passive_switch_faceplate.kicad_pcb` — panel / faceplate layout
- `quad_passive_switch.pdf` — rendered schematic
- `quad_passive_switch.kicad_pro` — KiCad project
- `production/` — Gerbers (`*_gerbers_v1.0.zip`, `*_faceplate_gerbers_v1.0.zip`),
  drill/netlist, BOM, designators, and pick-and-place position files for v1.0

## Building it

1. Open `quad_passive_switch.kicad_pro` in [KiCad](https://www.kicad.org/) 8.0+ to
   inspect or modify the design.
2. To fabricate, send `production/quad_passive_switch_gerbers_v1.0.zip` (PCB) and
   `production/quad_passive_switch_faceplate_gerbers_v1.0.zip` (panel) to a PCB
   manufacturer.
3. Solder the 12 jacks and 4 toggle switches per the BOM. There are no other
   components — no resistors, ICs, or power connector.

## Revision

- **v1.0** — initial release.
