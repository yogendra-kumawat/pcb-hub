# PCB Hub

A curated collection of custom PCBs designed in **KiCad**, spanning embedded systems, motion control, RF communication, and analog signal generation. Each board was designed from scratch — schematic capture, layout, and fabrication-ready Gerbers — with a focus on clean routing, proper power distribution, and real-world hardware integration.

---

## Projects

| Project | Description | Board Size | Layers |
|---|---|---|---|
| [Flight Controller](#flight-controller) | STM32 + LoRa + IMU flight controller | 91.4 × 69.4 mm | 2 |
| [Function Generator](#function-generator) | STM32-based multi-waveform signal generator | 90.4 × 45.0 mm | 2 |
| [Writing Machine](#writing-machine) | 2-DOF polar arm plotter motor driver board | 56.2 × 26.0 mm | 2 |

## Machines
|Item|Description|
|---|---|
| [Drill Machine](#drill-machine) | Speed-controlled PCB drill with motor driver 
| [Solution Machine](#solution-machine) | Automated liquid dispensing controller 

---

## Tools

- **EDA**: KiCad 10.0
- **Fabrication**: JLCPCB / standard 2-layer FR4, 1.6 mm
- **Design Rules**: 0.2 mm min trace, 0.2 mm min clearance

---

*All KiCad source files (`.kicad_pcb` + `.kicad_sch`) are included in each project's `/kicad` subfolder.*
