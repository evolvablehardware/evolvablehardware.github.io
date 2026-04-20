---
hide:
  - toc
---

# Transferability

In our [2025 paper](../publications/papers/2025/11_10_bitstream-evolution-toolkit.md) we performed some experiments on transferability of evolved circuits across different FPGA hardware.
This was performed by alternating evolution between two physical FPGAs ("A" and "B") every 200 generations. Each switch measures how quickly the population recovers and whether migrating across silicon can reveal new high-fitness behaviors.

## Variance Maximization Circuits

<div class="result-row">
  <figure>
    <img src="/assets/publications/2025-ieee-access/transferability/loyd6.png" alt="Variance maximization transferability fitness">
    <figcaption>Fitness of circuits throughout an experiment exploring the transferability of a circuit evolved for the max variance fitness function. Evolution occurs while alternating between FPGA "A" and "B" every 200 generations, as depicted in the plot.</figcaption>
  </figure>
  <p>
    Recovery time (generations to reach 95% of the previous interval’s peak) shrinks dramatically: 155 generations after the first transfer, 110 after the second, then only 22 after the third. The enforced hardware swaps help the population escape the first local optimum (320.7 fitness at generation 155) and discover a better solution (376.8 fitness by generation 392).
  </p>
</div>

<div class="result-row">
  <figure>
    <img src="/assets/publications/2025-ieee-access/transferability/loyd7.png" alt="Variance maximization transferability heatmap">
    <figcaption>This heatmap (with darker colors indicating higher frequency) shows the voltages of the best circuits throughout an experiment exploring transferability of circuit evolved for variance maximization fitness. FPGA "A" and "B" are alternated every 200 generations, as depicted in the plot.</figcaption>
  </figure>
  <p>
    Despite hardware changes, the highest-performing circuits converge toward a similar waveform: rapid toggling between rail voltages. Alternating boards keeps the search from collapsing into a single fragile genotype and instead encourages reusable motifs that reappear after each transfer.
  </p>
</div>

## 80&nbsp;kHz Oscillators

<div class="result-row">
  <figure>
    <img src="/assets/publications/2025-ieee-access/transferability/loyd8.png" alt="Pulse transferability fitness">
    <figcaption>Fitness of circuits throughout an experiment exploring transferability of oscillators targeting an 80 kHz frequency. Evolution occurs while alternating between FPGA "A" and "B" every 200 generations, as depicted in the plot.</figcaption>
  </figure>
  <p>
    Oscillators show the same pattern of shorter recovery windows after early transfers, but the fourth interval never regains the previous fitness plateau. The population devolves to the fitness levels seen in the very first interval, implying that crucial building blocks for board B were lost while adapting back on board A.
  </p>
</div>

<div class="result-row">
  <figure>
    <img src="/assets/publications/2025-ieee-access/transferability/loyd9.png" alt="Pulse transferability produced frequencies">
    <figcaption>Produced frequencies of circuits throughout an experiment exploring transferability of oscillators targeting an 80 kHz frequency. Evolution occurs while alternating between FPGA "A" and "B" every 200 generations, as depicted in the plot.</figcaption>
  </figure>
  <p>
    Frequency traces mirror the fitness swings: periods of tight clustering around 80&nbsp;kHz after transfers give way to broader spreads as evolution drifts. Taking two samples and scoring on the worst measurement increases pressure for consistent oscillators, but it also exposes how fragile single-board specializations can be.
  </p>
</div>

### Lessons Learned

- Automatic board swapping (TRANSFER_INTERVAL) is effective at escaping some local optima and accelerating recovery.
- Recovery is not guaranteed: the 80&nbsp;kHz case highlights that once board-specific genetic material is lost, subsequent transfers may stall.
- Seeding new runs with an evolved population—even from other hardware—still outperforms random initialization but needs diversity preservation to avoid converging on brittle solutions.
