# POS Terminal Setup

## Introduction

These instructions will guide you through the process of setting up one of the PAR POS terminals with touch capabilities. It will also list details for installing specific software relevant to the makerspace. These POS terminals only have 2 USB 2.0 ports, and lack an optical disk drive. In order to install anything through an optical DVD drive, a USB hub and USB Optical DVD Drive are required to have enough I/O for the drive, mouse, and keyboard.

## Download

1. Download whichever Linux distribution you would like to use. For these machines, a lightweight desktop is recommended. Something like Lubuntu or Ubuntu Mate

   **Create Boot media**

2. Use a USB bootable media creation tool like [https://etcher.io/](https://etcher.io/) to create a bootable usb

OR

1. Use whatever tools are available to burn the ISO to a blank DVD.

   **Boot**

   During the POS Boot up, there is a short window of time to choose \[1. Boot\] \[2. Setup\] \[3. No\]

2. Press \[1.Boot\]
3. Choose the number of the device that corresponds to the USB Optical Drive

OR

1. Press the \[delete\] key during startup to enter the main bios
2. Go to boot tab and change the hard drive priority to the bootable USB Drive
3. Go to boot order and verify that your USB is in fact the first bootable device
4. Press \[F10\] to reboot and save your changes

## Install

Follow the standard guided installation:

1. Wipe everything and use entire disk
2. check install updates during install \(requires network access\)
3. check install additional software drivers
4. User - rcl
5. Hostname - make it machine specific ex: "laser-station"

## Configure

These steps will ensure all makerspace POS terminals will provide the same interface at each station

1. Update the OS via either terminal or System &gt; Administration &gt; Software Updater
2. Reboot

### Touchscreen

[Download](https://drive.google.com/open?id=1PVsa7Y1Hx73PfP8g3j6lGAY13vjxcRs9) the Linux \(Single Touch\)\(64-bit\) Driver from 3M website

Open a terminal and enter the following commands one at a time:

```bash
 cd ~
 mkdir Documents/touchscreen_driver
 mv Downloads/touchscreen-driver-MT7.14.4.bin64 Documents/touchscreen_driver
 cd Documents/touchscreen_driver
 sudo chmod +x touchscreen-driver-MT7.14.4.bin64
 sudo ./touchscreen-driver-MT7.14.4.bin64
```

Hold the `page down` key until it stops scrolling

press `y` to blindly accept the agreement

```bash
tar xzf twscreen.7.14.4.tar.gz
cd twscreen
sudo ./Install
sudo service TWDrvStartup start
sudo service TWDrvStartup status
```

verify the service is running

Touch the screen like a child in wonderment

Don't close the terminal yet... continue to calibration section

Be careful to not delete twscreen folder. If you do it will remove the drivers and you will have to repeat these steps

### Calibration

```bash
sudo ./TwCalib
```

follow prompts on the screen to calibrate the touch functions

