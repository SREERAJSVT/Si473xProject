# SI4732 and Raspberry Pi Pico Radio Project

## Overview

This project is a radio receiver built using the **SI4732-A10-GS** IC and controlled by the **Raspberry Pi Pico**. The design includes a custom PCB created in **KiCad**, with all necessary Gerber files and 3D designs provided for manufacturing and assembly.

### Features:
- **SI4732-A10-GS**: A highly integrated IC for AM/FM/SW/LW radio reception.
- **Raspberry Pi Pico**: A versatile microcontroller serving as the main processor for controlling the SI4732 IC.
- Custom **PCB** with all components required for signal reception and processing.
- Breakout boards for testing and experimentation, designed for easy integration with breadboards.

## Project Structure

The project files are organized as follows:

- **Gerber Files**: These files are necessary for PCB fabrication. They contain information for each layer of the PCB, including copper traces, solder mask, and silkscreen layers.
- **3D Models**: 3D models of the PCB and components are included for visualization and verification before production.
- **Breakout Board Designs**: Schematics and PCB designs for breakout boards that allow easy testing on a breadboard.
- **BOM (Bill of Materials)**: The list of all components required for the project, including reference designators, values, footprints, and quantities.

## Images

### PCB Design and 3D Models
![3D PCB Design](https://github.com/user-attachments/assets/424be22d-f024-4497-952e-059343f89fda)

### Breakout Board for Testing
![Breadboard Breakout](https://github.com/user-attachments/assets/44f736cd-cd30-4c3b-8920-d6db453d7e3e)

### Final Radio Board Using Raspberry Pi Pico
![Final Radio Board](https://github.com/user-attachments/assets/e37367b4-a990-41a8-8ce4-c47739ac6233)
![Final Radio Board 2](https://github.com/user-attachments/assets/71ce5a44-2c63-4fc8-8a37-ab279e97686c)
![Final Radio Board 3](https://github.com/user-attachments/assets/716aeb7f-6ff4-4b4e-a1e4-f71169a73b50)

## Components

### Breakout for Experiments

| Reference | Value | Footprint | Qty |
|-----------|-------|-----------|-----|
| C2        | 1nF   | Capacitor_SMD:C_0805_2012Metric_Pad1.18x1.45mm_HandSolder | 1   |
| C3, C4    | 22pF  | Capacitor_SMD:C_0805_2012Metric_Pad1.18x1.45mm_HandSolder | 2   |
| R1        | 2.2K  | Resistor_SMD:R_0805_2012Metric_Pad1.20x1.40mm_HandSolder  | 1   |
| Y1        | 32.768K | Crystal:Crystal_C38-LF_D3.0mm_L8.0mm_Horizontal | 1 |
| C1        | 470nF | Capacitor_SMD:C_0805_2012Metric_Pad1.18x1.45mm_HandSolder | 1   |
| IC1       | SI4732-A10-GS | Package_SO:SOIC-16_3.9x9.9mm_P1.27mm | 1 |
| ANT?      | Conn_01x03_Pin | Connector_PinHeader_2.54mm:PinHeader_1x03_P2.54mm_Vertical | 1 |
| J2, J3    | Conn_01x05_Pin | Connector_PinHeader_2.54mm:PinHeader_1x05_P2.54mm_Vertical | 2 |
| J4, J5    | SMA_CONNECTOR | TestPoint:TestPoint_2Pads_Pitch2.54mm_Drill0.8mm | 2 |
| L1        | 180-450uH | Inductor_THT:L_Axial_L5.3mm_D2.2mm_P10.16mm_Horizontal_Vishay_IM-1 | 1 |

### Final Radio Board

- **Raspberry Pi Pico**: Serves as the controller for the SI4732-A10-GS.
- **SI4732-A10-GS**: The main IC for radio reception.
- **Passives**: Capacitors, resistors, and inductors necessary for the radio circuit to function correctly.
- **Connectors**: Headers for connecting the Raspberry Pi Pico and external antennas.
- **SMA Connectors**: Used for connecting external antennas for different radio bands.

## Assembly Instructions

1. **PCB Fabrication**: Use the provided Gerber files to manufacture the PCB. Ensure that the PCB manufacturer follows the specifications in the design files.
2. **Component Soldering**: Solder all the SMD and through-hole components onto the PCB following the BOM and placement files. Make sure to handle the IC and other sensitive components with care to avoid ESD damage.
3. **Testing**: Once the PCB is assembled, use the breakout boards for initial testing. Verify the operation of the SI4732 IC by checking signal reception on various radio bands.
4. **Final Integration**: Mount the Raspberry Pi Pico onto the main PCB and connect the necessary components, including antennas and power supply.

## Usage

- **Software Setup**: Load the radio control software onto the Raspberry Pi Pico. This software should include code for communicating with the SI4732 IC and handling radio signals.
- **Operation**: Use the Raspberry Pi Pico to tune into different radio stations by adjusting the frequency settings in the software. The radio signal can be outputted to speakers or headphones connected to the appropriate jacks.

## License

This project is open-source and released under the [MIT License](LICENSE).

## Contribution

Feel free to contribute to this project by submitting pull requests or reporting issues.

## Acknowledgements

Special thanks to the open-source community for providing tools like KiCad and Raspberry Pi Pico, which made this project possible.

---

Let me know if you need further adjustments!
