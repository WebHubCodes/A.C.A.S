# A.C.A.S (Advanced Chess Assistance System)

A.C.A.S is an **advanced chess assistance system** (some might even call it a "*cheat*") which enhances your chess performance with cutting-edge real-time move analysis. Just install the userscript, open the A.C.A.S GUI and you're good to go! No downloading needed.

* No anti-features (*e.g. ads, tracking*)
* Supports the most popular chess game sites (*e.g. chess.com, lichess.org*)
* Supports multiple move suggestions, move arrow markings, chess variants & fonts
* Impossible to detect (well, you can never be sure, so let's say it's *almost* impossible)

> **Warning**
> A.C.A.S is currently in development. Expect bugs, especially on variants.
> 
## Getting Started

Simply [install the A.C.A.S userscript](https://github.com/Hakorr/A.C.A.S/raw/main/acas.user.js), open the [A.C.A.S GUI](https://hakorr.github.io/A.C.A.S/) and a supported chess game site. Then, just start playing!

> **Note**
> You need to keep the A.C.A.S tab active to keep the whole system functional. Think of the tab as an engine of a car, the userscript alone is simply an empty hull, it won't run, nor move. The A.C.A.S GUI has the chess engine which calculates the moves.

| A.C.A.S (Tab #1)    | Chess Website (Tab #2)  |
|----------------------|----------------------|
| ![image](https://github.com/Hakorr/A.C.A.S/assets/76921756/750998aa-061e-478a-a2c2-5e7c5b341775) | ![image](https://github.com/Hakorr/A.C.A.S/assets/76921756/ad87db6b-4dc5-4443-8405-29ad140d5894) |
| The engine runs on a completely different tab than the chess game page, completely isolated from it. The site cannot block the usage of A.C.A.S. | A.C.A.S sends move data via [CommLink](https://github.com/AugmentedWeb/CommLink) and the userscript displays the data on the board using [UniversalBoardDrawer](https://github.com/Hakorr/UniversalBoardDrawer). (*If "Display Moves On External Site" setting is activated!*) |

## Q&A

### Why doesn't it work?

Do you not see any moves displayed on the chess site? Are you sure you have enabled "Display Moves On External Site" box on the A.C.A.S GUI settings? After enabling that setting, please refresh the chess site to see changes.

Are you trying to play variants on Chess.com? If so, it's not currently supported very well since I had to rush the project, sorry! Please don't make an issue about it, I know.

Otherwise, it could be a bug, please make an issue [here](https://github.com/Hakorr/Userscripts/issues).

## Used Libraries

* [Fairy Stockfish WASM](https://github.com/fairy-stockfish/fairy-stockfish.wasm) (*the chess engine of A.C.A.S*)
* [COI-Serviceworker](https://github.com/gzuidhof/coi-serviceworker) (*allowing WASM on GitHub pages, extremely important library!!!*)
* [Chessground X](https://github.com/gbtami/chessgroundx) (*for displaying a board on the GUI. Modified the library a bit*)
* [FileSaver](http://purl.eligrey.com/github/FileSaver.js) (*for saving the config file*)

## Used Libraries (Made for A.C.A.S)

* [UniversalBoardDrawer](https://github.com/Hakorr/UniversalBoardDrawer) (*for drawing arrows on the GUI and the chess site chessboards*)
* [CommLink](https://github.com/AugmentedWeb/CommLink) (*for cross-window communication between the GUI tab and chess sites*)
