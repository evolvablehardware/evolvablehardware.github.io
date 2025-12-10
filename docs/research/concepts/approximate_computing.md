# Approximate Computing

Approximate computing is a design philosophy that challenges a long-held assumption in computer science: that every calculation must be perfectly accurate. In many real-world tasks—like recognizing an object in an image, interpreting a sensor signal, or controlling a robot—absolute precision isn’t necessary. Small errors usually don’t matter, and sometimes the quest for perfect accuracy wastes energy, slows down processing, or makes hardware far more complex than it needs to be. Approximate computing embraces this reality by allowing systems to trade a bit of precision for major gains in speed, efficiency, and adaptability.

Instead of insisting on exact answers, approximate computing focuses on good enough answers delivered quickly and cheaply. This might mean using simplified arithmetic, reducing the resolution of certain signals, or designing circuits that intentionally skip or compress work when the stakes are low. The result is hardware that uses less power, reacts faster, and can tolerate noise or partial failures—qualities that are essential for modern devices operating in unpredictable or resource-limited environments.

For our community, approximate computing pairs naturally with evolvable hardware. When circuits can evolve directly on an FPGA, they often discover unconventional solutions that rely on approximation, analog behavior, or clever shortcuts humans would never design manually. These imperfect but efficient solutions can be more robust, adaptable, and biologically plausible than rigid, exact logic. By embracing approximation as a design tool rather than a flaw, we open the door to evolved systems that are faster, more resilient, and better suited to the messy complexity of the real world.

## Learn More: Approximate Computing

### Introductory & Review Papers
- "Approximate Computing: A Survey" (Mittal, 2016) — highly accessible and widely recommended as a starting point  
  https://www.sciencedirect.com/science/article/abs/pii/S0743731516301542

- "A Survey of Techniques for Approximate Computing" (Ankit et al., 2019) — comprehensive review of circuits, architectures, and modern applications  
  https://ieeexplore.ieee.org/document/8668555

- "Approximate Computing: From Circuits to Machine Learning" (Chippa et al., 2018) — mid-level introduction linking hardware approximation with AI  
  https://www.nowpublishers.com/article/Details/ELE-068

### Recorded Presentations
- YouTube: "Approximate Computing — Energy-Efficient Computing for the Future" (Srinivas Esmaeilzadeh, 30 min)  
  https://www.youtube.com/watch?v=VjzT1K7P4jI

- YouTube: "Approximate Computing for Reducing Energy" (J. Henkel, DATE Conference Talk, 25 min)  
  https://www.youtube.com/watch?v=LcICI6Q2FvU

- MIT CSAIL Talk: "Rethinking Accuracy in Modern Computing Systems" (Sasa Misailovic, 50 min)  
  https://www.youtube.com/watch?v=7dHqG2V1R2U

### Foundational Origins

- **Esmaeilzadeh et al., 2012 — "Architecture Support for Disciplined Approximate Programming"**  
  One of the earliest and most influential papers framing approximate computing as a deliberate architectural strategy for reducing energy and improving performance.  
  https://dl.acm.org/doi/10.1145/2388996.2389028

- **Han & Orshansky, 2013 — "Approximate Computing: A Survey"**  
  The first widely cited survey to unify terminology and scope, establishing approximate computing as a coherent research field.  
  https://ieeexplore.ieee.org/document/6624503
