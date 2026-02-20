

# Warnings

## Use the provided cables, if you use a bad cable, the boards may not connect properly when following the instructions here: https://pico2-ice.tinyvision.ai/md_programming__the__mcu.html

# FAQ

## No matter whether I use the BT to GND or sw1, the board does not enter the bootloader mode

* By default if you do not hold down the sw1 button or connect the BT to GND when plugging in the USB cable, the board load the default firmware which looks like this: 
  ![default firmware](../../assets/setup/pico2ice/default_firmware.gif){ width="50%" }

* To enter the bootloader mode, you need to either hold down the sw1 button or connect the BT to GND when plugging in the USB cable, then the board will enter the bootloader mode which looks like this:
    ![bootloader mode](../../assets/setup/pico2ice/bootloader_mode.png){ width="50%" }


    # We have a special job distributor for the Pico2-ICE boards, the software was developed by Jackson Heil and can be found here:
    https://github.com/heiljj/usbip-ice

iCE-FARM - FPGA Array for Rapid Measurement OR FPGA Array for Resource Management    