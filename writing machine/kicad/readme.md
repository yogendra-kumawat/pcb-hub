# KiCad Source — Writing Machine v3.0

This folder contains the complete KiCad project for the writing machine motor driver board.

## Files

| File | Description |
|---|---|
| `writin machine 3.0.kicad_sch` | Full schematic — STC8G1K08A MCU, 3× 2N2219 BJT motor drivers, AMS1117-5.0, UART header, motor output connectors |
| `writin machine 3.0.kicad_pcb` | 2-layer PCB layout — 56.2 × 26.0 mm, FR4 1.6 mm |

## Requirements

- KiCad **10.0** or later
- Custom symbol: `MCU_STC:STC8G1K08A-36I-DFN8` — included in the schematic's embedded library

## Design Notes

- Board thickness: **1.6 mm**

## How to Open

```bash
kicad "writin machine 3.0.kicad_pcb"
kicad "writin machine 3.0.kicad_sch"
```
