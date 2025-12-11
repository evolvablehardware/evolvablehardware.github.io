---
hide:
  - toc
---

# Fitness Sensitivity Studies

To quantify robustness, single circuits were frozen and repeatedly evaluated without modifying their bitstreams. Pulse-count oscillators were exercised for 24 hours, while variance-maximization circuits were sampled for shorter three-hour windows because their distributions remained stable.

## Pulse Count Oscillators

<div class="result-row">
  <figure>
    <img src="/assets/results/ieee/sensitivity/loyd10.png" alt="Pulse sensitivity 1D histogram">
    <figcaption>Distribution of recorded pulses over 24 hours (one target run).</figcaption>
  </figure>
  <p>
    Even after thousands of trials, pulse counts cluster tightly around the desired frequency (50&nbsp;kHz in this run). Desired frequencies from 30–90&nbsp;kHz were tested; the correlation between mean recorded frequency and coefficient of variation was only 0.0239, indicating that higher targets are not inherently less stable.
  </p>
</div>

<div class="result-row">
  <figure>
    <img src="/assets/results/ieee/sensitivity/loyd11.png" alt="Pulse sensitivity 2D histogram">
    <figcaption>Time-frequency heatmap for the same circuit.</figcaption>
  </figure>
  <p>
    Short-lived dips (e.g., near trial 8,000) appear before the circuit naturally recovers, suggesting minor environmental disturbances such as HVAC cycles or USB bus contention. Because the Bitstream Evolution runtime already samples each candidate multiple times per generation, these perturbations rarely derail ongoing experiments.
  </p>
</div>

<div class="result-row">
  <figure>
    <img src="/assets/results/ieee/sensitivity/loyd12.png" alt="Pulse sensitivity vs environment">
    <figcaption>Pulse count versus ambient temperature and humidity.</figcaption>
  </figure>
  <p>
    A pronounced drop in measured frequency aligns with a simultaneous change in temperature and humidity. Even after the environment returned to its baseline, the circuit never fully recovered, underscoring that certain conditions can induce lasting shifts in analog behavior.
  </p>
</div>

## Variance Maximization Circuits

<div class="result-row">
  <figure>
    <img src="/assets/results/ieee/sensitivity/loyd13.png" alt="Variance sensitivity heatmap">
    <figcaption>24-hour fitness distribution for an evolved variance circuit.</figcaption>
  </figure>
  <p>
    Pulling the best circuit from every tenth generation and replaying them for three hours revealed near-zero correlation between generation index and coefficient of variation (0.0046). In other words, variance circuits stay just as stable as evolution progresses, and stochastic noise in the measurement pipeline averages out over repeated sampling.
  </p>
</div>

### Practical Guidance

- Repeated self-evaluation is a quick litmus test before attempting transfers—unstable circuits will show high coefficients of variation long before they fail on a second FPGA.
- Logging temperature and humidity alongside fitness traces helps explain sudden performance cliffs and provides data for future environment-aware fitness functions.
- Because consistency does not automatically improve with fitness, consider multi-sample or variance-penalizing objectives when robustness is the primary goal.
