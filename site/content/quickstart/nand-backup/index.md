---
title: Backing up Switch NAND
description: A guide designed to get you started with yuzu quickly.
---

## Table of Contents

* [Introduction](/quickstart/)
* [Prerequisites](/quickstart/prerequisites/)
* [Preparing the microSD Card](/quickstart/prepare-sd-card/)
* [Booting into RCM](/quickstart/boot-to-rcm/)
* [Booting into Hekate](/quickstart/boot-to-hekate/)
* [Dumping Decryption Keys](/quickstart/dump-keys/)
* [**Backing up Switch NAND**](/quickstart/nand-backup/)
* [Dumping System Update Firmware](/quickstart/dump-firmware/)
* [Dumping Games](/quickstart/dump-games/)
* [Dumping Save Files](/quickstart/dump-saves/)
* [Rebooting the Switch Back to its Original State](/quickstart/reboot-to-stock/)
* [Running yuzu](/quickstart/running-yuzu/)
* [Mounting the microSD card to your computer in Hekate](/quickstart/hekate-ums/)

## Backing up Switch NAND (Optional but Recommended)

We will now boot Hekate to dump your Switch's NAND. This step is optional, but highly recommended to ensure you have a backup of your Switch's data in its internal storage.

1. Boot your Nintendo Switch into [RCM mode](../boot-to-rcm) (steps 3 to 6) and make sure it is connected to your computer.
2. Boot into [Hekate](../boot-to-hekate) (steps 2 to 3).
3. When it has successfully booted into the Hekate Home menu, tap on the `Tools` tab and select `Backup eMMC`.
4. Underneath the `Full` section, tap on `eMMC BOOT0 & BOOT1`. This may take a few seconds to load. After it is finished filling the progress bar it should say `Finished and verified!`. Beneath `Filepath:` you will see the location of the dump.
5. Tap on `Close` and select `eMMC RAW GPP`. This should take some time as the Switch's `rawnand.bin` is quite large. If the progress bar appears to go backwards at some points or turn green, do not worry as this is Hekate verifying the data. This should take between 15-45 minutes depending on the quality/speed of your SD card and the default verification setting. Please keep note of the location the output file is placed.
6. Tap on `Close` two times to return to the Tools menu.
7. [Mount the SD card to your computer in Hekate](../hekate-ums) (steps 1 to 3).
8. Navigate to your SD card drive and copy the `backup` folder to your computer.
9. Once you're done copying, [safely eject the SD card drive in your computer and return to the Hekate Home menu](../hekate-ums) (steps 4 to 5).
