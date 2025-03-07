---
lang: en-US
layout: wiki
section: twilightmenu
category: other
title: Controls
long_title: TWiLight Menu++ Controls
description: Controls for using TWiLight Menu++
---

#### Nintendo DSi, Nintendo 3DS, SEGA Saturn, and Homebrew Launcher themes
- <kbd>Left</kbd> / <kbd>Right</kbd>: Select a game / app
- <kbd class="face">A</kbd> / <kbd>START</kbd>: Launch game / app
- <kbd class="l">L</kbd> / <kbd class="r">R</kbd> or <kbd>SELECT</kbd> + <kbd>Left</kbd> / <kbd>Right</kbd>: Switch pages
- (DSi / Saturn / HBL theme) <kbd>SELECT</kbd> + <kbd>Up</kbd> / <kbd>Down</kbd> & release <kbd>SELECT</kbd>: Switch between the SD card and flashcard
- <kbd class="face">Y</kbd>: Per-game settings
   - <kbd class="face">X</kbd>: Cheat menu
      - <kbd class="face">A</kbd>: Toggle cheat
      - <kbd class="face">B</kbd>: Exit cheat menu
      - <kbd class="face">X</kbd>: Save and exit cheat menu
      - <kbd class="face">Y</kbd>: Show cheat description
      - <kbd class="l">L</kbd>: Disable all cheats
- <kbd class="face">X</kbd>: Delete/hide game
- (DSi / Saturn / HBL theme) <kbd>SELECT</kbd>: SELECT menu or DS Classic Menu (Where system menu, TWiLight Menu++ Settings, and GBA Mode can be accessed)

#### R4 theme
- <kbd>Up</kbd> / <kbd>Down</kbd>: Select a game / app
- <kbd class="face">A</kbd>: Launch game / app
- <kbd class="l">L</kbd>: Switch between the SD card and flashcard
- <kbd class="face">Y</kbd>: Per-game settings
   - <kbd class="face">X</kbd>: Cheat menu
      - <kbd class="face">A</kbd>: Toggle cheat
      - <kbd class="face">B</kbd>: Exit cheat menu
      - <kbd class="face">X</kbd>: Save and exit cheat menu
      - <kbd class="face">Y</kbd>: Show cheat description
      - <kbd class="l">L</kbd>: Disable all cheats

#### DS ROMs (using nds-bootstrap)
- <kbd class="l">L</kbd> + <kbd class="r">R</kbd> + <kbd>Up</kbd> + <kbd class="face">X</kbd> for 1 second: Swap the screens
- <kbd class="l">L</kbd> + <kbd class="r">R</kbd> + <kbd>Down</kbd> + <kbd class="face">A</kbd> for 3 seconds: Dump RAM to `sd:/_nds/nds-bootstrap`, as `ramDump.bin`
- <kbd class="l">L</kbd> + <kbd>Down</kbd> + <kbd>SELECT</kbd>: Open the in-game menu
   - RAM Viewer
      - <kbd>Up</kbd> / <kbd>Down</kbd>: Scroll
      - <kbd>Left</kbd> / <kbd>Right</kbd>: Fast scroll
      - <kbd class="face">A</kbd>: Enter RAM Editor
      - <kbd class="face">B</kbd>: Return to in-game menu
      - <kbd class="face">Y</kbd>: Specify an address to jump to
        - <kbd>Up</kbd> / <kbd>Down</kbd>: Increase / Decrease selected value
        - <kbd>Left</kbd> / <kbd>Right</kbd>: Select a value
        - <kbd class="face">A</kbd> / <kbd class="face">B</kbd>: Return to RAM Viewer/Editor at specified address
   - RAM Editor
      - <kbd>Up</kbd> / <kbd>Down</kbd> / <kbd>Left</kbd> / <kbd>Right</kbd>: Select a value
      - <kbd class="face">A</kbd>: Modify selected value
         - <kbd>Up</kbd> / <kbd>Down</kbd>: Increase / Decrease value by 1h
         - <kbd>Left</kbd> / <kbd>Right</kbd>: Increase / Decrease value by 10h
         - <kbd class="face">A</kbd> / <kbd class="face">B</kbd>: Finish modifying value
      - <kbd class="face">B</kbd>: Return to RAM Viewer
      - <kbd class="face">Y</kbd>: Specify an address to jump to
        - <kbd>Up</kbd> / <kbd>Down</kbd>: Increase / Decrease selected value
        - <kbd>Left</kbd> / <kbd>Right</kbd>: Select a value
        - <kbd class="face">A</kbd> / <kbd class="face">B</kbd>: Return to RAM Viewer/Editor at specified address
 - The in-game menu is not accessible in DSi Mode, so attempting to use the button combo in DSi Mode will instead exit the game.

#### Boot shortcuts
These should be pressed on the TWiLight Menu++ splash screen / right after the Nintendo DSi splash screen.

- <kbd>SELECT</kbd>: Open settings
- <kbd class="face">A</kbd> + <kbd class="face">B</kbd> + <kbd class="face">X</kbd> + <kbd class="face">Y</kbd>: Reset all TWiLight Menu++ settings
- <kbd class="face">B</kbd>: Boot the last ran ROM or vice versa depending on if autobooting the last ran ROM is enabled
