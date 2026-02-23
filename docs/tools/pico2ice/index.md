# pico2-ice

The pico2-ice is a development board from TinyVision.ai that combines a Raspberry Pi RP2350B microcontroller with a Lattice iCE40UP5K FPGA on a single compact PCB. It is the next-generation hardware platform for the Bitstream Evolution project, enabling on-board microcontroller-driven evolution and parallel evaluation across multiple boards via the [iCEFARM](../../projects/icefarm/hardware.md) system.

[:octicons-link-external-16: Official Documentation](https://pico2-ice.tinyvision.ai/){ .md-button .md-button--primary }
[:octicons-link-external-16: Purchase](https://tinyvision.ai/products/raspberry-pi-pico-2-development-board-with-fpga){ .md-button }
[:octicons-arrow-right-24: Hardware Setup Guide](../../projects/bitstream_evolution_pico2-ice/setup.md){ .md-button }

## Specifications

| Feature | Details |
| --- | --- |
| **FPGA** | iCE40UP5K — 5,280 LUTs, 1 Mbit SPRAM, 120 Kbit DPRAM, 8 multiplier blocks |
| **Microcontroller** | RP2350B — dual Arm Cortex-M33 + dual RISC-V Hazard3 cores |
| **External Memory** | 8 MB low-power qSPI SRAM |
| **Flash** | 4 MB SPI Flash (independent storage for FPGA and RP2350B) |
| **GPIO** | All RP2350 + 32 FPGA GPIO on 0.1" headers (Pmod-compatible) |
| **LEDs** | 2 RGB LEDs (one per processor) |
| **Buttons** | 2 pushbuttons |
| **PCB** | 4-layer with dedicated ground plane |

## Advantages Over the iCEstick

- **4x more logic** --- the UP5K provides 5,280 LUTs compared to the HX1K's 1,280 logic cells, offering significantly more resources for evolved circuits.
- **On-board microcontroller** --- the RP2350B could in principle run the evolutionary algorithm locally, eliminating the need for a separate host PC and external Arduino.
- **Programmable clock** --- the RP2350 supplies the FPGA clock, allowing software-controlled frequency adjustment.
- **Direct FPGA programming** --- the microcontroller can load bitstreams onto the iCE40UP5K, enabling streamlined evolutionary runs.
- **Array-friendly** --- the compact form factor and on-board MCU make it suitable for deploying multiple boards in the iCEFARM parallel evaluation system.

## Project Use

The pico2-ice is the hardware platform for the [Bitstream Evolution (Pico2-ICE)](../../projects/bitstream_evolution_pico2-ice/setup.md) project and the [iCEFARM](../../projects/icefarm/hardware.md) parallel evaluation system. Adopted in 2025 as part of an ARI-funded joint project between Vivum AI and Rose-Hulman Institute of Technology, it enables research into partial reconfiguration of FPGAs for autonomous control systems and larger-scale evolutionary experiments.
