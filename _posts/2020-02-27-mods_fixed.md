---
title: "BL2 + TPS Modding Fixed with Updated Hex Multitool"
---

# BL2 + TPS Modding Fixed with Updated Hex Multitool

Today (February 27, 2020), [Gearbox patched both Borderlands 2 and The Pre-Sequel](https://steamcommunity.com/games/49520/announcements/detail/1707365591060869371)
with some changes which adds support for upcoming cross-play between
various PC-based platforms.  This caused problems for the modding
community because our established hex editing methods stopped working.

A few hours after the fix, though, a new version of Hex Multitool was
released which works for hex editing once again:

- [Download Hex Multitool 1.29 on Nexus](https://www.nexusmods.com/borderlands2/mods/54/?tab=description)
- [Download Hex Multitool 1.29 on Github](https://github.com/c0dycode/Borderlands-Hex-Multitool)

So grab that and have at it!  Keep in mind that we still recommend using
Offline Mode for mods, thanks to some recent changes in how SHiFT is
interacting with the game.  Users won't get an error on the console
when executing the patch, but will notice that they don't have the "Running
UCP" notification on the BAR screens, and many changes from the patch won't
be applying properly.

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

