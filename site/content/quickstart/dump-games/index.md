---
title: Dumping Games
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
* [Dumping System Update Firmware](../7-dump-firmware/index.md)
* **Dumping Games**
* [Dumping Save Files](../9-dump-saves/index.md)
* [Rebooting the Switch Back to its Original State](../10-reboot-to-stock/index.md)
* [Running yuzu](11-running-yuzu/index.md)
* [Mounting the microSD card to your computer in Hekate](../hekate-ums/index.md)

## Dumping Cartridge Games

We will now dump the `NX Card Image (XCI)` file from your game cartridge(s), to use in yuzu. Insert the game cartridge of your choice.

1. Boot your Nintendo Switch into [RCM mode](#booting-into-rcm) (steps 2c. to 2f.) and make sure it is connected to your computer.
2. Boot into [Hekate](#booting-into-hekate) (steps 3b. to 3c.)
3. When it has successfully booted into the Hekate Home menu, tap on `Payloads`. This will show a list of payloads.
4. Tap on `fusee-primary.bin` in the list of payloads.
5. Your Switch will launch into Custom Firmware Mode (CFW), and once your Switch has booted into the HOME Menu, press and hold the `R` button on your controller and launch a game. This will launch the Homebrew Menu in `title override mode`.
6. Either use the touchscreen or navigate using your controller, and select `nxdumptool`.
7. Select the `Dump gamecard content` option.
8. Select the `Cartridge Image (XCI) dump` option.
9. Once the cartridge image has been dumped, press any button to return to the previous menu and then press `+` to return to the Homebrew Menu.
10. Select `Reboot to Payload` and then press `-` on your controller to return to the Hekate Home menu.
11. [Mount the SD card to your computer in Hekate](#mounting-the-microsd-card-to-your-computer-in-hekate) (steps 4a. to 4c.)
12. Navigate to your SD card drive. XCI dumps are located under `sd:/switch/nxdumptool/XCI`.
13. If your XCIs are dumped in parts with `.xc0`, `.xc1`, `.xc2`, etc extensions, use the `nxDumpMerger` tool you have downloaded in the prerequisites to assist in merging these parts into a complete XCI. If they were dumped as complete XCI files with the `.xci` extension, you can proceed to copy these to a game directory of your choice.
14. Extract the contents of `nxDumpMerger_Windows.zip` into a new folder and start the program.
15. Select the button with the triple dots `...` next to the `Input` field. This will open a file selector.
16. Find and select one of the parts and click `Open`.
17. Next, select the button with the triple dots `...` next to the `Output` field. This will open a folder selector.
18. Select a folder where you would like your games stored in your computer and then click `Select Folder`. (**NOTE:** Do not select a folder inside the SD card or you will quickly run out of space and experience slow transfer speeds in the merging process.)
19. After completing these steps, the parts are ready to be merged. Select `Merge Dump` and the program will merge the parts into a complete XCI located in the `Output` folder. Repeat these steps for all other games dumped as parts.
20. Once you're done merging, [safely eject the SD card drive in your computer and return to the Hekate Home menu.](#mounting-the-microsd-card-to-your-computer-in-hekate) (steps 5a. to 5b.)

## Dumping Installed Titles (eShop)

We will now dump the `Nintendo Submission Package (NSP)` file from your installed eShop game(s), to use in yuzu.

1. Boot your Nintendo Switch into [RCM mode](#booting-into-rcm) (steps 2c. to 2f.) and make sure it is connected to your computer.
2. Boot into [Hekate](#booting-into-hekate) (steps 3b. to 3c.)
3. When it has successfully booted into the Hekate menu, tap on `Payloads`. This will show a list of payloads.
4. Tap on `fusee-primary.bin` in the list of payloads.
5. Your Switch will launch into Custom Firmware Mode (CFW), and once your Switch has booted into the home menu, press and hold the R button on your controller and launch a game. This will launch the Homebrew Menu in `title override mode`.
6. Either use the touchscreen or navigate using your controller, and select `nxdumptool`.
7. Select the `Dump installed SD Card / eMMC Content` option.
8. Select the game you want to dump.
9. Select the `Nintendo Submission Package (NSP) dump` option.
10. If your game contains an update or DLC, you will see multiple dumping options such as `Dump base application NSP`, `Dump installed update NSP` or/and `Dump installed DLC NSP` in the next screen. Select `Dump base application NSP` to dump the base game.
11. Select the `Start NSP dump process` option and wait for the dumping process to finish.
12. Press the `B button` to return to the previous menu(s) and repeat the previous steps to dump the base, updates and DLC of all your games.
13. Once all your games are dumped, press any button to return to the previous menu and then press `+` to return to the Homebrew Menu.
14. Select `Reboot to Payload` and then press `-` on your controller to return to the Hekate Home menu.
15. [Mount the SD card to your computer in Hekate](#mounting-the-microsd-card-to-your-computer-in-hekate) (steps 4a. to 4c.)
16. Navigate to your SD card drive. NSP dumps are located under `sd:/switch/nxdumptool/NSP`.
17. If your NSPs are dumped as folders with `00`, `01`, `02`, etc parts within them, use the `nxDumpMerger` tool you have downloaded in the prerequisites to assist in merging these parts into a complete NSP. If they were dumped as files, you can proceed to copy these to a game directory of your choice.
18. Extract the contents of `nxDumpMerger` into a new folder and start the program. (Skip the extraction if you already followed step 9n.)
19. Select the button with the triple dots `...` next to the `Input` field. This will open a file selector.
20. Find a NSP that is dumped as a folder with parts. Select one of the parts within the folder and click `Open`.
21. Next, select the button with the triple dots `...` next to the `Output` field. This will open a folder selector.
22. Select a folder where you would like your games stored in your computer and then click `Select Folder`. (**NOTE:** Do not select a folder inside the SD card or you will quickly run out of space and experience slow transfer speeds in the merging process.)
23. After completing these steps, the parts are ready to be merged. Select `Merge Dump` and the program will merge the parts into a complete NSP located in the `Output` folder. Repeat these steps for all folder NSPs.
24. Once you're done merging, [safely eject the SD card drive in your computer and return to the Hekate Home menu.](#mounting-the-microsd-card-to-your-computer-in-hekate) (steps 5a. to 5b.)
