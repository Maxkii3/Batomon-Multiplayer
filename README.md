# BatoMulti — Batomon Showdown Multiplayer Mod

**Batomon Multiplayer for Steam on Windows: play Batomon Showdown with friends in private online rooms.**

BatoMulti is an unofficial Batomon Showdown multiplayer mod created and maintained by
[Maxkii3](https://github.com/Maxkii3). One player hosts a room: friends join with a short code or
find it in the public **room browser**. Everyone builds their team in the shop at the same time, then
battles round after round until only one trainer is left standing. Rooms hold up to 250 people, and
you can join as a spectator to watch friends live. Short on friends? Add **ghost bots** that play real
players' boards from the game's own ranked ghosts.

🏆 **Host a community tournament in one match.** One room seats up to **250 participants** (players +
spectators). Everyone fights in the same match, round after round, until one champion is left; the live
leaderboard and the final results screen give every placement. No bracket sheets, no external
tournament tools, no restarts between rounds — just share the room code.

**[Download BatoMulti](https://github.com/Maxkii3/Batomon-Multiplayer/releases)** ·
[Installation guide](#-how-to-install) ·
[Play with friends](#-how-to-play-with-friends) ·
[Report a bug](https://github.com/Maxkii3/Batomon-Multiplayer/issues)

Requires Batomon Showdown on **Steam for Windows** (built and tested on game **1.5.0**). Everyone playing
needs the same BatoMulti version and Steam running. This is a community mod, not an official multiplayer update.

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-yellow?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/maxkii3)

<div align="center">
  <a href="https://www.gsttopup.com/shop" target="_blank">
    <img src="docs/assets/gst_topup_logo.png" alt="GST Topup" width="280"/>
  </a>
  <br/>
  <sub>🎮 <b>Sponsored by / สนับสนุนโดย:</b> <a href="https://www.gsttopup.com/shop">GST Topup</a></sub>
  <br/>
  <sub><b>TH:</b> เติมเกมถูก รวดเร็ว ปลอดภัย แนะนำที่ GST Topup | <b>EN:</b> Affordable, fast, and secure game top-ups at GST Topup</sub>
</div>

---

## 📸 Preview

<table>
  <tr>
    <td width="50%"><img src="docs/screenshots/01_main_menu.png" alt="Main menu with the Multiplayer button"><br><sub><b>Main menu</b> — BatoMulti adds a <b>Multiplayer</b> button.</sub></td>
    <td width="50%"><img src="docs/screenshots/06_lobby_browser.png" alt="The Browse rooms tab: room name, host, players, spectators, status, speed, code and a lock on password rooms"><br><sub><b>Room browser</b> — find a public room: name, host, players, spectators, status and speed; 🔒 = password.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/02_lobby_room.png" alt="Room tab: room code, Copy and Chat up top, Host settings in three tabs (Content and Bans open: Region, Trainers and the four Ban buttons), the member list, and the bottom action bar with Leave room, the ready count, Force Start and Start"><br><sub><b>Your room</b> — room code + <b>Copy</b> up top, <b>Host settings</b> in three tabs (<b>Match</b> · <b>Players &amp; Bots</b> · <b>Content &amp; Bans</b>) beside the member list, and one action bar: <b>Leave room</b> · who's ready · <b>Force Start</b> + <b>Start</b>.</sub></td>
    <td width="50%"><img src="docs/screenshots/08_shop_overlay.png" alt="The shop with the live leaderboard and the next-opponent bar"><br><sub><b>Shop</b> — the live leaderboard and your <b>next opponent</b> while you build.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/03_gameplay_match.png" alt="A live battle with the leaderboard"><br><sub><b>Match</b> — everyone battles at the same time; the leaderboard tracks lives and wins.</sub></td>
    <td width="50%"><img src="docs/screenshots/04_eliminated.png" alt="The elimination card with Spectate buttons"><br><sub><b>Knocked out</b> — keep watching: follow the match or pick a player.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/05_spectator_mode.png" alt="Spectator mode watching a live battle"><br><sub><b>Spectator mode</b> — watch any player's shop and battles live, full screen; switch with &lt; &gt;.</sub></td>
    <td width="50%"><img src="docs/screenshots/07_results.png" alt="The results screen with every player's placement"><br><sub><b>Results</b> — final placements, then back to the menu with one click.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/09_region_host.png" alt="The Content and Bans tab: Region Mixed, Pantra, Jinto (Jinto lit), Trainers Random 3 or Free pick, and the four Ban buttons"><br><sub><b>Region</b> — on the <b>Content &amp; Bans</b> tab the host picks <b>Mixed</b> (every region), <b>Pantra</b> or <b>Jinto</b>.</sub></td>
    <td width="50%"><img src="docs/screenshots/10_region_guest.png" alt="A guest's room panel: the host's settings greyed out, Jinto lit, Ready Up! button"><br><sub><b>Guests</b> see every host setting (locked) in the same tabs, on joining and whenever it changes.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/11_free_pick.png" alt="Free pick: the game's trainer cards three per row in a scrolling list"><br><sub><b>Free pick</b> — the host can let every player choose any trainer, three per row.</sub></td>
    <td width="50%"><img src="docs/screenshots/12_comeback_draft.png" alt="Tactical Draft in the off-white dialog: three unit cards with their pictures, names and Defense / Offense / Support roles, Back and Confirm"><br><sub><b>Comeback</b> — on your last life, pick a boost such as <b>Tactical Draft</b> (Defense / Offense / Support), in the clean white dialog (0.7.3).</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/13_tier4_paragon.png" alt="Tier 4 event Paragon: its banner art and four choices, one reading +25% Damage, Shields, Heals and Status DoTs to all units"><br><sub><b>Tier 4 events</b> (0.7.0) — Day 12, 15, then every 3 days: the same event for everyone, <b>4 choices</b>, its own banner.</sub></td>
    <td width="50%"><img src="docs/screenshots/14_tier4_mythic_forge.png" alt="Tier 4 event Mythic Forge with Reforge, Apprentice, Master Polish and Master Smelter (+30% Damage to all units)"><br><sub><b>Mythic Forge</b> — every card says exactly what it boosts (here: <b>+30% Damage</b>).</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/15_trainer_ban_window.png" alt="The Ban Trainer window in the off-white theme: trainer portraits, three of them greyed out with a red X"><br><sub><b>Trainer Bans</b> (0.7.0) — the host clicks portraits to ban them (greyed, red X); at least 3 always stay.</sub></td>
    <td width="50%"><img src="docs/screenshots/16_trainer_ban_row.png" alt="The Bans grid: Ban Trainer (3) Banned, Ban Batomon, Ban Trinket and Ban Item None"><br><sub>The <b>Bans</b> grid shows each list: <b>None</b> or <b>(n) Banned</b>; guests see the lists read-only.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/17_trainer_ban_free_pick.png" alt="Free pick: the banned Chemist card greyed out with a red X next to two open trainers"><br><sub><b>Free pick</b> — banned cards stay in place, greyed and locked; <b>Random 3</b> never offers them.</sub></td>
    <td width="50%"><img src="docs/screenshots/18_chat_lobby.png" alt="The room tab with a yellow Chat button next to the room code and a NEW badge on it"><br><sub><b>Room chat</b> (0.7.0) — the yellow <b>Chat</b> button next to the room code; <b>NEW</b> = unread lines.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/19_match_header.png" alt="The shop's top bar: a compact NEXT MATCH pill, the heart counter, Day 2, the chat bubble with a red pip; the leaderboard shows one player shopping and two ready"><br><sub><b>Cleaner header</b> (0.7.0) — compact, draggable <b>NEXT MATCH</b>, the hearts visible again, the chat bubble (pip = unread), and <b>ready</b> / <b>shopping</b> for every player.</sub></td>
    <td width="50%"><img src="docs/screenshots/20_chat_ingame.png" alt="The Room chat window open in the shop: join notices, three players' lines with times, the input field and Send"><br><sub><b>Chat in the match</b> — names, times, notices; any language; typing never presses the game's hotkeys.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/21_whats_new.png" alt="The main menu with a What's New in BatoMulti window: ghost bots, why a bot is a different real player every Day, Trinket and Item bans, Day limit, tabs, bots fight on, and a yellow OK button"><br><sub><b>What's New</b> (0.7.1) — after an update, the new version's highlights once on the main menu.</sub></td>
    <td width="50%"><img src="docs/screenshots/24_trinket_grid.png" alt="Salvage Master in the off-white dialog: a scrolling grid of the player's trinkets, one framed, and the game's details box for Earth Crest beside it"><br><sub><b>Trinket picks</b> — your backpack as a scrolling grid with the game's details box (0.7.2), now in the clean white dialog (0.7.3).</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/22_batomon_ban_window.png" alt="The Ban Batomon window: search field, rarity tabs All to Legendary, Clear all, and a grid of unit pictures with rarity badges"><br><sub><b>Batomon Ban</b> (0.7.3) — the host bans units from the room's shops: pictures, rarity tabs, <b>Clear all</b>; 3 per rarity always stay.</sub></td>
    <td width="50%"><img src="docs/screenshots/23_batomon_ban_search.png" alt="The Ban Batomon window with pu typed: suggestion chips Puffloon, Venopuff, Pompummel and the matching units below"><br><sub><b>Live search</b> — the list filters as you type, small typos are forgiven, and <b>suggestions</b> complete the name.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/25_players_and_bots.png" alt="The Players and Bots tab: Max players, Spectators, Add bot, Ghost level Master; Bot 1 (Silver) and Bot 2 (Master) in the member list, ready, with Kick"><br><sub><b>Ghost bots</b> (new in 0.7.4) — pick a level, press <b>Add bot</b>: each bot keeps its own, shown in its name (<b>Bot 1 (Silver)</b>, <b>Bot 2 (Master)</b>); <b>Kick</b> removes it.</sub></td>
    <td width="50%"><img src="docs/screenshots/26_ghost_level.png" alt="The Ghost level dropdown open: Auto (my rank), Bronze, Silver, Gold, Platinum, Diamond, Master"><br><sub><b>Ghost level</b> — the next bot's level: <b>Auto</b> (your own rank) or a tier from <b>Bronze</b> up to <b>Master</b>.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/28_content_bans.png" alt="The Content and Bans tab: Region, Trainers and the Bans grid with Ban Trinket (3) Banned and Ban Item (2) Banned"><br><sub><b>Trinket + Item bans</b> (new in 0.7.4) — two more buttons in the <b>Bans</b> grid.</sub></td>
    <td width="50%"><img src="docs/screenshots/29_trinket_ban.png" alt="The Ban Trinket window: search, rarity tabs All to Mythical, Clear all, and trinket pictures with three of them crossed out"><br><sub><b>Ban Trinket</b> — pictures, search and rarity tabs; banned trinkets never show up in gifts, events or rewards.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/30_item_ban.png" alt="The Ban Item window: Cake crossed out, the shop's items with rarity badges"><br><sub><b>Ban Item</b> — banned items never roll in the shop's item slot.</sub></td>
    <td width="50%"><img src="docs/screenshots/27_day_limit.png" alt="The Match tab: shop timer, lives, On a tie, Day limit 37 Days, battle speed and events"><br><sub><b>Day limit</b> (new in 0.7.4) — type how many Days a match lasts (0 = no limit); then the most lives wins.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/31_only_bots_left.png" alt="An eliminated player's screen: Only bots are left: they fight on to the last one, with the leaderboard"><br><sub><b>Bots fight on</b> — when only bots are left they play to the last one; you watch the standings until the winner.</sub></td>
    <td width="50%"><img src="docs/screenshots/32_bot_night_lobby.png" alt="In the game: a room named Bot Night with the host, Bot 1 (Silver), Bot 2 (Gold), Bot 3 (Master), all ready, and a friend; Day limit 12 Days"><br><sub><b>A room with bots</b> — the host, a friend and three bots of different levels (Silver, Gold, Master); bots are ready at once.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/33_bot_night_results.png" alt="Game over at Round 9 of 12: Bot 3 (Master) wins with 1 life, then the host, a friend, Bot 1 (Silver) and Bot 2 (Gold)"><br><sub><b>Results</b> — bots are ranked like everyone else (here the Master bot won on Day 9 of 12).</sub></td>
    <td width="50%"><img src="docs/screenshots/34_bot_night_shop.png" alt="The shop on Day 4: the leaderboard Round 4/12 lists Bot 2 (Gold), Bot 3 (Master), the host, a friend and Bot 1 (Silver) with lives, wins and ready"><br><sub><b>In the match</b> — the leaderboard (and NEXT MATCH) name each bot's level; the header counts toward the <b>Day limit</b> (Round 4/12).</sub></td>
  </tr>
</table>

---

## 🛡️ Developer Stance & Safety

Players asked whether using BatoMulti could get them shadowbanned, so we asked the Batomon Showdown
developer directly. **berrymint** looked at the mod's scope and replied:

> *"This seems fine. It doesn't look like it messes with uploaded teams, and doesn't seem to touch
> anything that's server-sided, like saves or profiles."*

BatoMulti runs its rooms over Steam between players: it never tampers with uploaded teams,
server-sided profiles or saves. This is the developer's acknowledgement, not an official endorsement —
see the unofficial-mod disclaimer below.

<table>
  <tr>
    <td width="50%" valign="top"><img src="docs/assets/dev_stance_question.jpg" alt="Discord question to the developer: could you clarify your stance on this multiplayer mod? Players worry about getting shadowbanned"><br><sub><b>The question</b> — asking the developer about the mod and shadowban worries.</sub></td>
    <td width="50%" valign="top"><img src="docs/assets/dev_stance_answer.jpg" alt="berrymint replies: This seems fine. It doesn't look like it messes with uploaded teams, and doesn't seem to touch anything that's server-sided, like saves or profiles."><br><sub><b>berrymint's reply</b> — it doesn't touch uploaded teams or anything server-sided (saves, profiles).</sub></td>
  </tr>
</table>

---

## ✨ Cool features

- **Ghost bots** *(new in 0.7.4)* — no full room? The host picks a **Ghost level** and presses **Add bot**
  (on the **Players & Bots** tab) to seat a bot; every bot keeps the level it was added with, so one room
  can mix them (say a Silver bot and a Master bot). Each round a bot plays a **real player's board** from the game's own ranked ghosts,
  fetched the same way ranked play does, so the bots stay up to date with every game patch. Every round
  brings a different real player; the bot keeps its own lives and wins. Levels: **Auto** (your own rank) or
  **Bronze**, **Silver**, **Gold**, **Platinum**, **Diamond**, **Master**. Every bot's name shows its level
  everywhere (lobby, leaderboard, results): **Bot 1 (Silver)**, **Bot 2 (Master)**, or on Auto the host's
  rank, **Bot 3 (Auto: Diamond)**. Past **Day 16** the bots take their boards from the game's **Endless** ghosts, so they keep
  getting stronger as the Days go on (a new player every Day, [why](#is-a-bot-the-same-player-from-day-1-to-the-end)).
  When only bots are left, they **fight on** to the last one.
- **Trinket and Item bans** *(new in 0.7.4)* — **Ban Trinket** and **Ban Item** next to Ban Trainer and Ban
  Batomon: the same picture grid, search and rarity tabs. A banned trinket never comes up in gifts, events
  or rewards; a banned item never rolls in the shop's item slot. A few per rarity always stay.
- **Day limit** *(new in 0.7.4)* — type the number of Days a match lasts (**0** = no limit). On the last Day
  the player with the most lives (then wins) takes the match; the leaderboard shows **Round n/limit**.
- **Host settings in tabs** *(new in 0.7.4)* — the room's settings sit in three tabs: **Match** (timer, lives,
  ties, Day limit, speed, events), **Players & Bots** (room size, bots) and **Content & Bans** (region,
  trainers, every ban list).
- **Ready for game 1.5.0** *(fixed in 0.7.3)* — gift trinkets work with the game's 1.5.0 patch, also the
  new **Burglar**'s stolen trinket (its own card with **Confirm**), in single-player and in rooms. Room
  battles wait until their result is saved before leaving the battle screen, as the game now does.
- **Batomon Ban** *(new in 0.7.3)* — the host's **Ban Batomon** button opens every unit a shop can roll in
  the room's region, with pictures and rarity tabs. **Live search** filters as you type, forgives small
  typos and shows **suggestions**; **Clear all** removes every ban. Banned units never roll in a shop
  (events, drops and items can still give them). Guests see the list read-only.
- **Mixed region** *(new in 0.7.3)* — Region **All** is now **Mixed**: every region's Batomon in one shop
  pool. In Mixed (and with Batomon bans) the game's scripted first-run shop shelves are off.
- **Clean white theme** *(new in 0.7.3)* — Batomon Ban, Trainer Ban and the comeback / Tier 4 trinket and
  event pick dialogs use a clean off-white theme.
- **Backpack-style trinket picks** *(new in 0.7.2)* — Reforge, Salvage Master and Master Polish show your
  trinkets as the game's backpack slots in a scrolling grid (the picked one framed), with the game's
  details box beside it; Back and Confirm always stay on screen, however big your bag.
- **Real names in the battle intro** *(fixed in 0.7.1)* — the "vs" screen shows your opponent's **Steam
  name**, not their trainer; ghost rounds read **Name (Ghost)** there and in **NEXT MATCH** (a long name is
  shortened, the (Ghost) tag stays).
- **What's New** *(new in 0.7.1)* — after an update, the main menu shows the new version's highlights
  once; **OK** and it stays away until the next update. A first install skips it.
- **Tier 4 events** *(new in 0.7.0)* — the game's events stop after Day 9; in a room, long matches meet a
  **Tier 4 event** on **Day 12**, **Day 15**, then **every 3 days**: the same event for every player, each
  with **4 choices** and its own banner art (Fusion Altar, Champion's Arrival, Legendary Armory, Awakening
  Rite, Chrono Surge, Mythic Forge, Mythic Vault, Paragon, Overdrive Core). Output buffs say exactly what
  they boost: **+X% Damage, Shields, Heals & Status DoTs**. Rooms can start with up to **999 lives**
  (above 10, the battle shows 10 hearts and a **+n** badge).
- **Trainer Bans** *(new in 0.7.0)* — the host's **Ban Trainer** button opens the room region's trainers:
  click portraits to ban them (greyed out, red X; at least 3 stay). **Free pick** keeps banned cards in
  place, locked; **Random 3** never offers them; the room refuses a banned trainer's board.
- **Room chat** *(new in 0.7.0)* — a yellow **Chat** button in the lobby and a pixel chat bubble in the
  match's top bar (a pulsing **NEW** / glowing pip = unread). Names, times, join / leave notices,
  120 characters, any language (Thai, Japanese, Korean, Chinese...). While you type, the game's hotkeys
  are paused, so typing never rerolls or sells. Nothing is saved: the chat ends with the room.
- **Cleaner match header** *(new in 0.7.0)* — **NEXT MATCH** is a compact pill you can **drag** anywhere
  (the game's heart counter shows again), and the live leaderboard shows **ready** / **shopping** /
  **fighting** for every player.
- **1-click setup** — one file installs everything. Already using another mod? It's
  put safely aside and comes back exactly as it was when you uninstall.
- **Room browser** — the **Browse rooms** tab lists open rooms with their name, host, players,
  spectators, status and battle speed. Search by name or code, filter In lobby / Playing, and join
  with one click. Rooms refresh by themselves every 15 seconds.
- **Room names and passwords** — give your room a name, and add a password to keep it private (it shows
  a 🔒 in the browser and asks for the password on Join). A wrong password keeps the prompt open and
  shows the tries used ("Wrong password (1/3 tries)"); three wrong tries lock that player out for a
  minute, with a countdown.
- **Rooms with codes** — friends can still join straight from a code. Pick your own code (or keep the
  random one) and copy it with one click.
- **Big rooms & mini-tournaments** — the host sets **Max players** and **Spectators**: up to 250
  people per room (Steam's lobby limit). That makes a whole community tournament **one single match**:
  everyone plays at once, the leaderboard and results screen rank every participant, and spectators
  (casters, friends, eliminated players) watch any player live — no external bracket tools needed.
  The member list scrolls, so every seat stays reachable.
- **Host Kick** — the host can remove someone from the room (press **Kick**, then **Sure?**). A kicked
  player can't come back to that room, even if the host changes.
- **Speed controls** — the host picks 1x, 2x, 4x, 6x or 8x battle speed for everyone. New rooms start at
  **4x** (since 0.6.9): quick, but you still see every hit.
- **Free trainer pick** *(new in 0.6.9)* — the host's **Trainers** setting: **Random 3** (the game's usual
  three offers, default) or **Free pick**: every player chooses any trainer from the whole roster. The
  trainers keep the game's own cards, three per row, in a list you scroll with the mouse wheel; they are
  sorted the same way for everyone, so each trainer is always in the same spot.
- **Region pick** *(new in 0.6.11)* — the host's **Region** setting: **Mixed** (default, called **All**
  before 0.7.3: every region's
  units, trainers, trinkets and events in one pool), **Pantra** or **Jinto** (only that region). Guests
  see the host's choice on joining and whenever it changes; every run in the match starts in it.
- **Same events for everyone** *(new in 0.6.11)* — the host's **Events** setting: **Same for all**
  (default) gives every player the **same event** on Day 3, 6 and 9, at the same time, picked from the
  host's match seed; your own profile (new player or veteran) no longer changes which event you get.
  **Own luck** lets each player's game pick its own events, like before. New match, new events.
- **Ready for game 1.4.1** *(fixed in 0.6.12)* — **Black Belt** works again in rooms: its lone Fighting
  unit's On Victory now fires after **every** battle, as in the game's 1.4.1 patch. **Red Coin** really costs
  the life: the host's room count takes it (before, the next round gave it back while you kept the gold).
  **Sproutquill / Fernfowl** now count your team's battle damage toward their evolution in rooms too.
- **Works with Mod Loader** *(fixed in 0.6.10)* — the community Mod Loader (`Mods\mod_loader.gd`) and
  BatoMulti run side by side: the **Multiplayer** button is on the main menu whatever order their lines
  have in `override.cfg`. The setup keeps Mod Loader's line (and its `Mods` folder) untouched.
- **Ready check** — players press **Ready Up!**; the host starts when everyone is ready, or uses the
  red **Force Start** to go without waiting. In 0.6.8 everything sits in one bottom action bar:
  **Leave room** on the left, who's ready in the middle, **Force Start** + **Start match** (or
  **Ready Up!**) on the right.
- **Cancel after Battle!** — pressed Battle! too early? Press **Cancel** on the "searching" popup to go back to
  your shop while the others are still shopping, then press Battle! again.
- **Looks like the game** — every BatoMulti screen uses the game's own buttons, cards, fonts and colours.
- **Revamped Second Chance** — the first time you hit zero lives, you're back with 1 life and pick one
  of four comebacks:
  - **Board Upgrade** — every unit on your board levels up (up to level 3)
  - **Element Infusion** — give one of your units a new element
  - **Trinket** — choose a trinket whose rarity grows with the day: Common (Day 1-2), Rare (3-5),
    Super Rare (6-10), Legendary (11-16), Mythical (17+)
  - **Scaling Gold** — a pile of gold that grows the longer the match goes

  **Reworked in 0.6.8:** every comeback opens a preview first (what you gain, what
  a change costs) and only **Confirm** takes it. You see four cards:
  - **Rally Supplies** — 1.25× your next shop's base income in gold (rounded to 5, at most **130**)
    plus **3 free rerolls**. It is also the auto-pick when the choice timer runs out.
  - **Board Upgrade** — +1 level to every board unit below level 3.
  - **Element Infusion** *or* **Trinket** — Infusion offers two elements (one that fits your board, one
    wildcard) from **fire, water, grass, electric, rock, flying, fighting, toxic**; the unit keeps its
    own types and never gets one it already has. The Trinket follows the day table above.
  - **Reforge** *or* **Tactical Draft** — Reforge turns one **bench** unit into one of three species of
    the same rarity, keeping its level (the three stay the same if you cancel and come back). Tactical
    Draft offers three new units, one **Defense**, one **Offense** and one **Support**, at the best
    rarity your next shop can roll; from **Day 17** the run's **Mythical** units join that pool. With no
    free slot on your bench or board, you pick a bench unit to sell (for its normal sell value) to
    make room.
  - Draft and Reforge cards show each unit's **picture**, name and role.
  A card that can't help you (say, a board already at level 3) is swapped for another comeback.
- **Know your next opponent** — the shop shows who you fight next (⚔), so you can plan your board against them.
- **Scout your opponents** — click a name on the leaderboard to peek at their 3×2 board.
- **Spectator mode** — knocked out? Your screen becomes a live broadcast of a friend's game: their shop, board and every purchase as it happens, their gift boxes as they open them, then their battle. Flip between players with < > or the arrow keys.
- **Join as a Spectator** — just want to watch? The room list in the lobby lets everyone pick
  **Player** or **Spectator**. Spectators watch the whole match live from round 1 and never take a
  player's spot in the fights.
- **Results screen** — see who placed where, then head back to the menu with one click.
- **Auto-reconnect** — if someone's connection drops (or the game crashes), they jump right back in:
  restart the game and it rejoins the match by itself, back in your shop with your run. A dropped
  player shows as OFFLINE and never holds up the others. If the host leaves, someone else takes over and
  the match keeps going (bots included); if every other player leaves and no bot is left, the last player
  standing wins at once.
- **Back to room** — after the results, play another match in the same room with one click.

## 📥 How to install

1. **Download `BatoMulti-Setup-0.7.4.cmd`** from the [Releases](../../releases) page.
2. **Close Batomon Showdown**, then **double-click the file** and press Enter.
   It finds your game automatically and takes care of backups.
3. **Launch the game through Steam** — the main menu now has a **Multiplayer** button. Join a room!

> Windows may say "Windows protected your PC" — click **More info → Run anyway**. The setup is a plain
> text script; you can open it in Notepad to see exactly what it does.

**To uninstall**, run the same file again. Your game (and any mod it set aside) goes back to how it
was — details in [How to uninstall](#-how-to-uninstall).

**Updates.** From 0.6.2 on, BatoMulti tells you on the main menu when a new version is out:
**[Update Now]** downloads it (checked against the release's SHA-256), **[Restart Now]** installs it and
restarts the game. Coming from 0.6.1 or older? Run the new setup file once by hand. No internet? The
check stays silent and the game starts as usual. To turn the check off, add `[update]` and
`check=false` to `%APPDATA%\Godot\app_userdata\Batomon Showdown\batomulti.cfg`.

### Manual install (zip, no setup file)

Prefer a zip? Download **`BatoMulti-v0.7.4-ManualInstall.zip`** from the [Releases](../../releases) page
(it is also the file for mod sites). The zip holds only plain text: the `batomulti` folder (the mod's `.gd` scripts),
`override.cfg` and a `README.txt`. There is nothing to run.

1. **Close Batomon Showdown.** In Steam: right-click it → **Manage → Browse local files**.
2. **Extract the zip into that folder** so `batomulti\` and `override.cfg` sit directly next to
   `batomon_showdown.exe` (not inside a sub-folder).
3. **Launch the game through Steam** and look for the **Multiplayer** button on the main menu.

> ⚠️ The zip **replaces** the game folder's `override.cfg`. Any other mod that registers itself there
> (for example BatomonDPS) stops loading — back up your `override.cfg` first, or merge instead: keep
> yours and add `RunManager="*res://batomulti/run_manager_multi.gd"` and
> `BatoMulti="*res://batomulti/batomulti.gd"` under its `[autoload]` section. BatoMulti can't run with
> another mod that also replaces RunManager. Mod Loader is fine: keep its `ModLoader=` line, in any order.
> The setup file checks all of this for you; the zip can't.

To remove a manual install, delete `batomulti` and `override.cfg` (or restore your backup) — see
[How to uninstall](#-how-to-uninstall). Rooms need the exact same version: 0.7.4 only joins
0.7.4 rooms. A manual install does not update itself through the setup; download the new zip (or the
setup file) when a new version is out.

## 🎮 How to play with friends

Everyone needs BatoMulti installed (same version) and Steam running.

- **Host:** Multiplayer → give the room a name (and a password if you want) → set the room in the three
  **Host settings** tabs:
  - **Match:** shop timer, lives, ties, **Day limit**, battle speed (4x by default), events (**Same for all**
    or **Own luck**)
  - **Players & Bots:** room size, then for each bot a **Ghost level** + **Add bot**
  - **Content & Bans:** region (**Mixed**, **Pantra** or **Jinto**), trainers (**Random 3** or **Free pick**),
    **Ban Trainer** / **Ban Batomon** / **Ban Trinket** / **Ban Item**

  → keep the random **room code** or type your own (4-8 letters / digits) → **Create room** → press
  **Copy** and send the code to your friends → **Start match** once everyone is ready (or **Force Start** →
  **Confirm Force Start?** to go without waiting).
- **Friends:** Multiplayer → type the code → **Join**. Or open **Browse rooms**, find the room and
  press **Join** (enter the password if it shows a 🔒). Then press **Ready Up!**.
- **Player or Spectator:** the member list on the right of the lobby shows everyone (it scrolls in
  big rooms). Press your own **Player / Spectator** button to switch; the host can switch anyone and
  **Kick** anyone. Roles lock when the match starts, and a match needs at least 2 players.
- Build your team as usual and press **Battle** when you're ready (changed your mind? **Cancel** on the
  searching popup). When the timer runs out, your board is locked in automatically.
- **F1** opens the room panel at any time.

## Batomon Showdown multiplayer FAQ

### Can I play Batomon Showdown with friends in a private room?

Yes. With BatoMulti installed, open **Multiplayer** from the main menu. One player creates
a room and shares the room code; friends enter that code to join. Add a password and only
people who know it can get in, even from the room browser. A match needs at least two players. See [How to play with friends](#-how-to-play-with-friends) for the host settings.

### Can I play against bots?

Yes. In your room open **Players & Bots**, pick a **Ghost level** and press **Add bot**, once per bot:
each bot keeps its own level, so you can mix easy and hard bots. A bot plays a real player's board from the
game's ranked ghosts each round (a new player every round): **Auto** follows your own rank, **Master** is
the hardest. One player plus bots is enough to start
a match, and the bots fight on to the end if every player is knocked out.

### Where do the bots' teams come from?

From the same ghost download the game uses for ranked play, so they always match the current patch.
Bots only read those ghosts: a room never uploads a board, and ranked play is untouched.

### Is a bot the same player from Day 1 to the end?

No, on purpose. A bot keeps its own lives and wins, but every Day it plays a **different real player** of
the chosen level. The game's ghost files keep only a few Days of each player's run (many runs have only
one Day (44%), under 5% have Days 1-10, almost none reach Day 16), so one player's run could not last a match.
A fresh player every Day keeps the bot exactly as strong as that Day is, with no gaps, and BatoMulti only
uses what the game already downloads. Details in the [release notes](RELEASE_NOTES.md).

### Can I make a match shorter?

Yes. Type a **Day limit** on the **Match** tab. When the match reaches that Day, the player with the most
lives (then the most wins) is the winner. **0** means no limit.

### Which platforms does this Batomon multiplayer mod support?

BatoMulti supports the **Steam version of Batomon Showdown on Windows**. Each player
needs the mod installed, the same mod version, and Steam running.

### How many people fit in one room?

Up to 250 in total (Steam's lobby limit): the host sets **Max players** and **Spectators**
before the match starts. A full room turns away the next person.

### Can I run a tournament with BatoMulti?

Yes — a whole mini-tournament fits in **one match**. Create a room, raise **Max players** (and
**Spectators** for viewers) up to 250 people in total, add a password if it's invite-only, and press
**Start match** when everyone is in. All players battle round after round in the same lobby until one
is left; the leaderboard shows the standings live and the results screen gives every placement. No
bracket tool, no separate games to organise. Eliminated players and spectators can keep watching
anyone live.

### Do all players get the same events?

Yes (since 0.6.11), with the host's **Events** setting on **Same for all** (the default). The events on
Day 3, 6 and 9 are then the same for every player in a match, at the same time: the host's match seed
picks them, not each player's own luck or profile. **Own luck** switches back to per-player events. The host's
**Region** setting (**Mixed**, **Pantra** or **Jinto**) also decides which region's units, trainers,
trinkets and events everyone plays with.

### Can I watch friends without joining the match?

Yes. Choose **Spectator** in the lobby before the match starts. Spectators can watch
players' shops and battles live without taking a player slot. Eliminated players can
also keep watching.

### Is BatoMulti an official Batomon Showdown update?

No. BatoMulti is an unofficial community mod maintained by Maxkii3. It is not affiliated
with or endorsed by the developers or publisher of Batomon Showdown.
For mod support, [open an issue in this repository](https://github.com/Maxkii3/Batomon-Multiplayer/issues).

## 🧹 How to uninstall

**With the setup file (recommended)**

1. Close Batomon Showdown.
2. Double-click `BatoMulti-Setup-0.7.4.cmd` again. When BatoMulti is installed, the same file
   uninstalls it (it asks first). Or run it from a command prompt with an explicit action:
   ```
   BatoMulti-Setup-0.7.4.cmd uninstall
   BatoMulti-Setup-0.7.4.cmd uninstall "D:\SteamLibrary\steamapps\common\Batomon Showdown"
   BatoMulti-Setup-0.7.4.cmd status
   ```
3. It removes the `batomulti` folder and BatoMulti's `override.cfg`, and puts back any mod it had set
   aside (checked byte for byte). Your saves are not touched.

**By hand (if the setup file is gone)**

1. Close the game. In Steam: right-click Batomon Showdown → **Manage → Browse local files**.
2. Delete the **`batomulti`** folder and the **`override.cfg`** file in that folder.
3. Only if the setup had set another mod aside: copy everything inside
   `%LOCALAPPDATA%\BatoMulti\parked\<id>\files\` back into the game folder.

**Integrity check.** BatoMulti checks its own files every time the game starts. If any of its
files were edited, it switches itself off (the game then runs normally, without multiplayer) and
shows a short notice. Fix: download the setup again from the official release and reinstall.

**Back to pure vanilla**

Delete `batomulti`, `override.cfg` (and any other mod's folder) as above, then in Steam: right-click
Batomon Showdown → **Properties → Installed Files → Verify integrity of game files**. Note: Steam's
check repairs the game's own files but does **not** delete extra files such as `override.cfg`, so
delete those first. BatoMulti never modifies the game's `.exe` or `.pck`.

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

---

<sub>BatoMulti is an unofficial fan-made mod for Batomon Showdown (Steam, Windows). Multiplayer rooms run over
Steam between friends; matches never touch ranked play or your saved runs, and never upload ghosts (bots only read the game's own ranked ghosts).</sub>

