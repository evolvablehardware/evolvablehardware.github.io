---
hide:
    - toc
---

# Experiments

This section highlights specific experiments that have been conducted using the Bitstream Evolution toolkit. Each experiment showcases different aspects of evolvable hardware and provides insights into the capabilities and performance of the system. We begin with basic experiments that were conducted in 2021 and move towards more systematic experiments conducted since then. Most of these experiments can be reproduced using the open-source [Bitstream Evolution Toolkit](../../projects/bitstream_evolution/index.md).

We recommend starting with the [Variance Maximization](./variance_maximization.md) experiment, which serves as a "Hello World" for evolvable hardware.



| Experiment | Difficulty | Description |
|---|---|---|
| [Variance Maximization](./variance_maximization.md) | :material-circle:{ .beginner } Beginner | Evolve a circuit to maximize output signal variance |
| [Pulse Oscillation](./pulse_oscillation.md) | :material-circle:{ .beginner } Beginner | Evolve a circuit to oscillate at a target frequency |
| [Target Frequency Sweep](./target_frequency_study.md) | :material-circle:{ .intermediate } Intermediate | Benchmark oscillatory evolution across a range of frequencies |
| [Fitness Sensitivity](./fitness_sensitivity.md) | :material-circle:{ .intermediate } Intermediate | Analyze robustness of evolved circuits under prolonged evaluation |
| [Tone Discriminator](./tone_discriminator.md) | :material-circle:{ .advanced } Advanced | Evolve circuits to discriminate between input frequencies |
| [Transferability](./transferability.md) | :material-circle:{ .advanced } Advanced | Study transferability of evolved circuits across FPGA hardware |

<div class="grid cards" markdown>

-   :material-circle:{ .beginner } __Variance Maximization__

    ---

    Evolve a physical circuit on an FPGA to maximize the circuit's output variance (i.e., maximize noise). *Start here.*

    [:octicons-arrow-right-24: Learn More](./variance_maximization.md)

-   :material-circle:{ .beginner } __Pulse Oscillation__

    ---

    Evolve a circuit to oscillate at a target frequency (e.g., 1 kHz, 10 kHz, etc.).

    [:octicons-arrow-right-24: Learn More](./pulse_oscillation.md)

-   :material-circle:{ .intermediate } __Target Frequency Sweep (2025)__

    ---

    Benchmark how well circuits can evolve oscillatory behavior across a range of target frequencies.

    [:octicons-arrow-right-24: Learn More](./target_frequency_study.md)

-   :material-circle:{ .intermediate } __Fitness Sensitivity (2025)__

    ---

    Analyze the sensitivity and robustness of evolved circuits under prolonged evaluation.

    [:octicons-arrow-right-24: Learn More](./fitness_sensitivity.md)

-   :material-circle:{ .advanced } __Tone Discriminator__

    ---

    Evolve circuits to discriminate between different input frequencies. *Long-horizon objective, currently a work in progress.*

    [:octicons-arrow-right-24: Learn More](./tone_discriminator.md)

-   :material-circle:{ .advanced } __Transferability (2025)__

    ---

    Study the transferability of evolved circuits across different FPGA hardware.

    [:octicons-arrow-right-24: Learn More](./transferability.md)

</div>
