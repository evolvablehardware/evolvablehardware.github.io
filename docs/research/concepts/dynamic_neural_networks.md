# Dynamical Neural Networks

Dynamical Neural Networks

Dynamical neural networks are neural systems whose behavior unfolds continuously over time, driven not just by their architecture but by their evolving internal state. Unlike standard recurrent networks, where “state” often means the temporary activation carried from one timestep to the next, dynamical networks explicitly model how internal variables change according to differential or difference equations. These internal dynamics—oscillations, settling behaviors, attractors, and transient responses—are part of the computation itself. They allow the network to integrate information, maintain memory, and generate ongoing behavior rather than producing a single static output.

This broader category includes familiar models like traditional RNNs but also encompasses more expressive systems such as Continuous-Time Recurrent Neural Networks (CTRNNs), where neuron states evolve according to continuous equations, and Liquid Time-Constant Networks (LTCs), which adapt their internal time scales to the complexity of the input. It also connects to Reservoir Computing, where the recurrent dynamics are kept fixed but still serve as a rich dynamical substrate for computation.

For our community, dynamical neural networks provide a unifying lens for understanding how neural systems process time. Whether implemented in software or directly in hardware, these networks demonstrate that computation can arise from the flow of internal activity—not just from discrete steps or static functions. This perspective bridges artificial neural networks, continuous-time models, and evolvable hardware, helping students see how diverse architectures fit into one coherent conceptual landscape.


## RNN vs. CTRNN vs. LTC: A Conceptual Comparison

| Feature                         | RNN (Discrete)                                   | CTRNN (Continuous-Time)                                           | LTC (Liquid Time-Constant)                                              |
|--------------------------------|---------------------------------------------------|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| State Update                   | Discrete steps (t, t+1, t+2…)                     | Continuous evolution over time                                     | Continuous, with time constants that change based on input               |
| Internal State                 | Hidden activations passed between timesteps       | True dynamical variables governed by differential equations        | Same as CTRNNs but with adaptive time constants                          |
| Time Representation            | Fixed timestep                                    | Real-valued, continuous time                                       | Continuous time with context-sensitive scaling                           |
| Expressive Power               | Good for sequence modeling                        | Very high; can approximate any dynamical system                    | Very high; can adapt internal timescales for complex patterns            |
| Sensitivity to Noise           | Moderate                                          | Robust due to smooth dynamics                                      | Highly robust; time-scale adaptation aids stability                      |
| Training Methods               | Gradient-based (BPTT)                             | Often evolved or optimized via search; gradient methods possible    | Trained via gradient descent (closed-form ODE solutions)                 |
| Typical Uses                   | NLP, speech, sequence prediction                  | Adaptive control, embodied agents, dynamical modeling              | Edge AI, robotics, time-varying pattern recognition                      |
| Conceptual Identity            | Recurrent neural network with memory              | Dynamical system implemented as a neural network                   | Dynamical network whose internal timescales are themselves dynamic        |



## Learn More: Dynamical Neural Networks


### Introductory & Review Papers
- "A Dynamical Systems Perspective on Agent Behavior" (Beer, 1995) — clear introduction to interpreting neural networks through state-space trajectories, internal variables, and continuous-time behavior  
  https://direct.mit.edu/artl/article/1/1/37/2431/A-Dynamic-Systems-Perspective-on-Agent-Behavior

- "Recurrent Neural Networks as Dynamical Systems" (Sussillo & Barak, 2013) — influential paper explaining how recurrent networks create attractors, limit cycles, and transient dynamics  
  https://www.sciencedirect.com/science/article/pii/S089662731300461X

- "Dynamical Systems in Neuroscience" (Eve Marder & Larry Abbott, 2005 overview chapter) — accessible discussion of how internal state and nonlinear dynamics shape neural computation  
  https://www.sciencedirect.com/book/9780123740908/dynamical-systems-in-neuroscience (textbook chapters available online)

### Recorded Presentations
- YouTube: "Dynamics, Neural Systems, and Embodied Agents" (Randall Beer, 55 min) — excellent introduction to internal state, attractors, and dynamical interpretations of recurrent networks  
  https://www.youtube.com/watch?v=g6i4TqC3hE4

- YouTube: "Recurrent Neural Networks as Dynamical Systems" (LFADS Workshop / Sussillo, ~45 min) — clear explanation of how recurrent networks generate temporal structure via internal dynamics  
  https://www.youtube.com/watch?v=iwQUB1XSQjA

- YouTube: "Neural Differential Equations" (David Duvenaud, 45 min) — strong conceptual introduction to viewing neural networks as continuous-time dynamical processes  
  https://www.youtube.com/watch?v=nGnj9ZpHvak

- YouTube: "Dynamical Systems in the Brain" (Michael Breakspear, 50 min) — intuitive overview of how dynamical systems ideas explain neural and cognitive behavior  
  https://www.youtube.com/watch?v=adm1KXvV0fw

### Foundational Origins
- "Nonlinear Dynamics and Chaos" (Steven Strogatz, 1994) — the definitive, accessible introduction to dynamical systems theory, including attractors, stability, and continuous-time evolution  
  https://www.powells.com/book/nonlinear-dynamics-and-chaos-9780813349107

- "The Dynamical Systems Approach to Cognition" (Beer, 2000) — foundational perspective showing how cognitive and neural processes can be understood as evolving dynamical systems  
  https://academic.oup.com/joc/article/9/4/567/874762

- "Universal Approximation Using Dynamical Systems" (Funahashi & Nakamura, 1993) — early theoretical result demonstrating that recurrent networks with continuous internal state can approximate any dynamical system  
  https://www.sciencedirect.com/science/article/pii/S0893608005800833