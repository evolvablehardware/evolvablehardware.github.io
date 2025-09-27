# Research Areas

Evolvable Hardware research at our organization focuses on **FPGA-intrinsic analog evolution**, continuing the groundbreaking work pioneered by Adrian Thompson and others in the 1990s.

## Current Research Focus

### FPGA-Intrinsic Evolution

Our primary research area involves evolving analog circuits directly on FPGA hardware, exploiting device-specific characteristics including:

- Manufacturing variations and tolerances
- Physical effects below design specifications  
- Transistor-level analog behavior in digital devices
- Environmental sensitivity for adaptation

### Experimental Platform

We use the **Lattice iCE40hx1k** FPGA as our primary evolution platform, enabled by the [IceStorm](http://www.clifford.at/icestorm/) open-source toolchain that provides complete bitstream control.

#### Technical Specifications
- **Population Size**: 50 individuals
- **Typical Runtime**: 4-5 hours per experiment
- **Generations**: 100 (typical)
- **Mutation Rate**: 0.005
- **Crossover Rate**: 0.5

## Research Projects

### 1. Variance Maximization
**Status**: Completed ✅

The first proof-of-concept project demonstrating FPGA-intrinsic analog evolvable hardware. The fitness function maximizes the variance of the output signal, effectively evolving circuits with maximum amplitude variation.

**Fitness Function**: 
$$f = \frac{1}{n} \sum_{i=1}^{n-1} |x_{i+1} - x_i|$$

Where $x_i$ represents sequential ADC samples from the microcontroller.

**Key Results**:
- Successfully evolved circuits with increasing signal amplitude
- Demonstrated feasibility of analog evolution on modern FPGAs
- Established baseline methodology for future experiments

### 2. Pulse Oscillation  
**Status**: Completed ✅

Recreation of Thompson's seminal pulse generation experiment using modern hardware. The goal is to evolve an analog circuit capable of generating pseudo-stable periodic oscillations.

**Achievements**:
- Successfully replicated classic EHW results on iCE40 platform
- Generated stable oscillatory behavior without external clock
- Validated evolution of timing-sensitive analog circuits

### 3. Tone Discrimination
**Status**: Ongoing 🔬

The flagship project recreating Thompson's most famous experiment: evolving a circuit to discriminate between two different frequency tones (1kHz and 10kHz).

**Challenge**: This represents one of the most sophisticated analog signal processing tasks demonstrated in evolvable hardware.

**Progress**:
- Circuit evolution platform established
- Fitness evaluation system implemented  
- Initial population testing underway

## Video Presentation

Watch our comprehensive overview of the evolvable hardware project and experimental results:

[🎥 **Artificial Life Video Presentation**](https://evolvablehardware.org/videos/artificial-life-video.mp4)

*This presentation covers our motivation, methodology, experimental results, and future research directions.*

## Research Methodology

### Evolution Process
1. **Random Population Generation**: Create initial population of random bitstreams
2. **Hardware Configuration**: Program each individual onto FPGA
3. **Fitness Evaluation**: Measure analog output characteristics
4. **Selection**: Choose best performers for reproduction
5. **Genetic Operations**: Apply mutation and crossover
6. **Iteration**: Repeat for specified number of generations

### Measurement Setup
- **Analog Output Capture**: High-speed ADC sampling
- **Environmental Control**: Temperature and power monitoring
- **Reproducibility**: Multiple trial averaging
- **Data Logging**: Complete evolutionary history tracking

## Future Directions

### Near-term Goals
- Complete tone discrimination experiment
- Develop sine wave oscillator circuits
- Implement reservoir computing approaches

### Long-term Vision
- Multi-objective optimization for power/performance
- Self-adaptive mutation strategies  
- Distributed evolution across multiple FPGAs
- Integration with machine learning systems

## Collaboration Opportunities

We welcome collaboration from:
- **Academic researchers** in evolutionary computation
- **Hardware engineers** with FPGA expertise
- **Students** interested in bio-inspired systems
- **Industry partners** exploring adaptive electronics

Join our active research community through our [Slack workspace](../community/members.md#get-involved) or contribute to our [open-source repositories](https://github.com/evolvablehardware).