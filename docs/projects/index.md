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

    [:octicons-arrow-right-24: Setup Guide](./bitstream_evolution/setup.md)

-   :material-github:{ .lg .middle } __Software__

    ---

    The BitstreamEvolution toolkit — evolutionary algorithms, bitstream manipulation, and FPGA communication.

    [:octicons-arrow-right-24: GitHub Repository](https://github.com/evolvablehardware/BitstreamEvolution)

</div>

## Bitstream Evolution (Pico2-ICE)

Porting the Bitstream Evolution toolkit to the Pico2-ICE development board, enabling new hardware capabilities and parallel evaluation across multiple FPGAs.

<div class="grid cards" markdown>

-   :material-wrench:{ .lg .middle } __Hardware Setup__

    ---

    Setup instructions and troubleshooting for the Pico2-ICE development board.

    [:octicons-arrow-right-24: Setup Guide](./bitstream_evolution_pico2-ice/setup.md)

-   :material-github:{ .lg .middle } __Software__

    ---

    The Pico2-ICE port of the BitstreamEvolution toolkit with board-specific firmware and communication.

    [:octicons-arrow-right-24: GitHub Repository](https://github.com/evolvablehardware/BitstreamEvolutionPico2ice)

</div>

## iCEFARM

FPGA Array Resource Manager — a parallel evaluation system that distributes evolutionary runs across multiple Pico2-ICE boards simultaneously.

<div class="grid cards" markdown>

-   :material-wrench:{ .lg .middle } __Hardware Setup__

    ---

    Hardware configuration for deploying an array of Pico2-ICE boards for parallel FPGA evaluation.

    [:octicons-arrow-right-24: Setup Guide](./icefarm/hardware.md)

-   :material-github:{ .lg .middle } __Software__

    ---

    Job distribution and board management software for the iCEFARM parallel evaluation system.

    [:octicons-arrow-right-24: GitHub Repository](https://github.com/evolvablehardware/iCEFARM)

</div>
