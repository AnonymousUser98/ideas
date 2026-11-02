---
title: Fastboot Forwarder Creator (3DS)
permalink: /3ds/fastboot-forwarder/
---

# Fastboot Forwarder Creator
This program (which runs on a computer) would make it easy to create HOME Menu shortcuts to FIRMs on the SD card (for fastboot3ds).

## What It Should Look Like
It should have a GUI, and it should be easy to use. Here's how it should work:

1. Select the FIRM from your SD card (or type in the path).
1. Type in the short name, long name, and creator.
   - Short name is what gets displayed in Data Management, and long name is what appears on the HOME Menu. Lots of people get confused and use the "long name" field as a short description field, so this program should clearly label them as "short name" and "long/full name".
1. Import an image to use as the icon.
1. Import an image to use as the banner, or load an existing 3DS banner file.
1. Click the create button and get a CIA that's ready to install.


## How It Works
It's very simple: It uses [That-Shortcut-Thingy](https://github.com/SUOlivia/That-Shortcut-Thingy) to create the CIA, and it uses a custom program to create the `payload.firm` file.

Instead of directly embedding the FIRM in the shortcut, it would create and compile a simple FIRM that looks for and loads a FIRM on the SD card at a certain file path. Compiling can be hard for new users, so it should automatically download all the dependencies (preferrably to somewhere in AppData or the folder the program is being run from) and handle all the compiling for you.

This method of using a "forwarder FIRM" has a few advantages:
- If the target FIRM stores settings in a specific folder relative to where it's loaded from, it will share the same data as the one on the SD card (that gets chainloaded by Luma3DS).
- Users wouldn't need to recompile whenever there's an update because simply replacing the target file (updating normally) would cause the new file to be loaded.
- This isn't an advantage of using the forwarder FIRM method, but it would still be an advantage of using this program: Users who don't have devkitARM installed or don't know how to compile can still create HOME Menu shortcuts very easily. (I tried to make a shortcut once and I had to install devkitARM and it still complained about missing requirements and I didn't want to deal with installing all of them so I just gave up.)
