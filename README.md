# a7y18lte-Resources

Welcome to the a7y18lte-Resources repository! Here, you'll find resources that are designed to enhance and customize your device experience. 

## Getting Started 

For optimal performance and compatibility, please ensure your device is updated to the latest firmware.

## Kernel 

We have a new kernel that addresses several issues such as:

- Non-functional MTP in GSI
- Camera and flash not working

The new kernel file is named `repack-boot.7z`.

### Kernel Installation

To install the new kernel, follow the steps below:

1. Download the `repack-boot.7z` file.
2. Extract the .img file inside the .7z file.
3. Flash the extracted .img file in the boot partition of your device using recovery.

Please remember to backup your data before proceeding with the kernel installation.

## Fix for Brightness Slider in Android 11+ GSI

If the Brightness Slider isn't working as expected in Android 11 or newer versions, follow these steps:

1. Navigate to `Settings` > `PHH Treble Settings` > `Misc Features`
2. Scroll down to the **Backlight** section
3. Enable the following settings:
    - Use linear screen brightness slider
    - Force alternative backlight scale
    - Allows setting brightness to the lowest possible 

## Stock ROM 

In this repository, you'll find the de-googled version of the Android 10 Samsung OneUI 2.0 stock ROM for the device, named `Stockrom-Degoogled.zip`.

### Stock ROM Installation
To install, download the `Stockrom-Degoogled.zip` file and flash it in recovery. After that, ensure to flash the dm-verity to prevent the device from going into download mode.

**Note:** This ROM doesn't include Google Apps (GApps) by default. However, you can flash any GApps package of your choice if required.

We recommend using Open GApps, which can be downloaded from [here](https://opengapps.org/). 

**Recommended GApps Configuration:** ARM64 --> 10.0 --> Pico

## Recovery 

This repository includes both TWRP and PBRP recovery resources. They are compatible with the latest firmware of your device and won't result in the black line issues seen in earlier versions.

You can download the recoveries [here](https://github.com/DeadPool-4422/Action-TWRP-Builder/releases).

Always remember to back up your data before conducting any recovery operations. Enjoy your enhanced device experience!
