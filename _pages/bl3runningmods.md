---
permalink: /bl3-running-mods/
b3hmHowtoID: KYgUzKomXrk
---
# Running Borderlands 3 Mods

Modding in Borderlands 3 is a bit different from how you might be used to dealing
with mods in BL2/TPS.  You will *not* be using BLCMM to manage your mod list, and
you won't be using a console to run any `exec` commands.

Instead, BL3 modding requires that a program modifies the hotfixes that are being
sent from Gearbox, and so another program has to get in the way and do that.  This
is where [B3HM](https://www.nexusmods.com/borderlands3/mods/244) (Borderlands 3
Hotfix Merger) comes in!

# B3HM (Borderlands 3 Hotfix Merger)

B3HM is a tool written by c0dycode to merge in custom hotfixes for BL3 to pick up.
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

Borderlands 3 doesn't have a native Linux version, but Linux users have been
able to [run BL3 via proton](https://www.protondb.com/app/397540) for some
time now.  Unfortunately, with the limited testing done so far, we've not had
much success getting B3HM running in that environment.

Fortunately for Linux users, there's an alternate method which has been available
for some time now, although it requires quite a bit more manual setup than
B3HM does.  Check out [apocalyptech's bl3hotfixmodding repo](https://github.com/apocalyptech/bl3hotfixmodding)
for a general overview of the technique, and a [mitmproxy](https://mitmproxy.org/)-based
script to handle loading mods and getting the hotfix injection working right.
That page doesn't go into *all* the details necessary to get mitmproxy up and
running for this purpose, but feel free to ask apocalyptech about it in
[Shadow's Evil Hideout](https://discord.gg/shadowevil).

