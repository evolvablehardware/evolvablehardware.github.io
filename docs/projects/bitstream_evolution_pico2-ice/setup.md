---
hide:
  - toc
---

# Pico2-ICE Setup

!!! warning "Use the Provided Cables"
    If you use a bad cable, the boards may not connect properly when following the instructions here: [Programming the MCU](https://pico2-ice.tinyvision.ai/md_programming__the__mcu.html)

## FAQ

### The board does not enter bootloader mode (BT to GND or SW1)

By default, if you do not hold down the **SW1** button or connect **BT to GND** when plugging in the USB cable, the board loads the default firmware which looks like this:

<figure markdown="span">
  ![default firmware](../../assets/setup/pico2ice/default_firmware.gif){ width="400" }
  <figcaption>Default firmware behavior — board is <strong>not</strong> in bootloader mode.</figcaption>
</figure>

To enter the bootloader mode, you need to either hold down the **SW1** button or connect **BT to GND** when plugging in the USB cable. The board will then enter bootloader mode which looks like this:

<figure markdown="span">
  ![bootloader mode](../../assets/setup/pico2ice/bootloader_mode.png){ width="400" }
  <figcaption>Board successfully in bootloader mode.</figcaption>
</figure>

## iCE-FARM: FPGA Array Resource Manager

We have a special job distributor for the Pico2-ICE boards. The software was developed by Jackson Heil and can be found here:

[:octicons-mark-github-16: heiljj/usbip-ice](https://github.com/heiljj/usbip-ice){ .md-button }
