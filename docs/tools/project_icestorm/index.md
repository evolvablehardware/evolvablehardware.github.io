# Project IceStorm

Project IceStorm is a reverse-engineering effort that fully documents the bitstream format of Lattice iCE40 FPGAs and provides a suite of open-source tools for analyzing, creating, and programming bitstream files. Created by Claire Wolf and Mathias Lasser, it was first presented at the 32nd Chaos Communication Congress in Hamburg, Germany in 2015.

For evolvable hardware research, Project IceStorm is the foundational enabler --- it is the reason intrinsic analog EHW on FPGAs is possible again after the discontinuation of the Xilinx XC6200 series. The fully documented bitstream allows the Bitstream Evolution toolkit to read, mutate, and write bitstreams programmatically at the individual bit level.

[:octicons-link-external-16: Official Website](http://www.clifford.at/icestorm/){ .md-button .md-button--primary }
[:octicons-mark-github-16: GitHub Repository](https://github.com/YosysHQ/icestorm){ .md-button }

## Key Tools

| Tool | Description |
| --- | --- |
| **icepack / iceunpack** | Convert between human-readable ASCII (.asc) and binary bitstream (.bin) formats. Critical for EHW — enables programmatic mutation of bitstreams. |
| **iceprog** | Programs bitstream files directly to iCE40 FPGAs over USB for rapid iterative evaluation. |
| **icetime** | Performs timing analysis on bitstreams, estimating propagation delays. |
| **icebox** | Python library for bitstream analysis; useful for understanding the mapping between bitstream bits and physical FPGA resources. |
| **icepll** | Configures PLL (phase-locked loop) parameters. |
| **icebram** | Handles Block RAM content manipulation within bitstreams. |
| **icemulti** | Manages multi-image bitstream configurations. |

## Role in the Toolchain

Project IceStorm sits at the end of the open-source FPGA synthesis flow and is the entry point for evolutionary manipulation:

```
Yosys (synthesis) → nextpnr (place & route) → IceStorm/icepack (bitstream generation)
                                                        │
                                                   Seed Bitstream (.asc / .bin)
                                                        │
                                              Evolutionary Algorithm
                                         (mutate .asc via iceunpack/icepack)
                                                        │
                                                   iceprog → FPGA
                                                        │
                                                 Fitness Evaluation
```

## Supported Chips

Project IceStorm documents the complete bitstream format for:

- iCE40 LP/HX 1K, 4K, 8K
- iCE40 UltraPlus (UP5K) — including DSPs, oscillators, RGB LED drivers, and SPRAM

## Project Use

The **icepack/iceunpack** tools are essential to the Bitstream Evolution evolutionary loop: bitstreams are unpacked to ASCII, mutated by the evolutionary algorithm, repacked to binary, and then loaded onto the FPGA via **iceprog** for fitness evaluation. The **icebox** tools are also used for analyzing the structure of evolved circuits.
