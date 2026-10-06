# BatoMulti 0.6.3 — play with your friends!

Batomon Showdown, multiplayer: create a private room, share the code, and battle your friends round
after round until one trainer is left.

## New in this build (0.6.3)

- 🎁 **Spectator gift-box fix.** Switching to another player while watching now always shows *their*
  gift box exactly as they see it (it could keep showing the previous player's opened box), and a
  gift box with a single trinket now shows when it has been taken.
- 🔄 **On 0.6.2? Update from the main menu.** Start the game: the banner offers 0.6.3 →
  **[Update Now]** → **[Restart Now]**. On 0.6.1 or older, run this setup file once by hand.
- 🤝 **Everyone in a room needs 0.6.3.** A room only accepts players with exactly the same BatoMulti
  version, so 0.6.2 and older can't join a 0.6.3 room (and the other way round).

## Since 0.6.2

- 🔄 **In-game updates.** From now on BatoMulti checks for a new version when the game starts. If there
  is one, a small banner on the main menu says **"New version available"** with **[Update Now]** and
  **[Later]**. Update Now downloads the new setup in the background and checks it against this release
  page's SHA-256 fingerprint; then **[Restart Now]** closes the game, installs the update and starts
  the game again. Offline or GitHub unreachable? Nothing is shown and you play as usual. Don't want
  the check? Put `[update]` / `check=false` in `%APPDATA%\Godot\app_userdata\Batomon Showdown\batomulti.cfg`.
- ⚠️ **One manual update needed from 0.6.1 or older.** Those versions have no updater yet: run this
  setup file once by hand (close the game, double-click it). After that, updates come from the main menu.
- 👥 **Dedicated spectator slot — Player / Spectator roles in the lobby.** A room list next to the lobby shows everyone in the
  room with a **Player / Spectator** button. You can switch your own role; the host can switch
  anyone's. Spectators are never paired, never fight and don't appear in the standings. They watch
  the match full screen from round 1 and can switch between players at any time.
- 🎁 **Chest view in sync.** When the player you're watching gets a gift box (after a battle or in the
  shop), you see the box drop and open, the same trinkets they're offered, and which one they take,
  live.
- 🖥️ **Spectator polish.** The spectator's battle screen draws both real teams (correct units,
  levels and sides), personal buttons are hidden, and the spectator bar no longer overlaps.

## Install in 3 steps

1. Download **`BatoMulti-Setup-0.6.3.cmd`** below.
2. Close the game and **double-click the file** (press Enter to confirm). It finds your game and
   handles backups for you.
3. Start Batomon Showdown through Steam → **Multiplayer** → create or join a room.

Run the same file again to uninstall. Already have another mod installed? It's set aside safely
and restored exactly as it was when you uninstall.

## What's inside

- 🔑 **Private rooms** with a 6-letter code
- ⏩ **Battle speed** 1x / 2x / 4x, chosen by the host
- 💔 **Revamped Second Chance** — come back with 1 life and pick: Board Upgrade, Element Infusion,
  a Legendary/Mythical Trinket, or Scaling Gold
- ⚔️ **Next match preview** — see who you fight next while you shop
- 🔍 **Scouting** — peek at any opponent's 3×2 board from the leaderboard
- 👀 **Spectator mode** — knocked out, or joined as a Spectator? Watch any friend's game live, full screen: their shop as they buy, their gift boxes as they open them, then their battle — switching channels joins a fight right where it is, never from the start (switch with < >)
- 🏆 **Results screen** with everyone's placement
- 🔌 **Auto-reconnect** — drop out and jump back in; if the host leaves, the match carries on

Everyone in the room needs the same BatoMulti version. Windows + Steam version of the game.

## Uninstall

Close the game and run the same file again (or `BatoMulti-Setup-0.6.3.cmd uninstall`).
Manual removal and going back to pure vanilla (Steam → Verify integrity of game files): see
[How to uninstall](https://github.com/Maxkii3/Batomon-Multiplayer#-how-to-uninstall) in the README.

**Integrity check.** BatoMulti checks its own files every time the game starts. If any of its
files were edited, it switches itself off (the game then runs normally, without multiplayer) and
shows a short notice. Fix: download the setup again from the official release and reinstall.

## ⚠️ Unofficial mod — disclaimer

**BatoMulti is an UNOFFICIAL, third-party community mod.** It is not made, affiliated with,
sponsored, approved or endorsed by the developers or publisher of Batomon Showdown. "Batomon
Showdown" and its assets belong to their respective owners. Please do not contact the game's
developers for support with this mod.

**AS-IS, NO WARRANTY.** BatoMulti is provided "as is", without warranty of any kind, express or
implied, including fitness for a particular purpose. You install and use it entirely at your own
risk. To the fullest extent permitted by law, the author accepts **no liability** for any damage or
loss arising from its use, including but not limited to corrupted or lost save data, lost progress,
account restrictions or bans, bugs, crashes, or any other data loss. A game update can break the mod
at any time.
