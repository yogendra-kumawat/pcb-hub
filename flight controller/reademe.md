# Flight Controller PCB

A custom 2-layer flight controller designed in **KiCad**, built around an **STM32F** microcontroller with onboard LoRa RF communication, I²C IMU support, Bluetooth connectivity, and a regulated dual-rail power supply. Designed for small UAV and fixed-wing applications where wireless telemetry and compact integration matter.

---

## Board Overview

| Parameter | Value |
|---|---|
| Board Size | 91.4 × 69.4 mm |
| Layers | 1 (B.Cu) |
| Substrate | FR4, 1.6 mm |
| EDA Tool | KiCad 10.0 |

---

## Hardware Design

### Key ICs & Modules

- **STM32F** — ARM Cortex-M3 MCU; SWD debug header (SWDIO + SWCLK + RESET) exposed
- **Ai-Thinker Ra-01** — SX1278-based LoRa module; SPI interface (S_IN / S_OUT), onboard antenna
- **AMS1117-3.3** — 3.3 V LDO regulator powering the STM32 and LoRa module
- **AMS1117-5.0** — 5 V LDO regulator for servo/peripheral rail
- **Bluetooth module socket** — I²C breakout socket for wireless config
- **MPU header** — I²C bus (SDA + SCK) routed to a dedicated 4-pin socket for external MPU/IMU
- **Status LED** — Power-on indicator with current-limiting resistor

### Connector Layout

The board exposes a full set of headers for system integration:

- `P1`, `P2` — Main motor/ESC signal output headers (20-pin dual-row)
- `S1`–`S4` — Servo signal outputs (individual 3-pin headers, PWM-capable)
- `ADJ_IN_PC13` / `ADJ_OUT` — Analog adjust input/output for gain or throttle tuning
- `SWDIO`, `SWCLK`, `RESET` — SWD programming header
- `VIN` — Raw power input; regulated to 3.3 V and 5 V on-board

---

## PCB Photos

### Etched Copper (Initial Design)

UV-transfer + ferric chloride etched on single-sided copper-clad board. Labels handwritten on the copper layer for quick identification during assembly.

![Initial Design — Etched PCB](initial%20design.jpeg)

---

### Assembled Front Side

Components populated: AMS1117 regulators, filter capacitors, resistors, status LED, and all DIP socket headers. The board uses IC sockets throughout for ease of module swapping during development.

![Front Side — Assembled](front%20side.jpeg)

---

### Solder Side (Back)

Solder joints on the back, showing trace routing and through-hole component pads. Flying-wire patches visible for late-stage signal reroutes during bring-up.

![Back Side — Solder Joints](back%20side.jpeg)

---

### Fully Integrated — Modules Populated

LoRa Ra-01 module, STM32 Blue Pill, MPU6050 IMU, and Bluetooth HC-05 all seated in their sockets. LiPo battery connected via JST; green LED confirms 3.3 V rail healthy.

![With Modules — System Live](with%20modules.jpeg)

---

## Design Highlights

- Dual LDO architecture keeps the analog IMU rail clean and separate from the digital/RF rail
- LoRa SPI lines kept short and routed away from motor signal headers to reduce coupling
- SWD header placed at board edge for easy probe access during firmware development
- All module connectors use standard 2.54 mm pitch — field-replaceable without soldering

---

## KiCad Source Files

Full schematic and layout are in the [`kicad/`](kicad/) subfolder:

```
kicad/
├── flight_controller.kicad_sch   # Schematic
└── flight_controller.kicad_pcb   # PCB layout
```

> Open with **KiCad 10.0** or later.
