---
hide:
  - toc
---

# Variance Maximization

This early benchmark demonstrates that intrinsic analog evolution on the Lattice iCEstick HX1K can reliably amplify signal variance using only bitstream-level mutations. The run below mirrors the legacy tutorial but is formatted for the Bitstream Evolution knowledge base.

<div class="result-row">
	<figure >
		<img src="/assets/results/early/variancemaximization.gif" alt="Evolution of signal variance">
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
		<img src="/assets/results/early/varmaxevolution.png" alt="Variance maximization fitness trace">
		<figcaption>Variance maximization fitness trace</figcaption>
	</figure>
	<p>
		Because the search happens on real hardware, stochastic device noise influences each evolutionary trajectory. Even so, typical
		runs resemble the curve above: an initially flat fitness landscape gives way to rapid climbs once evolution discovers richer
		analog dynamics. Extending the generation budget beyond the default 100 iterations usually uncovers even higher-variance solutions.
	</p>
</div>
