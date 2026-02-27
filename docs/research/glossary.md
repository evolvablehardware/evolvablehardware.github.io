---
hide:
  - toc
---

# Glossary

Key terms used throughout this site. Terms are grouped by topic for easier navigation.

## Hardware & FPGAs

**FPGA (Field Programmable Gate Array)**
:   A reconfigurable integrated circuit whose logic and routing can be reprogrammed after manufacturing. FPGAs are the primary substrate for intrinsic evolvable hardware experiments.

**Bitstream**
:   The binary configuration file (composed of 1s and 0s) that programs an FPGA's logic cells, routing interconnects, and I/O blocks. In evolvable hardware, the bitstream *is* the genotype — the thing that evolves.

**LUT (Look-Up Table)**
:   The basic programmable logic element inside an FPGA. A k-input LUT can implement any Boolean function of k variables by storing the truth table in SRAM.

**CLB (Configurable Logic Block)**
:   A higher-level FPGA building block containing one or more LUTs, flip-flops, and local routing. CLBs are the repeated tiles that make up the FPGA fabric.

**Reconfiguration**
:   The process of loading a new bitstream onto an FPGA to change its function. Full reconfiguration replaces the entire design; partial reconfiguration changes only a region.

**iCE40**
:   A family of low-power (hence 'ice' in the name) FPGAs by Lattice Semiconductor. The iCE40 HX1K (on the iCEstick) and iCE40 UP5K (on the pico2-ice) are the primary platforms used in this project.

**iCEstick**
:   The Lattice iCEstick Evaluation Kit — a USB-form-factor development board with an iCE40 HX1K FPGA. One of the two supported hardware platforms for Bitstream Evolution (~$190).

**pico2-ice**
:   A compact development board combining an RP2350 microcontroller with an iCE40 UP5K FPGA. The lower-cost hardware platform for Bitstream Evolution (~$50).

## Evolution & Optimization

**Intrinsic Evolution**
:   Evolution performed directly on physical hardware, where each candidate circuit is configured on a real FPGA and its behavior is measured in the physical world. This exploits device-specific characteristics including analog effects, manufacturing variation, and parasitic properties.

**Extrinsic Evolution**
:   Evolution performed in simulation, where candidate circuits are evaluated in a software model. Results may optionally be transferred to physical hardware afterward.

**Fitness Function**
:   The objective function that evaluates how well a candidate circuit meets the design goal. In Bitstream Evolution, fitness is computed from real analog measurements (e.g., ADC samples) taken from the physical FPGA.

**Genetic Algorithm (GA)**
:   An optimization method inspired by natural selection that maintains a population of candidate solutions, selects the fittest, and produces new candidates through crossover and mutation.

**Genotype**
:   The encoded representation of a candidate solution. In evolvable hardware, the genotype is the bitstream — the binary configuration of the FPGA.

**Phenotype**
:   The expressed behavior of a candidate solution. In evolvable hardware, the phenotype is the resulting circuit's electrical behavior — the analog signals it produces.

**Mutation**
:   A genetic operator that introduces random changes to a candidate's genotype. In bitstream evolution, this means flipping bits in the FPGA configuration file.

**Crossover**
:   A genetic operator that combines portions of two parent genotypes to produce offspring. In bitstream evolution, this swaps segments of two bitstreams.

**Population**
:   The set of candidate solutions maintained during an evolutionary run. Typical population sizes in Bitstream Evolution experiments range from 10 to 50 individuals.

**Generation**
:   One cycle of the evolutionary loop: evaluate all candidates, select parents, produce offspring through crossover and mutation, and replace the population.

## Experiments & Analysis

**Variance Maximization**
:   The simplest evolvable hardware experiment — evolving a circuit to maximize the variance (dynamic range) of its analog output signal. Serves as the "Hello World" for the field.

**Pulse Oscillation**
:   An experiment that evolves a circuit to produce a periodic output signal at a target frequency.

**Tone Discriminator**
:   An advanced experiment that evolves circuits to produce different outputs depending on the frequency of an input signal.

**Transferability**
:   The degree to which an evolved circuit maintains its functionality when moved to a different physical FPGA chip. A key open question in evolvable hardware.

**Robustness**
:   The ability of an evolved circuit to maintain its functionality under varying conditions (temperature, voltage, time, etc.).

## Infrastructure

**Bitstream Evolution**
:   The open-source Python toolkit developed by this research group for conducting intrinsic evolvable hardware experiments on iCE40 FPGAs.

**iCEFARM**
:   iCE40 FPGA Array Resource Manager — infrastructure for providing remote access to physical FPGA hardware for evolution experiments.

**Project IceStorm**
:   The open-source reverse-engineered toolchain for Lattice iCE40 FPGAs, including `icepack`/`iceunpack` for bitstream manipulation. Essential for bitstream-level evolution since it provides access to the raw configuration format.

**ADC (Analog-to-Digital Converter)**
:   A device that converts continuous analog voltage signals into discrete digital values. Used to measure the output behavior of evolved FPGA circuits for fitness evaluation.
