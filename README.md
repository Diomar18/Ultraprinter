# Ultraprinter
Custom CoreXY 3D printer — 430×360×400mm, welded steel frame, integrated BMG direct drive. Designed from scratch since 2021.
Custom CoreXY 3D printer designed from scratch by Diomar Quesada, starting November 2021 at age 17. 84 design versions documented in Fusion 360 over 5 years.

## Specifications

| Parameter | Value |
|---|---|
| Kinematics | CoreXY |
| Build volume | 430 × 360 × 400 mm (61,920 cm³) |
| Frame | Custom welded steel tubular profiles |
| Extruder | Direct drive — BMG integrated into carriage |
| Hotend | E3D V6 Volcano, 0.6mm nozzle, max 300°C |
| Bed | 220V AC silicone heater with SSR, max 120°C |
| Control board | BTT SKR V1.x + TMC2209 UART |
| Firmware | Klipper on BTT Pi 1.2 |
| Print speed | 200–300 mm/s |
| Materials | PLA, PETG, ABS/ASA, TPU |

## Development history

Started November 2021 (Fusion 360 V1) — current version V84.
Three complete extruder redesigns over 5 years.
Designed empirically before formal engineering education.

## Design decisions

### Welded steel frame
Started as a budget decision — structural steel is cheaper than aluminum extrusion locally. Turned out to be technically superior: monolithic structure with no joints to loosen from vibration.

### Integrated BMG direct drive
BMG gears extracted and integrated directly into the carriage body. No external housing, no extra mounting bolts. Reduces moving mass while preserving BMG gear reduction ratio (50:17).

### Single motor Z-axis
One NEMA 17 drives four T8 lead screws simultaneously via closed GT2 belt loop (16T motor pulley → 4× 30T screw pulleys). Self-locking by reduction ratio — no Z-drop without power.

### 220V AC bed with SSR
Silicone heater running on mains voltage controlled by SSR relay. Reaches 120°C easily — standard 24V beds struggle with this build volume.

## Repository contents

- `/CAD` — STEP file of full assembly (Fusion 360 v77)
- `/PrintedParts` — STL files for all custom printed components
- `/Config` — Klipper printer.cfg with annotations
- `/Docs` — BOM, wiring notes, design decisions
- `/Images` — Render and development history screenshots

## Known issues & planned upgrades

- Z-wobble from threaded rods → upgrade to T8 lead screws or ballscrews
- Smooth rods → MGN linear rails
- Standard hotend → high-flow hotend
- Drivers → TMC2209/TMC5160 silent drivers

## License

MIT License — see LICENSE file.

## Author

Diomar Sergio Quesada Aldazabal  
Mechanical Engineering student — Universidad Nacional de Ingeniería, Lima, Peru  
Zenodo DOI: [10.5281/zenodo.19129317](https://doi.org/10.5281/zenodo.19129317)  
Hackaday: [hackaday.io/Diomar](https://hackaday.io/Diomar)
