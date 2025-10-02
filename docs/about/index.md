# About the Evolvable Hardware Organization

![iCE40 FPGA](../assets/setup/ice40/ice40pinout_pin_overlay.png){: align=right : width=400}

*The Lattice iCE40hx1k FPGA - our primary evolution platform*

## Our Mission

Since the turn of the century, evolvable hardware research began migrating into many different directions away from the initial **FPGA-intrinsic analog method**. The excitement for this field of research was a result of the prospect of using evolutionary search to create analog circuits - a significant engineering challenge.

Our mission was to determine why evolvable hardware appeared to have abandoned this vein of research, attempt to recreate its seminal experimental results, press the research forward, and get others involved. This website serves as a focal point for communicating projects, connecting researchers, and targeting new and promising directions.

## Research Focus

### FPGA-Intrinsic Analog Evolution
Our specialized focus is on **intrinsic analog evolvable hardware design**, where populations of circuits are evolved directly on FPGA hardware substrates. This approach exploits:

- Physical device characteristics normally abstracted away
- Manufacturing variations and tolerances  
- Real-world semiconductor physics effects
- Environmental sensitivity for adaptation

### The Reality Gap Solution
Unlike extrinsic (simulation-based) evolution, our intrinsic approach eliminates the **reality gap** - the distance between simulated and real system behavior. By evolving directly on hardware, we can exploit physical properties that simulations cannot capture.

### Continuing Thompson's Legacy
We continue the groundbreaking work of **Adrian Thompson**, **Tetsuya Higuchi**, **Hugo de Garis**, and other pioneers who established FPGA-intrinsic evolution in the 1990s.

## Our Platform: Lattice iCE40

Thanks to [**Project IceStorm**](http://www.clifford.at/icestorm/) by Claire Wolf and Mathias Lasser, complete reverse engineering of the Lattice iCE40 bitstream format has unlocked the capability to perform genetic evolution of hardware bitstreams after a 20-year hiatus.

### Why iCE40?
- **Open bitstream format**: Complete documentation available
- **Cost-effective**: Economy-grade FPGA for accessible research
- **Analog capabilities**: Exploitable transistor-level behavior
- **Community support**: Active development and documentation

## Open Source Commitment

### GitHub Organization
We are keeping this project completely **open-source** to aid in the further development and continuity of this particular domain of research. All code is available at [github.com/evolvablehardware](https://github.com/evolvablehardware).

**We welcome contributors:**
- Testing and debugging
- Feature additions  
- New experiment ideas
- Novel hardware designs
- General criticisms and improvements

### Active Community
Our group is very active and communicates daily using **Slack**. We have channels for different methods, focus areas, and general interests. Contact [Derek](mailto:derek.whitley1@gmail.com) with subject "EHW SLACK" to join our workspace.

## Current Research Projects

### ✅ Completed Experiments
- **Variance Maximization**: First proof-of-concept on iCE40
- **Pulse Oscillation**: Recreation of Thompson's timing circuits

### 🔬 Ongoing Research  
- **Tone Discrimination**: The flagship Thompson experiment
- **Hardware platform optimization**
- **Evolutionary algorithm enhancements**

### 📅 Future Directions
- Sine wave oscillator development
- Reservoir computing approaches
- Speech synthesis and recognition
- Multi-objective circuit optimization

## Collaboration Opportunities

We welcome collaboration from:

### Academic Partners
- **University research groups** in evolutionary computation
- **FPGA laboratories** and digital systems teams
- **Student researchers** for thesis projects
- **International collaborations** on evolvable hardware

### Industry Partners  
- **Hardware platform development**
- **Technology licensing** opportunities
- **R&D collaboration** projects
- **Funding and resource** support

## Impact and Vision

Evolvable hardware represents a paradigm shift from traditional static designs to **adaptive, self-optimizing systems**. Applications span:

- **Space electronics**: Radiation-tolerant adaptive circuits
- **IoT devices**: Power-efficient adaptive sensors  
- **Robotics**: Adaptive control and sensor systems
- **Signal processing**: Self-optimizing analog circuits
- **Research tools**: Open platforms for evolutionary experiments

## Join Our Mission

Whether you're interested in the science, engineering, or just tinkering - **you're welcome here!** Connect with our growing community through [Slack](../community/members.md#slack-channel), contribute to our [open-source projects](https://github.com/evolvablehardware), or start your own evolvable hardware experiments using our [setup guides](../resources/hardware.md).

*Together, we're reviving and advancing one of the most fascinating areas of evolutionary computation and adaptive systems.*

Today's research focuses on:

- **Scalability**: Evolving larger and more complex systems
- **Real-time adaptation**: Faster evolution for dynamic environments
- **Multi-objective optimization**: Balancing performance, power, and area
- **Hybrid systems**: Combining evolved and designed components

## Applications and Impact

Evolvable hardware has found applications in various domains:

- **Space technology**: Radiation-tolerant systems
- **Automotive**: Adaptive control systems
- **Telecommunications**: Self-optimizing signal processing
- **Robotics**: Adaptive locomotion and control
- **Medical devices**: Personalized treatment systems

The field continues to grow as hardware becomes more flexible and evolutionary algorithms become more sophisticated.