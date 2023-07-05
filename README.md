# a7y18lte-Resources

Welcome to the a7y18lte-Resources repository! Here, you'll find resources to help customize your device experience. 

## Getting Started 

To begin, extract the `repack-boot.7z` file and flash it in the boot partition of your device.

## Fix for Brightness Slider in Android 11+ GSI

If the Brightness Slider is not working as expected, please follow the steps below:

1. Navigate to `Settings` > `PHH Treble Settings` > `Misc Features`
2. Scroll down to the **Backlight** section
3. Enable the following settings:
    - Use linear screen brightness slider
    - Force alternative backlight scale
    - Allows setting brightness to the lowest possible 

## Stock ROM 

You'll find the Android 10 Samsung OneUI 2.0 stock ROM for the device in this repository. The file is named `Stockrom-Degoogled.zip`.

### Installation
To install, download the file and flash it in recovery. Don't forget to flash the dm-verity afterwards to prevent the device from going into download mode.

**Note:** This ROM doesn't include Google Apps (GApps) by default. However, you can flash any GApps of your choice. 

We recommend using Open GApps, which can be downloaded from [here](https://opengapps.org/). 

**Recommended GApps Configuration:** ARM64 --> 10.0 --> Pico

## Recovery 

We have included both TWRP and PBRP recovery resources compatible with the latest firmware of the device. These resources won't result in the black line issue experienced in earlier versions.

You can find the recoveries [here](https://github.com/DeadPool-4422/Action-TWRP-Builder/releases).

Remember to always back up your data before performing recovery operations. Happy modding!
