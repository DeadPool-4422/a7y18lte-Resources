# Custom Android Recovery Installation on Samsung A7 2018 (a7y18lte) 

This README provides a step-by-step guide on how to install a custom Android recovery onto a Samsung A7 2018 device using either Windows or Linux OS.

## Prerequisites

- **Device Backup:** Before proceeding, make sure you have backed up all important data from your Samsung A7 2018.
- **Samsung USB drivers (for Windows):** If you're using Windows, ensure you have the latest Samsung USB drivers installed on your computer. You can download the drivers from the [official Samsung website](https://developer.samsung.com/mobile/android-usb-driver.html).

## Download Required Files

1. **Odin (for Windows) / odin4linux (for Linux):** This is a software used on the PC to flash firmware to Samsung devices.
   - For Windows, download the latest version of Odin from [here](https://odindownload.com/download/).
   - For Linux, download `odin4linux` from [here](https://github.com/DeadPool-4422/a7y18lte-Resources).
   
2. **Custom Recovery (TWRP for a7y18lte):** Download the latest custom recovery for Samsung A7 2018 (a7y18lte) from [here](https://github.com/DeadPool-4422/Action-TWRP-Builder/releases).

## Installation Process

### Step 1: Enable Developer Options, USB Debugging and OEM Unlocking

To enable developer options:
1. Go to **Settings** -> **About phone** -> **Software information**.
2. Tap on **Build number** seven times. You will see a message saying "Developer mode has been enabled".

To enable USB debugging and OEM unlocking:
1. Go to **Settings** -> **Developer options**.
2. Scroll down to find **USB debugging** and turn it on.
3. Find **OEM unlocking** and make sure it's enabled.

### Step 2: Boot into Download Mode

1. Power off your Samsung A7 2018 device.
2. Press and hold both **Volume Up** and **Volume Down** buttons simultaneously, then connect your device to your PC using a USB cable. You should see a warning screen.
3. Press **Volume Up** to continue and enter Download mode.

### Step 3: Flash the Custom Recovery

#### Windows:
1. Extract the Odin ZIP file you downloaded earlier.
2. Run the Odin .exe file as an administrator.
3. Connect your Samsung A7 2018 device to your PC using a USB cable. Odin should display "Added!" in the Log box if your device is detected.
4. Click on the "AP" button in Odin and select the TWRP .tar file you downloaded earlier for your device.
5. Make sure only "F. Reset Time" and "Auto Reboot" are checked in the options.
6. Click "Start" to begin the flashing process. Odin will display "PASS!" once the process is successful.

#### Linux:
1. Download `odin4linux` from the [resources repository](https://github.com/DeadPool-4422/a7y18lte-Resources).
2. Set up your Linux system to detect your device by creating a `51-android.rules` file in `/etc/udev/rules.d/` and adding the following line to the file: 
    ```
    SUBSYSTEM=="usb", ATTR{idVendor}=="04e8", MODE="0666", GROUP="plugdev"
    ```
    Refer to the [Android Developers guide](http://developer.android.com/tools/device.html) for more information. 
3. Unload the `cdc_acm` module by running `sudo rmmod cdc_acm` in the terminal.
4. Connect your Samsung A7 2018 device to your Linux machine.
5. Run `odin4 -a <PATH_TO_TWRP_FILE>` in the terminal, replacing `<PATH_TO_TWRP_FILE>` with the path to your downloaded TWRP file. This begins the flashing process.

### Step 4: Boot into Custom Recovery

1. Once the flash is successful, disconnect your Samsung A7 2018 device.
2. Immediately boot into recovery mode by holding down the **Volume Up** + **Power** buttons.
3. You should now boot into the custom recovery you installed.

Congratulations, you have successfully installed a custom Android recovery on your Samsung A7 2018 device!

## Disclaimer

Please note that flashing a custom recovery may void your warranty and potentially brick your device. Proceed with caution and always ensure you have a backup of your data. This guide is to be followed at your own risk. The developers and I are not responsible for any damage that may occur from following this guide.

## Support

If you encounter issues or have questions, feel free to submit a new [issue](https://github.com/DeadPool-4422/Action-TWRP-Builder/issues) on our GitHub repository.
