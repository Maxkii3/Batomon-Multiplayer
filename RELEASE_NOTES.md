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
