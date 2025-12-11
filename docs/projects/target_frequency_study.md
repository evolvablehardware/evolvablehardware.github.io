# Target Frequency Sweep

The IEEE Access study benchmarked how quickly oscillatory circuits emerge when they are evaluated against different pulse-count targets. Each run shared the same evolutionary settings (population 50, 6 trials per target, 800 generations aggregated) and differed only in the desired frequency.

## Comparative Fitness Trajectories

<div class="result-row">
  <figure>
    <img src="/assets/results/ieee/target_frequency/loyd5.png" alt="Fitness traces for seven target frequencies">
    <figcaption>Mean overall best, generation best, and generation average fitness across seven targets.</figcaption>
  </figure>
  <p>
    Evolution consistently reaches viable oscillators across the full 1&nbsp;kHz–80&nbsp;kHz sweep, but some frequencies are clearly easier to discover. The 40&nbsp;kHz trials start with a strong random baseline (~40&nbsp;kHz) and remain ahead in every metric, while the 80&nbsp;kHz runs trail despite being a simple harmonic of 40&nbsp;kHz. Lower bands (1, 10, 20&nbsp;kHz) track closely with 30–50&nbsp;kHz runs, highlighting that difficulty is not purely correlated with either absolute frequency or its distance from the 40&nbsp;kHz hotspot. These aggregates mirror anecdotal observations from day-to-day tinkering: certain bands repeatedly “click” on modern iCEstick hardware, hinting that shared noise sources (e.g., the Arduino sampling clock) are providing exploitable structure.
  </p>
</div>

## Takeaways

- Evolvability is banded: 40&nbsp;kHz oscillators reliably outpace all others; 80&nbsp;kHz oscillators underperform despite being a harmonic.
- Generation-best curves for 40&nbsp;kHz often match the overall-best curves for other frequencies, implying a denser set of workable bitstreams in that band.
- Because experiments ran on five distinct FPGAs, the shared bias is unlikely to stem from single-board quirks—further instrumentation (temperature, MCU jitter, supply noise) is needed to isolate the cause.
- Practically, 40&nbsp;kHz targets make excellent “sanity check” experiments, while 80&nbsp;kHz oscillators stress-test new firmware or selection policies.
