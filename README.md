# Deity Zenith WBC3

A summoning and leveling CE table for **Warlords Battlecry 3**, by Bener Kaya.

Deity Zenith lets you play god in **Warlords Battlecry 3**. Pick something in Cheat Engine table, point at the map with the mouse, press the summon key, and it appears there:

- **Units** of every faction, plus elementals, dragons, titans, neutral creatures and the hero templates
- **Buildings** of every faction, plus mines, towers, walls and neutral buildings (temples, lairs, guardians, shrines...)

You also choose **whose side** the summons are on: **your own side**, any other side (**Side 0 to 5**), or the **Neutral** side. You can summon 1 to 20 units per key press.

Deity Zenith can also **level up the selected unit**: select a unit in the game (yours, an enemy, an ally or a neutral creature), pick a level up to 20 and press the level up key. The game levels the unit itself, as if it had earned the experience in battle: normal stat gains, the level-up effect and a small heal.

Everything runs through the game's own routines (the same ones it uses for its own summon spells and level-ups), so summons and level-ups behave like normal game units.

## Features

- **Summon at the mouse cursor** (or at the screen center), for any side.
- **One list for units and buildings:** "Summon Type" switches the list between Units and Buildings. Each list remembers its own pick.
- **One summon key** (F10 by default) for both units and buildings.
- **Buildings appear fully built.** The mouse marks the top middle of the building.
- **Level up any selected unit** to level 1 to 20, with **one key** (F11 by default) or by ticking "Level Script".
- **Categorized lists** with the game's own names: the 16 factions, Elementals, Dragons, Titans, Neutral and Hero for units; the 16 factions, Mine, Towers, Walls and Neutral for buildings. Full lists: [unit_list.txt](unit_list.txt) and [building_list.txt](building_list.txt).
- **Silent:** no chat messages and no popups while you play. The "Diagnostics" section shows what happened.

## What you need

- **Warlords Battlecry 3**, GOG version 1.03 (Windows). Deity Zenith only works with this exact `Battlecry III.exe`:
  - SHA-256 `77D47D0EFF727BDEC9845B0CC47E63147F470B6059D379C3F0121DBD5B5689CE`
  - Any other version is refused safely (see Troubleshooting).
