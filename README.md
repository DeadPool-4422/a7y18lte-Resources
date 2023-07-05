# a7y18lte-Resources

## Disclaimer

By using the resources provided in this repository, you understand and accept that I am not responsible for any damages or issues that may arise from the use of these resources. Moreover, you also understand that using these advanced resources may void your device's warranty.

## Introduction

Welcome to the a7y18lte-Resources repository! Here you will find resources that are designed to enhance and customize your device experience. 

## Getting Started 

This repository's resources are compatible with a variety of devices owing to their identical processor and structure. The supported devices are as follows:

- SM-A750F / Galaxy A7
- SM-A750FN / Galaxy A7 (2018)
- SM-A750G / Galaxy A7 0
- SM-A750GN / Galaxy A7
- SM-A750N / Galaxy A7
- SM-A750C / Galaxy A7

To ensure optimal performance and compatibility, update your device to the latest firmware. You can download the latest firmware from [here](https://samfw.com/).

## Kernel 

We provide a new kernel file named `repack-boot.7z` which addresses several issues, including:

- Non-functional MTP in GSI
- Non-working camera and flash

### Kernel Installation

To install the new kernel, perform the following steps:

1. Download `repack-boot.7z`.
2. Extract the .img file inside the .7z file.
3. Flash the extracted .img file in the boot partition of your device using recovery.

Please remember to back up your data before proceeding with the kernel installation.

### Original Kernel

The original kernel of the OneUI 2.0 is also included in this repository for future reference and use, if needed. It's named `stock-boot.7z` and can be installed following the same steps as for `repack-boot.7z`.

## Stock ROM 

This repository includes a de-googled version of the Android 10 Samsung OneUI 2.0 stock ROM for the device, named `Stockrom-Degoogled.zip`.

### Stock ROM Installation

To install the Stock ROM, perform the following steps:

1. Download `Stockrom-Degoogled.zip`.
2. Flash it in recovery.
3. After that, ensure to flash the dm-verity to prevent the device from going into download mode.

**Note:** This ROM does not include Google Apps (GApps) by default. You can flash any GApps package of your choice if required.

We recommend using Open GApps, which can be downloaded from [here](https://opengapps.org/). 

**Recommended GApps Configuration:** ARM64 --> 10.0 --> Pico

## Recovery 

This repository includes TWRP and PBRP recovery resources that are compatible with the latest firmware of your device and prevent the black line issues encountered with earlier versions.

You can download the recoveries from [this link](https://github.com/DeadPool-4422/Action-TWRP-Builder/releases).

Always back up your data before conducting any recovery operations.

## Recommended GSIs

We recommend the following GSIs to enhance your device experience:

- [TrebleDroid](https://github.com/TrebleDroid/treble_experimentations): Use `system-arm64-ab-vndklite-vanilla.img.xz`.
- [/e/ OS GSI](https://doc.e.foundation/support-topics/install-GSI): Use `system-arm64-ab.img.xz`.

## Miscellaneous

### Fix for Brightness Slider in Android 11+ GSI

If the Brightness Slider is not working as expected in Android 11 or newer versions, perform the following steps:

1. Navigate to `Settings` > `PHH Treble Settings` > `Misc Features`.
2. Scroll down to the **Backlight** section.
3. Enable the following settings:
   - Use linear screen brightness slider
   - Force alternative backlight scale
   - Allows setting brightness to the lowest possible

# Caution #
Remember to always back up your data before conducting any recovery operations. Enjoy your enhanced device experience!

--------------------------------------------------------------------------------
|                                                                              |
|                     Enjoy your enhanced device experience!                   |
|                                                                              |
--------------------------------------------------------------------------------
