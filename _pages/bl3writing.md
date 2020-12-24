---
permalink: /bl3-writing-mods/
---

# Writing Borderlands 3 Mods

Writing Borderlands 3 mods can be a somewhat daunting task.  The game isn't
really geared towards easily doing mod-like activity, and there are a number
of different components you'll need to get together in order to get going.
Fortunately, there's a pretty wide array of existing mods for you to look
at now, which should help get you going.

For the modder who's already familiar with modding BL2/TPS, there *are* many
similarities between the two.  BLCMM abstracts a lot of the details when
writing mods, but in the end you can think of BL3 hotfixes as just a collection
of weird-looking `set` statements (though you'll never actually see the word
`set` in the hotfixes).  But past experience in dealing with BL2/TPS arrays,
and knowing how to dive into attributes using hotfix syntax, etc, will definitely
make the transition to BL3 hotfix modding much easier.

The main resource for getting used to writing these kind of hotfix mods is
the main [BLCMods Wiki](https://github.com/BLCM/BLCMods/wiki/Borderlands-3-Modding-Info).
Here's some of the main pages you'll want to look into:

- [Accessing BL3 Data](https://github.com/BLCM/BLCMods/wiki/Accessing-Borderlands-3-Data) -
  Since we don't have something like BLCMM for BL3 modding, one of the bigger
  challenges is having game data to work with.  This page details all of our
  currently-known ways of pulling information from the game, which will be
  a great help in figuring out what to change in the game.
- [Borderlands 3 Hotfixes](https://github.com/BLCM/BLCMods/wiki/Borderlands-3-Hotfixes) -
  For this style of modding, you're basically writing raw hotfixes, so knowing how
  they're laid out and how to read them is extremely useful.
- [Borderlands 3 Hotfix Modding](https://github.com/BLCM/BLCMods/wiki/Borderlands-3-Hotfix-Modding) -
  This page is a primer for getting used to writing BL3 hotfixes.  This page is,
  unfortunately, written mostly from the perspective of someone who's already
  familiar with BL2/TPS modding.  This page goes into some detail about some of
  the differences between modding in BL2/TPS and BL3.

One invaluable resource to look at, of course, is existing hotfixes.  There's a few
places to look to take a look at those:

- The main [BL3 mod repository](https://github.com/BLCM/bl3mods/wiki) contains a lot of
  known-working examples.
- Gearbox's official hotfixes have been being collected since very shortly after the
  game launch, at [the bl3hotfixes repo](https://github.com/BLCM/bl3hotfixes/).
- A Google Sheets of the combined set of Gearbox-provided hotfixes is also available,
  in a nice spreadsheet format:
  [https://docs.google.com/spreadsheets/d/1kfkC2hJs0hZSr12bvrQlY0GyEH4S_KAI_xIAqnGmKnQ/](https://docs.google.com/spreadsheets/d/1kfkC2hJs0hZSr12bvrQlY0GyEH4S_KAI_xIAqnGmKnQ/)

Some other information about writing mods with the assistance of Python code (which
will actually be *easier* in many cases than doing it entirely by hand) can be
found [right at the main bl3mods repository](https://github.com/BLCM/bl3mods/blob/master/README-authors.md).

