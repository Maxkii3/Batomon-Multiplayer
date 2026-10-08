# BatoMulti 0.6.8 — reworked comeback, new room layout

Batomon Showdown, multiplayer: create a room, share the code (or let people find it in the room browser),
and battle round after round until one trainer is left.

**Updating from 0.6.2-0.6.7:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.6.8: 0.6.7 and 0.6.8 players can't share a room.

## Last Life comeback, reworked

The first time you hit zero lives you come back with 1 life and choose one of four cards. Every card now
opens a **preview** (gold before → after, every unit's level, the unit's new types, what a Reforge loses)
with **Back** and **Confirm**; nothing is spent until you confirm. If the choice timer runs out you get
Rally Supplies.

- 💰 **Rally Supplies** — gold = **1.25 × the next shop's base income**, rounded to the nearest 5 and
  capped at **130**, plus **3 free rerolls**.
- ⬆️ **Board Upgrade** — +1 level to every board unit below level 3.
- 🧪 **Element Infusion** — two elements are offered: one that fits your board, one wildcard. Only
  **electric, fighting, fire, flying, grass, rock, toxic and water** can roll. A unit never gets an
  element it already has and keeps its own types.
- 🎁 **Trinket** — rarity by day: Common (Day 1-2), Rare (3-5), Super Rare (6-10), Legendary (11-16),
  Mythical (17+).
- 🔁 **Reforge** — turns one **bench** unit into one of three species of the same rarity at the same level.
  The three are fixed for that unit (cancelling and coming back shows the same three). Eggs and other
  event-only units can't be reforged. The preview names what is lost (for example its ability's progress).
- 🎯 **Tactical Draft** — three new units, one **Defense**, one **Offense** and one **Support**, at the best
  rarity your next shop can roll (up to Legendary). From **Day 17** the run's **Mythical** units join the
  pool. With no free slot on your bench or board, you pick a bench unit to sell for its normal value.
- Cards come in four slots (Rally · Board Upgrade · Infusion or Trinket · Reforge or Draft); a card that
  can't help you is replaced by another comeback. Offers are stored with your run, so a reconnect or a
  crash rejoin shows exactly the same cards.

## Look and feel

- 🖼️ **Unit pictures.** Tactical Draft shows three cards with each unit's picture, name and role; Reforge
  lists its three species with their pictures in a side panel next to the game's unit picker (clear of
  your team and the picker's buttons).
- 🧭 **New room layout.** Room / Browse rooms on the left with the room code and **Copy** on the right of
  the same row; host settings next to the member list; one **bottom action bar**: **Leave room** on the
  left, who's ready in the middle, and on the right **Start match** (host) with a smaller red **Force
  Start** right next to it, or **Ready Up!** (players). The Create room / Join row only shows before you
  are in a room. Long room and player names are shortened with "..." and never push the buttons away.

## Install

- **`BatoMulti-Setup-0.6.8.cmd`** (recommended): close the game, double-click it, launch the game through
  Steam. It finds the game, sets other mods aside safely and uninstalls when run again.
- New: **`BatoMulti-v0.6.8-ManualInstall.zip`** (also for mod sites) with only the `batomulti` scripts,
  `override.cfg` and a plain-text `README.txt` — nothing to run. Extract it next to
  `batomon_showdown.exe`. It replaces `override.cfg`, so other autoload mods (such as BatomonDPS) stop
  loading; see the README for merging and uninstalling.

---

# BatoMulti 0.6.7 — room browser, passwords and big rooms

Batomon Showdown, multiplayer: create a room, share the code (or let people find it in the new room
browser), and battle round after round until one trainer is left.

## New in this build (0.6.7)

- 🏆 **Community tournaments in a single match.** With rooms of up to **250 participants** (players +
  spectators), a whole mini-tournament is now just one BatoMulti match: everyone battles round after
  round in the same room until one champion is left, the live leaderboard ranks everybody, and the
  results screen gives every placement. Spectators can follow any player live. No external bracket
  tools, no separate games to schedule — share one room code (and a password if it's invite-only).
- 🔎 **Room browser.** A new **Browse rooms** tab in the Multiplayer window lists open rooms: room name,
  host, players, spectators, status (In lobby / Playing) and battle speed. Search by name or code,
  filter In lobby / Playing / Other versions, press **Refresh** (it also refreshes by itself every
  15 seconds), and **Join** with one click. Joining by code works as before.
- 🔒 **Room names and passwords.** Name your room when you create it, and add a password if you want.
  Password rooms show a lock in the browser and ask for the password on Join. A wrong password keeps
  the prompt open, gives the field back for retyping and shows the tries used (*"Wrong password (1/3
  tries)"*); three wrong tries lock that player out for a minute with a live countdown. A refused try
  never puts you in the room. Players who reconnect to a match they were already in don't need
  to type it again.
- 👢 **Host Kick.** Every member in the host's list has a red **Kick** button (press **Kick**, then
  **Sure?**). The kicked player sees *"You were kicked by the host"* and can't come back to that room,
  even after the host changes.
