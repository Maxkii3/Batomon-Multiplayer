# BatoMulti 0.7.6 — rooms with bots no longer get stuck after Battle!

A bug-fix update (player report, thanks!): *"playing with 5 Gold bots, after pressing Battle the game thinks
I'm still shopping; the timer ran out but stayed at 0:01, I had to exit the room."*

**Updating from 0.6.2-0.7.5:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.7.6: 0.7.5 and 0.7.6 players can't share a room.
Built and tested on Batomon Showdown **1.5.1**.

## 🐞 Fixes

- **Bots no longer hold the round after Battle!** A bot's ghost board comes from the game's ghost files or
  servers. When that was slow (a ghost file still downloading, a slow server answer), the room waited for it
  until the **whole shop timer** ran out, even after every player had pressed **Battle!**. With a long timer
  (5 minutes) that looked like a stuck room. Now, once every player is locked in, a bot gets at most a few
  more seconds; then it fights its last board (or a copy of a player's board on its first Day), the same
  fallback a bot already used when no ghost was found.
- **The shop timer no longer freezes at 0:01.** The leaderboard header stopped redrawing while you waited
  after **Battle!**, so it showed **0:01** forever when time ran out. It now counts down to the end.
- **A room no longer waits forever for a player stuck on an earlier screen.** If no player reached the next
  shop (for example a game left on the searching popup after a round with no fight), the room waited
  without end. It now opens the round after its usual 2-minute limit, like it already did when at least one
  player was there; the late player joins with the time left.
- **A battle that cannot be simulated counts as a draw** instead of stopping the round half-built on the
  host and the players' games.

---

# BatoMulti 0.7.5 — Batomon Showdown 1.5.1 fix, Room Presets, badge count past 10

An update for the Batomon Showdown **1.5.1** patch (2026-11-11), plus two community requests.

**Updating from 0.6.2-0.7.4:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.7.5: 0.7.4 and 0.7.5 players can't share a room.
Built and tested on Batomon Showdown **1.5.1**.

## 🐞 Batomon Showdown 1.5.1 fixes

- **Events were missing in ranked and solo runs with 0.7.4** (player report, thanks!): 1.5.1 changed how
  the game picks the Day 3 / 6 / 9 event (each run's pick is now locked to that run). BatoMulti's run layer
  still used the old way, so the game got no event back and skipped it, in **every** run while the mod was
  installed, not only in rooms. BatoMulti no longer replaces the game's event pick at all: the game picks
  as usual, and only inside a room with **Events: Same for all** is the result swapped for the room's
  shared event. Ranked and solo runs now get exactly the game's own events.
- **Cancel after Battle! in rooms:** 1.5.1 hides the searching popup's **Cancel** 1.5 s after **Battle!**.
  In a room the board can be taken back until the round starts, so **Cancel** now stays while the room
  is still waiting for other players, and goes away when the shop time is over.

## 💾 Room Presets (host settings)

- A **Presets** button at the end of the **Host settings** row opens the **Room Presets** window.
- **Save setting:** type a name and keep the room's rules on your PC (the same name replaces it). Each
  saved preset shows a one-line summary (shop timer, lives, speed, region, Day limit, bans) with **Load**,
  **Export** and **Delete**.
- **Export setting** saves the rules as a **`.bmpreset` file** wherever you pick (Windows' save dialog);
  **Import setting** opens one. The imported preset joins your list and, for the host, loads into the room.
  Run every match of a tournament with the same rules, or share an interesting design with friends.
- A preset holds the **rules only**: shop timer, lives, tie rule, Day limit, battle speed, events, room
  size, bot level, region, trainer pick and all four ban lists. Never the room name or the password.
- An imported file is checked value by value: numbers are kept in range, unknown choices are ignored, and
  bans the game doesn't know (or that would leave too few of a rarity) are left out, with a note.
- Guests can save, export and import the room's rules; only the host can load them into the room.

## 🏅 Badge count past 10 wins

- Room matches go on past 10 wins. From the **11th badge** the win screen shows the badge and **x11**,
  **x12**... like the game's Extended Mode, instead of a 10-slot badge case with the new badges placed
  off the screen.

---

# BatoMulti 0.7.4 — Ghost bots, Trinket & Item bans, Day limit

Play with bots when the room is short of friends, plus three new host settings.

**Updating from 0.6.2-0.7.3:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.7.4: 0.7.3 and 0.7.4 players can't share a room.
Built and tested on Batomon Showdown **1.5.0**.

## 🤖 Ghost bots

- Pick a **Ghost level** and press **Add bot** (host, **Players & Bots** tab) to seat a bot. Every bot keeps
  the level it was added with, so a room can mix levels (a Silver bot and a Master bot). A bot is always
  ready; **Kick** removes it, and it stays in the room after **Back to room**.
- Each round a bot plays a **real player's board** from the game's own ranked ghosts: the same ghost
  download the game uses for ranked play, so bots always match the current patch. Bots only read those
  ghosts; a room never uploads a board.
- **Ghost level:** **Auto** (your own rank) or a fixed tier: **Bronze**, **Silver**, **Gold**, **Platinum**,
  **Diamond**, **Master**. With a fixed tier the game downloads that tier's ghost files in the background
  the first round.
- Every bot's **name shows its level** for everyone, in the lobby, the leaderboard, NEXT MATCH and the
  results: **Bot 1 (Silver)**, **Bot 2 (Master)**; on Auto the host's own rank, **Bot 3 (Auto: Diamond)**.
- **Past Day 16** the bots take their boards from the game's **Endless** ghosts, so they keep getting
  stronger as the Days go on.
- **When only bots are left, they fight on** to the last one. Knocked-out players see the standings and a
  note while the bots finish the match.

### Why a bot meets you with a different player every Day

A bot keeps its own lives and wins for the whole match, but its board comes from a **different real
player every Day**, not from one player's run growing Day after Day. That is on purpose:

- The game's ghost files are a **sample**: one saved board per player per Day, and only a few Days of each
  run. In the files we checked (about 9,000 ranked runs, both regions), **44%** of the runs have a
  single Day, **under 5%** have every Day from 1 to 10, and **almost none** have Days 1 to 16. Hardly any
  run continues into the Endless Days.
- So "the same player growing" would last a few Days at most, then have to switch players or reuse an
  old board anyway (a bot that stops growing).
- Asking the game's server for one player's whole run is something the game itself never does. BatoMulti
  only uses what the game already downloads, so it stays away from anything server-sided.
- A fresh player of the chosen tier every Day keeps every bot at the strength that Day really has, with
  no gaps.

## 🚫 Trinket and Item bans (host)

- **Ban Trinket** and **Ban Item** join Ban Trainer and Ban Batomon in the **Bans** grid: pictures, search,
  rarity tabs and **Clear all**, like Ban Batomon.
- A banned trinket never comes up in gifts, events or battle rewards; a banned item never rolls in the
  shop's item slot. Each rarity always keeps a few (3 trinkets, 1 item).
- Guests see the lists read-only; each row shows **None** or **(n) Banned**.

## 📅 Day limit (host)

- Type how many Days a match lasts (**0** = no limit). After that Day's battles the match ends: the player
  with the most lives wins (then the most wins). The leaderboard shows **Round n/limit**.

## 🗂️ Host settings in tabs

- The room settings sit in three tabs: **Match** (shop timer, lives, ties, Day limit, battle speed,
  events), **Players & Bots** (room size, bots) and **Content & Bans** (region, trainers, every ban list).

---

# BatoMulti 0.7.3 — Batomon Showdown 1.5.0 update, Mixed region, Batomon Ban

An update for the Batomon Showdown **1.5.0** patch (2026-11-07), plus two new host settings.

**Updating from 0.6.2-0.7.2:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.7.3: 0.7.2 and 0.7.3 players can't share a room.
Built and tested on Batomon Showdown **1.5.0**.

## 🐞 Batomon Showdown 1.5.0 compatibility

- **Gift trinkets:** 1.5.0 changed how a gift pick is confirmed: the game now reports a second, stolen
  trinket (the new **Burglar**) and shows it on its own card with **Confirm**. BatoMulti's run layer now
  passes that result through exactly like the game, so gift picks (also the Burglar's stolen trinket)
  work in single-player and in rooms.
- **Room battles** now wait until the battle result is saved before leaving the battle screen, the same
  safety the game added in 1.5.0 (at x4-x8 speed a battle could end before its result was saved).

## ✨ Mixed region

- The host's Region **All** is now called **Mixed**: every region's Batomon in one shop pool.
- In **Mixed** (and in any room with Batomon bans) the game's scripted first-run shop shelves are off, so
  everyone gets normal shops.

## ✨ Batomon Ban (host)

- A new **Ban Batomon** button in the Trainers row opens a ban window with every Batomon of the room's
  region that a shop can roll (Common to Legendary), sorted by rarity, with their pictures and rarity
  tabs. Each rarity always keeps a few unbanned Batomon.
- **Live search:** type a name and the list filters as you type; small typos are forgiven and
  **suggestions** appear under the field (click one or press Enter). **Clear all** removes every ban.
- Banned Batomon never appear in **shop rolls**. Events, drops and items can still give them, on purpose.
- Guests see the host's list read-only; the row shows **None** or **(n) Banned**.
- Bans are picked by hand: there is no "Community picks" preset list.

## 🎨 Clean white theme

- The **Batomon Ban**, **Trainer Ban** and the comeback / Tier 4 trinket and event pick dialogs use a
  clean off-white theme.

---

# BatoMulti 0.7.2 — Backpack-style trinket picks

A small update on top of 0.7.1, from a player report.

**Updating from 0.6.2-0.7.1:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.7.2: 0.7.1 and 0.7.2 players can't share a room.
Built and tested on Batomon Showdown **1.4.1**.

## 🐞 Fixes

- **Trinket picks ran off the screen:** the Tier 4 choices that take your own trinkets (**Reforge**,
  **Salvage Master**, **Master Polish**, Day 12 and later) listed every trinket as a text button. With a
  big bag the list ran past the bottom of the screen and pushed **Confirm** out of view. The choices now
  sit in a scrolling area: the title, **Back** and **Confirm** always stay on screen, and every dialog
  opens at the top of its list.

## ✨ Backpack-style trinket grid

- Your trinkets show as the game's own **backpack slots** (the trinket icons, 5 per row). The picked slot
  gets a yellow frame, the slot under the mouse a blue one.
- A **details box** beside the dialog shows the hovered trinket's name, rarity and effect, in the game's
  own description style; with nothing hovered it shows the trinket you picked. It never covers the grid
  or the buttons, and **Back** clears it.
- In one-pick choices (Salvage Master, Master Polish), clicking another slot moves your pick there.

---

# BatoMulti 0.7.1 — Real names in the battle intro, What's New

A small update on top of 0.7.0.

**Updating from 0.6.2-0.7.0:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.7.1: 0.7.0 and 0.7.1 players can't share a room.
Built and tested on Batomon Showdown **1.4.1**.

## 🐞 Fixes

- **Battle intro names:** the "vs" screen at the start of a room battle showed your opponent's
  **trainer** (e.g. "Bug Catcher") instead of the player. It now shows their **Steam name**, the same
  name as NEXT MATCH and the leaderboard. With the game's *Hide usernames* setting on, it still shows
  trainer names, as in the base game.
- **Ghost rounds:** when the odd player out fights a copy of someone's board, the intro and NEXT MATCH
  read **Name (Ghost)**. A long name in the NEXT MATCH pill is shortened before the tag, so **(Ghost)**
  never disappears. Spectators watching a ghost round see the tag too.
- **Crash guard:** if one of the game's key hints ever appears while its action has no key bound (the
  path behind the 0.7.0 crash after a battle), BatoMulti puts the game's default keys back first, so the
  game keeps running.

## ✨ What's New window

- After an update, the main menu shows **What's New in BatoMulti** with the new version's highlights,
  once. Press **OK** (or Enter / Esc) and it stays away until the next update.
- A brand-new install skips it. The version you acknowledged is kept in `batomulti.cfg`.

---

# BatoMulti 0.7.0 — Tier 4 events, Trainer Bans, Room chat

Batomon Showdown, multiplayer: create a room, share the code (or let people find it in the room browser),
and battle round after round until one trainer is left.

**The biggest update since the room browser:** late-game events for long matches, host trainer bans, a
room chat in the lobby and during the match, a cleaner match header, and a crash fix.

**Updating from 0.6.2-0.6.12:** the main menu shows the update banner: **[Update Now]**, then
**[Restart Now]**. Everyone in a room needs 0.7.0: 0.6.12 and 0.7.0 players can't share a room.
Built and tested on Batomon Showdown **1.4.1**.

## 🌋 Tier 4 late-game events

The game's events stop after Day 9. In a room, long matches now meet **Tier 4 events**: the first on
**Day 12**, the second on **Day 15**, then one **every 3 days**. Every player in the room gets the
same event on the same Day, and every event offers **4 choices** with its own banner art.

| Event | The 4 choices |
|---|---|
| Fusion Altar | 1 unit Shiny · a free Shiny Berry in the shop · +15 % output (board) · +10 free rerolls +150 gold |
| Champion's Arrival | swap a unit for 1 of 3 Lv2 Legendaries · the same 3 to the bench · +25 % output (2 units) · next 2 monsters free +5 rerolls |
| Legendary Armory | 1 of 3 Legendary trinkets · a sealed Legendary trinket +80 gold · scrap 1 trinket for +20 % output (board) · +12 free rerolls |
| Awakening Rite | +1 level (Lv4 max) · board units under Lv3 to Lv3 · +35 % output (1 unit) · shop rank +1, +100 gold |
| Chrono Surge | +60 % cooldown speed (1 unit) · +30 % (2 units) · +15 % (board) · that Day's shop at half price |
| Mythic Forge | 2 trinkets into 1 of 3 a tier higher · shop rank +1 with Mythic luck · +1 copy of a held trinket · release the bench: **+30 % Damage** (board) |
| Mythic Vault | 1 of 3 Mythical trinkets · 2 sealed Mythical trinkets · +15 % output (board) + a Shiny Berry · +20 free rerolls +250 gold |
| Paragon | +1 level & Shiny · 2 units Shiny · +25 % output (board) · 1 of 3 top-tier species, Lv3 Shiny |
| Overdrive Core | +100 % cooldown speed (1 unit) · +50 % (2 units) · +25 % (board) · +150 % on the slowest unit |

"Output" is spelled out on every card: **+X % Damage, Shields, Heals & Status DoTs** (Burn, Poison,
Shock) — the game's own output multipliers, permanent like the game's buffs.

- **Room lives up to 999:** the host can start everyone with many lives to reach the late Days. Above 10
  lives the battle screen shows 10 hearts and a **+n** badge instead of running off the screen.
- **Second Chance is unchanged:** the last-life comeback plays exactly like 0.6.12; Tier 4 events are
  separate and never replace it.

## 🚫 Trainer Bans (host)

- **Ban Trainer** in the room settings opens the trainer list of the room's region: the host clicks
  portraits to ban them (greyed out with a red X). Guests see the list read-only.
- The room row shows the status: **None** or **(n) Banned**, the names in the tooltip.
- **Free pick:** banned cards stay in place, greyed and locked. **Random 3:** banned trainers are never
  offered. At least 3 trainers always stay playable.
- The host's room refuses a board with a banned trainer, so nobody can play one.

## 💬 Room chat

- **Lobby:** a yellow **Chat** button next to the room code, with a pulsing **NEW** badge for unread lines.
- **During the match:** a pixel chat-bubble icon in the top bar, next to the game's own icons; a glowing
  pip on its corner means unread lines.
- The window shows the name, time and text of every line (your lines, other players and room notices
  such as "X joined the room" in their own colours). Type up to 120 characters, **Enter** or **Send**,
  close with the red **X**.
- **Any language:** Thai, Japanese, Korean, Chinese and Latin all display; while you type, the game's
  hotkeys (R / D reroll, E sell, Space) are paused, so typing never plays your shop and IME conversion
  with Space works. Click outside the chat to hand the keys back.
- Chat lives only in the room: it is gone when you leave, nothing is saved. A short flood limit keeps it
  readable.

## 🧭 Cleaner match header

- **NEXT MATCH** is now a compact pill as wide as its text, so the game's **heart counter** is visible
  again. **Drag it** anywhere; the place is remembered. A click still scouts your next opponent.
- **Ready / Shopping** in the live leaderboard for every player and spectator: a green check +
  "ready" once a player pressed Battle!, "shopping" while they build, "fighting" during battles.

## 🐞 Fixes

- **Crash after a battle:** a room-code or password field could lose every key binding of the game;
  the next shop then closed the game (release build). The bindings are never lost now.
- **Typing in chat** no longer rerolls, sells or confirms behind the window (any keyboard language, IME
  included).
- **Host reconnect:** the game's own exit icon took the host to the title mid-match with no way back.
  The title now offers **Back to match** and you continue in the same round.
- **Spectator gift boxes:** a spectator watching a shop could see a new gift box's cards before the
  player opened it.
- **Ready column:** "ready" vanished once you pressed Battle! yourself, and spectators never saw it.

## Compatibility

- Batomon Showdown **1.4.1** (Steam, Windows). Every player in a room needs **BatoMulti 0.7.0**
  (protocol 9).
- Works side by side with the community **Mod Loader**.
