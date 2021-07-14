---
title: Quickstart Guide
description: A guide designed to get you started with yuzu quickly.
---

## Table of Contents

* **Introduction**
  * [Hardware Requirements](#hardware-requirements)
    * [CPU](#cpu)
    * [Dedicated Graphics](#dedicated-graphics)
    * [Integrated Graphics](#integrated-graphics)
    * [RAM](#ram)
    * [Notes](#notes)
* [Prerequisites](/quickstart/prerequisites/)
* [Preparing the microSD Card](/quickstart/prepare-sd-card/)
* [Booting into RCM](/quickstart/boot-to-rcm/)
* [Booting into Hekate](/quickstart/boot-to-hekate/)
* [Dumping Decryption Keys](/quickstart/dump-keys/)
* [Backing up Switch NAND](/quickstart/nand-backup/)
* [Dumping System Update Firmware](/quickstart/dump-firmware/)
* [Dumping Games](/quickstart/dump-games/)
* [Dumping Save Files](/quickstart/dump-saves/)
* [Rebooting the Switch Back to its Original State](/quickstart/reboot-to-stock/)
* [Running yuzu](/quickstart/running-yuzu/)
* [Mounting the microSD card to your computer in Hekate](/quickstart/hekate-ums/)

## Introduction

Welcome to the Quickstart Guide! To start playing commercial games, yuzu needs a couple of system files and folders from your switch in order to play them properly.
To check if your Switch is hackable, visit <https://damota.me/ssnc/checker> and test your Switch's serial number.

<article class="message has-text-weight-semibold">
    <div class="message-body">
        <p>NOTE:</p>
        <ul>
            <li>If your Switch is patched, you will be unable to complete the following steps.</li>
            <li>The 2019 Switch revision (HAC-001(-01)/Red box) and the Switch Lite are both patched and you will not be able to complete the following steps.</li>
        </ul>
    </div>
</article>

This guide will help you copy all your system files, games, updates, and DLC from your switch to your computer and organize them in a format yuzu understands. This process should take about 60 to 90 minutes.

But first, we must determine whether your computer meets the following hardware requirements for running yuzu.

<!-- ## Downloading and Installing yuzu

{{< youtube j0fXerrGjF4 >}} -->

## Hardware Requirements

### CPU

Any x86_64 CPU with support for the FMA instruction set. 6 threads or more are recommended.

* Minimum: Intel Core i5-4430 / AMD Ryzen 3 1200

* Recommended: Intel Core i5-10400 / AMD Ryzen 5 3600

### Dedicated Graphics

OpenGL 4.6 or Vulkan 1.1 compatible hardware and drivers are mandatory. Half-float support and 4GB of VRAM are recommended.

* Minimum for Linux: NVIDIA GeForce GT 1030 2GB / AMD Radeon R7 240 2GB

* Minimum for Windows: NVIDIA GeForce GT 1030 2GB / AMD Radeon RX 550 2GB

* Recommended: NVIDIA GeForce GTX 1650 4GB / AMD Radeon RX Vega 56 8GB

### Integrated Graphics

Integrated graphics will produce very low performance. A dedicated GPU will produce better results on all scenarios.
This is only for listing iGPU support.

* Minimum for Linux: Intel HD 5300 / AMD Radeon R5 Graphics

* Minimum for Windows: Intel HD Graphics 520 / AMD Radeon Vega 3

* Recommended: Intel UHD Graphics 750 / AMD Radeon Vega 7

### RAM

Since an integrated GPU uses system RAM as its video memory (VRAM), our memory requirement in this configuration is higher.

* Minimum with dedicated graphics: 8GB

* Minimum with integrated graphics: 12GB

* Recommended: 16GB

### Notes

* Windows users are recommended to run Windows 10 1803 or newer to get the best performance.

* Our recommended specifications don't guarantee perfect performance in most games, but rather strive to provide a cost effective recommendation while still considering performance.

* Most games are playable on older Nvidia GPUs from the Fermi family (400 series) or later, but at least Pascal (1000 series) is strongly recommended.

* CPUs lacking the FMA instruction set will produce very poor results. Intel Core gen 3 series or older, AMD phenom II or older and all Pentium/Celeron/Atom CPUs will not produce optimal results.

* Mobile CPUs will not reach the same performance as their desktop counterparts due to thermal, power, and technical limitations.

* Old GCN 1.0 and GCN 2.0 Radeon GPUs on Linux require manually forcing the amdgpu kernel module.

* **GPUs must support OpenGL 4.6 & OpenGL Compatibility profile, or Vulkan 1.1 (or higher).** To find out if your GPU meets these requirements, visit <https://opengl.gpuinfo.org> or <https://vulkan.gpuinfo.org/> and check your GPU details.

Sample Image:

![GPUInfo](./gpu_info.png)

### If you need any help during this process or get a strange error during or while using yuzu, feel free to ask for help on the yuzu discord! Happy Emulating
