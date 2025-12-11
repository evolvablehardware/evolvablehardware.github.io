# Continuous-Time Recurrent Neural Networks

Continuous-Time Recurrent Neural Networks (CTRNNs) are neural networks whose activity evolves smoothly in real time according to differential equations. In contrast to traditional recurrent neural networks that update in discrete steps, CTRNN neurons have internal states that change continuously based on incoming signals, feedback from other neurons, and their own intrinsic dynamics. This continuous evolution allows CTRNNs to generate rich temporal behavior such as oscillations, stable attractors, and transient responses—forms of computation that emerge naturally from their underlying dynamics.

CTRNNs are especially powerful because they integrate sensing, memory, and action into a unified dynamical process. Rather than computing a single output for each input, they produce ongoing patterns of activity that can adapt as conditions change. This makes them well-suited for modeling agents interacting with real physical environments, where timing, feedback, and fluid responses matter. CTRNNs also serve as a bridge between biological neural systems and artificial ones: they capture the essence of neurons as dynamical units while remaining mathematically tractable and analytically rich.

For our community, CTRNNs highlight how neural computation can arise from the continuous flow of internal state rather than discrete operations. They provide a foundation for exploring adaptive controllers, embodied agents, and evolvable dynamical systems in both simulation and hardware.


## Learn More About CTRNNs

[Wikipedia Entry on Recurrent Neural Networks (CTRNNs in the context of other classes)](https://en.wikipedia.org/wiki/Recurrent_neural_network#Continuous-time)

[Interactive Visualization Tool for a 2 Neuron CTRNN](https://cooperuser.github.io/ctrnn-visualizer/)

[A nice introductory blog post about analyzing a CTRNN](https://indy9000.blog/posts/analysis-of-a-simple-ctrnn.html)

[Excellent chapter on CTRNNs, with an explanation and motivation](https://drive.google.com/file/d/1hKOGRqYsPv-yi0Ww9be2aoF417DaTT0V/view?usp=sharing)

[Evolutionary Robotics course. Lecture 10: Continuous Time Recurrent Neural Networks](https://www.youtube.com/watch?v=NHmej5i22aE&ab_channel=JoshBongard)
