# Voice of Cards Access

A mod that makes Voice of Cards: The Isle Dragon Roars playable with a screen reader. Menus, story, cards, battles, shops and the card game are spoken, and a scanner tells you what is on the board and how to walk there.

This is version 1.2.0. The whole game was played to the end with it. If something stays silent or is read wrongly, please report it.

## Download

Get the file VoiceOfCardsAccess-1.2.0.zip from the releases page: https://github.com/jeremdo95/VoiceOfCardsAccess/releases/latest

## What you need

- Voice of Cards: The Isle Dragon Roars on Steam, for Windows. The mod was tested on game version 1.0.3, Steam build 20266240.
- A screen reader. The mod was tested with NVDA only. It uses the Prism library, which also knows other screen readers, but they are untested.
- A keyboard, or an Xbox gamepad. Other gamepads are untested.
- An internet connection for the first launch.

## Known limits

- The story was played once, with one set of choices. Other choices and the optional places may hold text that stays silent.
- The mod speaks French when the game's text language is French, and English in all other languages. Text coming from the game itself stays in the game's language.
- English was tested less than French. Some English words for terrain cards are the mod's own guesses.
- The game master's spoken lines are read only while the game's subtitles are on (Options, Other, Subtitles). With subtitles off, you hear only the recorded voice, in English or Japanese: the mod stays silent on the story cards he reads aloud, and still reads choices, menus and cards without a voice, about a second late. A new game shows subtitles until it asks whether you want them.
- A game update can break the mod.

## Install

1. Find the game folder. In your Steam library, open the context menu of the game, then choose Manage, then Browse local files. The usual folder is:

   C:\Program Files (x86)\Steam\steamapps\common\VoiceofCardsTheIsleDragonRoars

2. Extract the zip anywhere, for example on your desktop. Windows puts the files in a new folder named VoiceOfCardsAccess-1.2.0. Open that folder, select everything with Ctrl + A, and copy it with Ctrl + C.
3. Open the game folder and paste with Ctrl + V. Windows may ask for administrator permission. The file version.dll must now be directly in the game folder, beside VoiceofCardsTheIsleDragonRoars.exe, not in a subfolder. This is the most common mistake: with the files in a subfolder, the game runs without the mod.
4. Start your screen reader, then start the game from Steam as usual.
5. The first launch is silent for a minute or more, sometimes several minutes on a slow computer. MelonLoader, the tool that loads the mod, downloads what it needs and prepares the game. Please wait and do not close anything. Later launches are quick.
6. You hear "Voice of Cards Access loaded." The title menu is then spoken as you move through it.

## Keys of the game

- Arrow keys, or W, A, S, D: move on the board and in menus. On a French keyboard, these are Z, Q, S, D.
- Enter: confirm.
- Backspace: go back.
- Escape: open the menu. In battle, during a turn's choices, it opens the flee menu.
- E: on the board, show the current objective again. In battle, open the card details.

## Keys of the mod

### On the board

- End: say your current card and its neighbours again.
- F3: turn off, or back on, the announcement of your card and its neighbours after each step. When it is off, a step says nothing, but events, blocked moves and the steps left of a timed escape are still said, and End still works. The mod remembers this choice for the next launch.
- Page Down: next item of the scanner.
- Page Up: previous item of the scanner.
- Home: repeat the current scanner item.
- Shift + Page Down: next scanner category.
- Shift + Page Up: previous scanner category.
- Shift + Home: say the objective card, if one is marked.

The scanner lists items nearest first. The categories are All, Exits, People, Shops, Chests and Others. Each item comes with the walk to reach it, for example "2 left, 1 up". "No walking path" means that no walk exists yet. The mod does not walk for you: you follow the steps with the movement keys.

A hidden treasure enters the scanner once you own the card that hints at it.

### In battle

- F6: all units with their state.
- T: whose turn it is.
- G: the party's gems.
- H: the party's hit points.

### In the card game

- H: your hand.
- G: the pot.
- T: the scores.
- F6: the sets.

### In the game menu

- Ctrl + Left or Right Arrow: previous or next character sheet.
- Ctrl + Up or Down Arrow: previous or next stat of that sheet: level, HP, attack, defense, speed, next level.

### Anywhere

- G: the party's gold. In battle G says the gems and in the card game the pot instead.
- F1: help, the mod's keys for where you are (board, battle, card game, menu). With a gamepad plugged in, it gives the gamepad buttons instead.
- F2: repeat the mod's last sentence.
- F9: write what is on screen to a file, for a bug report.

### With an Xbox gamepad

Tested with an Xbox gamepad only. A PlayStation gamepad has not been tested: it may work with the buttons in the same places (R2 for RT, cross for A, circle for B, square for X, triangle for Y, L1 and R1 for LB and RB), but this is not proven.

Hold the right trigger (RT), then press a button. While RT is held, the game ignores the gamepad, so nothing moves.

- On the board: D-pad down and up, next and previous scanner item. D-pad right and left, next and previous category. A, repeat the item. B, your current card and its neighbours. X, turn their announcement after each step off or on, like F3. Y, the objective card. RB, the party's gold.
- In battle: RB, the gems. LB, the hit points. X, whose turn it is. Y, all units.
- In the card game: RB, the pot. LB, your hand. X, the scores. Y, the sets.
- In the game menu: D-pad for the character sheets, as Ctrl + arrows.

In this game, B confirms and A goes back. When you choose a card to jump to, the right stick moves the cursor and the mod says each card.

## If something goes wrong

- The game starts but the mod stays silent: check that your screen reader was running, and that version.dll is directly beside the game's exe file, not in a subfolder. Then wait through one full launch.
- Still silent: the mod needs Microsoft's .NET 6 Desktop Runtime, 64-bit. MelonLoader should install it by itself, but this is untested. You can install it yourself from https://dotnet.microsoft.com/en-us/download/dotnet/6.0
- Your antivirus removes version.dll: this can happen with mod loaders. You may have to add an exception for the game folder.
- After a game update, the first launch takes as long as the very first one, and the mod may need an update of its own.

## Reporting a bug

Open an issue on https://github.com/jeremdo95/VoiceOfCardsAccess/issues

Please say what you did, what you heard, and what you expected. If you can, press F9 at the moment of the problem. Then attach these files, from the folder UserData\VoiceOfCardsAccess in the game folder:

- VoiceOfCardsAccess.log, the mod's log, and VoiceOfCardsAccess-previous.log if it is there: when the log grows too big, its older part moves to that file.
- The newest dump file, such as dump-1.txt, if you pressed F9.

The log holds the game's folder path, which can show your Windows user name, and the sentences spoken during your game, such as your character's name.

## Uninstall

Delete these from the game folder: the file version.dll, and the folders MelonLoader, Mods, Plugins, UserData and UserLibs. Your saved games are not in these folders, but the enemy weaknesses the mod remembers are in UserData and go with it. The game then runs as it did before.

## Credits and licences

- Voice of Cards Access by jeremdo95, made with the help of Claude. Free to use. This is a fan project, not affiliated with or endorsed by Square Enix.
- MelonLoader, Apache License 2.0: see the folder MelonLoader\Documentation.
- Prism, Mozilla Public License 2.0: see the folder UserData\VoiceOfCardsAccess\third-party\prism. Source: https://github.com/ethindp/prism
- No file of the game is included. You need your own copy of the game.
