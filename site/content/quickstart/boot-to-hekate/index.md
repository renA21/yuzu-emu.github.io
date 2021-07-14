---
title: Booting into Hekate
description: A guide designed to get you started with yuzu quickly.
---

## Table of Contents

* [Introduction](../)
* [Prerequisites](../prerequisites)
* [Preparing the microSD Card](../prepare-sd-card)
* [Booting into RCM](../boot-to-rcm)
* **Booting into Hekate**
* [Dumping Decryption Keys](../dump-keys)
* [Backing up Switch NAND](../nand-backup)
* [Dumping System Update Firmware](../dump-firmware)
* [Dumping Games](../dump-games)
* [Dumping Save Files](../dump-saves)
* [Rebooting the Switch Back to its Original State](../reboot-to-stock)
* [Running yuzu](../running-yuzu)
* [Mounting the microSD card to your computer in Hekate](../hekate-ums)

## Booting into Hekate

We will now boot your Nintendo Switch into Hekate, a custom bootloader.

1. Extract the `hekate_ctcaer_X.X.X.bin` file from the `hekate_ctcaer_X.X.X_Nyx_X.X.X.zip` file you downloaded from the [prerequisites section](../prerequisites) to any accessible directory on your computer.
2. Open the TegraRcmGUI window. In the `Payload` tab of TegraRcmGUI, click on the folder icon and navigate to the `hekate_ctcaer_X.X.X.bin` file you extracted earlier.

    ![Folder icon](folder_icon.png)
    ![Hekate payload selection](hekate_payload.png)
3. Click on `Inject Payload` and your Switch will boot into the Hekate menu.

    ![Hekate Home menu](hekate.png)
    **NOTE:** Upon first boot, Hekate prompts you to set the current date and time. This step is optional.

    ![Hekate Date & Time prompt](hekate_date.png)
