---
permalink: /running-mods/
blcmmID: VkRgUqru3oU
---

# Running Mods

There are a couple of different types of mods available for Borderlands 2
and The Pre-Sequel: "traditional" text-based mods, and PythonSDK-based
mods.  Historically, BLCMM and/or Hex Multitool were used to prepare the
game for using text-based mods, whereas PythonSDK had its own installation
method for using PythonSDK mods.

However, nowadays installing PythonSDK is the first step to running mods,
regardless of what type of mod you're running.  We recommend that *all*
mod users install PythonSDK, whether you're using PythonSDK mods or not.

# Installing PythonSDK

The PythonSDK website itself has detailed installation instructions,
including pictures and a video: https://bl-sdk.github.io/#sdk-installation.
You can also check out a dedicated [Python SDK](/sdk-mods/) page on this
site.

The quick steps can be found here, though:

1. [Download the latest release here](https://github.com/bl-sdk/PythonSDK/releases).
   Make sure that you download `PythonSDK.zip`, *not* either source code link.
   The correct file should only contain a few dlls, a zip file, and a "Mods" folder.
2. Open up the game's folder - in Steam you can right click the game, properties ->
   local files -> browse local files - and browse to `Binaries/Win32`.
   This should be the folder containing the game's exe.
3. Extract all the files from inside the zip you downloaded to this folder. Extract
   the files, not the folder, you want there to be a `Win32/ddraw.dll`, and not a
   `Win32/PythonSDK/ddraw.dll`.
4. [Download and install this](https://aka.ms/vs/16/release/vc_redist.x86.exe)
   Microsoft Visual C++ Redistributable. Most of the time this will already be
   installed.
5. If you're trying to install the SDK on Linux, there are aa few extra steps:
   https://bl-sdk.github.io/#installing-on-linux.

You'll know that the PythonSDK is loaded properly when your BL2/TPS main menu
includes a "Mods" entry.

Now that PythonSDK is installed, you'll be able to start making use of traditional
text-based mods, in addition to PythonSDK mods.  See the [Python SDK](/sdk-mods/)
page for some more information on running PythonSDK mods, but the rest of this
page will deal with managing the text-based sort.

# Managing Text-Based Mods: Starting BLCMM

For "traditional" text-based mods, though the main tool to use to manage
them is the Borderlands Community Mod Manager, or BLCMM.

[Click here to download and install BLCMM](https://www.nexusmods.com/borderlands2/mods/61) *(Most Recent Version: v1.2.0, on May 22, 2020)*

BLCMM will auto-update to the latest version, if needed, from its splash
screen.

**NOTE:** BLCMM includes some methods of trying to hex-edit the game which
*no longer work* in a wide variety of situations.  When you start up BLCMM for
the first time, it will bring up a dialog which attempts to set up the game
for modding, but *PythonSDK has already done this for you*.  This dialog
should be **ignored** -- even though it may throw an error, or tell you that
it can't find the game, just click through that dialog and put it out of your
mind.  You won't need to see it again.

# Managing Text-Based Mods: Using BLCMM

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
be able to execute it from the console. You have to do this every time you
launch the game.

**Windows Users:** You must execute the mod from the *main menu*.  Wait a few
seconds for the game to talk to the Gearbox servers to do a bit of setup, then
hit the key that you configured for the console, and then type in
`exec patch.txt` (or `exec reborn.txt`, or whatever the filename was that you
used).  Depending on how your system saved the file, you may need to end up
doing something like `exec patch.txt.txt` instead).

**Mac Users:** You must execute the mod from the *Press any key* screen,
but you have to have been to the main menu at least once first.  Once you get
to the main menu, wait a few seconds for the game to talk to the Gearbox servers,
then hit `Esc` and then "yes" to go back out to that *Press any key* screen.
Then hit your console key and use the same `exec` commands that Windows users
use.  Note that there are a [few extra gotchas when running mods on Mac](https://github.com/BLCM/BLCMods/wiki/Linux-and-Mac-Setup-Gotchas).

**Linux Users:** The "native" Linux versions of BL2/TPS have become rather out
of date, unfortunately -- neither have the most recent patches from Gearbox,
and BL2 in particular doesn't have the latest story DLC (Commander Lilith and
the Fight for Sanctuary).  That DLC made some changes to the game data, and
many mods needed to be updated to account for the new data, and so won't work
totally properly on the native Linux version.  As such, it's actually
recommended to run the Windows versions of BL2/TPS using Proton, rather than
the native versions.  To do so, right click on the game in Steam, go to
`Properties`, and select `Force the use of a specific Steam Play compatibility
tool`.  Choose the latest Proton version, and you should be good to go!  You
can follow the Windows instructions above.  If you choose to use the native
Linux version anyway, all of the advice for the Mac section applies as well,
so be sure to read that, and click through to the wiki for the extra gotchas.

When running most major modpacks you will get a message on the screen telling
you to check your BAR page in-game to make sure that the mods applied properly.
If they did you should see a message like this:

[![Running UCP Message](/img/running-ucp-message.png)](/img/running-ucp-message.png)

**NOTE:** Whether or not you use UCP, Reborn, or any other combination of mods,
they should **always** be stored in your one single patch file, and you should
**only** ever execute a single file from the console.  Never `exec` multiple
files one after the other -- just use the one.

If you have any problems running mods or suspect that something's not working
properly, see the [Community / Support](/community/) section.

# Uninstalling Mods

If you've run a mod, but decided you don't actually want to play with it. To
"uninstall" the mod, just restart the game. Mods don't make permanent changes.

If you've merged multiple mods into a single file using BLCM, and you only want
to remove one of them, you can simply disable that category. To properly remove
it from the file, enable structural edits in BLCMM's settings, then delete
should be an option whenever you right click a category.

# Other Links

For information on some of the major mod packs, see [Major Mod Packs](/mod-packs/).
For information on how to find other mods to use, see [Finding Mods](/finding-mods/).

