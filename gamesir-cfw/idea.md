---
title: GameSir CFW
permalink: /gamesir/
---

# Custom Firmware for GameSir Super Nova
There's a really good game controller called the **GameSir Super Nova** (aka. "GameSir Nova Pro", "GameSir T4n Pro"), but it has quite a bit of room for improvement on the software side of things. I thought of this idea for a custom firmware (or some other kind of softmod) that adds these improvements.


## Unlocked Gyroscope

I want to use the motion controls with emulators (actual motion controls instead of mapping the gyro to a control stick), but the DS4 and Switch modes don't allow all the controller's features to be used. There should be an option to have the gyroscope directly accessible by programs (by having a separate HID device running alongside the Xinput device).



## Unlocked Paddles & Capture

> [!NOTE]
> This wouldn't be possible with Xinput, but maybe there could be another mode (like SDL or DirectInput) that can still interact with the GameSir Connect app.

There should be a way to have the rear paddle/grip buttons behave as separate buttons (instead of being mapped to another button). Similarly, there should be a way to make the screenshot button behave like a controller button instead of being mapped to a key on the keyboard.



## Hold Modifiers

There should be an option to make the grip buttons act as hold switches for turbo (and other modifiers).

For example, you could have the <kbd>X</kbd> button behave normally, but it would be a turbo button if you press it while holding the right grip button. You could also make the left stick less sensitive or make the <kbd>A</kbd> button behave like the <kbd>R</kbd> button while holding the left grip button.



## amiibo (NFC) Emulation

> [!NOTE]
> I'm not sure if this is possible with the internal storage of the controller, but it would be a great feature if it's possible to add.

When running in Switch mode (connected to Nintendo Switch), you could press a button combo (such as <kbd>L+Down+Function Button</kbd>) to put the controller in amiibo menu mode. This would change the RGB lighting to the amiibo colours (the 6 colours used in the amiibo logo (and the "new" in New 3DS)) and temporarily make the controller stop sending your button inputs to the console. You would then be able to use the d-pad to select an amiibo to mount. For example, it might allow you to store up to 9 virtual amiibo and represent each one with a colour (red, orange, yellow, green, cyan, blue, purple, pink, white). You would use the d-pad to control the colour of the RGB lighting and press the <kbd>A</kbd> button to select the amiibo that's assigned to the currently displayed colour. This amiibo would then get mounted as if it were on the NFC touchpoint of an actual Switch controller.

When you're done with an amiibo, you would be able to unmount it by pressing the amiibo menu button combo and then pressing <kbd>X</kbd> (or a different button). You could also switch directly to another amiibo.

The user would need to provide the `unfixed-info.bin` and `locked-secret.bin` files in order to use this feature.



## More RGB Control

You're pretty limited in what the RGB lighting can be set to. There should be a way to create custom gradients (and gradient animations), and maybe even a custom cycle (e.g. solid green for 1 second, flashing blue for 0.5 seconds, moving red-yellow gradient for 3 seconds, repeat).



## Macros

If the controller's internal storage can handle it, there should be support for macros.



## Better Vibration on Switch

The vibrations on Nintendo Switch could use improvement. It doesn't have HD rumble, but it could still be inproved by doing a better job mapping the HD rumble signals to the controller's vibration motors.


## Switch 2 Mode

There should be a special _Nintendo Switch 2_ mode. It would map the rear paddle/grip buttons to the <kbd>GL</kbd> and <kbd>GR</kbd> buttons on the Switch 2, and it would add a key combo for the GameChat button.

