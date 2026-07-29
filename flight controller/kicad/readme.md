# KiCad Source — Flight Controller

This folder contains the complete KiCad project for the flight controller PCB.

## Files

| File | Description |
|---|---|
| `flight_controller.kicad_sch` | Full schematic — STM32F, Ra-01 LoRa, AMS1117-3.3/5.0 regulators, IMU header, servo outputs |
| `flight_controller.kicad_pcb` | 2-layer PCB layout — 91.4 × 69.4 mm, FR4 1.6 mm |

## Requirements

- KiCad **10.0** or later
- All symbols and footprints used are from the KiCad standard library or bundled custom symbols

## Design Notes

- Board thickness: **1.6 mm**
- Copper layers: **F.Cu** (components + signal) and **B.Cu** (ground pour + power traces)
- Paper size: **A4**

## How to Open

```bash
# Open the PCB layout
kicad flight_controller.kicad_pcb

# Open the schematic
kicad flight_controller.kicad_sch
```

Or launch KiCad and open either file from **File → Open**.
