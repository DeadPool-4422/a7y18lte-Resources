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
## Kernel 

We provide a new kernel file named `repack-boot.7z` which addresses several issues, including:

- Non-functional MTP in GSI
- Non-working camera and flash
- Better GSI Compatibility

This kernel was built from the source tree available at this [repository](https://github.com/AKSharma87/kernel_samsung_a7y18lte).

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

These recoveries were built from the source tree available at this [repository](https://github.com/AKSharma87/TWRP_device_samsung_a7y18lte).

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




Sure, I understand. Here's a cleaned-up and advanced section of README file containing those details.

## Advanced Section
This advanced section provides some more in-depth instructions for getting information about your device's partitioning and how to use `parted` utility to inspect and modify those partitions.

### Checking Device Block Information
You can list the block devices present on your system by running the command `ls -al /dev/block/` in the terminal. This will give you detailed information about each block device, including its permissions, ownership, and the date it was last modified.

**Example Output:**

```bash
total 0
drwxr-xr-x  4 root root     1220 2023-06-25 18:19 .
...
brw-------  1 root root 179,   0 2023-06-25 18:19 mmcblk0
brw-------  1 root root 179,   8 2023-06-25 18:19 mmcblk0boot0
...
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

Sure, here is the refined version of the section you provided:

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


After exiting the `parted` interface, you may want to utilize built-in commands for formatting partitions into different file formats. This is especially helpful if you're encountering errors like "Cannot mount /preload" in recovery. The commands shown below are intended to address this particular error, but you can adjust the partition path as needed for your circumstances.

**Formatting Partitions:**

Firstly, unmount the problematic partition with the `umount` command:

```bash
umount /dev/block/bootdevice/by-name/preload
```

Next, format the partition to the `ext4` file system using the `mke2fs` command:

```bash
mke2fs -t ext4 /dev/block/bootdevice/by-name/preload
```

Replace `/dev/block/bootdevice/by-name/preload` with the path to the partition you want to format.

**Note:** These commands carry the potential to erase data. Always remember to backup your data prior to executing these operations, and only perform these steps if you're comfortable with potential data loss. The `/dev/block/bootdevice/by-name/preload` path used in this example is specific to the "Cannot mount /preload" error. If you're looking to format a different partition, replace this path with the appropriate partition path for your device.