- **[Cheat Engine](https://www.cheatengine.org/) 7.x**, started with **Run as administrator**. The GOG game runs as administrator, so Cheat Engine must too.
- Optional: **[cnc-ddraw](https://github.com/FunkyFr3sh/cnc-ddraw)**, for windowed mode and easy Alt+Tab between the game and Cheat Engine.

## Install

Nothing to install. Put these files in any folder:

| File | What it is |
|---|---|
| `Deity Zenith WBC3.CT` | the Cheat Engine table |
| `unit_list.txt` | every unit in the list, with its game code |
| `building_list.txt` | every building in the list, with its game code |
| `README.md` | this file |

The table works on its own: the lists are built into it. The two `.txt` files are only there for reference and can be kept anywhere (or left out).

## How to use it

1. Start **Warlords Battlecry 3** and start a game (for example a Skirmish). Wait until you see your units.
2. Start **Cheat Engine** with **Run as administrator** and open **`Deity Zenith WBC3.CT`**.
3. Tick **"Deity Zenith - Enable"**. Cheat Engine connects to the game by itself (no need to pick the process).
4. **Summon:** choose "Summon Type" (Units or Buildings), pick what to summon under "Summon", choose "Side" and "Count", put the mouse on the map and press **F10**.
5. **Level up:** select a unit in the game, set "Level" and press **F11** (or tick "Level Script"; the tick clears itself).
6. Untick "Deity Zenith - Enable" before closing the game.

## The table

| Entry | What it does | Default |
|---|---|---|
| **Deity Zenith - Enable** | turns Deity Zenith on (connects to the game and checks its version) | off |
| ---Summon Units/Buildings--- | section title, does nothing | |
| **Summon Type** | Units or Buildings: switches the "Summon" list | Units |
| **Summon** | what to summon (the unit list or the building list) | first entry of each list (Knight: Archon / Knight: Cathedral) |
| **Side** | My side, Side 0 to 5, Side 6 (Neutral) | My side |
| **Count** | units per key press, 1 to 20 (buildings: always 1) | 1 |
| **Where** | Cursor or Screen center | Cursor |
| **Summon Key** | the summon key: F10, F11, Insert, Home, End, Page Up, Page Down, Pause, Middle mouse or Off | F10 |
| ---Level Up Selected Units--- | section title, does nothing | |
| **Level** | the level to raise the selected units to, 1 to 20 | 20 |
| **Level Script** | tick it to level up the selected units now; it unticks itself | |
| **Level Up Key** | the level up key (same choices as Summon Key) | F11 |
| ---Other--- | section title, does nothing | |
| **Diagnostics** | results of the last summon / building / level up, counters, cursor tile | |
| **Tuning** | cursor calibration, battle check, unit and building limits (normally left alone) | |

If you choose the same key for Summon Key and Level Up Key, the one you changed last keeps the key and the other one switches to Off.

## Good to know

- **Sides:** Side 0 to 5 are the six player slots (Red, Blue, Green, Purple, Black, Yellow). **Side 6 is the Neutral side** (the map's neutral creatures). "My side" is always your own side, whatever slot you play.
- **Neutral summons** are run by the game like the map's own neutral creatures.
- **Limits:** the game has room for 1000 units and 500 buildings. Deity Zenith stops at 850 units and 450 buildings ("Unit limit" / "Building limit" under Diagnostics), so the game never runs out. Each time you tick "Deity Zenith - Enable" you can summon up to 300 units and 150 buildings ("Session limit"); untick and tick it again for more.
- **Buildings need room:** water, cliffs, trees, units and other buildings block a building. The game then simply refuses it ("Blocked here" under Diagnostics).
- **Spawned enemy buildings belong to that side.** In "destroy everything" games you must destroy them too before you can win.
- **Units reach at most level 20** in this game version.
- **Levels are only raised.** A unit already at or above the chosen level is left as it is.
- **Heroes and titans are not leveled.** Heroes level through the hero screen, and the game never gives titans experience. Buildings in the selection are ignored too.
- **Drag-selecting only keeps your own units** (that is how the game works). Enemy, allied and neutral units are selected and leveled one at a time.
- Every unit that levels up shows the game's own "Gained Level" text; the flash and sound play only for your own units.
- The **"Hero"** units in the list are the game's hero templates. They may behave oddly as summons; try them on a throwaway skirmish.
- Deity Zenith is made for **single player**.

## Troubleshooting

| Message | What it means |
|---|---|
| **Start Warlords Battlecry 3 first.** | The game is not running. Start it, then tick "Deity Zenith - Enable" again. |
| **Run Cheat Engine as administrator (the game runs as admin).** | Cheat Engine cannot read the game. Close Cheat Engine and start it again with right-click > **Run as administrator**. |
| **This game version is not supported.** | Your `Battlecry III.exe` is not the GOG 1.03 version (for example a patched exe). Nothing was changed in the game. |

If a summon or level up does nothing, open **Diagnostics**:

| Diagnostics says | What to do |
|---|---|
| Not in battle | Start or resume a battle; the map must be showing. |
| Cursor off map | Put the mouse over the map, not over the interface. |
| Side refused | That side can't be used here (for example in multiplayer). |
| Unit limit / Building limit | Too many units or buildings on the map. |
| Session limit | Untick and tick "Deity Zenith - Enable" again. |
| Blocked here | Pick a free, flat spot for the building. |
| Nothing selected | Select a unit in the game first. |
| Already at level | The unit is already at that level or higher. |
| Heroes skipped | Heroes can't be leveled by Deity Zenith. |

## Credits

Deity Zenith WBC3 by **Bener Kaya**.
Warlords Battlecry is a trademark of its respective owners. This is an unofficial fan-made table.
