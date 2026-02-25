# Contributing as a Student

Evolvable hardware is an active area of undergraduate and graduate research. The combination of hands-on hardware, evolutionary algorithms, and open questions makes it well-suited for course projects, independent studies, and capstone work.

## What Students Have Done

Past and current student contributions have spanned software, hardware, and experimental research:

- **Software tooling** — Extending the [Bitstream Evolution](../projects/bitstream_evolution/index.md) toolkit with new fitness functions, analysis tools, and automation
- **Hardware platforms** — Porting the evolution framework to new FPGA boards (e.g., the [pico2-ice](../projects/bitstream_evolution_pico2-ice/index.md) platform)
- **Experiments** — Designing and running new experiments, such as the [Target Frequency Sweep](../research/experiments/target_frequency_study.md), [Fitness Sensitivity](../research/experiments/fitness_sensitivity.md), and [Transferability](../research/experiments/transferability.md) studies
- **Supporting tools** — Building utilities like the [iCE40 Floorplan Viewer](../tools/ice40_viewer/index.md), [iCE40 Memory Controller](../projects/ice40_memory_controller/index.md), and [PUFFs](../projects/puffs/index.md) testing framework

## How to Get Started

1. **Understand the basics** — Read [What Do I Need to Know?](../research/concepts/what_to_know.md) and [Concepts for Makers](../research/concepts/concepts_for_makers.md)
2. **Get hardware running** — Follow the setup guide for [pico2-ice](../projects/bitstream_evolution_pico2-ice/hardware_setup.md) (~$50) or [iCEstick](../projects/bitstream_evolution/hardware_setup.md) (~$190)
3. **Replicate an existing experiment** — Start with [Variance Maximization](../research/experiments/variance_maximization.md) and document your results
4. **Explore open questions** — Browse [Future Research Directions](../research/future_directions/index.md) for scoped project ideas
5. **Propose a variation** — New fitness functions, mutation strategies, or analysis methods are all good starting points
6. **Contribute your work** — Submit a pull request to the [BitstreamEvolution repo](https://github.com/evolvablehardware/BitstreamEvolution) or the [website repo](https://github.com/evolvablehardware/evolvablehardware.github.io)

## Project Scope Ideas

These are examples of project scopes that have worked well for students at different levels:

=== "Course Project (1 quarter / semester)"

    - Replicate 2–3 existing experiments and compare results
    - Implement a new fitness function and characterize its behavior
    - Port the toolkit to a new FPGA platform
    - Build a visualization or analysis tool for evolution data

=== "Independent Study (1–2 quarters)"

    - Design and execute a new experiment with statistical rigor
    - Investigate a specific [future research direction](../research/future_directions/index.md)
    - Contribute a significant feature to the software toolkit
    - Write up results suitable for a workshop or conference submission

=== "Capstone / Thesis"

    - Multi-experiment study addressing an open research question
    - New hardware platform design and validation
    - Comparative study across evolutionary strategies or FPGA architectures
    - Publication-ready research with formal analysis

## Mentorship

Interested in a guided research experience? [Contact us](../contact.md) with:

- Your background (year, major, relevant coursework)
- What interests you about evolvable hardware
- What kind of project you're looking for (hands-on, theoretical, software, etc.)
- Your timeline (course project, summer research, thesis, etc.)
