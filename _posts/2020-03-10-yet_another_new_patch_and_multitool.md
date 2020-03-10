---
title: "Yet Another BL2 + TPS Patch, Another Hex Multitool Version (v1.32)"
---

# Hex Multitool Patched Again in Response to Game Patches

Today (March 10, 2020), Gearbox patched both Borderlands 2 and The Pre-Sequel.
This ended up breaking the hex-editing features in Hex Multitool for a
little bit, until the Multitool could get updated.

Not long after the fix, though, a new version of Hex Multitool was
released which works for hex editing once again:

- [Download Hex Multitool 1.32 on Nexus](https://www.nexusmods.com/borderlands2/mods/54/?tab=description)
- [Download Hex Multitool 1.32 on Github](https://github.com/c0dycode/Borderlands-Hex-Multitool)

So grab that and have at it!  One other potential avenue for dealing with
hex editing issues is also using [PythonSDK](https://github.com/bl-sdk/PythonSDK),
which enables a completely different kind of BL2/TPS mod, but also has the
side effect of enabling modding when it's loaded.  (The SDK does not currently
do other edits like increasing backpack space or disabling sanity checks,
though.)

Keep in mind that we still recommend using Offline Mode for mods, thanks to
some recent changes in how SHiFT is interacting with the game.  Users won't get
an error on the console when executing the patch, but will notice that they
don't have the "Running UCP" notification on the BAR screens, and many changes
from the patch won't be applying properly.

The solution for this is to switch your patch to "offline" mode.  BLCMM
can do this very easily: open your patch file in BLCMM, check the "offline"
checkbox at the bottom of the screen, and then re-save the file.  When you
re-execute the patch on the main menu, it should apply properly.  Note that
"offline" in this context *only* means the SHIFT components -- you can still
play coop with your friends while using an "offline" version of your patch
file.

[![Offline Mode Screenshot](https://i.imgur.com/hJcjq4z.png)](https://i.imgur.com/hJcjq4z.png)

If you're using just the BL2 UCP, a pre-saved offline patch is available
at both [Github](https://github.com/BLCM/BLCMods/tree/master/Borderlands%202%20mods/Community%20Patch%20Team)
and [Nexus](https://www.nexusmods.com/borderlands2/mods/50).

