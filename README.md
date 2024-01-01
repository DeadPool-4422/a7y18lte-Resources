# a7y18lte-Resources

## Disclaimer

By using the resources provided in this repository, you understand and accept that I am not responsible for any damages or issues that may arise from the use of these resources. Moreover, you also understand that using these advanced resources may void your device's warranty.

## Introduction

Welcome to the a7y18lte-Resources repository! Here you will find resources that are designed to enhance and customize your device experience. 

## Getting Started 

This repository's resources are compatible with a variety of devices owing to their identical processor and structure. The supported devices are as follows:

- SM-A750F / Galaxy A7
- SM-A750FN / Galaxy A7 (2018)
- SM-A750G / Galaxy A7
- SM-A750GN / Galaxy A7
- SM-A750N / Galaxy A7
- SM-A750C / Galaxy A7

Please note that these different model names represent the various regions in which the device was launched, and not differences in software resources.

To ensure optimal performance and compatibility, update your device to the latest firmware. You can download the latest firmware from [here](https://samfw.com/).

### Kernel Installation

To install the new kernel, perform the following steps:

1. Navigate to the [Releases](https://github.com/DeadPool-4422/kernel_samsung_a7y18lte/releases) page of the repository.
2. Download the `boot.img` file from the most recent release.
3. Flash the downloaded `boot.img` file in the boot partition of your device using recovery.

Please remember to back up your data before proceeding with the kernel installation.

### Original Kernel

The original kernel of the OneUI 2.0 is also included in this repository for future reference and use, if needed. It's named `stock-boot.7z`. Here are the steps to install it:

1. Download `stock-boot.7z`.
2. Extract the boot.img file inside the .7z file.
3. Flash the extracted boot.img file in the boot partition of your device using recovery.

Please remember to back up your data before proceeding with the kernel installation.

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

Note : - The zips seem to be failing to install use the recovery.img instead to install the recoveries instead

These recoveries were built from the source tree available at this [repository](https://github.com/AKSharma87/TWRP_device_samsung_a7y18lte).

### Recovery Installation

To install the custom recovery, follow the instructions detailed in this [guide](https://github.com/DeadPool-4422/a7y18lte-Resources/blob/main/install-recovery.md).

Always back up your data before conducting any recovery operations.

## Recommended GSIs and Installation Guide for A7 2018 (a7y18lte)

Enhance your device experience with our recommended Generic System Images (GSIs).

### Recommended GSIs:

1. **TrebleDroid**: A versatile GSI for various devices.
   - **Download**: [TrebleDroid Repository](https://github.com/TrebleDroid/treble_experimentations)
   - **Image File**: `system-arm64-ab-vndklite-vanilla.img.xz`

2. **/e/ OS GSI**: Privacy-centric Android OS.
   - **Download**: [/e/ OS GSI Documentation](https://doc.e.foundation/support-topics/install-GSI)
   - **Image File**: `system-arm64-ab.img.xz`

3. **LineageOS GSI**: A popular open-source operating system.
   - **Download**: [LineageOS GSI SourceForge](https://sourceforge.net/projects/andyyan-gsi/files/)
   - **Image File**: Look for `arm64-b??` files

### Pre-Installation Requirement:

Ensure that you have a stock ROM flashed on your device. If not, download and flash the provided [stock-Degoogled ROM](https://github.com/DeadPool-4422/a7y18lte-Resources/blob/main/stock-Degoogled.zip) from this repository.

### Entering Recovery Mode:

- **If the device is turned off**: Hold the Power and Volume Up buttons simultaneously.
- **If the device is turned on**: Hold the Power and Volume Down buttons. As soon as the screen goes dark, switch to holding the Power and Volume Up buttons.

### Installation Steps:

1. **Flash Stock ROM**: If you don't already have a stock ROM, flash the provided `stock-Degoogled.zip` first.

2. **Extract GSI Image**: GSI images are often compressed (`.xz` format). Extract the `.img` file from the downloaded GSI package.

3. **Flash GSI**: Use the recovery mode to flash the extracted `.img` file. When prompted, select the 'system' partition for installation.

## Upgrading to the Latest Magisk Version on `a7y18lte`

Due to specific requirements for the `a7y18lte` device, direct flashing of the latest Magisk versions from recovery is not supported , instead you'll get a bootloop unless you follow the below steps to get the latest magisk version (26.1 while writing) working . Follow this step-by-step guide to upgrade from version 21.4:

### 1. Flash Magisk 21.4 via Recovery
Start by flashing Magisk version 21.4 through your recovery. You can get the  Magisk 21.4 from [this link](https://github.com/topjohnwu/Magisk/releases/download/v21.4/Magisk-v21.4.zip). Note - rename apk to zip if it doesn't shows up in recovery. Once this is done, boot your device normally.

### 2. Download & Install the Latest Magisk App
After booting, download and install the [Magisk APK](https://github.com/topjohnwu/Magisk/releases). This app will facilitate the upgrade to the latest Magisk version.

### 3. Upgrade Magisk Through the App
- Launch the Magisk app you just installed.
- Tap on the "`Update`" button.
- Choose the "`Direct Install (Recommended)`" > "`Let's Go`".
- Allow the process to complete, as the app will install the latest Magisk version.

### 4. Reboot Your Device
After the installation completes, tap on the "Reboot" button.

**Congratulations! 🎉**

Your `a7y18lte` device is now running the latest version of Magisk!

> **Note:** Always ensure you have adequate backups before making system-level modifications to your device. Enjoy the latest Magisk features on your `a7y18lte`!

## Miscellaneous

### Fix for Brightness Slider in Android 11+ GSI

If the Brightness Slider is not working as expected in Android 11 or newer versions, perform the following steps:

1. Navigate to `Settings` > `PHH Treble Settings` > `Misc Features`.
2. Scroll down to the **Backlight** section.
3. Enable the following settings:
   - Use linear screen brightness slider
   - Force alternative backlight scale
   - Allows setting brightness to the lowest possible
4. Reboot the Device

### "Cannot mount /preload" Error

If you encounter the "Cannot mount /preload" error in recovery, please refer to the [Resolving Cannot Mount Preload Error in Recovery](#resolving-cannot-mount-preload-error-in-recovery) section for detailed steps on how to rectify this issue. Please proceed with caution as these steps involve partition formatting which could lead to data loss. Always ensure to take a backup of your data before performing these operations.

# Caution 

Remember to always back up your data before conducting any recovery operations. Enjoy your enhanced device experience!

---

|                                                        |
|:------------------------------------------------------:|
|    ⚡️ **Enjoy your enhanced device experience** ⚡️    |
|                                                        |

---

⚠️🔩 **Advanced Section** 🔩⚠️

This section is for advanced users and involves procedures that carry the risk of data loss or damage to your device. Always proceed with caution and ensure you have a reliable backup of your data. 

Here, we provide in-depth instructions for obtaining information about your device's partitioning and using the `parted` utility to inspect and modify those partitions. Proceed only if you are comfortable with advanced operations and have adequately backed up your data.

### Checking Device Block Information
You can list the block devices present on your system by running the command `ls -al /dev/block/` in the terminal. This will give you detailed information about each block device, including its permissions, ownership, and the date it was last modified.

**Example Output:**

```bash
total 0
drwxr-xr-x  4 root root     1220 2023-06-25 18:19 .
drwxr-xr-x 10 root root     3320 2023-06-25 18:19 ..
drwxr-xr-x  2 root root      600 2023-06-25 18:19 by-name
brw-------  1 root root   7,   0 2023-06-25 18:19 loop0
brw-------  1 root root   7,   1 2023-06-25 18:19 loop1
brw-------  1 root root   7,   2 2023-06-25 18:19 loop2
brw-------  1 root root   7,   3 2023-06-25 18:19 loop3
brw-------  1 root root   7,   4 2023-06-25 18:19 loop4
brw-------  1 root root   7,   5 2023-06-25 18:19 loop5
brw-------  1 root root   7,   6 2023-06-25 18:19 loop6
brw-------  1 root root   7,   7 2023-06-25 18:19 loop7
brw-------  1 root root 179,   0 2023-06-25 18:19 mmcblk0
brw-------  1 root root 179,   8 2023-06-25 18:19 mmcblk0boot0
brw-------  1 root root 179,  16 2023-06-25 18:19 mmcblk0boot1
brw-------  1 root root 179,   1 2023-06-25 18:19 mmcblk0p1
brw-------  1 root root 259,   2 2023-06-25 18:19 mmcblk0p10
brw-------  1 root root 259,   3 2023-06-25 18:19 mmcblk0p11
brw-------  1 root root 259,   4 2023-06-25 18:19 mmcblk0p12
brw-------  1 root root 259,   5 2023-06-25 18:19 mmcblk0p13
brw-------  1 root root 259,   6 2023-06-25 18:19 mmcblk0p14
brw-------  1 root root 259,   7 2023-06-25 18:19 mmcblk0p15
brw-------  1 root root 259,   8 2023-06-25 18:19 mmcblk0p16
brw-------  1 root root 259,   9 2023-06-25 18:19 mmcblk0p17
brw-------  1 root root 259,  10 2023-06-25 18:19 mmcblk0p18
brw-------  1 root root 259,  11 2023-06-25 18:19 mmcblk0p19
brw-------  1 root root 179,   2 2023-06-25 18:19 mmcblk0p2
brw-------  1 root root 259,  12 2023-06-25 18:20 mmcblk0p20
brw-------  1 root root 259,  13 2023-06-25 18:19 mmcblk0p21
brw-------  1 root root 259,  14 2023-06-25 18:19 mmcblk0p22
brw-------  1 root root 259,  15 2023-06-25 18:19 mmcblk0p23
brw-------  1 root root 259,  16 2023-06-25 18:19 mmcblk0p24
brw-------  1 root root 259,  17 2023-06-25 18:19 mmcblk0p25
brw-------  1 root root 259,  18 2023-06-25 18:19 mmcblk0p26
brw-------  1 root root 259,  19 2023-06-25 18:19 mmcblk0p27
brw-------  1 root root 259,  20 2023-06-25 18:19 mmcblk0p28
brw-------  1 root root 179,   3 2023-06-25 18:19 mmcblk0p3
brw-------  1 root root 179,   4 2023-06-25 18:19 mmcblk0p4
brw-------  1 root root 179,   5 2023-06-25 18:19 mmcblk0p5
brw-------  1 root root 179,   6 2023-06-25 18:19 mmcblk0p6
brw-------  1 root root 179,   7 2023-06-25 18:19 mmcblk0p7
brw-------  1 root root 259,   0 2023-06-25 18:19 mmcblk0p8
brw-------  1 root root 259,   1 2023-06-25 18:19 mmcblk0p9
brw-------  1 root root 179,  24 2023-06-25 18:19 mmcblk0rpmb
drwxr-xr-x  3 root root       60 2023-06-25 18:19 platform
brw-------  1 root root   1,   0 2023-06-25 18:19 ram0
brw-------  1 root root   1,   1 2023-06-25 18:19 ram1
brw-------  1 root root   1,  10 2023-06-25 18:19 ram10
brw-------  1 root root   1,  11 2023-06-25 18:19 ram11
brw-------  1 root root   1,  12 2023-06-25 18:19 ram12
brw-------  1 root root   1,  13 2023-06-25 18:19 ram13
brw-------  1 root root   1,  14 2023-06-25 18:19 ram14
brw-------  1 root root   1,  15 2023-06-25 18:19 ram15
brw-------  1 root root   1,   2 2023-06-25 18:19 ram2
brw-------  1 root root   1,   3 2023-06-25 18:19 ram3
brw-------  1 root root   1,   4 2023-06-25 18:19 ram4
brw-------  1 root root   1,   5 2023-06-25 18:19 ram5
brw-------  1 root root   1,   6 2023-06-25 18:19 ram6
brw-------  1 root root   1,   7 2023-06-25 18:19 ram7
brw-------  1 root root   1,   8 2023-06-25 18:19 ram8
brw-------  1 root root   1,   9 2023-06-25 18:19 ram9
brw-------  1 root root 253,   0 2023-06-25 18:19 vnswap0
```
Each line represents a block device. The series of characters at the start represent the permissions, the first number is the major number, and the second is the minor number.

### Using `parted` utility
`parted` is a utility for manipulating disk partitions. It supports multiple partition table formats, including MBR and GPT.

You can download `parted` and other partition tools from the repo itself. Look for the file named `parted_gdisk_fdisk_mkfs-ext4-aarch64.zip` and extract `parted` from it.

**Steps:**

1. Extract the `parted` binary:

```bash
7z x parted_gdisk_fdisk_mkfs.ext4-AARCH64.zip
cd parted_gdisk_fdisk_mkfs.ext4-AARCH64
```

2. Transfer `parted` to your device using ADB:

```bash
adb push parted /parted
```

Once `parted` is transferred to your device, it can be executed from the recovery terminal. To do so, type `parted` followed by the partition block that you wish to interact with. For example:

```bash
parted /dev/block/mmcblk0
```

Upon initiating `parted`, the `(parted)` prompt will appear. Here, you can manage your device's partitions. To view the partition table, enter 'print' at the `(parted)` prompt. This will display the partition layout of the specified block device.

**Example Output:**

```bash
GNU Parted 1.8.8.1.179-aef3

Using /dev/block/mmcblk0

Welcome to GNU Parted! Type 'help' to view a list of commands.

(parted) print

Model: MMC DUTA42 (sd/mmc)

Disk /dev/block/mmcblk0: 125GB

Sector size (logical/physical): 512B/512B

Partition Table: gpt

  

Number  Start   End     Size    File system  Name        Flags

 1      4194kB  8389kB  4194kB               BOTA0

 2      8389kB  12.6MB  4194kB               NA

 3      12.6MB  33.6MB  21.0MB  ext4         EFS

 4      33.6MB  41.9MB  8389kB  ext4         CPEFS

 5      41.9MB  50.3MB  8389kB               CM

 6      50.3MB  54.5MB  4194kB               m9kefs1

 7      54.5MB  58.7MB  4194kB               m9kefs2

 8      58.7MB  62.9MB  4194kB               m9kefs3

 9      62.9MB  64.0MB  1049kB               NAD_REFER

10      64.0MB  72.4MB  8389kB               PARAM

11      72.4MB  106MB   33.6MB               BOOT

12      106MB   146MB   39.8MB               RECOVERY

13      146MB   150MB   4194kB               DTBO

14      150MB   158MB   8389kB               BOTA1

15      158MB   159MB   1049kB               MISC

16      159MB   207MB   47.2MB               RADIO

17      207MB   207MB   524kB                PERSISTENT

18      207MB   211MB   4194kB               STEADY

19      211MB   218MB   6816kB               RESERVED2

20      218MB   4312MB  4094MB  ext4         SYSTEM

21      4312MB  4832MB  520MB   ext4         VENDOR

22      4832MB  5402MB  570MB   ext4         ODM

23      5402MB  5664MB  262MB   ext4         CACHE

24      5664MB  5769MB  105MB   ext4         HIDDEN

25      5769MB  5822MB  52.4MB  ext4         OMR

26      5822MB  5827MB  5243kB               CP_DEBUG

27      5827MB  5848MB  21.0MB               NAD_FW

28      5848MB  125GB   119GB                USERDATA  
```

Should you need additional guidance or accidentally enter an incorrect command, the `help` command can be used. This provides a list of all commands along with a brief description of their functionality.

**Example Usage and Output of the Help Command:**

```bash
(parted) help
 check NUMBER                            do a simple check on the file system
 cp [FROM-DEVICE] FROM-NUMBER TO-NUMBER  copy file system to another partition
 help [COMMAND]                          print general help, or help on COMMAND
 mklabel,mktable LABEL-TYPE              create a new disklabel (partition table)
 mkfs NUMBER FS-TYPE                     make a FS-TYPE file system on partition NUMBER
 mkpart PART-TYPE [FS-TYPE] START END    make a partition
 mkpartfs PART-TYPE FS-TYPE START END    make a partition with a file system
 move NUMBER START END                   move partition NUMBER
 name NUMBER NAME                        name partition NUMBER as NAME
 print [devices|free|list,all|NUMBER]    display the partition table, available devices, free space, all found partitions, or a particular partition
 quit                                    exit program
 rescue START END                        rescue a lost partition near START and END
 resize NUMBER START END                 resize partition NUMBER and its file system
 rm NUMBER                               delete partition NUMBER
 select DEVICE                           choose the device to edit
 set NUMBER FLAG STATE                   change the FLAG on partition NUMBER
 toggle [NUMBER [FLAG]]                  toggle the state of FLAG on partition NUMBER
 unit UNIT                               set the default unit to UNIT
 version                                 display the version number and copyright information of GNU Parted
(parted) quit
```

To exit the `parted` interface, simply type 'quit' at the `(parted)` prompt.

After exiting the `parted` interface, you may want to utilize built-in commands for formatting partitions into different file formats. This is particularly useful if you're experiencing specific errors during recovery, such as the "Cannot mount /preload" error.

## Resolving "Cannot mount /preload" Error in Recovery

This section offers steps to resolve the "Cannot mount /preload" error often encountered during recovery. 

🚨 **Important: The following steps involve partition formatting, which can cause data loss. It's crucial to back up your data before performing these operations. Proceed with extreme caution.** 🚨

**Formatting Partitions:**

1. Unmount the problematic partition using the `umount` command:

    ```bash
    umount /dev/block/bootdevice/by-name/preload
    ```

2. Format the partition to the `ext4` file system using the `mke2fs` command:

    ```bash
    mke2fs -t ext4 /dev/block/bootdevice/by-name/preload
    ```

Should you encounter a similar error with a different partition, you can use the same process. However, replace `/dev/block/bootdevice/by-name/preload` with the path corresponding to the partition causing the error.

**Note:** Again, these operations can lead to data loss. Please ensure all valuable data is backed up before proceeding. The `/dev/block/bootdevice/by-name/preload` path used in this example is specific to the "Cannot mount /preload" error. If you're experiencing issues with a different partition, replace this path with the relevant partition path for your device.

