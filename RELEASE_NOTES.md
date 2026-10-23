# BatoMulti 0.6.11 — Region pick & same events for everyone

Batomon Showdown, multiplayer: create a room, share the code (or let people find it in the room browser),
and battle round after round until one trainer is left.

**Updating from 0.6.2-0.6.10:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.6.11: 0.6.10 and 0.6.11 players can't share a room.
Built and tested on Batomon Showdown **1.4.0**.

## 🗺️ Host Region setting

The host's settings have a new **Region** row: **All** · **Pantra** · **Jinto**.

- **All** (default for new rooms): units, trainers, trinkets and events from every region in one pool.
- **Pantra** or **Jinto**: only that region's pool, just like picking it for a solo run.
- The names come from the game itself, so a future region shows up on its own.
- Guests see the host's choice (locked), on joining and live whenever the host changes it. Everyone's run
  starts in that region when the match begins.

## 🎲 Same events for everyone

New host setting **Events**, next to Region: **Same for all** (default) · **Own luck**.

With **Same for all**, the random events on **Day 3, 6 and 9** are the **same for every player** in a
match, at the same time. The host's match seed (sent to everyone when the match starts, and kept through reconnects and host
changes) picks them, so no player gets a luckier event than the others.

- Every player's own profile no longer matters: the game's tutorial events for new players and its
  "games played" unlocks don't apply inside a lobby, so a new player and a veteran see the same event.
- With **Second Chance**, the comeback comes first and the round's event right after it: the same event
  as everyone else.
- Each new match still rolls new events; they are only shared inside one match.
- **Own luck** = each player's game picks its own events, like 0.6.10 and solo runs.
- Guests see the host's choice (locked), on joining and whenever the host changes it.
- What an event offers can still fit your own team (for example a monster that matches your types),
  exactly like in a solo run: the **event** is the same for everyone, your board is your own.

Nothing else changes: **4x** battles, **Free pick** trainers, the reworked comeback and Mod Loader
support all work as before.

## Install

- **`BatoMulti-Setup-0.6.11.cmd`** (recommended): close the game, double-click it, launch the game through
  Steam. It finds the game, sets other mods aside safely and uninstalls when run again.
- **`BatoMulti-v0.6.11-ManualInstall.zip`** (also for mod sites) with only the `batomulti` scripts,
  `override.cfg` and a plain-text `README.txt` — nothing to run. Extract it next to
  `batomon_showdown.exe`. It replaces `override.cfg`, so other autoload mods stop loading unless you
  merge (keep Mod Loader's `ModLoader=` line); see the README.

**Downloads:** `BatoMulti-Setup-0.6.11.cmd` (recommended, 1-click setup) or `BatoMulti-v0.6.11-ManualInstall.zip` (plain files, see its README.txt).
