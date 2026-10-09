# BatoMulti 0.6.9 — 4x battles by default, Free pick trainers

Batomon Showdown, multiplayer: create a room, share the code (or let people find it in the room browser),
and battle round after round until one trainer is left.

**Updating from 0.6.2-0.6.8:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.6.9: 0.6.8 and 0.6.9 players can't share a room.

## ⏩ Battles start at 4x

New rooms now play every battle at **4x**: quick, but you still see every hit. The host can still pick
1x, 2x, 6x or 8x in the room settings before the match starts; everyone in the room always plays at the
host's speed.

## 🧑‍🤝‍🧑 Free pick trainers (host setting)

A new **Trainers** row in the host settings:

- **Random 3** (default) — the game's usual three random trainers to choose from.
- **Free pick** — every player picks **any trainer** from the whole roster of the card set.

The Free pick screen uses the game's own trainer cards, **three per row** like the normal screen, in a
list you scroll with the mouse wheel (or a controller). Trainers are sorted the same way for every player,
so each trainer always sits in the same spot. Guests see the host's choice in the room panel; it locks
when the match starts. A Free pick doesn't touch your normal "recently offered trainers" history.

## Install

- **`BatoMulti-Setup-0.6.9.cmd`** (recommended): close the game, double-click it, launch the game through
  Steam. It finds the game, sets other mods aside safely and uninstalls when run again.
- **`BatoMulti-v0.6.9-ManualInstall.zip`** (also for mod sites) with only the `batomulti` scripts,
  `override.cfg` and a plain-text `README.txt` — nothing to run. Extract it next to
  `batomon_showdown.exe`. It replaces `override.cfg`, so other autoload mods (such as BatomonDPS) stop
  loading; see the README for merging and uninstalling.

**Downloads:** `BatoMulti-Setup-0.6.9.cmd` (recommended, 1-click setup) or `BatoMulti-v0.6.9-ManualInstall.zip` (plain files, see its README.txt).
