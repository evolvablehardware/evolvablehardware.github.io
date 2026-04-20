# Dynamical Neural Networks

Dynamical neural networks are neural models whose behavior unfolds continuously over time, driven not just by their architecture but by their evolving internal state and can be used to approximate [Dynamical Systems](./dynamical_systems.md). Unlike standard recurrent networks, where “state” often means the temporary activation carried from one timestep to the next, dynamical networks explicitly model how internal variables change according to differential or difference equations. These internal dynamics—oscillations, settling behaviors, attractors, and transient responses—are part of the computation itself. They allow the network to integrate information, maintain memory, and generate ongoing behavior rather than producing a single static output.

This broader category includes familiar models like traditional RNNs but also encompasses more expressive systems such as Continuous-Time Recurrent Neural Networks (CTRNNs), where neuron states evolve according to continuous equations, and Liquid Time-Constant Networks (LTCs), which adapt their internal time scales to the complexity of the input. It also connects to Reservoir Computing, where the recurrent dynamics are kept fixed but still serve as a rich dynamical substrate for computation.

For our community, dynamical neural networks provide a unifying lens for understanding how neural systems process time. Whether implemented in software or directly in hardware, these networks demonstrate that computation can arise from the flow of internal activity—not just from discrete steps or static functions. This perspective bridges artificial neural networks, continuous-time models, and evolvable hardware, helping students see how diverse architectures fit into one coherent conceptual landscape.

## Learn More

[An excellent introduction to Artificial Neural Networks with Dynamical Systems Theory](http://jackterwilliger.com/biological-neural-networks-part-i-spiking-neurons/)

