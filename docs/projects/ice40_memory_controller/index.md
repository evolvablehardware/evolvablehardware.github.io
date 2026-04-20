---
hide:
  - toc
---

# iCE40 Memory Controller

A Verilog-based hardware project for reading and writing to Block RAM (BRAM) on iCE40 FPGAs. The memory controller supports both the HX1K and UP5K devices, with SPRAM support for the UP5K.

[:octicons-mark-github-16: evolvablehardware/ice40_memory_controller]({{config.extra.link.project.iCE_memory_controller.repo}}){ .md-button }

## Overview

The memory controller provides a standardized interface for BRAM operations on iCE40 devices, enabling reliable data storage and retrieval during evolutionary experiments. It includes Python host-side communication via UART and a shell interface for testing.

## Key Features

- **BRAM read/write** for iCE40 HX1K and UP5K devices
- **SPRAM support** for the UP5K
- **UART communication** with Python host scripts
- **Automated testbench** utilities for verification
- **Compatible** with pico-ice and pico2-ice development boards

## Related Projects

- [Bitstream Evolution (pico2-ice)](../bitstream_evolution_pico2-ice/index.md)
