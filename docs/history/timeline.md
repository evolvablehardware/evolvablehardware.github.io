# Timeline of Evolvable Hardware

- [**1991 – Early Vision**](historical_review.md#inception-and-history): Hugo de Garis describes embryological electronics and suggests that complex circuits could be "grown" through evolutionary search, laying the conceptual groundwork for evolvable hardware.

- [**1993 – Field Named**](historical_review.md#inception-and-history): De Garis and Tetsuya Higuchi formally coin evolvable hardware (EHW), defining it as the application of evolutionary algorithms to hardware during design or operation.

- [**1996–1998 – Sussex Breakthroughs**](historical_review.md#inception-and-history): Adrian Thompson evolves oscillators and the famous tone discriminator directly on Xilinx FPGAs, proving that intrinsic analog evolution can exploit latent device physics.

- [**Early 2000s – XC6200 Retired**](historical_review.md#xilinx-discontinues-xc6200): Xilinx discontinues the openly documented XC6200 series, removing the community's only bitstream-level platform and pausing intrinsic analog EHW progress.

- [**2015 – Project Icestorm**](historical_review.md#project-icestorm): Reverse-engineering work unveiled the full Lattice iCE40 bitstream at the Chaos Communication Congress, restoring a modern, open substrate for intrinsic experiments ([Project Icestorm](http://www.clifford.at/icestorm/)).

- [**2021 – Field Resurrected**](historical_review.md#bitstream-evolution-with-the-icestick-hx1k-2021): The ALIFE paper ["Resurrecting FPGA Intrinsic Analog Evolvable Hardware"](../research/publications/papers/2021/7_19_Resurrect-FPGA-EHW.md) reproduces seminal analog behaviors on iCE40 devices and introduces an open-source experimentation stack.

- [**2022 – Demonstrating Robust Analog Evolution**](historical_review.md#bitstream-evolution-with-the-icestick-hx1k-2021): Artificial Life article ["Intrinsic Evolution of Analog Circuits Using Field Programmable Gate Arrays"](../research/publications/papers/2022/11_1_evolution-of-analog-FPGA.md) details evolved amplitude maximization and pulse oscillation circuits plus robustness studies, formalizing the Bitstream Evolution roadmap.

- [**2022 – CoBEA Framework Introduced**](historical_review.md#project-icestorm): The GECCO paper ["CoBEA: framework for evolving hardware by direct manipulation of FPGA bitstreams"](https://dl.acm.org/doi/10.1145/3520304.3528821) debuts an integrated stack that unifies low-level bitstream mutation, device communication, and on-board evaluation, enabling >100× faster iCE40 reconfiguration and lowering the barrier to intrinsic experiments.

- [**2025 – Bitstream Evolution Toolkit**](historical_review.md#bitstream-evolution-with-the-pico2ice-boards-2025): IEEE Access piece ["Bitstream Evolution: an Open-Source FPGA Intrinsic Evolvable Hardware Toolkit"](../research/publications/papers/2025/11_10_bitstream-evolution-toolkit.md) packages the hardware, software, and processes so new teams can evolve analog FPGA circuits and extends the published experiments with deeper analyses on circuit robustness, cross-die transferability, and sensitivity to environmental shifts.

