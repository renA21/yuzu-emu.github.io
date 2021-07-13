---
title: Dumping System Update Firmware
description: A guide designed to get you started with yuzu quickly.
---

## Table of Contents

* [Introduction](../../index.md)
* [Prerequisites](../1-prerequisites/index.md)
* [Preparing the microSD Card](../2-prepare-sd-card/index.md)
* [Booting into RCM](../3-boot-to-rcm/index.md)
* [Booting into Hekate](../4-boot-to-hekate/index.md)
* [Dumping Decryption Keys](../5-dump-keys/index.md)
* [Backing up Switch NAND](../6-nand-backup/index.md)
* **Dumping System Update Firmware**
* [Dumping Games](../8-dump-games/index.md)
* [Dumping Save Files](../9-dump-saves/index.md)
* [Rebooting the Switch Back to its Original State](../10-reboot-to-stock/index.md)
* [Running yuzu](11-running-yuzu/index.md)
* [Mounting the microSD card to your computer in Hekate](../hekate-ums/index.md)

## Dumping System Update Firmware

Some games such as `Mario Kart 8 Deluxe` require the use of files found inside the `Nintendo Switch System Update Firmware` to be playable. In this step, we will now dump the firmware files from your Switch for use in yuzu.

1. Boot your Nintendo Switch into [RCM mode](#booting-into-rcm) (steps 2c. to 2f.) and make sure it is connected to your computer.
2. Boot into [Hekate](#booting-into-hekate) (steps 3b. to 3c.)
3. When it has successfully booted into the Hekate Home menu, tap on `Payloads`. This will show a list of payloads.
4. Tap on `TegraExplorer.bin` in the list of payloads.
5. After TegraExplorer has successfully booted, navigate through the menu using the `VOL+/VOL-` buttons to highlight and select `Dump Firmware` by pressing the `POWER` button.
6. Once the dumping process is finished, the `.nca` files will be located in your SD card at `sd:/tegraexplorer/Firmware/` inside a folder with a name of the firmware revision.
7. Press any button to return to the main menu.
8. Select the `Reboot to bootloader/update.bin` option. (Alternatively, you can select the `reboot_payload.bin` option if `update.bin` is not available.) You should now be booted back into Hekate.
9. [Mount the SD card to your computer in Hekate](#mounting-the-microsd-card-to-your-computer-in-hekate) (steps 4a. to 4c.)
10. Navigate to your SD card drive and copy the contents in the firmware folder (step 8f.) to `%YUZU_DIR%/nand/system/Contents/registered`. Alternatively, you can write `%appdata%\yuzu\nand\system\Contents\registered` in the address bar of a file explorer. The `registered` folder should be full of `.nca` files.
11. Once you're done copying, [safely eject the SD card drive in your computer and return to the Hekate Home menu.](#mounting-the-microsd-card-to-your-computer-in-hekate) (steps 5a. to 5b.)
