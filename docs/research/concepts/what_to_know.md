---
hide:
  - toc
---

# What Do I Need to Know?

Evolvable hardware sits at the intersection of several fields, but you don't need to be an expert in all of them to get started. Below is an honest breakdown of what background helps, what's optional, and what you can pick up along the way.

## Enough to Get Started

!!! tip "The Minimum Viable Background"
    If you have these three things, you can run your first evolution today:

    - **Basic programming (Python)** — The [Bitstream Evolution](../../projects/bitstream_evolution/index.md) toolkit is Python-based. If you can write a loop, call a function, and read a traceback, you're ready.
    - **Comfort with the command line** — You'll need to navigate directories, run scripts, and occasionally install packages. Linux/macOS terminal or WSL on Windows.
    - **Curiosity about hardware** — You don't need prior FPGA experience, but you should be willing to plug things in, read a wiring diagram, and troubleshoot connections.

## Helpful but Not Required

These topics will deepen your understanding but aren't blockers for getting started:

| Topic | Why It Helps | Where to Learn |
|---|---|---|
| **Digital logic basics** | Understand what FPGAs are doing at the gate level | Any intro digital design course or textbook |
| **Evolutionary algorithms** | Understand how the optimization works | [Evolutionary Computation](evolutionary_computation.md) concept page |
| **FPGA architecture** | Understand LUTs, routing, and bitstreams | [Reconfigurable Hardware](reconfigurable_hardware.md) concept page |
| **Signal processing fundamentals** | Interpret oscilloscope traces and frequency content | Helpful for experiments beyond variance maximization |
| **Basic electronics** | Voltage, current, ADC readings, breadboard wiring | Needed for hardware setup |

## For Deeper Research

If you're pursuing evolvable hardware as a research topic (thesis, independent study, publication), these areas become more relevant:

- **Dynamical systems & control theory** — For understanding evolved circuit behavior as continuous dynamical processes. See [Dynamical Systems](dynamical_systems.md).
- **Neuroscience-inspired models** — CTRNNs, LTCs, and other models that connect to how evolved circuits can implement neural-like computation. See [CTRNNs](ctrnns.md) and [LTC Networks](ltc_nns.md).
- **Statistics & experimental design** — For designing rigorous experiments, analyzing fitness curves, and drawing valid conclusions across stochastic runs.
- **Verilog/VHDL** — For understanding or modifying the hardware description layer beneath the bitstream.

## Don't Worry About

- **You don't need an EE degree.** Many contributors come from CS, math, or biology backgrounds.
- **You don't need to understand every concept page.** The [advanced topics](#) are there for researchers going deep — they're not prerequisites for running experiments.
- **You don't need expensive equipment.** A [$50 pico2-ice setup](../../projects/bitstream_evolution_pico2-ice/hardware_setup.md) is enough to start.

## Recommended Path by Background

=== "CS / Software Engineering"

    You already have the programming skills. Focus on:

    1. [Concepts for Makers](concepts_for_makers.md) — Quick conceptual grounding
    2. [Hardware Setup](../../projects/bitstream_evolution/hardware_setup.md) — The unfamiliar part for most CS students
    3. [Variance Maximization](../experiments/variance_maximization.md) — Your first experiment

=== "Electrical / Computer Engineering"

    You already understand the hardware. Focus on:

    1. [Evolutionary Computation](evolutionary_computation.md) — How the optimization works
    2. [Software Setup](../../projects/bitstream_evolution/software_setup.md) — Python environment and toolchain
    3. [Pulse Oscillation](../experiments/pulse_oscillation.md) — Connects to familiar signal concepts

=== "Biology / Other Sciences"

    The biological metaphors in evolvable hardware are real, not just marketing. Focus on:

    1. [Biologically Inspired Computing](bio_inspired_computing.md) — See the connections to your field
    2. [Concepts for Makers](concepts_for_makers.md) — Practical grounding without assuming hardware background
    3. [Variance Maximization](../experiments/variance_maximization.md) — See evolution happen in real time
