# ATtiny85 Breakout Board

A minimal breakout board for the ATtiny85 microcontroller designed in KiCad 8. Provides ICSP programming support, decoupling capacitors, and easy access to all I/O pins for compact embedded projects.

---

## Features
- ATtiny85 DIP-8 socket for easy chip swapping
- 6-pin ICSP header for programming
- Onboard 5V operation with decoupling
- All 6 I/O pins broken out to headers
- Reset button and power LED
- Compact form factor

## Specifications

| Parameter | Value |
|-----------|-------|
| MCU | ATtiny85 |
| Clock Speed | 8MHz (internal) / 16MHz (PLL) |
| Operating Voltage | 5V |
| I/O Pins | 6 (PB0–PB5) |
| Flash Memory | 8KB |
| EEPROM | 512B |
| Programming | ICSP / USBasp / Arduino as ISP |
| PCB Layers | 2 |
| Designed With | KiCad 8 |

## Project Structure

```
├── Schematic/       # KiCad schematic (.kicad_sch, PDF)
├── PCB/             # PCB layout (.kicad_pcb, .kicad_pro)
├── Gerbers/         # Fabrication files
├── BOM/             # Bill of materials (CSV)
├── 3D/              # 3D model (.step)
└── Images/          # PCB renders and schematic screenshots
```

## How It Works

The ATtiny85 runs from its internal 8MHz oscillator. Programming is done via the 6-pin ICSP header using an Arduino as ISP or USBasp programmer. The Arduino IDE supports ATtiny85 via the ATTinyCore board package.

## Programming Setup (Arduino IDE)

1. Install ATTinyCore board package
2. Select: **ATtiny85 @ 8MHz (internal)**
3. Use **Arduino as ISP** or **USBasp** as programmer
4. Burn bootloader, then upload sketch

## Bill of Materials (Summary)

| Component | Value | Qty |
|-----------|-------|-----|
| MCU | ATtiny85-20PU | 1 |
| DIP-8 Socket | — | 1 |
| Decoupling Cap | 100nF | 2 |
| Bulk Cap | 10µF | 1 |
| ICSP Header | 2×3, 2.54mm | 1 |
| Reset Button | Tactile | 1 |

## Fabrication

Gerber files are in `/Gerbers`, ready for JLCPCB, PCBWay, or similar.

## License

This project is licensed under the [CERN Open Hardware Licence Version 2 - Strongly Reciprocal (CERN OHL-S v2)](https://ohwr.org/cern_ohl_s_v2.txt).

## Author

**Abhi90808** — [GitHub Profile](https://github.com/Abhi90808)
