# iCEstick Evaluation Kit

The Lattice iCEstick Evaluation Kit (ICE40HX1K-STICK-EVN) is a low-cost, USB thumb-drive form factor development board featuring the iCE40-HX1K FPGA. It is the original hardware platform used in the Bitstream Evolution project, serving as the target FPGA for intrinsic analog evolutionary experiments from 2018 through 2025.

[:octicons-link-external-16: Lattice Semiconductor](https://www.latticesemi.com/icestick){ .md-button .md-button--primary }
[:octicons-arrow-right-24: Hardware Setup Guide](../../projects/bitstream_evolution/bitstream_evolution/setup.md){ .md-button }

## Specifications

| Feature | Details |
| --- | --- |
| **FPGA** | iCE40-HX1K — 1,280 logic cells, 64 Kbit block RAM |
| **Configuration** | SRAM-based (unlimited reprogramming, no wear-out) |
| **USB Interface** | FTDI FT2232H — dual-channel for programming and UART |
| **Digital I/O** | 16 pins, LVCMOS/LVTTL 3.3V on 0.1" headers |
| **Pmod Connector** | 2x6 standard peripheral connector |
| **LEDs** | 5 onboard |
| **Power** | USB-powered, no external supply needed |
| **Form Factor** | USB thumb-drive |

## Why the iCEstick for EHW

- **SRAM-based configuration** --- the iCE40 can be reprogrammed on the fly without wear-out concerns, which is critical for EHW where thousands of bitstreams may be loaded during a single evolutionary run.
- **Fully documented bitstream** --- via [Project IceStorm](../project_icestorm/index.md), every bit in the configuration file maps to a known physical resource.
- **Low cost** --- originally ~$25, making it one of the most affordable FPGA development boards and lowering the barrier to entry for EHW research.
- **FTDI dual-channel USB** --- allows the evolutionary algorithm on the host to program candidate bitstreams and read fitness measurements over a single USB connection.

## Project Use

The iCEstick was the hardware platform for all published Bitstream Evolution work from inception (~2018) through the 2025 IEEE Access paper. In the experimental setup, the iCEstick is paired with an Arduino Nano-compatible microcontroller which reads the analog output of the FPGA and reports fitness values back to the host PC running the evolutionary algorithm.

See the [hardware setup guide](../../projects/bitstream_evolution/bitstream_evolution/setup.md) for assembly instructions and wiring diagrams.
