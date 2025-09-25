# Datasets and Benchmarks

## Research Datasets

### Circuit Evolution Datasets

**EvoCircuit-1K**
*1,000 evolved analog circuits with performance metrics*

- **Size**: 1,000 circuit designs with SPICE netlists
- **Applications**: Amplifiers, filters, oscillators
- **Metrics**: Power consumption, frequency response, noise
- **Format**: SPICE, JSON metadata
- **License**: CC BY 4.0

[Download](https://data.evolvablehardware.org/evocircuit-1k) | [Paper](https://doi.org/10.1109/example)

**FPGA-Evo Benchmarks**
*Standardized benchmark suite for FPGA evolution*

- **Circuits**: 50 digital benchmark problems
- **Platforms**: Xilinx and Intel FPGA targets
- **Metrics**: Area, timing, power consumption
- **Difficulty**: Graded from beginner to expert
- **Tools**: Automated evaluation scripts

[GitHub Repository](https://github.com/evolvablehardware/fpga-evo-benchmarks)

### Fault Tolerance Datasets

**RadHard-Test Suite**
*Radiation effects on evolved circuits*

- **Scenarios**: Various radiation environments
- **Circuits**: Space-qualified evolved designs
- **Data**: Pre/post-radiation performance
- **Applications**: Satellite and space missions
- **Collaboration**: NASA Goddard contributions

**Self-Healing Circuits**
*Fault injection and recovery data*

- **Fault Types**: Stuck-at, parametric drift, open/short
- **Recovery**: Autonomous healing mechanisms
- **Metrics**: Recovery time, performance impact
- **Platforms**: Both analog and digital systems

## Simulation Environments

### Virtual Hardware Platforms

**EvoSim Cloud**
*Scalable cloud-based evolution platform*

- **Compute**: GPU-accelerated fitness evaluation
- **Scale**: Up to 10,000 parallel evaluations
- **Models**: Accurate circuit simulation
- **Access**: Academic research accounts available

**FPGA-in-the-Loop**
*Remote access to physical FPGA hardware*

- **Boards**: Xilinx, Intel, Microsemi platforms
- **Access**: 24/7 remote laboratory
- **Scheduling**: Fair-share resource allocation
- **Support**: Technical assistance available

### Benchmark Suites

**NASA EHW Challenge**
*Real-world space system problems*

Problems derived from actual NASA missions requiring adaptive hardware solutions:

1. **Autonomous Navigation**: Evolve control systems for spacecraft
2. **Communication Adaptation**: Adaptive signal processing for deep space
3. **Power Management**: Optimize energy harvesting and distribution
4. **Sensor Fusion**: Integrate multiple sensor inputs adaptively

**Industrial Benchmarks**
*Commercial application scenarios*

1. **Automotive Control**: Adaptive engine management systems  
2. **Telecommunications**: Self-optimizing base station hardware
3. **Medical Devices**: Personalized pacemaker algorithms
4. **IoT Optimization**: Power-efficient sensor network nodes

## Educational Resources

### Teaching Datasets

**EvoLearn Beginner**
*Introductory problems for students*

- **Complexity**: Simple 2-4 component circuits
- **Goals**: Understand basic evolution principles
- **Support**: Video tutorials and solutions
- **Integration**: Compatible with popular EDA tools

**Advanced Research Problems**
*Graduate-level research challenges*

- **Complexity**: Multi-objective optimization
- **Scope**: System-level design problems
- **Support**: Literature references and baselines
- **Community**: Discussion forums for researchers

### Simulation Models

**Device Models**
Accurate models for evolutionary hardware research:

- **Transistor Models**: Advanced SPICE models
- **FPGA Models**: Timing and power modeling
- **Memristor Models**: Emerging device characteristics
- **Process Variations**: Manufacturing tolerance modeling

## Data Formats and Standards

### File Formats

**Circuit Descriptions**
- **SPICE**: Industry standard netlist format
- **VHDL/Verilog**: Hardware description languages
- **JSON**: Structured metadata and parameters
- **HDF5**: Large-scale experimental data

**Evolution Data**
- **Population Files**: Generational data storage
- **Fitness Logs**: Performance tracking over time
- **Configuration Data**: Algorithm parameters and settings
- **Result Archives**: Best solutions and analyses

### Metadata Standards

All datasets include standardized metadata:

- **Author Information**: Researcher credits and affiliations
- **Experimental Setup**: Hardware, software, and parameters used
- **Performance Metrics**: Standardized measurement definitions
- **Reproduction Info**: Instructions for replicating results
- **Citation Guidelines**: Proper attribution requirements

## Contributing Data

### Submission Guidelines

**Data Requirements**
1. **Quality**: Verified and validated results
2. **Documentation**: Complete experimental setup description
3. **Format**: Standard file formats and metadata
4. **License**: Open-source compatible licensing
5. **Ethics**: No proprietary or restricted information

**Review Process**
1. **Technical Review**: Data quality and completeness
2. **Peer Evaluation**: Community feedback period
3. **Integration Testing**: Compatibility verification
4. **Publication**: Addition to repository with DOI

### Community Data Projects

**Collaborative Datasets**
Join ongoing community efforts:

- **Global Circuit Database**: Worldwide circuit collection
- **Benchmark Standardization**: Common evaluation metrics
- **Educational Resources**: Teaching material development
- **Tool Integration**: Cross-platform compatibility

## Data Access and Usage

### Academic Access

**Free Access**: All datasets available for academic research
**Registration**: Simple researcher registration required
**Support**: Technical assistance and documentation
**Citation**: Proper attribution guidelines provided

### Commercial Usage

**Licensing**: Contact for commercial licensing terms
**Support**: Professional technical support available
**Custom Data**: Commissioned dataset development
**Collaboration**: Industry-academia partnerships

### Privacy and Ethics

**Data Protection**: No personal or proprietary information
**Open Science**: Supporting reproducible research
**Global Access**: Available worldwide without restrictions
**Ethical Use**: Research ethics guidelines compliance

---

*Datasets are regularly updated and expanded based on community contributions and research advances. New datasets are announced through our news section and mailing list.*