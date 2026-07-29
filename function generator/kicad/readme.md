# KiCad Source — Function Generator

This folder contains the complete KiCad project for the function generator PCB.

## Files

| File | Description |
|---|---|
| `oscilloscope_power_other.kicad_sch` | Full schematic — STM32, AMS1117-3.3/5.0/ADJ regulators, 1N4007, OLED header, switches, potentiometers, barrel jack |
| `oscilloscope_power_other.kicad_pcb` | 2-layer PCB layout — 90.4 × 45.0 mm, FR4 1.6 mm |

## Requirements

- KiCad **10.0** or later
- All symbols from KiCad standard libraries (`Device`, `Connector`, `Regulator_Linear`, `Diode`, `Switch`)

## Design Notes

- Board thickness: **1.6 mm**
- Copper layers: **F.Cu** (top) and **B.Cu** (bottom)
- The schematic file name reflects the board's original dual purpose — function generator + oscilloscope port — from early planning

## How to Open

```bash
kicad oscilloscope_power_other.kicad_pcb
kicad oscilloscope_power_other.kicad_sch
```
