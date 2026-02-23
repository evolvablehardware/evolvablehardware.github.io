# Tools

This section provides background on the key software tools and hardware platforms used in evolvable hardware research. Each tool page explains what it is, how it fits into the workflow, and how it is used in our projects.

## Software Tools

<div class="grid cards" markdown>

-   :material-snowflake:{ .lg .middle } __Project IceStorm__

    ---

    Reverse-engineered bitstream documentation and tools for Lattice iCE40 FPGAs. The foundation that makes bitstream-level evolution possible.

    [:octicons-arrow-right-24: Learn More](./project_icestorm/index.md)

-   :material-routes:{ .lg .middle } __nextpnr__

    ---

    Open-source FPGA place-and-route tool. Generates seed bitstreams that initialize evolutionary populations.

    [:octicons-arrow-right-24: Learn More](./nextpnr/index.md)

-   :material-application-braces:{ .lg .middle } __Yosys__

    ---

    Open-source HDL synthesis framework. Converts Verilog designs into netlists as the first stage of the FPGA toolchain.

    [:octicons-arrow-right-24: Learn More](./yosys/index.md)

</div>

## Hardware Platforms

<div class="grid cards" markdown>

-   :material-chip:{ .lg .middle } __iCEstick (HX1K)__

    ---

    The original Lattice iCE40-HX1K development board used for Bitstream Evolution experiments from 2018 to 2025.

    [:octicons-arrow-right-24: Learn More](./icestick/index.md)

-   :material-developer-board:{ .lg .middle } __pico2-ice (UP5K)__

    ---

    Next-generation board combining an RP2350B microcontroller with an iCE40UP5K FPGA for on-board evolution and parallel evaluation.

    [:octicons-arrow-right-24: Learn More](./pico2ice/index.md)

-   :material-memory:{ .lg .middle } __Arduino Nano__

    ---

    Compact ATmega328P microcontroller used for fitness evaluation in the iCEstick Bitstream Evolution hardware setup.

    [:octicons-arrow-right-24: Learn More](./arduino_nano/index.md)

</div>
