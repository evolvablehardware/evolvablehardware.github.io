# Software Resources

## Evolution Platforms

### IceStorm Toolchain
**The foundation of modern FPGA-intrinsic evolvable hardware**

[**Project IceStorm**](http://www.clifford.at/icestorm/) provides complete open-source toolchain for Lattice iCE40 FPGAs:

- **Bitstream reverse engineering**: Complete documentation of iCE40 bitstream format
- **Synthesis tools**: Converting hardware descriptions to bitstreams
- **Programming utilities**: Direct FPGA configuration control
- **Analysis tools**: Bitstream inspection and modification

**Installation:**
```bash
# Ubuntu/Debian
sudo apt install fpga-icestorm arachne-pnr yosys

# From source
git clone https://github.com/cliffordwolf/icestorm.git
cd icestorm && make && sudo make install
```

### Evolutionary Algorithm Framework
**Custom GA implementation optimized for hardware evolution**

Our evolutionary framework provides:
- **Population management**: Efficient bitstream population handling
- **Genetic operators**: Hardware-specific mutation and crossover
- **Fitness evaluation**: Real-time FPGA measurement integration
- **Evolution tracking**: Comprehensive generational data logging

**Key Features:**
- Population size: 50 (configurable)
- Mutation rate: 0.005 (adaptive)
- Crossover rate: 0.5
- Selection: Tournament with elitism

## Hardware Interfaces

### Microcontroller Integration
**Arduino-based fitness evaluation system**

```cpp
// Example ADC sampling for fitness evaluation
int evaluateCircuit() {
    float variance = 0.0;
    int samples[SAMPLE_SIZE];
    
    // Collect analog samples
    for(int i = 0; i < SAMPLE_SIZE; i++) {
        samples[i] = analogRead(OUTPUT_PIN);
        delayMicroseconds(SAMPLE_DELAY);
    }
    
    // Calculate variance fitness
    for(int i = 1; i < SAMPLE_SIZE; i++) {
        variance += abs(samples[i] - samples[i-1]);
    }
    
    return variance / SAMPLE_SIZE;
}
```

### FPGA Programming Interface
**Direct bitstream manipulation and upload**

- **iceprog**: Command-line FPGA programming utility
- **Custom scripts**: Automated evolution loop control
- **Safety mechanisms**: Circuit protection and monitoring

## Data Analysis Tools

### Evolution Visualization
**Python-based analysis and plotting**

```python
import matplotlib.pyplot as plt
import numpy as np

# Plot evolutionary progress
def plot_fitness_evolution(generations, fitness_data):
    plt.figure(figsize=(10, 6))
    plt.plot(generations, fitness_data['max'], label='Best Fitness')
    plt.plot(generations, fitness_data['avg'], label='Average Fitness')
    plt.xlabel('Generation')
    plt.ylabel('Fitness Value')
    plt.title('Circuit Evolution Progress')
    plt.legend()
    plt.grid(True)
    plt.show()
```

### Signal Analysis
**Real-time waveform analysis and characterization**

- **FFT analysis**: Frequency domain characterization
- **Statistical measures**: Variance, amplitude, period detection
- **Comparative analysis**: Generation-to-generation improvements
- **Export formats**: CSV, HDF5, MATLAB compatibility

## Simulation and Design Tools

### Circuit Simulation
**Verification and pre-evolution analysis**

- **SPICE integration**: Analog circuit simulation
- **Verilog synthesis**: Digital component modeling
- **Mixed-signal simulation**: Analog-digital interface modeling

### Design Validation
**Post-evolution circuit analysis**

- **Bitstream decode**: Understanding evolved solutions
- **Circuit extraction**: Reverse-engineering successful individuals
- **Robustness testing**: Environmental variation analysis

## Project-Specific Software

### Variance Maximization
**Simple fitness function implementation**

```python
def variance_fitness(adc_samples):
    """Calculate variance-based fitness function"""
    differences = np.abs(np.diff(adc_samples))
    return np.mean(differences)
```

### Pulse Oscillation
**Timing-based fitness evaluation**

```python
def pulse_fitness(adc_samples, target_period):
    """Evaluate pulse generation quality"""
    # Detect pulse periods
    peaks = find_peaks(adc_samples)
    if len(peaks) < 2:
        return 0
    
    # Calculate period stability
    periods = np.diff(peaks)
    period_variance = np.var(periods)
    
    # Reward stable periods near target
    target_match = np.exp(-abs(np.mean(periods) - target_period))
    stability = np.exp(-period_variance)
    
    return target_match * stability
```

### Tone Discrimination
**Frequency analysis for tone detection**

```python
def tone_discrimination_fitness(adc_samples, tone1_freq, tone2_freq):
    """Evaluate tone discrimination capability"""
    # FFT analysis
    fft = np.fft.fft(adc_samples)
    freqs = np.fft.fftfreq(len(adc_samples), 1/SAMPLE_RATE)
    
    # Find response at target frequencies
    idx1 = np.argmin(np.abs(freqs - tone1_freq))
    idx2 = np.argmin(np.abs(freqs - tone2_freq))
    
    # Maximize discrimination ratio
    response_ratio = abs(fft[idx1]) / max(abs(fft[idx2]), 1e-6)
    return response_ratio
```

## Development Environment

### Prerequisites
**Required software and dependencies**

- **Python 3.8+**: Main development environment
- **Arduino IDE**: Microcontroller programming
- **GCC toolchain**: Cross-compilation support
- **Git**: Version control and collaboration

### Setup Script
```bash
#!/bin/bash
# Complete development environment setup

# Install system dependencies
sudo apt update
sudo apt install python3-pip arduino-ide build-essential git

# Install Python packages
pip3 install numpy matplotlib scipy pandas jupyter

# Clone project repositories  
git clone https://github.com/evolvablehardware/ice40-evolution.git
git clone https://github.com/evolvablehardware/ga-framework.git

# Install IceStorm toolchain
git clone https://github.com/cliffordwolf/icestorm.git
cd icestorm && make -j$(nproc) && sudo make install

echo "Development environment ready!"
```

## Contributing

We welcome contributions to our software ecosystem:

1. **Bug reports and feature requests** via [GitHub Issues](https://github.com/evolvablehardware)
2. **Code contributions** through pull requests
3. **Documentation improvements** and tutorials
4. **Educational content** and example projects
5. **Benchmark problems** and test cases

### Contribution Guidelines
- Follow Python PEP 8 style guidelines
- Include unit tests for new functionality
- Document all public APIs
- Provide example usage where appropriate
- Test on multiple platforms when possible

## Support and Training

- **GitHub Discussions**: Community Q&A and project discussions
- **Slack workspace**: Real-time collaboration and support
- **Video tutorials**: Step-by-step setup and usage guides
- **Workshop materials**: Conference presentations and training resources

### Getting Help

1. **Documentation**: Start with our comprehensive guides
2. **Community forums**: Search existing discussions
3. **Slack channel**: Real-time help from active researchers
4. **GitHub issues**: Report bugs or request features
5. **Email**: Direct contact for complex questions

---

*All software tools are maintained by the evolvable hardware community and are available under open-source licenses. We're committed to keeping this field accessible to researchers worldwide.*