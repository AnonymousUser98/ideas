---
title: Winglish-CA
---

# Winglish-CA
This would add actual support for Canadian English (en-CA) to Windows 10 and Windows 11, instead of just being a slightly modified British English.

## Current Problem
Windows doesn't know what Canadian English is. It just takes British English and changes stuff like "elevator/lift" and other word differences. It doesn't even change all the spellings (e.g. "tyre" becomes "tire", but "programme" doesn't get changed to "program"). It's almost identical to British English.

This seems to happen because Windows doesn't have a "local experience pack" for en-CA, meaning it doesn't actually support it internally.

## Solution Idea
**Winglish-CA** would simply add true en-CA support to Windows. It would use the en-US and en-GB language packs as a base, and it would modify them to create an actually correct en-CA option for Windows. Even better if it works without admin access.

## Customi(s/z)ation
In Canadian English, both the British and American spellings are correct for some words, and the one you should use just depends on your preference.
This program would include a simple settings menu where you can specify your preferences. It would have the following options:

### S-Z Preference
This would decide if certain words are spelled with an S or a Z. This setting would be for words like customize/customise, organization/organisation, and other words where one of the letters can be an S or a Z.

### C-S Preference
This would control the following words:
- License/Licence
  - Just remember that the verb form (e.g. "licensed" and "licensing") is always spelled with an S.
- Offense/Offence
- Defense/Defence

It would **not** affect practice/practise (which is always spelled with a C).

This setting might even have a custom mode (e.g. for anyone that wants to use "license", "offense", and "defence", or another mix of British and American spellings).
