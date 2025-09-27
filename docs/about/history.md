# History of Evolvable Hardware

## Field Overview

The broader field of evolvable hardware is taxonomized into several subdomains: digital or analog, intrinsic, extrinsic, or mixtrinsic, adaptive hardware (AH) or evolvable hardware design (EHD). Our work focuses specifically on **intrinsic analog evolvable hardware design**, meaning populations of circuits are evolved intrinsic to a hardware substrate and do not actively adapt to changes in their environment.

At its origin, evolvable hardware aimed to revolutionize electronics design, both digital and analog. Unlike digital design, analog circuit development must inherently contend with unique semiconductor physics at each timescale relevant to operational states - an obstacle that digital design overcomes by abstracting continuous state values through clock signals and logic levels.

**Analog evolvable hardware offered a revolutionary approach**: delegating the complex search and design process to artificial evolution, capable of exploiting physical properties that would otherwise be abstracted away during digital operation or simulation.

![Thompson's Tone Discriminator Circuit](../evolvablehardware.org/images/discriminatorcircuit.png)
*Adrian Thompson's famous tone discriminator circuit*

## The Reality Gap Challenge

One hallmark characteristic of intrinsic analog EHW is evolution's ability to employ physical properties of target hardware that are typically abstracted away due to the complex nature of real-world semiconductor physics. Simulations generally perform this abstraction to account for fabrication variations (transistor doping levels, copper tracing thickness variations, etc.).

These manufacturing "imperfections" create non-linear effects that interact unpredictably - the **reality gap** between simulated and real system behavior. **This is where intrinsic evolution shines.**

## Inception and Pioneers (1991-1999)

### Genesis of the Field

**1991**: Hugo de Garis postulated that evolutionary algorithms "will probably lead to electronic circuits being 'grown' in special hardware," initially in the context of embryological electronics.

**1993**: In conjunction with Tetsuya Higuchi, de Garis conceptualized **evolvable hardware (EHW)** - the application of evolutionary algorithms to hardware systems during design, operation, or both.

### The FPGA Revolution

Field Programmable Gate Arrays (FPGAs) became the primary research tool because their physically reprogrammable architecture could emulate candidate circuits. Combined with evolutionary algorithms running on host CPUs, researchers could:

1. Select circuits from populations
2. Load them onto FPGAs  
3. Evaluate performance via fitness functions
4. Select for reproduction
5. Apply mutation and recombination
6. Gradually improve circuit performance

### Thompson's Breakthrough Experiments

![Adrian Thompson](../evolvablehardware.org/images/thompson1.png)

**Adrian Thompson** at the University of Sussex evolved a series of bitstream-evolution circuits that canonized the evolutionary approach to circuit design. His achievements include:

- **Analog millisecond oscillator**: A temporal bridge for biological-timescale signals
- **Tone discriminator circuit**: A fully analog FPGA circuit distinguishing between 1kHz and 10kHz tones using only 42 configurable logic blocks

**Thompson's tone discriminator** famously exploited physical properties of the FPGA, using only 100 logic gates of the available 24,000 to accomplish what was thought impossible under such resource constraints.

## The Dark Period (2000-2014)

### Xilinx Discontinues XC6200

![XC6216 FPGA](../evolvablehardware.org/images/xc6216.png)

Unfortunately, shortly after the cornerstone achievements of the late 1990s, **Xilinx Corporation discontinued the XC6200 series FPGA** - the tool of choice for evolvable hardware research.

#### Understanding the Loss

The **bitstream** of an FPGA is the binary configuration file defining circuit architecture - the lowest level of programmable instruction. It's essentially the **genome of physically realizable circuits**.

The XC6200 series was unique because its bitstream format was openly documented - 1:1 relationships between configuration entries and silicon resources were available to users. However, for cost and security reasons, FPGA manufacturers moved to strongly encrypted bitstreams.

#### Research Impact

Without complete bitstream knowledge, EHW researchers couldn't perform analog experiments intrinsic to FPGAs. While other reconfigurable hardware existed (FPAAs, FPTAs), none were as developed, accessible, or widely adopted as FPGAs.

**Intrinsic analog evolvable hardware research was effectively halted for nearly two decades.**

## Renaissance: Project IceStorm (2015-Present)

![iCE40 FPGA Map](../evolvablehardware.org/images/icemaphx1k.png)

### The Breakthrough

Recent reverse-engineering efforts by [**Project IceStorm**](http://www.clifford.at/icestorm/) paved a new path using different FPGA technology. The **Lattice iCE40** - an ultra-low power, economy-grade FPGA - had its bitstream fully documented through work demonstrated at the Chaos Communication Congress in Hamburg, Germany, in 2015.

Although reverse-engineering the iCE40 wasn't motivated by EHW research, **a fully documented bitstream is now available** for exactly that purpose.

### Current Revival

This breakthrough has enabled the continuation of FPGA-intrinsic analog evolvable hardware research after a 20-year hiatus. Our organization is dedicated to:

- Recreating seminal experiments on modern hardware
- Advancing the field with new methodologies
- Maintaining open-source accessibility
- Building an active research community

## Key Historical Figures

### Hugo de Garis
- Conceptualized evolvable hardware
- Pioneer of embryological electronics
- Advocate for evolutionary approaches to hardware design

### Tetsuya Higuchi  
- Co-founder of the evolvable hardware field
- Advanced digital evolution techniques
- Leader in adaptive hardware systems

### Adrian Thompson
- Creator of the most famous evolvable hardware experiments
- Demonstrated intrinsic evolution's power
- Proved analog circuits could exploit physical device properties

### Claire Wolf & Mathias Lasser
- Reverse-engineered the Lattice iCE40 bitstream
- Inadvertently unlocked modern evolvable hardware research
- Created the open-source IceStorm toolchain

## Timeline Summary

| Period | Key Development |
|--------|----------------|
| **1991** | Hugo de Garis proposes evolved circuits |
| **1993** | EHW field officially conceptualized |  
| **1996-1999** | Thompson's breakthrough experiments |
| **2000** | Xilinx discontinues XC6200 series |
| **2000-2014** | Research hiatus period |
| **2015** | Project IceStorm reverse-engineers iCE40 |
| **2020-Present** | Modern EHW research revival |

---

*This historical narrative demonstrates how technological constraints can halt entire research domains, and how open-source efforts can resurrect them decades later.*
Focus shifted toward deployable systems:

- Industrial applications in telecommunications
- Automotive adaptive systems
- Medical device personalization
- Energy-efficient computing solutions

**2013-2015: Algorithmic Advances**
Sophisticated evolution strategies emerged:

- Coevolutionary approaches
- Novelty search techniques
- Developmental models for circuit growth
- Hybrid symbolic-numeric evolution

**2016-2019: Edge Computing Era**
The IoT revolution created new opportunities:

- Resource-constrained evolution algorithms
- Distributed evolution across device networks
- Real-time learning in deployed systems
- Energy harvesting adaptive systems

### 2020s: Modern Developments

**2020-2022: AI Integration**
Machine learning transformed evolvable hardware:

- Neural network guided evolution
- Reinforcement learning for hardware design
- Automated design space exploration
- Neuromorphic computing applications

**2023-2025: Quantum and Beyond**
Emerging technologies opened new frontiers:

- Quantum circuit evolution
- Memristive computing arrays
- Photonic evolvable systems
- Molecular electronics experiments

## Key Contributors

### Pioneering Researchers

**Adrian Thompson (University of Sussex)**
Revolutionary work on intrinsic hardware evolution, demonstrating that evolved circuits could exploit physical properties not captured in conventional models.

**Tetsuya Higuchi (National Institute of Advanced Industrial Science)**
Leadership in establishing evolvable hardware as a field, organizing early conferences and developing comprehensive frameworks.

**Jim Torresen (University of Oslo)**
Foundational contributions to digital evolution and FPGA-based systems, advancing both theory and practical applications.

**Andres Upegui (EPFL)**
Pioneering bio-inspired approaches and self-organizing hardware systems, bridging biology and electronics.

### Institutional Contributors

**NASA Goddard Space Flight Center**
Driving practical applications in space technology and establishing evolvable hardware as a solution for extreme environments.

**University of Sussex**
Home to groundbreaking intrinsic evolution experiments and the Centre for Computational Neuroscience and Robotics.

**National Institute of Advanced Industrial Science and Technology (AIST), Japan**
Major research initiatives in evolvable hardware and adaptive systems.

**Universidad Politécnica de Madrid**
Leading European research in evolutionary electronics and reconfigurable computing.

## Technological Milestones

### 1990s Achievements
- First evolved transistor-level circuits
- Demonstration of intrinsic evolution
- Basic evolutionary algorithms for electronics
- Proof-of-concept FPGA evolution

### 2000s Breakthroughs
- Fault-tolerant evolved systems
- Real-time circuit adaptation
- Space-qualified evolvable hardware
- Commercial FPGA evolution tools

### 2010s Innovations  
- Multi-core evolution platforms
- Cloud-based evolution services
- Mobile and embedded evolution
- Industry adoption in telecommunications

### 2020s Advances
- AI-accelerated evolution
- Quantum hardware evolution
- Edge computing integration
- Sustainable and green evolution

## Conference and Community History

### IEEE Congress on Evolutionary Computation (CEC)
Regular special sessions on evolvable hardware since 1999, providing a venue for the latest research.

### NASA/DoD Conference on Evolvable Hardware
Annual conference from 1999-2005, establishing the field and bringing together researchers and practitioners.

### International Conference on Adaptive Hardware and Systems (AHS)
Launched in 2006, becoming the premier venue for evolvable and adaptive hardware research.

### Journal Publications
- IEEE Transactions on Evolutionary Computation
- Genetic Programming and Evolvable Machines (launched 2000)
- Applied Soft Computing
- IEEE Transactions on Computers

## Evolution of Applications

### Early Applications (1990s)
- Academic research projects
- Simple filter and amplifier design
- Proof-of-concept demonstrations
- Laboratory experiments

### Space Era (2000s)
- NASA mission-critical systems
- Radiation-hardened circuits
- Autonomous spacecraft components
- Deep space communication systems

### Commercial Adoption (2010s)
- Telecommunications equipment
- Automotive control systems
- Industrial automation
- Consumer electronics optimization

### Modern Applications (2020s)
- Edge AI acceleration
- IoT device optimization
- Autonomous vehicle systems
- Smart grid infrastructure
- Personalized medical devices

## Future Directions

The history of evolvable hardware points toward several exciting future developments:

- **Quantum-Classical Hybrid Systems**: Combining quantum and classical evolution
- **Massive Parallelization**: Exploiting modern many-core architectures
- **Biological Integration**: Direct interface with living systems
- **Sustainable Computing**: Energy-aware evolutionary optimization
- **Human-AI Collaboration**: Interactive evolution with human designers

This rich history demonstrates how evolvable hardware has evolved from a curious academic pursuit to a practical technology with real-world impact, constantly adapting to new challenges and opportunities in computing and electronics.