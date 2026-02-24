# Arduino Nano

The Arduino Nano is a compact, breadboard-friendly microcontroller board based on the Atmel ATmega328P. In the Bitstream Evolution project, a Nano-compatible clone serves as the fitness evaluation MCU: it reads the analog output of the iCEstick FPGA through its built-in 10-bit ADC, computes fitness values, and communicates results back to the host PC over USB serial.

[:octicons-link-external-16: Arduino Documentation](https://docs.arduino.cc/hardware/nano/){ .md-button .md-button--primary }
[:octicons-arrow-right-24: Hardware Setup Guide](../../projects/bitstream_evolution/setup.md){ .md-button }

## Specifications

| Feature | Details |
| --- | --- |
| **Microcontroller** | ATmega328P (8-bit AVR) |
| **Clock Speed** | 16 MHz |
| **Flash Memory** | 32 KB (2 KB used by bootloader) |
| **SRAM** | 2 KB |
| **Analog Input Pins** | 8 (10-bit ADC, 0--5V range) |
| **Digital I/O Pins** | 14 (6 with PWM) |
| **Communication** | UART, I2C, SPI |
| **USB** | Mini-B (clones often use CH340 USB-serial chip) |
| **Operating Voltage** | 5V |
| **Approximate Cost** | ~$3--10 (Nano-compatible clone) |

## Role in Bitstream Evolution

The iCEstick FPGA does not have a built-in analog-to-digital converter, so the Arduino Nano fills this role as an intermediary between the FPGA's analog output and the host PC running the evolutionary algorithm.

```
FPGA (analog output, pin 10) → Arduino A0 (ADC) → USB Serial → Host PC
```

In the standard wiring:

- **FPGA pin 10** connects to **Arduino pin A0** --- the ADC reads the evolved circuit's output voltage
- **Arduino pin D2** is bridged to **A0** --- provides a digital interrupt for pulse counting experiments
- The host PC requests fitness readings over USB serial, and the Arduino responds with ADC samples

## Why the Arduino Nano

- **10-bit ADC** --- 1024-level resolution (4.9 mV per step) is sufficient for distinguishing fitness gradients in EHW experiments
- **Breadboard-friendly** --- DIP-style pin headers plug directly into the breadboard alongside the iCEstick
- **Extremely low cost** --- Nano-compatible clones are available for ~$3--10
- **Easy to program** --- fitness evaluation firmware is straightforward to write and customize using the Arduino IDE or PlatformIO

## Project Use

The Arduino Nano is used exclusively in the [Bitstream Evolution (iCEstick)](../../projects/bitstream_evolution/setup.md) hardware setup. The newer [pico2-ice](../pico2ice/index.md) platform integrates the microcontroller (RP2350B) directly on the same board as the FPGA, eliminating the need for a separate Arduino.

!!! note "Clone Driver Note"
    Nano-compatible clones using the CH340 USB-serial chip may require a separate driver installation on some operating systems.
