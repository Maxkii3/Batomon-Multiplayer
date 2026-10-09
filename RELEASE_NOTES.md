# BatoMulti 0.6.10 — works with Mod Loader

Batomon Showdown, multiplayer: create a room, share the code (or let people find it in the room browser),
and battle round after round until one trainer is left.

**Updating from 0.6.2-0.6.9:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.6.10: 0.6.9 and 0.6.10 players can't share a room.

## 🧩 Mod Loader fix

With the community **Mod Loader** installed (`Mods\mod_loader.gd`), the **Multiplayer** button could
vanish from the main menu: when Mod Loader's line came before BatoMulti's in `override.cfg`, Mod Loader
swapped in its own title screen first and BatoMulti no longer recognised it.

BatoMulti now recognises the game's title screen even when another mod has extended it, so the
**Multiplayer** button is there **whatever order** the lines have in `override.cfg`. Mod Loader keeps
working too: its title screen and its mods still load.

Updating keeps everything else as it was: Mod Loader's line and its `Mods` folder, your other
`override.cfg` settings, your saves and your BatoMulti settings.

Nothing else changes: battles still start at **4x** and the host's **Free pick** trainer setting from
0.6.9 works as before.

## Install

- **`BatoMulti-Setup-0.6.10.cmd`** (recommended): close the game, double-click it, launch the game through
  Steam. It finds the game, sets other mods aside safely and uninstalls when run again.
- **`BatoMulti-v0.6.10-ManualInstall.zip`** (also for mod sites) with only the `batomulti` scripts,
  `override.cfg` and a plain-text `README.txt` — nothing to run. Extract it next to
  `batomon_showdown.exe`. It replaces `override.cfg`, so other autoload mods stop loading unless you
  merge (keep Mod Loader's `ModLoader=` line); see the README.

**Downloads:** `BatoMulti-Setup-0.6.10.cmd` (recommended, 1-click setup) or `BatoMulti-v0.6.10-ManualInstall.zip` (plain files, see its README.txt).