- 🏟️ **Big rooms, up to 250.** The host sets **Max players** and **Spectators** for the room (together up
  to 250, Steam's lobby limit). Spectators now count toward the Steam lobby size too, so a room with
  every player seat filled still lets spectators in (in 0.6.6 they were turned away on Steam).
- 📜 **Scrolling member list.** The member list next to the lobby scrolls once there are more than 8
  people, and every row keeps its Player / Spectator and Kick buttons. Long names are shortened with
  "..." everywhere (hover to see the full name), so nothing overlaps.
- ↩️ **Cancel after Battle!** Pressed Battle! too early? Press **Cancel** on the "searching" popup to go
  back to your shop while others are still shopping, then press Battle! again. If everyone is already
  ready, the battle starts as usual.
- ✅ **Ready check.** Players press the big **Ready Up!** button under the member list (it turns green
  when you're ready; press again to cancel), and everyone sees who is ready from the dots next to the
  names. The host's **Start match** starts once all players are ready; to start without waiting, the
  host presses the red **Force Start**, then **Confirm Force Start?**.
- 🔌 **Much stronger reconnect.** Game crashed or closed by accident mid-match? Start it again: BatoMulti
  rejoins your match in the background and puts you back in your shop with your run, lives and gold.
  It never turns into a solo run, and an old or finished match never pops up on a normal start. A
  dropped player shows as **OFFLINE** on the leaderboard and never holds up the others: their last
  board fights for them until they're back (after 90 s away the seat is given up).
- 🏁 **Last one standing wins at once.** When every other player has left, the survivor goes straight
  to the results — no more waiting on "Waiting for other players to finish...".
- ↩️ **Back to room.** After the results, **Back to room** takes you to the same room for another match
  (the host can leave meanwhile; the room keeps going).
- ⏱️ **Comeback timer.** The Second Chance pick counts down from 60 seconds; if you don't choose,
  Scaling Gold is taken for you so the room never waits. Once you're out of lives, no more event or
  gift-box popups.
- 🎨 **Looks like the game.** Every BatoMulti screen (lobby, leaderboard, results, spectator bar,
  elimination card, update banner) now uses the game's own buttons, cards, fonts and colours.
- 📡 **Smoother spectating in big rooms.** Spectators only receive the shop of the player they're
  watching (switching shows *Loading...* for a moment), which keeps the host's upload low in big rooms.
- 🔄 **On 0.6.2 – 0.6.6? Update from the main menu.** Start the game: the banner offers 0.6.7 →
  **[Update Now]** → **[Restart Now]**. On 0.6.1 or older, run this setup file once by hand.
- 🤝 **Everyone in a room needs 0.6.7.** A room only accepts players with exactly the same BatoMulti
  version, so 0.6.6 and older can't join a 0.6.7 room (and the other way round). Rooms from 0.6.6
  and older don't appear in the browser.

## In 0.6.6

- ⏩ **Faster battles: x6 and x8**, shown as buttons with the room's speed lit in yellow.
- 📋 **Copy the room code** with one click.
- 🎁 **Second Chance trinket by day:** Common (Day 1-2), Rare (3-5), Super Rare (6-10), Legendary
  (11-16), Mythical (17+).

## In 0.6.5

- 🏷️ **Author name corrected.** The copyright notice in every BatoMulti file now reads **Maxkii3**
  (the GitHub account). No gameplay changes.

## In 0.6.4

- ✏️ **Pick your own room code.** The lobby's room code is now a text field: keep the random code or
  type your own — 4 to 8 letters and digits (A-Z, 0-9; typed letters become capitals, anything else
  is dropped). Friends join with exactly that code.
- 🚫 **No duplicate rooms.** Before a room is created, BatoMulti checks Steam for a live room with the
  same code. If one exists you see *"Room code already in use. Please choose another code."* and
  nothing is created — pick another code.

## In 0.6.3

- 🎁 **Spectator gift-box fix.** Switching to another player while watching now always shows *their*
  gift box exactly as they see it (it could keep showing the previous player's opened box), and a
  gift box with a single trinket now shows when it has been taken.

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

1. Download **`BatoMulti-Setup-0.6.7.cmd`** below.
2. Close the game and **double-click the file** (press Enter to confirm). It finds your game and
   handles backups for you.
3. Start Batomon Showdown through Steam → **Multiplayer** → create or join a room.

Run the same file again to uninstall. Already have another mod installed? It's set aside safely
and restored exactly as it was when you uninstall.

## What's inside

- 🔎 **Room browser** with search and filters, **room names** and optional **passwords**
- 🔑 **Room codes** (random, or your own 4-8 letters / digits) for joining directly
- 🏟️ **Up to 250 people per room** (players + spectators), set by the host — a whole community
  tournament in one match; host **Kick**
- ⏩ **Battle speed** 1x / 2x / 4x / 6x / 8x, chosen by the host; **Cancel** after Battle!
- 💔 **Revamped Second Chance** — come back with 1 life and pick: Board Upgrade, Element Infusion,
  a Trinket (rarity grows with the day), or Scaling Gold
- ⚔️ **Next match preview** — see who you fight next while you shop
- 🔍 **Scouting** — peek at any opponent's 3×2 board from the leaderboard
- 👀 **Spectator mode** — knocked out, or joined as a Spectator? Watch any friend's game live, full screen: their shop as they buy, their gift boxes as they open them, then their battle — switching channels joins a fight right where it is, never from the start (switch with < >)
- 🏆 **Results screen** with everyone's placement
- 🔌 **Auto-reconnect** — drop out and jump back in; if the host leaves, the match carries on

Everyone in the room needs the same BatoMulti version. Windows + Steam version of the game.

## Uninstall

Close the game and run the same file again (or `BatoMulti-Setup-0.6.7.cmd uninstall`).
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
