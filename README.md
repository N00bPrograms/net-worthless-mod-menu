# Net Worthless Mod Menu

An in-game cheat menu for **Net Worthless** (Godot 4.7, Steam app 4878900). Press **Insert** to open or close it. It uses the game's own theme and drives the game's own systems, so the HUD, logs and saves stay consistent.

## Install
Copy the contents of `mod/` into the game folder, next to `net_worthless.exe`:

```
Net Worthless/
  net_worthless.exe
  override.cfg          <- adds the menu as an autoload
  NWModMenu/nw_mod_menu.gd
```

To uninstall, delete `override.cfg` and the `NWModMenu` folder.

## Features
- **Player:** +$1K/10K/100K/1M, set exact cash, lock cash, full health and happiness, lock health and happiness at 100, cure negative status effects
- **Skills:** a slider for each skill (intellect, charisma, fitness, cunning, creativity), max all, lock all at 100
- **Life:** skip ahead N months (events auto-resolve with the first workable choice), age ±1/−5 years (minimum 18), move into any home for free, re-roll Marketplace and Classifieds listings
- **Settings:** block Steam achievements (on by default). While this is on, the achievement system's month-end and game-over checks are detached, so neither Steam nor the local achievement ledger records anything.

## Notes
- Big cash jumps can meet a run's net-worth goal right away, which ends the run with "Goal achieved". Use **Continue without a goal** to keep playing.
- Dev testing: set `DEV_CMD := true` and the menu reads commands from `NWModMenu/nwcmd.txt` (`money 1000`, `skip 3`, `shot`, `eval <expr>`, `newrun [archetype]`...) and writes the results to `nwcmd.out`.
