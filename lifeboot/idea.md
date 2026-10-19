---
title: Lifeboot (Wii Brick Protection)
permalink: /wii/lifeboot
---

Lifeboot would provide amazing BootMii-as-boot2-level brick protection for all Wiis, including the Wii Mini. It works by using [nandboot](https://wiki.raregamingdump.ca/index.php?title=boot2#nandboot), which has a valid signature that boot1 will accept.

## Installer
When you open the installer from the Homebrew Channel, it would work like this:

1. Ask the user to make a NAND backup.
1. Automatically back up any data already at NAND pages 0x80-0xAF.
1. Automatically back up any IOS211 that's already installed (if there is one).
1. Ask user to confirm installation.
1. Install the Lifeboot boot program to NAND pages 0x80-0xAF.
1. Install Lifeboot IOS as IOS211.
1. Check system to make sure everything is ready and compatible.
1. Warn user about bricks from power failure when installing a new boot2.
1. Automatically back up SEEPROM and boot2.
1. Set boot2 version byte to 0 in SEEPROM (to make boot1 accept it).
1. Install nandboot.
1. Verify that everything was installed correctly.

## Lifeboot Boot Program
This is what gets loaded by nandboot. It's mostly a workaround for not being able to use a custom boot2. It uses [MINI](https://wiibrew.org/wiki/MINI) and has very basic code. All it does is boot into Lifeboot IOS. However, if it finds a file called `rescue.dol` or `rescue.elf` on the root of an inserted SD card, it will immediately boot that file instead of Lifeboot IOS. This is used in the rare case that Lifeboot IOS gets corrupted.

Lifeboot IOS is much more likely to get corrupted than the boot program because the boot program is designed to be almost never updated. However, Lifeboot IOS could receive updates, and it's also installed as IOS211, which can be easily overwritten by the user.

If the user is using a Wii Mini (or doesn't have access to an SD card), they can use **Disc Boot Mode** to fix a broken IOS211.

### Disc Boot Mode
If you hold down the POWER and EJECT buttons while turning on your Wii, the Lifeboot boot program will enter Disc Boot Mode. In this state, you can boot any Wii or GameCube disc, and if your drive is compatible, you can also load a DOL or ELF file from a burned DVD.

On the Wii Mini, you would instead hold down the POWER button while the disc tray is open.

## Flowchart
[Click here](../lifeboot/Boot%20Process%20Flowchart.png) to see a flowchart of the Wii's boot process with Lifeboot installed.

## Lifeboot IOS
This is similar to BootMii. When it loads, it looks for a config file on the SD card or USB drive, which tells it what to do next. By default, the autoboot setting is enabled, causing it to simply load the Wii Menu normally. If the autoboot setting is disabled, the Lifeboot Menu will open whenever the console is turned on. If there is no SD card or USB drive, it will just open the Wii Menu.

Holding down the space bar on a USB keyboard or holding the A, B, X, Y, and Z buttons on a GameCube controller in port 4 will force Lifeboot IOS to ignore the autoboot setting and open the Lifeboot Menu.

## Lifeboot Menu
There are 2 ways to access this menu:

- Through Lifeboot IOS (when autoboot is disabled or bypassed)
- By running a "Lifeboot Menu Loader" homebrew app

The Lifeboot Menu would be navigated using the console's POWER and RESET buttons. On a Wii Mini, there's no RESET button, so you would instead hold the POWER button for a half-second to confirm your menu selection.\
You would also be able to navigate it using a USB keyboard or GameCube controller.

### Menu Options

- **Wii Menu**
- **Homebrew Channel**
- **Load DOL/ELF**
  - SD:/boot.dol
  - SD:/boot.elf
  - USB:/boot.dol
  - USB:/boot.elf
  - USB:/bootmini.dol
  - USB:/bootmini.elf
  - File Browser
- **Useful Apps** (See table below for details)
- **NAND Manager**
  - BootMii IOS
  - nanddumper@IOS
  - Emergency Tool
    - Backup (SD)
    - Backup (USB)
    - Restore (SD)
    - Restore (USB)
- **Config Editor**

### Homebrew App Shortcuts
The _Useful Apps_ option in the menu opens a sub-menu with a list of homebrew apps that can be used to recover from a brick. A few important apps are stored in a special location in the NAND, in case the SD card or USB drive won't work. Loading is attempted from SD, then USB, then NAND (if it's saved to the NAND).\
This menu is mostly for convenience when you already have a homebrew app on your storage device, allowing you to skip copying the `boot.dol` file to the root directory.

|Homebrew App|Stored in NAND?|
|---|---|
|HackMii Installer|No|
|YAWM ModMii Edition|Yes|
|SysCheck ModMii Edition|No|
|Priiloader Installer|No|
|Any Region Changer ME|Yes|
|WiiXplorer-SS|No|
|KoreanKii|No|
|nanddumper@IOS|No|
|Dump Mii NAND|No|
|SEEPROM Viewer|Yes|
|csm-installer|No|
|Wii Mod Lite|No|

### Emergency NAND Manager
Mainly used for restoring NAND backups when BootMii is unavailable. Uses a GameCube controller or USB keyboard for Konami code input.

## Challenges
There's a major roadblock preventing this idea from being created and widely used: nandboot is copyrighted content, and the homebrew community won't want to distribute it. Even if it was an independent project, the homebrew community wouldn't recommend using it.

I don't know what the specific DMCA laws are, and I don't know how nandboot could be legally distributed. It would need to use some kind of indirect distribution or something that exploits a loophole. I've heard that console hacking is perfectly legal for repairs (it's only legally grey for homebrew), so maybe that could be used to our advantage?

However, if we could get around the legal issues, this idea would provide very good brick protection for all Wiis, including Wii Family Edition and Wii Mini.
