# Yosys

Yosys (Yosys Open SYnthesis Suite) is a free and open-source framework for RTL synthesis, primarily targeting Verilog-2005 designs. It converts hardware description language (HDL) code into technology-mapped gate-level netlists and serves as the synthesis front-end in the fully open-source iCE40 FPGA toolchain. Yosys was created by Claire Wolf, who also created Project IceStorm.

In the Bitstream Evolution workflow, Yosys is invoked with its `synth_ice40` command to synthesize Verilog source files into JSON netlists, which are then placed, routed, and packed into the seed bitstreams that the evolutionary algorithm subsequently mutates.

[:octicons-link-external-16: Official Website](https://yosyshq.net/yosys/){ .md-button .md-button--primary }
[:octicons-mark-github-16: GitHub Repository](https://github.com/YosysHQ/yosys){ .md-button }

## Key Features

- **`synth_ice40` command** --- a built-in synthesis flow specifically targeting Lattice iCE40 FPGAs. Runs a full pipeline: Verilog parsing, hierarchy resolution, process conversion, flattening, FSM extraction, memory mapping, technology mapping to iCE40 primitives, and optimization.
- **Multiple output formats** --- emits BLIF, EDIF, or JSON netlists. The JSON output is consumed by nextpnr for place-and-route.
- **Scriptable synthesis passes** --- synthesis is composed of modular, composable passes that can be scripted and customized, useful for constraining or modifying the synthesis process.
- **Broad FPGA target support** --- ships with mature flows for iCE40, Lattice ECP5, and Xilinx 7-Series, with experimental support for others.
- **Formal verification** --- supports formal equivalence checking, SAT solving, and circuit analysis, which could be valuable for analyzing evolved circuits.
- **No vendor tools required** --- combined with nextpnr and Project IceStorm, Yosys enables a completely vendor-free Verilog-to-bitstream flow.

## Role in the Toolchain

Yosys is the first stage of the open-source FPGA synthesis flow:

```
Yosys (.v → .json) → nextpnr (.json → .asc) → icepack (.asc → .bin)
```

A typical invocation for iCE40 synthesis:

```bash
yosys -p "synth_ice40 -json output.json" design.v
```

## Project Use

Yosys generates the seed bitstreams that initialize evolutionary populations in the [Bitstream Evolution](../../projects/bitstream_evolution/setup.md) project. While the evolutionary process itself operates directly on bitstream files (bypassing Yosys entirely), the quality of the initial synthesized design can influence the starting point of evolution.
