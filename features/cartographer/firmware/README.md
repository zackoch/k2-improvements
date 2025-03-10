# Cartographer Firmware

## NOTE

It is best if you only have one Cartographer (or similar USB 3d printer accessory) attached to the system you are using for flashing.  As the VID:PID combination for the Cartographer is not unique, as indicated from this `lsusb` output:

```raw
Bus 001 Device 017: ID 1d50:614e OpenMoko, Inc. stm32f446xx
Bus 001 Device 016: ID 1d50:614e OpenMoko, Inc. stm32g0b1xx
Bus 001 Device 015: ID 1d50:614e OpenMoko, Inc.
```

## Linux

The linux flash script is provided by JaminCollins and is suitable to run on Debian and Ubuntu OS's, this can be a bootable live usb if necessary.

1. Connect the Cartographer via the supplied USB cable
2. Open terminal and download the script by running the following in a terminal:

    ```bash
    wget https://raw.githubusercontent.com/jamincollins/k2-improvements/refs/heads/main/features/cartographer/firmware/flash.sh
    ```

3. Run script by entering `bash ./flash.sh` in the terminal and hitting enter

The script should automatically do everything and leave you with a flashed Cartographer.

## Windows Install

The Windows installation is a modified version of the above provided by bigadz and can be run on Windows using WSL2 Ubuntu and usbipd-win. This was tested using Ubuntu 20.04 under WSL2 and usbipd-win 4.4.0 however latest version should be fine.

1. Install [Ubuntu WSL2](https://documentation.ubuntu.com/wsl/en/latest/howto/install-ubuntu-wsl2/)
2. Install [usbipd-win msi installer](https://github.com/dorssel/usbipd-win/releases)
3. Connect the Cartographer via the supplied USB cable
4. Open Ubuntu WSL (as Administrator) and download the flash script by entering

    ```bash
    wget https://raw.githubusercontent.com/jamincollins/k2-improvements/refs/heads/main/features/cartographer/firmware/WSLFlash.sh
    ```

5. Run the script by entering `bash ./WSLFlash.sh` in the terminal and hitting enter

The script should automatically do everything and leave you with a flashed Cartographer.
