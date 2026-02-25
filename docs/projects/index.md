---
hide:
    - toc
---

# Projects

Explore the active projects in Evolvable Hardware research.

## Bitstream Evolution (iCEstick)

An open-source platform for intrinsic analog evolvable hardware research using the Lattice iCE40 HX1K FPGA on the iCEstick development board.

<div class="grid cards" markdown>

-   :material-wrench:{ .lg .middle } __Hardware Setup__

    ---

    Bill of materials, assembly instructions, and wiring guide for the iCEstick evaluation board.

    [:octicons-arrow-right-24: Setup Guide](./bitstream_evolution/hardware_setup.md)

-   :material-github:{ .lg .middle } __Software__

    ---

    The BitstreamEvolution toolkit — evolutionary algorithms, bitstream manipulation, and FPGA communication.

    [:octicons-arrow-right-24: GitHub Repository](https://github.com/evolvablehardware/BitstreamEvolution)

</div>

## Bitstream Evolution (pico2-ice)

Porting the Bitstream Evolution toolkit to the pico2-ice development board, enabling new hardware capabilities and parallel evaluation across multiple FPGAs.

<div class="grid cards" markdown>

-   :material-wrench:{ .lg .middle } __Hardware Setup__

    ---

    Setup instructions and troubleshooting for the pico2-ice development board.

    [:octicons-arrow-right-24: Setup Guide](./bitstream_evolution_pico2-ice/hardware_setup.md)

-   :material-github:{ .lg .middle } __Software__

    ---

    The pico2-ice port of the BitstreamEvolution toolkit with board-specific firmware and communication.

    [:octicons-arrow-right-24: GitHub Repository](https://github.com/evolvablehardware/BitstreamEvolutionPico2ice)

</div>

## iCEFARM

FPGA Array Resource Manager — a parallel evaluation system that distributes evolutionary runs across multiple pico2-ice boards simultaneously.

<div class="grid cards" markdown>

-   :material-wrench:{ .lg .middle } __Hardware Setup__

    ---

    Hardware configuration for deploying an array of pico2-ice boards for parallel FPGA evaluation.

    [:octicons-arrow-right-24: Setup Guide](./icefarm/hardware.md)

-   :material-github:{ .lg .middle } __Software__

    ---

    Job distribution and board management software for the iCEFARM parallel evaluation system.

    [:octicons-arrow-right-24: GitHub Repository](https://github.com/evolvablehardware/iCEFARM)

</div>

## iCE40 Memory Controller

A Verilog-based hardware project for reading and writing to Block RAM (BRAM) on iCE40 FPGAs, supporting both the HX1K and UP5K devices.

<div class="grid cards" markdown>

-   :material-information-outline:{ .lg .middle } __Overview__

    ---

    BRAM and SPRAM interfaces with UART communication and automated testbenches for iCE40 devices.

    [:octicons-arrow-right-24: Learn More](./ice40_memory_controller/index.md)

-   :material-github:{ .lg .middle } __Software__

    ---

    Verilog memory controller with Python host scripts for pico-ice and pico2-ice boards.

    [:octicons-arrow-right-24: GitHub Repository](https://github.com/evolvablehardware/ice40_memory_controller)

</div>

## PUFFs

PyTest Unified Framework for FPGA Simulation — a testing framework combining pytest with cocotb for hardware design verification.

<div class="grid cards" markdown>

-   :material-information-outline:{ .lg .middle } __Overview__

    ---

    Unified testing environment for FPGA designs using familiar Python workflows with cocotb simulation.

    [:octicons-arrow-right-24: Learn More](./puffs/index.md)

-   :material-github:{ .lg .middle } __Software__

    ---

    Python-based testing framework with gold models, unit tests, and RTL design verification.

    [:octicons-arrow-right-24: GitHub Repository](https://github.com/evolvablehardware/PUFFS)

</div>
