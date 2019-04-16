---
title: "Modding Status: Hex Multitool for hex edits, BLCMM for Everything Else"
---

# Current State of BL2+TPS Mod Support

A few weeks ago, Gearbox patched both BL2 and TPS, which has caused the hex-editing
portion of BLCMM to stop working.  We've been unable to get a new version of BLCMM
out to address that problem, but for the meantime, here's what enabling mods looks
like on BL2 and TPS:

### 1. Use c0dycode's Hex Multitool for the hex-editing bits

This is the part which enables the full console, so that you can execute mods once
you're at the main menu.

[Hex Multitool can be found here](https://github.com/c0dycode/Borderlands-Hex-Multitool/raw/master/BL%20Hex-Multitool%20.NET%204.5.zip),
and instructions for it [can be found here](https://github.com/c0dycode/Borderlands-Hex-Multitool).

### 2. Use BLCMM for everything else, as usual

BLCMM can still be used for literally everything except for the hex-editing component.
Importing mods, changing mod configurations, tweaking any of the performance options
it supports, etc.  All of that will still work fine, so feel free to keep using it!
You *will* see an "Error" if you go into the `Set up game files for mods` screen, next
to the "Hex Edit" line, but ignore that.

### 3. That's It!

In summary: the only real change is that to hex-edit your game, you'll be using the
Hex Multitool instead of BLCMM.  Enjoy taking down those bandits!
