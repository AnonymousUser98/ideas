# Super Mario World - Definitive Edition

This ROM hack would make the game better. It would use the standalone version or the All-Stars version as a base.

If using the standalone version as a base, Luigi would be replaced with his unique All-Stars sprite.



### Basic Improvements

* When saving, the game will remember the current lives, score, power-up status, coins, bonus stars, and stored item. This would be saved separately for both players.
* The game will also remember which of each level's dragon coins have been collected.
* Castles can be replayed in multiplayer mode (no longer requires L+R).
* In the top-secret area, the player can easily choose between any of the Yoshi colours they've unlocked. This would be done with the L and R buttons; pressing them would change the colour of the middle item box, which would indicate the currently selected colour.
* Various bugs and glitches would be fixed.
* Mushrooms no longer overwrite feathers and fire flowers in the item storage.
* After unlocking the fall colours, you can change between the regular and fall appearances by pressing L+R on the save menu.
* An option to copy a save file would be added to the file select screen.



### Convenience Menu

Pressing the Y button on the map would open the convenience menu. It would have the following options:

* **WORLD TELEPORT** - Teleport to the start of any unlocked world.
* **MAP SPEED** *(1-5)* - Makes Mario move faster on the map. Can be changed from 1x to 5x (in intervals of 0.25x). If *Save Speed* is enabled, this value will be synced with the *Default Map Speed* setting.
* **TOP SECRET AREA** - Instantly and remotely enter the top-secret area. When the player leaves, they appear on the world map in the same spot they were in when they did the remote entry. Only appears if the top-secret area has been unlocked.
* **GO TO STAR ROAD** - Teleport to Star Road. This option appears after at least 1 entrance has been opened.



### Players Menu

Pressing the X button on the map would open the players menu. It would have the following options:

* **SWITCH PLAYERS** - Switches between Mario's turn and Luigi's turn. Only appears in 2-player mode.
* **TRANSFER LIVES** - Opens the life transfer screen that is normally accessed with L or R. Only appears in 2-player mode.
* **LEAVE PLAYER 2** - Changes to singleplayer mode. Only appears when 2P is active.

In singleplayer mode, pressing the X button would open a prompt asking if you want to switch to multiplayer.



### Save Menu

Pressing the SELECT button on the map would open the save menu. It would have the following options:

* **CONTINUE**
* **SAVE \& CONTINUE**
* **SAVE \& QUIT**

The game menu would also display the text "PRESS Y FOR OPTIONS".

After defeating Bowser, the text "PRESS X FOR STATUS" is added and the status menu is unlocked.



### Options Menu

Pressing the Y button in the save menu would open the options menu. These options get saved when you save your game, and they allow you to change a few settings that affect the game.

Pressing the R button in the options menu would display a description of the currently selected option.

* **AUTO DROP** *(Off/Small/On) \[Ask]* - If enabled, the item storage will automatically release the item when you take damage. The *Small* option only appears when *Easy Hit* is enabled, and it makes the item only drop when you take damage that makes you small.
* **EASY HIT** *(Off/On) \[Ask]* - If enabled, getting hit with a flower or feather will not make you become small. This is the behaviour used in most Mario games (including SMB3) and in *Super Mario Advance 2*.
* **MAP SPEED** *(Submenu)*:

  * **DEFAULT** *(1x-5x, change by 0.25x) \[1.25x]* - The default movement speed on the map screen. This value gets loaded into the current map speed value (in the convenience menu) whenever you load your save file.
  * **SAVE SPEED** *(Off/Session/On) \[Session]* - If enabled, the *Map Speed* option in the convenience menu will sync with the default map speed instead of acting as a temporary override. If set to *Session*, the current map speed value will only be reset after a power off. If disabled, the current map speed value will be reset after each level.
* **FACE BUTTONS** *(Type A/Type B) \[Type A]* - Type A is the control scheme used in the vanilla game. Type B uses {A:Jump, B:Sprint, X:Sprint, Y:Spin}.
* **GBA MODE** *(Off/On) \[Off]* - If enabled, spin jump is remapped to the R button, and L+Dpad scrolls the screen.
* **PAUSE MENU** *(Off/On) \[On]* - If disabled, the pause menu will not be displayed by default when pausing the game. You can still show the pause menu by pressing SELECT.
* **FREE ESCAPE** *(Off/On) \[Off]* - If enabled, you will be able to manually exit levels you haven't completed.



###### The above list uses the following format:

**Option** *(Choices) \[Default]* **-** Description

If `\[Default]` is `\[Ask]`, then there is no default, and the player will be asked about the option when creating a save file.



### Pause Menu

Pausing the game during a level would open a pause menu (can be hidden or shown by pressing SELECT).

This menu would have the following options:

* **CONTINUE** - Close the pause menu and continue playing. Same as pressing START.
* **LEVEL STATUS** - Opens the status menu and shows the details for the current level. Only appears after unlocking the status menu.
* **OPTIONS** - Shows a limited version of the options menu with the following options:

  * Auto Drop
  * Face Buttons
  * GBA Mode
* **RETURN TO MAP** - Exits the level and returns to the map screen. Only appears if you've completed the level (unless *Free Escape* is enabled).

### Save Decorations

On the file select screen, extra space will be added to the right of the exit counter on each file. This extra space is used to display star decorations (similar to NSMB). You can earn up to 5 stars:

1. Defeat Bowser and finish the game.
2. Complete all 7 worlds.
3. Finish the special world.
4. Find all 96 exits.
5. Find all 96 exits and collect every dragon coin.



### Status Menu

After defeating Bowser, you unlock the status menu. This menu shows your stats for each level, which include exits found, dragon coins found, most coins collected, highest score, and best time.



### Startup Menu

Booting the game while holding L+R will open a menu that allows you to change the logo that gets displayed on the title screen. It would have the following options:

* **DEFAULT** - The default title screen logo used in the vanilla game. *\[Default]*
* **JAPANESE** - The title screen logo used in the Japanese version of the game (left-aligned with SMB4 label).
* **LEFT-BLANK** - Just like JAPANESE, but without the SMB4 sub-logo.
* **LEFT-DE** - Just like JAPANESE, but the SMB4 sub-logo is replaced with the text "DEFINITIVE EDITION".
* **CENTER-DE** - Just like DEFAULT, but the text "DEFINITIVE EDITION" is added below the main logo.



