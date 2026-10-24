# BatoMulti 0.6.12 — Hotfix for Batomon Showdown 1.4.1

Batomon Showdown, multiplayer: create a room, share the code (or let people find it in the room browser),
and battle round after round until one trainer is left.

**A compatibility and bug-fix update for the game's 1.4.1 balance patch.** No new features, no new
settings: rooms play exactly like 0.6.11, with these fixes.

**Updating from 0.6.2-0.6.11:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.6.12: 0.6.11 and 0.6.12 players can't share a room.
Built and tested on Batomon Showdown **1.4.1**.

## 🥋 Black Belt works again

The game's 1.4.1 patch moved Black Belt's bonus (the lone Fighting monster's **On Victory**) from "at the
start of battle" to "after each battle". BatoMulti's room battles never ran that new step, so in rooms
Black Belt did nothing at all. Now it fires after every battle, win or lose, exactly like in a solo run,
on both sides of a battle.

## 🪙 Red Coin really costs the life

Red Coin trades 1 life for 20 gold. In a room the host keeps everyone's lives, and the next round put the
spent life back while you kept the gold. Now the spent life goes to the host: the room's count (and the
leaderboard) takes it at the start of the round.

- It still can't take your last life (the item needs 2 lives), as in the game.
- Each match counts from zero.

## 🌱 Sproutquill / Fernfowl evolve in rooms

These Jinto units evolve after your team has dealt enough battle damage. In rooms that damage was never
counted, so they never evolved. Now every room battle counts it, as in a solo run.

## ✅ Checked against the 1.4.1 patch

- Basic Bait (cost 0 -> 10), Summon Potion (5 -> 10), Glamour Potion (+30 sell value per monster) and
  Fate Potion (double base sell value, 8 free rerolls) come straight from the game: nothing to change.
- Tempo Charm, Metal Bat and Ancient Plume are Unique now: the game's shop and events never offer a
  second copy, BatoMulti's comeback trinkets use the same rule, and every player's game reads boards
  the same way, so the battles stay in sync.

## Install

- **`BatoMulti-Setup-0.6.12.cmd`** (recommended): close the game, double-click it, launch the game through
  Steam. It finds the game, sets other mods aside safely and uninstalls when run again.
- **`BatoMulti-v0.6.12-ManualInstall.zip`** (also for mod sites) with only the `batomulti` scripts,
  `override.cfg` and a plain-text `README.txt` — nothing to run. Extract it next to
  `batomon_showdown.exe`. It replaces `override.cfg`, so other autoload mods stop loading unless you
  merge (keep Mod Loader's `ModLoader=` line); see the README.

**Downloads:** `BatoMulti-Setup-0.6.12.cmd` (recommended, 1-click setup) or `BatoMulti-v0.6.12-ManualInstall.zip` (plain files, see its README.txt).
