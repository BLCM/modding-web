---
title: "OpenBLCMM v1.3.0 Has Been Released!"
openblcmmTrailerID: iBBB6jmo2Wc
---

# Text Mod Management With OpenBLCMM

OpenBLCMM is a community-managed 100% opensource fork of the original BLCMM
app, and fixes up a few of the longstanding issues w/ BLCMM.  As with the
original, OpenBLCMM is a tool for managing text-based mods in BL2, TPS, and the
standalone AoDK.  Many thanks to LightChaosman for opensourcing the BLCMM core
last year, and for everyone who's helped test and debug OpenBLCMM during its
development!

Some notable changes:
1. It's 100% open-source
2. The Windows version is entirely contained in an EXE.  No Java install is
   required!  There's also an installer which will get OpenBLCMM into your
   Start Menu.
3. "Pure Java" versions support all current Java versions, up through Java 20
4. Support for Assault on Dragon Keep (including OE data!)
5. Object Explorer datapack handling is significantly different, and OE
   features various speedups and some streamlining.

Downloads:
OpenBLCMM: https://github.com/BLCM/OpenBLCMM/releases/
OE Data Packs: https://github.com/BLCM/OpenBLCMM-Data/releases/
Full Changelog: https://github.com/BLCM/OpenBLCMM/blob/main/src/CHANGELOG.md

If you run into problems, feel free to ask questions in the [community mod
support Discord](/community/).  Bug reports and feature requests can be
submitted at the [project Github](https://github.com/BLCM/OpenBLCMM/issues).
Enjoy!

{% include youtubeplayer.html id=page.openblcmmTrailerID %}

# More Detailed Changes

The day-to-day use of OpenBLCMM hasn't really changed much from the original
BLCMM, but there are a few things which are worth noting.  I'll break them
out in three sections: one for installation details, another for app changes
for all users, and another for modders.

### Installation

The main change here is that Windows users should have an easier time.  OpenBLCMM
is compiled up into an EXE, so Windows users no longer have to have Java
installed to run the app.  Additionally, the recommended way to install is via
the new installer.  Give it a run, click through some hopefully-familiar-looking
dialogs, and you'll end up with an `OpenBLCMM` entry in your Start Menu, and
also on your Desktop if you chose that option.

There's also a zipfile of the EXE release, in case you don't want to use the
installer for whatever reason.  Keep in mind that the zipfile EXE requires you
to have the [MS Visual C++ Runtime](https://aka.ms/vs/17/release/vc_redist.x64.exe)
installed.  That's commonly installed by other programs, so you probably already
have it, and the Installer package will install it automatically if need be.  if
you try to run the EXE and have errors about not finding `VCRUNTIME140.dll`, though,
that's the package you'll need to install.

Users on other platforms have archives available which require you to already have
Java installed, as you're probably already used to.  We recommend installing
[Adoptium Temurin](https://adoptium.net/temurin/) for Java.  OpenBLCMM currently
supports Java 8, 11, 17, and 20.

### Changes For All Users

The first thing you might notice is there's no longer a launcher for OpenBLCMM --
you're sent directly into the app.  One side-effect of this is that OpenBLCMM
doesn't do any auto-updates.  When new versions are available, the app will let
you know in the status area at the bottom, but you'll have to download and
install the updates yourself, if you want.  You can turn off the new-version
checking from the settings.

You may notice that various things have actually been *removed* from OpenBLCMM,
such as the game launch button, Hex Multitool integration, the old "plugins"
system, etc.  One of OpenBLCMM's goals was simplifying its operation a bit, and
many of those features were complicating the codebase and causing maintainability
problems.

The other main thing that users may notice is that the "Setup game files for mods"
dialog now redirects you to [PythonSDK](https://github.com/bl-sdk/bl2-mod-manager/)
instead of offering the hex edits.  Installing PythonSDK has been the recommended
method of enabling the in-game console and supporting text mods for some time now,
and direct hex editing for BL2/TPS/AoDK isn't actually required.  The hex edits
*are* still available via a new "Legacy Hex Edits" dialog if you want, but we
strongly recommend just installing PythonSDK instead.

### Changes for Modders

The biggest change for modders is that the Object Explorer datapack handling is
totally different.  Originally, BLCMM would download those from the launcher, based
on some settings in the main app.  In OpenBLCMM, though, you [download them
separately](https://github.com/BLCM/OpenBLCMM-Data/releases) and place them in
the same directory where your `OpenBLCMM.exe`/`OpenBLCMM.jar` lives.  Then when
the app starts up the next time, it'll see the data, do a little bit of processing,
and they'll be good to go.  The datapacks are also no longer split up by category.
Instead, each datapack contains *all* the available data for the game.  This includes
classes which have historically been left out of the BLCMM dataset.  OpenBLCMM also
has support for the standalone Assault on Dragon Keep, and there's a datapack
available for that game.  You can see info about which datapacks OpenBLCMM has
loaded from the `Help -> About` menu.

Object Explorer itself had its whole datalib backend rewritten for OpenBLCMM, and
there's been some streamlining and performance improvements as a result.  The
Class Browser and Object Browser can be used without restriction, instead of having
to worry about classes with a lot of objects.  There's a dropdown for the active
game inside OE itself, instead of using the dropdown from the main OpenBLCMM
window.  If you type in a search term which isn't an object name, OpenBLCMM will
immediately switch to fulltext searching mode, rather than popping up a dialog
to let you know.  There's been a lot of other little tweaks, which should hopefully
be welcome to modders.

Finally, there *is* still a tab in the settings menu to choose data categories, but
those checkboxes *only* apply to fulltext searches and "refs" searches.  The more
categories you have selected, the slower those two operations will be, just like
with the original BLCMM.  Unlike the original, you can change those settings without
having to restart the app.  So you can feel free to change those whenever you like.
As before, including the StaticMesh category will end up noticeably slowing down
your searches.  There's also a new "Others" category which includes all the classes
which were historically absent from the BLCMM data set.

# That's It!

If you have any bug reports or feature requests, feel free to [submit them at the
Github page](https://github.com/BLCM/OpenBLCMM/issues), or ask in the [community
mod support Discord](/community/).  You can also check out the Github if you're
interested in helping out with the project, or if you were just curious and wanted
to check out the sourcecode.

Happy modding!

