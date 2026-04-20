# nextpnr

nextpnr is a vendor-neutral, timing-driven, open-source FPGA place-and-route tool developed by the YosysHQ team. It is the successor to arachne-pnr (now deprecated) and serves as the place-and-route stage in the fully open-source FPGA toolchain. In the Bitstream Evolution workflow, nextpnr is used to generate initial seed bitstreams from Verilog HDL designs, which then serve as starting points for evolutionary runs.

[:octicons-mark-github-16: GitHub Repository](https://github.com/YosysHQ/nextpnr){ .md-button .md-button--primary }

## Key Features

- **Timing-driven placement and routing** --- produces optimized initial configurations that serve as high-quality seed bitstreams for evolutionary experiments.
- **iCE40 architecture support** --- first-class support for Lattice iCE40 FPGAs via Project IceStorm's chip databases, directly targeting the same hardware used by Bitstream Evolution.
- **Retargetable architecture** --- supports multiple FPGA families beyond iCE40 (ECP5, Lattice Nexus, Gowin, and more).
- **Python scripting API** --- enables programmatic control of placement and routing, useful for generating or constraining seed designs.
- **Optional GUI** --- allows visual inspection of placed and routed designs.

## Role in the Toolchain

nextpnr sits between Yosys (synthesis) and IceStorm (bitstream packing):

```
Yosys (.v → .json) → nextpnr (.json → .asc) → icepack (.asc → .bin)
```

For EHW, nextpnr is primarily used to produce the initial seed bitstreams. The evolutionary algorithm then operates directly on the .asc (or .bin) representation, bypassing nextpnr entirely during evolution.

## Project Use

nextpnr generates the seed bitstreams that initialize evolutionary populations in the [Bitstream Evolution](../../projects/bitstream_evolution/index.md) project. While the evolutionary process itself does not use nextpnr (mutations operate directly on bitstream files), the quality of the initial seed can influence how quickly evolution discovers viable circuits.
