# Weather Station Rain Gauge (Pluviometer) V2
![image-removebg-preview (6)](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/1f387b13-7fc2-4eb4-ab38-0ad2a61a9cc9)

This rain gauge is designed to measure rainfall amount and includes:

- A 3 mm diameter, 30 mm long steel or aluminum rod.
- A 1.8 × 7 mm reed switch.
- A 4 × 2 mm round neodymium magnet.
- Two M3 × 6 mm screws and four screws or bolts to fix the base to the support.
- Wires and connectors of choice to connect to the reed switch.
- A drop of glue to secure the magnet.

The rain gauge was 3D printed using the following files:  
[Pluviometer Gcode's.zip](https://github.com/user-attachments/files/15755285/Pluviometro.Gcode.s.zip)

The funnel is attached to the base through a printed thread, using Aubend's Poor Man’s OpenSCAD thread library  
([https://www.thingiverse.com/thing:8796](https://www.thingiverse.com/thing:8796)).  
The small tower behind the sensor is used to secure the output wire with a cable tie.

## Printing Settings
- Printer: Prusa i3 MK2S  
- No brim or supports required  
- Resolution: 0.25  
- Infill: 20%  
- Filament brand: Grossiste3D  
- Filament color: White  
- Filament material: PLA  

**Note:** The funnel must be printed upside down. Make sure to rotate it 180° in the slicing software (do not mirror it) so that the thread works correctly. An STL file for a reed switch pin-bending tool is also included.

## Connections
| Rain Gauge | ESP WROOM 32 | ESP32 Pin Number |
|:----------:|:------------:|:---------------:|
|     VCC    |      5V      |       5V        |
|     GND    |      GND     |       GND       |
|     DAT    |     GPIO     |     GPIO13      |

## Results
![WhatsApp Image from 2024-06-18 at 14:07:22_d13f54c4](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/7b3a73ce-3cfa-42ea-844d-313018212cbe)
