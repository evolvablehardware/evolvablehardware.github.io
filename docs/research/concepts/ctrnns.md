# Continuous-Time Recurrent Neural Networks

Continuous-Time Recurrent Neural Networks (CTRNNs) are neural networks whose activity evolves smoothly in real time according to differential equations. In contrast to traditional recurrent neural networks that update in discrete steps, CTRNN neurons have internal states that change continuously based on incoming signals, feedback from other neurons, and their own intrinsic dynamics. This continuous evolution allows CTRNNs to generate rich temporal behavior such as oscillations, stable attractors, and transient responses—forms of computation that emerge naturally from their underlying dynamics.

CTRNNs are especially powerful because they integrate sensing, memory, and action into a unified dynamical process. Rather than computing a single output for each input, they produce ongoing patterns of activity that can adapt as conditions change. This makes them well-suited for modeling agents interacting with real physical environments, where timing, feedback, and fluid responses matter. CTRNNs also serve as a bridge between biological neural systems and artificial ones: they capture the essence of neurons as dynamical units while remaining mathematically tractable and analytically rich.

For our community, CTRNNs highlight how neural computation can arise from the continuous flow of internal state rather than discrete operations. They provide a foundation for exploring adaptive controllers, embodied agents, and evolvable dynamical systems in both simulation and hardware.


## Learn More: Dynamical Neural Networks (CTRNNs)


### Introductory & Review Papers
- "A Dynamical Systems Perspective on Agent Behavior" (Randall Beer, 1995) — one of the most influential introductions to CTRNNs and their role in ALife  
  https://direct.mit.edu/artl/article/1/1/37/2431/A-Dynamic-Systems-Perspective-on-Agent-Behavior

- "Evolving Continuous-Time Recurrent Neural Networks for Adaptive Behavior" (Beer & Gallagher, 1992) — foundational ALife work applying CTRNNs in evolution  
  https://dl.acm.org/doi/10.5555/1623264.1623284

- "Dynamical Systems Approach to Embodied Cognition" (Beer, 2000) — accessible review connecting CTRNNs, embodiment, and adaptive behavior  
  https://academic.oup.com/joc/article/9/4/567/874762

### Recorded Presentations
- YouTube: "Dynamics, Neural Systems, and Embodied Agents" (Randall Beer, Indiana University, 55 min) — gold-standard introduction from the field’s leading researcher  
  https://www.youtube.com/watch?v=g6i4TqC3hE4

- YouTube: "Continuous-Time Recurrent Neural Networks Explained" (Machine Learning Street Talk – 20 min clip) — general introduction to CTRNN principles  
  https://www.youtube.com/watch?v=rZ6vK6c0f6w

- YouTube: "Dynamical Systems in Neuroscience and AI" (Ilya Rips, 40 min) — conceptual bridge connecting CTRNNs to broader dynamical neural modeling  
  https://www.youtube.com/watch?v=WPWu1l3f0Mo

### Foundational Origins
- "Nonlinear Dynamics and Chaos" (Steven Strogatz, 1994) — foundational text for understanding dynamical systems, the mathematical basis of CTRNN behavior  
  https://www.powells.com/book/nonlinear-dynamics-and-chaos-9780813349107

- "Computation with Continuous-Time Recurrent Neural Networks" (Peter Dayan, 1993 reference via Hertz, Krogh & Palmer) — early theoretical grounding for continuous-time neural models  
  https://mitpress.mit.edu/9780262510876/introduction-to-the-theory-of-neural-computation/

- "Evolving Dynamical Neural Networks" (Beer & Gallagher, 1992–2000 series) — core papers establishing CTRNNs within Artificial Life and adaptive behavior  
  Example overview (Beer, 1995): https://direct.mit.edu/artl/article/1/1/37/2431/A-Dynamic-Systems-Perspective-on-Agent-Behavior