# Hardware Resources

## Primary Platform: Lattice iCE40hx1k

![EHW Setup](../evolvablehardware.org/images/EHWsetup.jpg)
*Complete evolvable hardware experimental setup*

The **Lattice iCE40hx1k** FPGA serves as our primary evolution platform, enabled by the [IceStorm project's](http://www.clifford.at/icestorm/) complete reverse-engineering of the bitstream format.

### Key Specifications
- **Logic Elements**: 1,280 LUTs (4-input lookup tables)
- **Block RAM**: 16 x 256-bit RAM blocks
- **I/O Pins**: Up to 96 user I/O pins
- **Package Options**: QFN32, TQFP144, csBGA132, csBGA81
- **Power**: Ultra-low power consumption (< 1mW standby)
- **Voltage**: 1.2V core, 1.8V-3.3V I/O

### Why iCE40hx1k?
1. **Open bitstream format**: Complete documentation available
2. **Analog capabilities**: Transistor-level analog behavior exploitation
3. **Cost-effective**: Economy-grade pricing for research
4. **Tool support**: Full open-source toolchain
5. **Community support**: Active development and documentation

## Development Boards

### iCEstick Evaluation Kit
**Primary recommendation for beginners**

![iCE40 Pin Overlay](../evolvablehardware.org/images/ice40pinout_pin_overlay.png)

- **FPGA**: iCE40HX1K in TQFP144 package
- **USB interface**: Built-in programming and communication
- **External connections**: 2x6 pin headers for I/O access
- **LEDs**: 5 user-controllable LEDs
- **Oscillator**: 12 MHz crystal
- **Flash memory**: 32 Mbit SPI flash for configuration storage

**Advantages:**
- Plug-and-play USB connectivity
- Established pin-out documentation
- Community tutorials and examples
- Affordable entry point (~$25)

### Custom PCB Designs
**For advanced research applications**

We provide open-source PCB designs optimized for evolvable hardware research:

- **Enhanced analog connectivity**: Dedicated analog output pins
- **Measurement interfaces**: Built-in ADC connections
- **Power management**: Clean power supplies for analog evolution
- **Expansion headers**: Modular sensor and actuator connections

## Microcontroller Interface

### Arduino Integration
**Fitness evaluation and control system**

```cpp
// Hardware connection pins
#define FPGA_OUTPUT_PIN A0
#define FPGA_PROGRAM_PIN 8
#define FPGA_DONE_PIN 9
#define SAMPLE_SIZE 1000
#define SAMPLE_RATE 10000  // Hz

// Analog sampling configuration
void setup() {
    Serial.begin(115200);
    pinMode(FPGA_PROGRAM_PIN, OUTPUT);
    pinMode(FPGA_DONE_PIN, INPUT);
    
    // Configure ADC for high-speed sampling
    ADCSRA = (ADCSRA & 0xf8) | 0x04; // Set prescaler to 16 (1MHz)
    ADMUX = (1<<REFS0); // AVcc reference
}
```

### Measurement Setup
**High-speed data acquisition**

- **ADC Resolution**: 10-bit (Arduino) or 12-bit (ARM Cortex)
- **Sampling Rate**: Up to 15 kHz continuous
- **Buffer Management**: Circular buffers for continuous sampling
- **Trigger Support**: External trigger for synchronized measurements

## Complete System Architecture

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Host PC       │    │  Microcontroller │    │  iCE40 FPGA     │
│                 │    │                  │    │                 │
│ Evolution       │◄──►│  Fitness         │◄──►│  Evolved        │
│ Algorithm       │USB │  Evaluation      │ADC │  Circuit        │
│                 │    │                  │    │                 │
│ Population      │    │  Control         │    │  Analog         │
│ Management      │    │  Timing          │    │  Output         │
└─────────────────┘    └──────────────────┘    └─────────────────┘
        │                        │                        │
        │                        │                        │
        ▼                        ▼                        ▼
  Data Logging              Real-time ADC           Circuit Evolution
  Statistical Analysis      Signal Processing       Bitstream Mutation
```

## Setup Tutorial

### Step 1: Hardware Assembly

![Setup Tutorial 1](../evolvablehardware.org/images/setup_tutorial_1.jpg)
![Setup Tutorial 2](../evolvablehardware.org/images/setup_tutorial_2.jpg)

1. **Connect iCEstick to computer** via USB cable
2. **Verify FPGA recognition** using `lsusb` command
3. **Install IceStorm toolchain** following [installation guide](software.md#icestorm-toolchain)

### Step 2: Arduino Connection

![Setup Tutorial 3A](../evolvablehardware.org/images/setup_tutorial_3A.jpg)
![Setup Tutorial 3B](../evolvablehardware.org/images/setup_tutorial_3B.jpg)

**Critical connections:**
- **FPGA Pin 95** → **Arduino A0** (analog output monitoring)
- **FPGA Pin 96** → **Arduino Pin 2** (digital control)
- **Common ground** between all systems

### Step 3: Software Configuration

![Setup Tutorial 4](../evolvablehardware.org/images/setup_tutorial_4.jpg)
![Setup Tutorial 5](../evolvablehardware.org/images/setup_tutorial_5.jpg)

1. **Test FPGA programming:**
   ```bash
   iceprog test_bitstream.bin
   ```

2. **Verify Arduino communication:**
   ```cpp
   // Upload test sketch
   void loop() {
       int reading = analogRead(A0);
       Serial.println(reading);
       delay(10);
   }
   ```

### Step 4: Evolution Framework

![Setup Tutorial 6](../evolvablehardware.org/images/setup_tutorial_6.jpg)
![Setup Tutorial 7](../evolvablehardware.org/images/setup_tutorial_7.jpg)

**Run first evolution experiment:**
```bash
# Clone evolution framework
git clone https://github.com/evolvablehardware/ice40-evolution.git
cd ice40-evolution

# Start variance maximization experiment
python3 evolve_variance.py --generations 100 --population 50
```

### Step 5: Results Validation

![Setup Tutorial 8A](../evolvablehardware.org/images/setup_tutorial_8A.jpg)
![Setup Tutorial 8B](../evolvablehardware.org/images/setup_tutorial_8B.jpg)

**Monitor evolution progress:**
- Real-time fitness plotting
- Signal waveform visualization
- Population diversity metrics
- Best individual tracking

## Project-Specific Hardware Configurations

### Variance Maximization
**Simplest starting experiment**

**Hardware Requirements:**
- Single analog output pin (Pin 95)
- Arduino ADC connection
- Basic signal monitoring

**Expected Results:**
- Increasing signal amplitude over generations
- 4-5 hour experiment duration
- Clear evolutionary progress visualization

![Variance Evolution](../evolvablehardware.org/images/variancemaximization.gif)

### Pulse Oscillation
**Timing-sensitive analog circuits**

**Additional Requirements:**
- Precision timing measurements
- Oscilloscope for validation (recommended)
- High-resolution ADC sampling

**Circuit Characteristics:**
- Self-sustaining oscillations
- No external clock dependency
- Biological timescale operation

![Pulse Evolution](../evolvablehardware.org/images/pulseevolution.png)

### Tone Discrimination  
**Advanced signal processing**

**Additional Hardware:**
- Function generator for tone inputs
- Precision analog inputs
- Differential measurement capability

**Input Requirements:**
- 1 kHz reference tone
- 10 kHz test tone  
- Clean power supply for analog precision

![Tone Function](../evolvablehardware.org/images/tonefunction.png)

## Advanced Configurations

### Multi-FPGA Evolution
**Distributed population processing**

- **Parallel fitness evaluation**: Multiple FPGAs, single control system
- **Population migration**: Exchange individuals between populations
- **Specialized roles**: Different FPGAs for different evolutionary pressures

### Environmental Testing
**Robustness and adaptation studies**

- **Temperature variations**: Controlled thermal environments
- **Power supply modulation**: Variable voltage testing
- **EMI exposure**: Electromagnetic interference studies
- **Long-term stability**: Extended operation monitoring

## Troubleshooting

### Common Hardware Issues

**FPGA Not Recognized:**
```bash
# Check USB connection
lsusb | grep -i lattice

# Verify permissions
sudo chmod 666 /dev/ttyUSB*
```

**Programming Failures:**
- Check power supply stability
- Verify ground connections
- Ensure proper USB cable quality
- Test with known-good bitstream

**Measurement Inconsistencies:**
- Validate ADC reference voltage
- Check for ground loops
- Minimize cable lengths
- Shield analog signals

### Hardware Validation Tests

**FPGA Programming Test:**
```bash
# Create simple LED blink test
echo "module top(output LED); reg [23:0] counter; always @(posedge CLK) counter <= counter + 1; assign LED = counter[23]; endmodule" > test.v
yosys -p "synth_ice40 -top top -blif test.blif" test.v
arachne-pnr -d 1k -P tq144 test.blif -o test.txt
icepack test.txt test.bin
iceprog test.bin
```

**Arduino ADC Test:**
```cpp
// Validate ADC sampling rate
unsigned long start = micros();
for(int i = 0; i < 1000; i++) {
    int val = analogRead(A0);
}
unsigned long duration = micros() - start;
Serial.print("ADC rate: ");
Serial.print(1000000.0 * 1000 / duration);
Serial.println(" samples/sec");
```

## Safety Considerations

### Electrical Safety
- **ESD protection**: Use anti-static wrist straps
- **Power limits**: Never exceed FPGA specifications
- **Isolation**: Proper ground isolation between systems
- **Monitoring**: Continuous current and voltage monitoring

### Experimental Safety
- **Backup bitstreams**: Always maintain working configurations
- **Kill switches**: Emergency stop mechanisms
- **Data integrity**: Regular backup of experimental data
- **Documentation**: Complete setup documentation for reproducibility

## Procurement Information

### Essential Components
| Component | Vendor | Part Number | Estimated Cost |
|-----------|---------|-------------|----------------|
| iCEstick | Lattice/Digikey | ICE40HX1K-STICK-EVN | $25 |
| Arduino Uno | Arduino/Various | A000066 | $25 |
| Jumper Wires | Various | - | $10 |
| USB Cables | Various | - | $10 |
| **Total Basic Kit** | | | **~$70** |

### Recommended Additions
- Digital multimeter ($50-100)
- Basic oscilloscope ($200-500)  
- Function generator ($100-300)
- Anti-static mat and wrist strap ($20)
- High-quality jumper wires ($20)

---

*Complete hardware setup enables reproduction of all historical evolvable hardware experiments on modern, accessible platforms.*




