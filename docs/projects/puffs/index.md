---
hide:
  - toc
---

# PUFFS

**PyTest Unified Framework for FPGA Simulation** — a Python-based testing framework that combines pytest with cocotb simulation for verifying hardware designs.

[:octicons-mark-github-16: evolvablehardware/PUFFS]({{config.extra.link.project.PUFFS.repo}}){ .md-button }

## Overview

PUFFS provides a unified testing environment for FPGA designs by integrating pytest's testing conventions with cocotb's hardware simulation capabilities. This allows hardware designs to be verified using familiar Python testing workflows, with channel-level abstractions enabling Python-based testbench interactions.

## Key Features

- **pytest integration** for conventional testing workflows
- **cocotb simulation** for Verilog/SystemVerilog designs
- **Channel-level abstractions** enabling Python-based testbench interactions
- **Gold model support** with Python reference implementations alongside RTL

## Project Structure

- `src/models/` — Python gold models (reference implementations)
- `src/unit/` — Unit tests
- `src/verilog/` — RTL designs

## Related Projects

- [Bitstream Evolution (iCEstick)](../bitstream_evolution/index.md)
- [Bitstream Evolution (pico2-ice)](../bitstream_evolution_pico2-ice/index.md)
