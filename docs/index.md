
# Evolvable Hardware
![200](./assets/branding/logo.png){: align=right : width=300}

Welcome to the Open Source **Evolvable Hardware** community - a hub for researchers, engineers, and enthusiasts working on adaptive and self-reconfiguring hardware systems through evolutionary computation.

!!! info "Watch Our Research"
    Explore our [video presentation](about/research.md#video-presentation) to see evolvable hardware in action.

## What is Evolvable Hardware?

Evolvable hardware is the application of evolutionary algorithms to hardware systems during design, operation, or both. It can be used to simulate parameter optimization for physical designs or search for new and counterintuitive designs altogether. For reconfigurable hardware, such as field programmable gate arrays (FPGAs) and other programmable logic devices, the evolutionary process can be performed intrinsic to the hardware itself and exploit device-specific characteristics, including manufacturing errors and physical effects that fall below fabrication tolerances.

This field combines principles from:

- **Evolutionary algorithms** for circuit optimization
- **Reconfigurable computing** for hardware flexibility  
- **Analog circuit design** for unconventional solutions
- **Bio-inspired systems** for self-organization
- **FPGA-intrinsic evolution** for real-world adaptation

## Key Research Areas

### Analog Evolvable Hardware
Circuits that can adapt their analog characteristics through evolutionary processes, enabling fault tolerance and optimization in real-world conditions.

### Digital Evolution
Self-modifying digital systems using FPGAs and reconfigurable architectures to evolve solutions to complex computational problems.

### Evolutionary Electronics
Hardware that undergoes physical evolution at the transistor level, creating novel circuit topologies through guided search processes.

### Adaptive Systems
Systems that can reconfigure themselves in response to changing environments, requirements, or component failures.

## Current Research Projects

### Completed Projects

!!! success "Variance Maximization"
    The first and simplest project, aimed at generating an evolved circuit with a maximally noisy output analog signal using FPGA-intrinsic evolution on the Lattice iCE40.
    
    [Learn more about Variance Maximization →](resources/datasets.md#variance-maximization)

!!! success "Pulse Oscillation"
    From Thompson's first EHW experiments, an analog circuit capable of generating a pseudo-stable periodic oscillator, recreated on modern hardware.
    
    [Learn more about Pulse Oscillation →](resources/datasets.md#pulse-oscillation)

### Ongoing Projects

!!! info "Tone Discrimination"
    The seminal EHW experiment recreated on modern hardware: an analog circuit to discriminate between input tones, following Adrian Thompson's pioneering work.

### Future Directions

- **Sine Wave Oscillator** - Developing clean oscillators from analog components
- **Reservoir Computing** - Treating unclocked FPGA fabric as a reservoir with physical readout layers
- **Speech Synthesis and Recognition** - Evolving analog circuits for biological timescale audio signals

## Applications

- **Fault-tolerant systems** - Hardware that self-repairs and adapts
- **Space electronics** - Radiation-hardened adaptive circuits  
- **Signal processing** - Self-optimizing analog filters and processors
- **Robotics** - Adaptive control and sensor systems
- **IoT devices** - Power-efficient adaptive sensors
- **Research platforms** - Open-source tools for EHW experimentation

## Getting Started

- Browse our [Publications](publications/index.md) for the latest research
- Explore [Software Tools](resources/software.md) for evolution platforms and datasets
- Check out [Hardware Resources](resources/hardware.md) for FPGA setup and tutorials
- Join our active [Community](community/members.md) and [Slack workspace](community/members.md#slack-channel)
- Follow [News](news/index.md) for recent developments and experimental results

## Open Source Commitment

As research into FPGA-intrinsic analog evolvable hardware has been limited for the last 20 years, we're committed to making this field accessible again. Thanks to the [IceStorm project](http://www.clifford.at/icestorm/) by Claire Wolf and Mathias Lasser, complete reverse engineering of the Lattice iCE40 bitstream format has unlocked the capability to perform genetic evolution of hardware bitstreams.

This website continues research pioneered by Adrian Thompson, Tetsuya Higuchi, Hugo de Garis, and many others, with all code available on [GitHub](https://github.com/evolvablehardware) under open-source licenses.

## Featured Content

!!! info "Latest Research"
    Stay updated with cutting-edge developments in FPGA-intrinsic evolvable hardware research through our experimental results, open-source tools, and detailed project documentation.

!!! tip "Active Community"
    Join our growing community! Connect with researchers worldwide working on evolvable hardware systems. We maintain an active [Slack workspace](community/members.md#get-involved) for daily collaboration, sharing experimental results, and advancing the field together.

!!! example "Hardware Setup"
    Get started with your own evolvable hardware experiments using our detailed [setup guides](resources/hardware.md) and [troubleshooting resources](resources/hardware.md#troubleshooting).