---
permalink: /sdk-mods/
---

# SDK Mods

The [Python SDK](https://github.com/bl-sdk/PythonSDK) is a plugin allowing Python
scripts to interact directly with Unreal Engine objects. This opens up many new
avenues for modding, from simply allowing modifying dynamically generated objects
to letting modders run arbitrary game functions whenever they please. SDK mods
are a superset of "regular" text mods, they can do all the same things plus more.

# Installing the SDK

Installing the SDK is rather simple. The exact same release is compatible with
both BL2 and TPS, as well as both Steam and Epic versions of them, these
instructions apply to all of them.

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

Updating the SDK works much the same, though note that occasionally you may have
to delete files from older versions.

# SDK Mods Menu

A few mods are installed with the SDK by default. One of these replaces the DLC
menu with an in-game Mods menu. Seeing this menu means that the SDK is properly
installed.

The Mods menu is primarily used to enable/disable mods, but each mod can also
define additonal actions you can perform there.

[![SDK Mods Menu](/img/sdk-mods-menu.png)](/img/sdk-mods-menu.png)

# Finding SDK Mods

Currently there are not many SDK mods, so there is no centralized repository.
Instead mods tend to be stored in the author's own repositories.

The best way to keep track of SDK mods is simply to join one of the [community discord servers](/community/)
and pay attention to their mod downloads channels.

Otherwise, here is a list of locations to check:
 - [apple1417's repo](https://github.com/apple1417/bl-sdk-mods)
 - [juso40's repo](https://github.com/juso40/bl2sdk_Mods/)
 - [PythonSDK repo](https://github.com/bl-sdk/PythonSDK/tree/master/Mods)

# Installing SDK Mods

All SDK mods are installed into the `Binaries/Win32/Mods` folder that you extracted
when installing the SDK. You can either access this through Steam the same way
you originally found it, or by selecting the "General" mod and pressing 'O'.

Each mod is placed in it's own folder. This folder needs to contain a file
`__init__.py`, and it may also contain other files. This file is something the
mod author needs to define, if you couldn't find one you can't just create your
own one. Usually when downloading an SDK mod this folder structure will already
be setup for you, you'll just have to copy the folder into the Mods folder.

# Writing SDK Mods

There is not yet a lot of documentation on writing SDK Mods, it's best to learn
by looking at existing mods. If you need help you can always ask in the [PythonSDK discord](/community/).

Unsurprisingly given the name, you will need to be at least somewhat proficient
with Python, specifically the SDK currently uses version 3.7. There are many
good tutorial series teaching it available online, though you will always still
have to get used to the exact way the SDK works.

Something else good to do when writing SDK mods is to decompile the game's UPKs.
This will you let you view all the UnrealScript functions and most of the source
code behind them, greatly helping development.

1. Download [Gildor's Unreal Package Decompressor](https://www.gildor.org/downloads)
   and [UE Explorer](https://eliotvu.com/portfolio/view/21/ue-explorer).
2. Open up `WillowGame/CookedPCConsole`, and run the decompressor on some of
   the UPKs there. You do not need to decompress everything, the most useful
   UPKs are `WillowGame`, `Engine`, and `GearboxFramework`.
3. Open the extracted UPKs in UE Explorer, switch to object view, and search
   for whatever class you want to view. You can also extract the decompiled
   scripts to disk, if you prefer to use a different editor.
