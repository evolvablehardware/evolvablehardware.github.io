---
hide:
  - toc
---

# Variance Maximization

!!! tip "Start Here: Your First Evolution"
    This is the simplest evolvable hardware experiment — a great first project for newcomers. You'll evolve a circuit that maximizes output signal variance. **Time estimate:** ~1–2 hours from powered hardware to first evolved result. **Prerequisites:** Completed [hardware setup](../../projects/bitstream_evolution_pico2-ice/hardware_setup.md) and [software setup](../../projects/bitstream_evolution_pico2-ice/software_setup.md).

This early benchmark demonstrates that intrinsic analog evolution on the Lattice iCEstick HX1K can reliably amplify signal variance using only bitstream-level mutations. This is the simplest experiment and can serve as a "Hello World" for your introduction to Evolvable Hardware. By maximizing the variance of the output signal, we encourage the evolution of complex, dynamic behavior that can be difficult to design manually. This experiment serves as a starting point for understanding the capabilities of the Bitstream Evolution toolkit and provides a foundation for more complex experiments that involve specific target behaviors, robustness analysis, and transferability studies.
<div class="result-row">
	<figure >
		<img src="/assets/experiments/variancemaximization.gif" alt="Evolution of signal variance">
		<figcaption>Evolution of signal variance</figcaption>
	</figure>
	<p>
		Early runs started with near-zero activity before evolution discovered rich analog dynamics. The animation captures a
		representative population member as its output swings grow generation-by-generation.
	</p>
</div>

## Experiment Snapshot

| Runtime | Population | Generations | Mutation Rate | Crossover Rate |
| --- | --- | --- | --- | --- |
| 4–5 hours | 50 | 100 | 0.005 | 0.5 |

## Fitness Function

<div class="result-row">
	<figure class="equation">
		<img src="/assets/equations/varmax.png"  alt="Variance maximization equation">
		<figcaption>Variance maximization equation</figcaption>
	</figure>
	<p>
		The fitness function averages the absolute difference between sequential ADC samples captured by the MCU. Maximizing this
		average differential rewards circuits that swing further between readings, naturally increasing output amplitude/variance
		over successive generations.
	</p>
</div>

## Results

<div class="result-row">
	<figure>
		<img src="/assets/experiments/varmaxevolution.png" alt="Variance maximization fitness trace">
		<figcaption>Variance maximization fitness trace</figcaption>
	</figure>
	<p>
		Because the search happens on real hardware, stochastic device noise influences each evolutionary trajectory. Even so, typical
		runs resemble the curve above: an initially flat fitness landscape gives way to rapid climbs once evolution discovers richer
		analog dynamics. Extending the generation budget beyond the default 100 iterations usually uncovers even higher-variance solutions.
	</p>
</div>
