# ◍ ATLAS//QUIZ — name every country on the map

![macOS](https://img.shields.io/badge/macOS-Übersicht-3ef0ff?style=flat-square&logo=apple&logoColor=white&labelColor=040914) ![Vibecoded](https://img.shields.io/badge/vibecoded-with%20Claude-ff5ad9?style=flat-square&labelColor=040914)

A map quiz on your desktop, in the style of Sporcle's *Countries of the World*. The map is in front of you; type a name and that country **lights up green**. Name them all before the clock runs out. It's a 2-column widget (472 × 314) in the same retro-terminal look as the rest of the collection.

| File | What |
|:--|:--|
| `atlas.jsx` | The widget |
| `atlas-data.json` | Map shapes and the answer list (332 KB, generated; see *Data* below) |

## Modes

| Tab | Quiz | Answers | Time |
|:--|:--|:-:|:-:|
| `WORLD` | Countries of the world | 197 | 15:00 |
| `AF` | Africa | 54 | 6:00 |
| `AS` | Asia | 48 | 6:00 |
| `EU` | Europe (Russia counts here) | 46 | 6:00 |
| `NA` | North America, incl. Central America and the Caribbean | 23 | 4:00 |
| `SA` | South America | 12 | 2:00 |
| `OC` | Oceania (Pacific-centred map) | 14 | 3:00 |
| `US` | US states | 50 | 8:00 |

The 197 are the 193 UN members plus Vatican City, Palestine, Kosovo and Taiwan, the same list Sporcle uses. Each continent view zooms in on its region; countries outside the quiz stay grey.

## Play

- Pick a tab, then press **START** or just start typing in the field. The timer starts on your first keystroke.
- A correct name turns its country green and the field clears itself. **No ⏎ needed.**
- Spelling is forgiving about case, accents and punctuation. Common alternates count: *Ivory Coast*, *Czech Republic*, *USA*, *UK*, *Burma*, *Holland*, *East Timor*, *Swaziland*, *DRC*, *St Lucia*…
- A name that is also the start of another open answer (*Niger* → *Nigeria*, *Dominica* → *Dominican Republic*) waits a moment so you can keep typing. Press ⏎ to lock it in right away.
- Countries too small to see show as **circles**, which turn green as well.
- **PAUSE** / **RESUME**. **GIVE UP** or running out of time shows everything you missed in **red**. **AGAIN** starts a new round.
- **▾** folds the widget to a one-line bar with your score and best; **▸** opens it again. Switching tabs pauses the current quiz, so each mode keeps its own round.
- Best per mode (most found, then fastest) is kept in `~/Library/Application Support/STUDYTERM/atlas-best.json`.

## Data

`atlas-data.json` is built from [world-atlas](https://github.com/topojson/world-atlas) (Natural Earth 1:50m, public domain) and [us-atlas](https://github.com/topojson/us-atlas) (US Census Bureau, public domain). The pipeline: Natural Earth projection, Visvalingam simplification to 18 % of the points, rounding to 0.1 px. Tuvalu has no polygon at that scale, so it's a marker at its real position. Somaliland is drawn as part of Somalia and Northern Cyprus as part of Cyprus. Borders follow Natural Earth's de-facto lines and are not a political statement.

## 🚀 Install

1. Download this repo (green **Code** button → *Download ZIP*) and double-click **`install.command`**. The first time, macOS may block it: right-click → *Open*.
   It installs [Übersicht](https://tracesof.net/uebersicht/) if you don't have it, copies `atlas.jsx` into its widgets folder and the map data to `~/Library/Application Support/STUDYTERM/`.
2. Click the text field and start typing. If clicks fall through to the desktop: Übersicht menu-bar icon → this widget → turn on interaction.

- **Needs:** macOS 13+ · nothing else
- **By hand:** copy `atlas.jsx` into Übersicht's widgets folder and `atlas-data.json` into `~/Library/Application Support/STUDYTERM/`.
- **Remove:** delete `atlas.jsx` from the widgets folder.

## 🎨 Look and position

Out of the box it sits in its default spot in the cyan terminal theme; found countries are always green. Install [**WIDGET//CTL**](https://github.com/SlicingReaper/widgetctl) to drag it anywhere on a grid (it takes two columns) and pick from 16 colour schemes × 8 styles, and to get `⌃⌥⌘W`, which hides all widgets at once.

## 🧩 Part of a collection

This widget is one of fifteen that share the same retro-terminal look, the same theming and the same show/hide hotkey. Each works on its own; together they make a desktop dashboard.

| | Widget | What |
|:-:|:--|:--|
| 💰 | [**WALLET//Ð**](https://github.com/SlicingReaper/points-wallet-widget) | Points wallet: earn for habits, spend on rewards, lock savings, keep a streak |
| 🔥 | [**75//HARD**](https://github.com/SlicingReaper/75-hard-widget) | 75 Hard challenge tracker: 7 daily tasks, day counter, auto-fail on a missed day |
| ⏱️ | [**STUDY//TERM**](https://github.com/SlicingReaper/study-timer-widget) | Study stopwatch that logs what you did, with a stats page and points |
| ✎ | [**NOTE//PAD**](https://github.com/SlicingReaper/notepad-widget) | Checklist notes with deadline countdowns, auto-expiry and a bin |
| “ | [**QUOTE//DAY**](https://github.com/SlicingReaper/quote-of-the-day-widget) | A new quote every midnight from a pool of 300, with likes and your own quotes |
| ▦ | [**TETRIS//GRID**](https://github.com/SlicingReaper/tetris-widget) | Tetris on the desktop: hold, ghost piece, levels, best score |
| ◉ | [**PONG//SOLO**](https://github.com/SlicingReaper/pong-widget) | Single-player Pong: keep the ball up, it speeds up every hit |
| ◎ | [**PONG//DUO**](https://github.com/SlicingReaper/pong-duo-widget) | Two-player Pong, 3 widgets wide: W/S vs ↑/↓, first to 7 |
| ⊞ | [**2048//TILE**](https://github.com/SlicingReaper/2048-widget) | 2048 with undo, keyboard or drag, saved between sessions |
| ⌂ | [**OUTPOST//**](https://github.com/SlicingReaper/outpost-colony-widget) | Colony-trading game: claim land, outfit robots, trade against 3 AI rivals |
| ☠ | [**DOOM//TERM**](https://github.com/SlicingReaper/doom-widget) | DOOM shareware Episode 1 in a 2-column widget: WebAssembly engine, savegames kept |
| ◍ | [**GLOBE//GUESS**](https://github.com/SlicingReaper/globe-widget) | Daily mystery country on a spinning globe: every guess glows hotter the closer it is |
| ◍ | [**ATLAS//QUIZ**](https://github.com/SlicingReaper/atlas-quiz-widget) ← you are here | Sporcle-style map quiz: type a name, the country lights up green. World, continents, US states |
| W | [**WORDLE//**](https://github.com/SlicingReaper/wordle-widget) | The daily five-letter word game: six tries, streaks, guess distribution, unlimited practice |
| 🎛️ | [**WIDGET//CTL**](https://github.com/SlicingReaper/widgetctl) | Menu-bar app that arranges and themes all the widgets, plus a ⌃⌥⌘W show/hide hotkey |

**Install all of them at once:** [`vibecoded` → install-all.command](https://github.com/SlicingReaper/vibecoded) · 🤖 Vibecoded with [Claude](https://claude.ai): I designed, directed and tested it, the AI wrote most of the code.
