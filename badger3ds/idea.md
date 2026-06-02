---
title: Badger
---

# Badger
This 3DS homebrew app would allow for custom badges, and it would be a lot better than Anemone.

## Problems with Anemone
Anemone3DS already supports custom badges, but I have some complaints:
- Downloading badges from ThemePlaza does not give you the option to sort them into categories (you need to do that manually with a computer).
- Homebrew badges often have filenames that don't make good labels.
  - When you place a badge on your HOME menu, a label appears on the top screen (below the 3D rendering of the badge) when you put the cursor on it.
  - If the badge was a Mario face badge, for example, you would want it to be labelled "Mario", "Super Mario badge", or "Super Mario - Mario". You wouldn't want it to be called "mario" (with no capital letters), "smbchar01", "mario1", "badge01", "001", or some other label that looks like an internal name.
  - Official badges have good labels, but not if you use Anemone to install an archive of them in PNG format.
- Installing badges from the archive of official badges doesn't work well. Badge labels are bad, categories must be sorted manually, category images aren't included, and multi-tile badges don't get grouped together properly (in the badge list and on the top screen).
- You can install archived official badges (or from NUS) with Advanced Badge Editor and Simple Badge Injector, but if you want to change your custom badges after that, you need to create the badge data file again (which requires Advanced Badge Editor on a computer).

## Alternative Option
Badger would fix all these problems. Badges would be able to have good labels, official badge injection would be easy, multi-tile badges would work properly, and badges from ThemePlaza would have multiple options for automatic sorting.

---

Badger would be a homebrew app that you install on your 3DS. Opening it would allow you to easily manage badges.
It would have a built-in badge editor, making it easy to import PNG images and convert them to badges (with good labels).

## Extra Badges
Because of the badge data structure, you can only have 1000 badges installed. However, Badger would create its own custom badge data file that can support up to 9999 badges. It would apply patches and sysmodules to the HOME menu to make it use the custom badge data file instead.

Another advantage of doing this is the ability to keep your badges (and not need to reinstall them) when you switch between NNID and PNID.

## Better Scaling
Some badges don't look good when they're placed on a zoomed-out (or zoomed-in) HOME menu (or when they're attached to folders, because they get zoomed out a bit to fit on the folder icon). Badger would fix the problem by saving each badge in multiple sizes (which can be done manually or from a single PNG image (but you would be able to choose the scaling methods)). There would be 8 badge sizes:
- Full image (for rendering on top screen)
- 1-column/2-column
- 1-column/2-column (on folder)
- 3-column
- 3-column (on folder)
- 4-column
- 5-column
- 5-column (on folder)

Additionally, some badges are inconsistent when attached to folders; installing them with Anemone works fine, but adding badges with Advanced Badge Editor causes them to get weird glitchy shadows when you attach them to a folder. Badger would fix all these problems.

## Direct Official Badge Download
You can get all the official badges by downloading `allbadge.dat` directly from Nintendo (and using update data to obtain any missing ones). Normally, this requires a computer. Badger would allow you to do this directly on the 3DS (and it would let you choose which groups and individual badges you want).

> [!TIP]
> This is **not** piracy. The download comes from the official source, which provides it for free.

## Launcher Badges
Some official badges act as shortcuts or alternate icons for the 3DS system apps. Badger would fully support this, and it would allow homebrew badges to launch apps (including games and homebrew apps).

## Badge Arcade Support
There would be an option to install a patch to Nintendo Badge Arcade that makes it send badges to Badger instead of the vanilla badge data file.

