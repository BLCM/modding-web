---
title: "UCP 4.2, Hex Multitool 1.27 Released - Compatibility with Lilith DLC"
---

# UCP 4.2 Released

UCP 4.2 was released today, and is available from either
[Github](https://github.com/BLCM/BLCMods/tree/master/Borderlands%202%20mods/Community%20Patch%20Team) or
[Nexus](https://www.nexusmods.com/borderlands2/mods/50).  This
is a reasonably small release which mostly just adds in support
for the recently-released fifth story DLC for Borderlands 2,
[Commander Lilith and the Fight for Sanctuary](https://store.steampowered.com/app/872280/Borderlands_2_Commander_Lilith__the_Fight_for_Sanctuary/).

The complete changelog for UCP 4.2 is:

- Included a new message in the Badass Rank section to make sure your Patch is properly activated.
- Changed the Toothpick to have the correct Muzzleflash.
- Retainer is no longer area restricted and also correctly says its unique effect.
- Buttstallion now drops her legendaries again.
- Less Cluttering Particles updated.
- Fixed the Infection Cleaner's Skin.
- Fixed Unrecognized Objects popping up when executing the Patch.
- Pete now drops his Seraph if you Bloodsplode him.
- Spikers/Darts no longer display their health bar when shooting.
- The buff to Damage over time in UVHM is now 50% instead of 150% (150% was too much according to feedback and it made Gaige completely broken in some aspects).

Note that Linux users do not have access to the new DLC yet, and
should avoid upgrading UCP until that DLC drops.

## Hex Multitool 1.27 Released

Also, an updated version of [Hex Multitool](https://github.com/c0dycode/Borderlands-Hex-Multitool) was released recently,
which includes a small fix for the recent patch.  As a reminder,
Hex Multitool is currently the recommended way to enable mods on
both BL2 and TPS.

## BLCMM's hex editing still broken, still works for everything else, but now has some incomplete/inaccurate data in OE

As it's been since the UHD update, BLCMM still works fine for most things,
but it can't hex-edit your game anymore (which is why you're using Hex
Multitool for that).  The other issue with BLCMM right now is for modders -
if you're using Object Explorer, note that it does **not** contain any of
the new DLC data, and a bunch of object names have changed thanks to the
new DLC, so some object names (and data) might not be accurate anymore.
Be sure to check your data with `obj dump` while in-game!

## Some mods may be partially broken, though many will be fine.

The new DLC added a bunch of stuff, and made some changes to some of the
game's data, but in the end the incompatibilities weren't too great.  All
the mods hosted on the Github have been updated to use the updated object
names -- mods on Nexus may still need updating for that fix.  There may
certainly be other incompatibilities which haven't been discovered yet,
but in general you'll probably be okay to keep using the mods you're used
to using.
