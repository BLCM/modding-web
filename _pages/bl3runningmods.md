---
permalink: /bl3-running-mods/
b3hmHowtoID: KYgUzKomXrk
ohlHowtoID: gHX3dtZIojY
---
# Running Borderlands 3 Mods

Modding in Borderlands 3 is a bit different from how you might be used to dealing
with mods in BL2/TPS.  You will *not* be using OpenBLCMM to manage your mod list, and
you won't be using a console to run any `exec` commands.

Instead, BL3 modding requires that a program modifies the hotfixes that are being
sent from Gearbox, and so another program has to get in the way and do that.  There
are now two methods to do this: [OpenHotfixLoader](https://github.com/apple1417/OpenHotfixLoader),
and [B3HM](https://www.nexusmods.com/borderlands3/mods/244) (Borderlands 3 Hotfix
Merger).

# OHL (OpenHotfixLoader)

OpenHotfixLoader is a fully open-source tool written by apple1417 to do local
hotfix injection without having to mess with network streams (like B3HM does).
It's fully compatible with both BL3 and Wonderlands, and features a bit more
hotfix support than what B3Hm currently has (as of October 26, 2022).

Some handy links for OHL:

- [Main Github Site](https://github.com/apple1417/OpenHotfixLoader)
- [Releases](https://github.com/apple1417/OpenHotfixLoader/releases)

{% include youtubeplayer.html id=page.ohlHowtoID %}

# B3HM (Borderlands 3 Hotfix Merger)

B3HM is a tool written by c0dycode to merge in custom hotfixes for BL3 to pick up.
As of October 26, 2022, it does not yet support Wonderlands, but once v1.0.2 is
released (likely in September), Wonderlands should be supported as well.

It's available either as a standalone EXE, or as a DLL which you can inject in
a variety of methods.  You can find B3HM in these locations:

- [B3HM at Nexusmods](https://www.nexusmods.com/borderlands3/mods/244)
- [B3HM at Github Releases](https://github.com/c0dycode/BL3HotfixWebUI/releases)

The B3HM project has [documentation right at its github page](https://github.com/c0dycode/BL3HotfixWebUI/wiki/B3HM-Wiki).

For the DLL version, it's recommended that you use
[FromDarkHell's BL3DX11Injection/PluginLoader](https://github.com/FromDarkHell/BL3DX11Injection/releases)
to inject the B3HM into the Borderlands 3 process.  For the EXE version, just
download the EXE and give it a run.

See the [B3HM documentation](https://github.com/c0dycode/BL3HotfixWebUI/wiki/B3HM-Wiki) for
further information about how to use the app!  There's also an [easy-to-follow
HOWTO about running PluginLoader + B3HM](https://docs.google.com/document/d/1gdJX7eje3v-S7INIX5ZzIvaLfzGaWjauB2rcPgPqslw),
written by FromDarkHell, and a tutorial video by FromDarkHell:

{% include youtubeplayer.html id=page.b3hmHowtoID %}

# Finding Mods

For information on where to look for BL3 Hotfix mods, check out our
[Finding BL3 Mods](/bl3-finding-mods) page.

# Info for Linux Users

B3HM and OHL should both run just great on modern Proton versions, whether
via the [GloriousEggroll versions](https://github.com/GloriousEggroll/proton-ge-custom)
or Steam's own Proton.  The PluginLoader (DLL) version will be the easiest
to get running (and is the *only* option for running OHL).  If you try the EXE
version of B3HM, you'll have to make sure to be running both the game and B3HM
inside the same `WINEPREFIX`, and have various environment variables set properly.
Remember that nowadays the correct way to launch other apps inside a Proton
prefix is with a `proton run <foo>` command, rather than running a Wine
binary directly.

A "legacy" modding method for Linux users is still available as well, though
it takes more setup and technical knowhow.  Check out [apocalyptech's
bl3hotfixmodding repo](https://github.com/apocalyptech/bl3hotfixmodding)
for a general overview of the technique, and a [mitmproxy](https://mitmproxy.org/)-based
script to handle loading mods and getting the hotfix injection working right.
That page doesn't go into *all* the details necessary to get mitmproxy up and
running for this purpose, but feel free to
[ask apocalyptech about it](https://apocalyptech.com/contact.php).

