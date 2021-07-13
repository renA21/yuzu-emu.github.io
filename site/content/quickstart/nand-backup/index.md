---
title: Backing up Switch NAND
description: A guide designed to get you started with yuzu quickly.
---

## Table of Contents

* [Introduction](../index.md)
* [Prerequisites](../prerequisites/index.md)
* [Preparing the microSD Card](../prepare-sd-card/index.md)
* [Booting into RCM](../boot-to-rcm/index.md)
* [Booting into Hekate](../boot-to-hekate/index.md)
* [Dumping Decryption Keys](../dump-keys/index.md)
* **Backing up Switch NAND**
* [Dumping System Update Firmware](../dump-firmware/index.md)
* [Dumping Games](../dump-games/index.md)
* [Dumping Save Files](../dump-saves/index.md)
* [Rebooting the Switch Back to its Original State](../reboot-to-stock/index.md)
* [Running yuzu](../running-yuzu/index.md)
* [Mounting the microSD card to your computer in Hekate](../hekate-ums/index.md)

## Backing up Switch NAND (Optional but Recommended)

We will now boot Hekate to dump your Switch's NAND. This step is optional, but highly recommended to ensure you have a backup of your Switch's data in its internal storage.

1. Boot your Nintendo Switch into [RCM mode](#booting-into-rcm) (steps 2c. to 2f.) and make sure it is connected to your computer.
2. Boot into [Hekate](#booting-into-hekate) (steps 3b. to 3c.)
3. When it has successfully booted into the Hekate Home menu, tap on the `Tools` tab and select `Backup eMMC`.
4. Underneath the `Full` section, tap on `eMMC BOOT0 & BOOT1`. This may take a few seconds to load. After it is finished filling the progress bar it should say `Finished and verified!`. Beneath `Filepath:` you will see the location of the dump.
5. Tap on `Close` and select `eMMC RAW GPP`. This should take some time as the Switch's `rawnand.bin` is quite large. If the progress bar appears to go backwards at some points or turn green, do not worry as this is Hekate verifying the data. This should take between 15-45 minutes depending on the quality/speed of your SD card and the default verification setting. Please keep note of the location the output file is placed.
6. Tap on `Close` two times to return to the Tools menu.
7. [Mount the SD card to your computer in Hekate](#mounting-the-microsd-card-to-your-computer-in-hekate) (steps 4b. to 4c.)
8. Navigate to your SD card drive and copy the `backup` folder to your computer.
9. Once you're done copying, [safely eject the SD card drive in your computer and return to the Hekate Home menu.](#mounting-the-microsd-card-to-your-computer-in-hekate) (steps 5a. to 5b.)
