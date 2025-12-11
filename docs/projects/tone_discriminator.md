---
hide:
	- toc
---

# Tone Discriminator *(Work in Progress)*

Recreating Adrian Thompson's classic tone discriminator remains a long-horizon objective for Bitstream Evolution. The goal is to evolve an FPGA circuit that receives either a 1 kHz or 10 kHz tone and outputs a digital HIGH/LOW classification signal, all without conventional digital logic.

## Experiment Snapshot

| Runtime | Population | Generations | Mutation Rate | Crossover Rate |
| --- | --- | --- | --- | --- |
| ~24 days | 50 | 5000 | 0.001 | 0.7 |

<div class="result-row">
	<figure>
		<img src="/assets/results/early/discriminator.png" alt="Tone discriminator output vs input">
		<figcaption>Output (blue) vs input (yellow)</figcaption>
	</figure>
	<p>
		The evolving circuit must output a HIGH signal for 1&nbsp;kHz inputs and LOW for 10&nbsp;kHz inputs, despite being encoded directly as
		FPGA configuration bits without traditional digital logic.
	</p>
</div>

## Fitness Function

<div class="result-row">
	<figure>
		<img src="/assets/equations/tonefunction.png" alt="Tone discriminator fitness">
		<figcaption>Tone discriminator fitness</figcaption>
	</figure>
	<p>
		Two sets of samples are collected—one per tonal stimulus—and summed before taking their absolute difference. Hand-tuned hardware constants
		$k$ (from Thompson's original work) introduce a slight gradient that guides incremental improvements through the integrating op-amp front-end
		and into the MCU's ADC readings.
	</p>
</div>

Two sets of samples are collected—one per tonal stimulus—and summed before taking their absolute difference. Hand-tuned hardware constants $k$ (from Thompson's original work) introduce a slight gradient that guides incremental improvements through the integrating op-amp front-end and into the MCU's ADC readings.

## Results

<div class="result-row">
	<figure>
		<img src="/assets/results/early/toneevolution.png" alt="Tone discriminator fitness trace">
		<figcaption>Tone discriminator fitness trace</figcaption>
	</figure>
	<p>
		These ultra-long runs tend to plateau for thousands of generations before discovering a new optimum. To date, only low-fitness discriminators
		have emerged on the iCEstick platform, but observed jumps in both best and mean fitness suggest that continued exploration plus tooling refinements
		could eventually reproduce Thompson-level performance.
	</p>
</div>
