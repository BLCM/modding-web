---
permalink: /running-mods/
blcmmID: VkRgUqru3oU
---

# Running Mods

The main tool to use to manage Borderlands 2 / Pre-Sequel mods, and prepare
your game for running mods, is the Borderlands Community Mod Manager, or
BLCMM.

{% include youtubeplayer.html id=page.blcmmID %}

[Click here to download and install BLCMM](https://www.dropbox.com/sh/rsljh5c55s8e9ah/AABMuarIfYCxJb8GiSY1IF6La?dl=0) *(Most Recent Version: v1.1.8, on November 9, 2018)*

BLCMM will auto-update to the latest version, if needed, from its splash
screen.

# Preparing Borderlands for Modding

The first time you start up BLCMM, it will launch a dialog to help you prepare
BL2 and TPS for accepting mods.  The main two things which have to happen is
hex-editing the game to accept the console commands we need, and setting up a
console key to use in the game.  It will look like this:

[![BLCMM Setup Game Files Dialog](/img/blcmm-setup-files.png)](/img/blcmm-setup-files.png)

If you don't have those options, there should be some text describing what to
do to fix it.  Click the `Apply` button for `Hexedit executable`, and then
choose a console key from the dropdown.  Then hit the `OK` button and your
game should be ready to run mods!

If you want to return to this screen at any time, you can get to it with the
`Tools -> Setup game files for mods` menu option.

**NOTE:** Cracked versions of Borderlands are very often not able to run mods
properly, since BL2+TPS modding relies on using Gearbox's "hotifx" mechanisms
to do their work.  Also, the Russian-localized version of BL2 can't currently
be patched.

# Managing Mods

Because of how BL2/TPS modding works, all of your mods that you use have to
be combined into a *single* file to run from the console.  Some folks start
with a bigger modpack like UCP, and then add more mods to that
file.  You can get some information about those modpacks on the
[Major Mod Packs](/mod-packs) page.  If you're using one of those modpacks,
save it in your game's `Binaries` directory.  When you open BLCMM, it should
find them automatically, though if they're named something different you
may have to `File -> Open` to get to it.

If you don't want to use a bigger mod pack, that's fine - you can choose
`File -> New file` in BLCMM to create a new file.  Just save the file in the
game's `Binaries` directory (with a name like `patch.txt` if you want to
stay consistent with the usual names) and use that as the base.

From this point forward, when you open BLCMM, it will open your main patch
file, and you can use `File -> Import mod file(s)` to import new mods.  They'll
be stored in a `mods` folder, and you can toggle them on/off with the checkbox
next to their names.  Use `File -> Save` (or `Ctrl-S`) to save the patch file
after each change!  See [Finding Mods](/finding-mods/) for some tips on finding
mods to use.

Note that if BLCMM was able to detect your Borderlands installation directory,
its Open/Save dialogs will have a button on the side to go directly to your
`Binaries` directory, so you shouldn't have to find it yourself:

[![BLCMM Binaries Buttons](/img/blcmm-binaries-buttons.png)](/img/blcmm-binaries-buttons.png)

# Actually Running Your Patch File

Once you have your patch file in the game's `Binaries` directory, you should
be able to execute it from the console.

**Windows Users:** You must execute the mod from the *main menu*.  Wait a few
seconds for the game to talk to the Gearbox servers to do a bit of setup, then
hit the key that you configured for the console, and then type in
`exec patch.txt` (or `exec reborn.txt`, or whatever the filename was that you
used).  Depending on how your system saved the file, you may need to end up
doing something like `exec patch.txt.txt` instead).

**Mac/Linux Users:** You must execute the mod from the *Press any key* screen,
but you have to have been to the main menu at least once first.  Once you get
to the main menu, wait a few seconds for the game to talk to the Gearbox servers,
then hit `Esc` and then "yes" to go back out to that *Press any key* screen.
Then hit your console key and use the same `exec` commands that Windows users
use.  Note that there are a [few extra gotchas when running mods on Mac/Linux](https://github.com/BLCM/BLCMods/wiki/Linux-and-Mac-Setup-Gotchas).

If you are running UCP for Borderlands 2, you will get a message on the screen
telling you to check your character's skill tree in-game to make sure that the
patch applied properly, otherwise you will probably see nothing.

**NOTE:** Whether or not you use UCP, Reborn, or any other combination of mods,
they should **always** be stored in your one single patch file, and you should
**only** ever execute a single file from the console.  Never `exec` multiple
files one after the other -- just use the one.

If you have any problems running mods or suspect that something's not working
properly, see the [Community / Support](/community/) section.

# Other Links

For information on some of the major mod packs, see [Major Mod Packs](/mod-packs/).
For information on how to find other mods to use, see [Finding Mods](/finding-mods/).
