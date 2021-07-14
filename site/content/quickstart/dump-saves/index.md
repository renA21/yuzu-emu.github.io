---
title: Dumping Save Files
description: A guide designed to get you started with yuzu quickly.
---

## Table of Contents

* [Introduction](../)
* [Prerequisites](../prerequisites)
* [Preparing the microSD Card](../prepare-sd-card)
* [Booting into RCM](../boot-to-rcm)
* [Booting into Hekate](../boot-to-hekate)
* [Dumping Decryption Keys](../dump-keys)
* [Backing up Switch NAND](../nand-backup)
* [Dumping System Update Firmware](../dump-firmware)
* [Dumping Games](../dump-games)
* **Dumping Save Files**
* [Rebooting the Switch Back to its Original State](../reboot-to-stock)
* [Running yuzu](../running-yuzu)
* [Mounting the microSD card to your computer in Hekate](../hekate-ums)

## Dumping Save Files (Optional)

We will now dump the games' save files from your switch to use in yuzu.

1. Download [JKSV.nro](https://github.com/J-D-K/JKSV/releases/latest)
2. Boot your Nintendo Switch into [RCM mode](../boot-to-rcm) (steps 3 to 6) and make sure it is connected to your computer.
3. Boot into [Hekate](../boot-to-hekate) (steps 2 to 3).
4. [Mount the SD card to your computer in Hekate](../hekate-ums) (steps 1 to 3).

    [comment]: # (TODO: Adapt save file dumping instructions from Checkpoint to JKSV.)
5. Navigate to your SD card drive and create a folder named `Checkpoint` within the `switch` folder of your SD card and place the `Checkpoint.nro` file inside it.
6. Once you're done, [safely eject the SD card drive in your computer and return to the Hekate Home menu.](#mounting-the-microsd-card-to-your-computer-in-hekate) (steps 5a. to 5b.)
7. Tap on `Payloads`. This will show a list of payloads.
8. Tap on `fusee-primary.bin` in the list of payloads.
9. Your Switch will launch into Custom Firmware Mode (CFW), and once your Switch has booted into the home menu, press and hold the `R` button on your controller and launch a game. This will launch the Homebrew Menu in `title override mode`.
10. Either use the touchscreen or navigate using your controller, and choose `Checkpoint`.
11. Pick the games that you want to dump their save files (multiselect with the `Y` button), and press the `L` button to backup the saves.
12. Once you have backed up the save files, press any button to return to the previous menu and then press `+` to return to the Homebrew Menu.
13. Select `Reboot to Payload` and then press `-` on your controller to return to the Hekate menu.
14. [Mount the SD card to your computer in Hekate](#mounting-the-microsd-card-to-your-computer-in-hekate) (steps 4a. to 4c.)
15. Navigate to your SD card drive. Your save files will be located in the `switch/Checkpoint` folder.
16. Follow the instructions in the [How do I add a Save to my Game](https://yuzu-emu.org/wiki/faq/#how-do-i-add-a-save-to-my-game) section of our [FAQ.](https://yuzu-emu.org/wiki/faq/)
17. Once you're done transferring your save files, [safely eject the SD card drive in your computer and return to the Hekate Home menu.](#mounting-the-microsd-card-to-your-computer-in-hekate) (steps 5a. to 5b.)
