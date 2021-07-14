---
title: Dumping Decryption Keys
description: A guide designed to get you started with yuzu quickly.
---

## Table of Contents

* [Introduction](/quickstart/)
* [Prerequisites](/quickstart/prerequisites/)
* [Preparing the microSD Card](/quickstart/prepare-sd-card/)
* [Booting into RCM](/quickstart/boot-to-rcm/)
* [Booting into Hekate](/quickstart/boot-to-hekate/)
* [**Dumping Decryption Keys**](/quickstart/dump-keys/)
* [Backing up Switch NAND](/quickstart/nand-backup/)
* [Dumping System Update Firmware](/quickstart/dump-firmware/)
* [Dumping Games](/quickstart/dump-games/)
* [Dumping Save Files](/quickstart/dump-saves/)
* [Rebooting the Switch Back to its Original State](/quickstart/reboot-to-stock/)
* [Running yuzu](/quickstart/running-yuzu/)
* [Mounting the microSD card to your computer in Hekate](/quickstart/hekate-ums/)

## Dumping Decryption Keys

We will now dump your `prod.keys` and `title.keys` for decryption of your game files.

1. From the Hekate Home menu, tap on `Payloads`.

    ![Payloads option](payloads_option.png)
2. Tap on `Lockpick_RCM.bin` in the list of payloads.

    ![Lockpick_RCM selection](lockpick.png)
3. After Lockpick_RCM has successfully booted, hold your console vertically. The screen should show an interface like this:

    ![Dump from SysNAND](dump_sysnand.png)

    **NOTE:** As of the Switch's `12.1.0` System Update, `Key generation`  should be at level `11`. If a lower level is shown, select the `Reboot (OFW)` option instead and [update the console to the latest version.](https://en-americas-support.nintendo.com/app/answers/detail/a_id/22418/~/how-to-perform-a-system-update) Once the Switch is up to date, start from the [Booting into RCM](../boot-to-rcm) section.
4. Press the `POWER` button to select `Dump from SysNAND`.
5. Lockpick_RCM will now automatically boot to `sept` and start deriving the keys. Wait for it to finish deriving the keys.
6. After Lockpick_RCM has finished deriving the keys, please make note of the location of the key files. Default is: `sd:/switch/prod.keys` and `sd:/switch/title.keys`.

    ![Key derivation](key_derivation.png)

    If things went well, Lockpick_RCM should output a message of `Found through master_key_0B`. If this is not the case, refer to the NOTE in step 3.
7. Press any button to return to the menu, then navigate with the `VOL+/VOL-` buttons to highlight and select `Payloads...` by pressing the `POWER` button.
8. Select `reboot_payload.bin` from the list of payloads. You should now be booted back into Hekate.
9. [Mount the microSD card to your computer in Hekate](../hekate-ums) (steps 1 to 3).
10. Navigate to your SD card drive and copy both `prod.keys` and `title.keys` to the `%YUZU_DIR%/keys` directory.
11. Once you're done copying, [safely eject the SD card drive in your computer and return to the Hekate Home menu](../hekate-ums) (steps 4 to 5).
