
# 2048 in C

A **C language** implementation of a simplified [2048](https://en.wikipedia.org/wiki/2048_(video_game)) puzzle game for a college assignment. Build it using the included **Makefile**, then run multiple test games with different board sizes and win conditions.

## Features

- **3 Demo Games**:
  1. 3×3 board, win at 16
  2. 2×2 board, win at 32
  3. 4×4 board, win at 2048 (classic)

- **Single Merge Rule**: Only **one** tile merge allowed per row or column per move – a requirement from the assignment, differing from standard 2048.  
- **Scoring**: In this variant, each new tile can adjust your best tile-based score. (Standard 2048 typically sums merges.)

## File Overview

- **`main.c`**: Provided by the lecturer, runs multiple sample games in a row.  
- **`game.c / game.h`**:
  - `initGame(...)`, `playGame(...)` orchestrate the session (reset board, random tiles, etc.).  
- **`board.c / board.h`**:
  - Board-related functions: clearing the board, checking for valid moves, adding random tiles.  
- **`move.c / move.h`**:
  - Core shifting and merging logic (`pushAllLines`, `moveAndMerge`) for up/down/left/right.  
- **`displayGame.c / displayGame.h`**:
  - ASCII rendering in the console, shows scores, draws row separators, etc.

## Build & Run

1. **Clone** the repo:
   ```bash
   git clone https://github.com/GurevichTom/C-2048-Game.git
   cd 2048-c
   ```
2. **Compile**:
   ```bash
   make
   ```
   This produces an executable **`game_2048`**.

3. **Run**:
   ```bash
   ./game_2048
   ```
    - It launches three example games. Follow on-screen instructions:
        - **N** or **n** for new game
        - **R** or **r** for move right
        - **L** or **l** for move left
        - **U** or **u** for move up
        - **D** or **d** for move down
        - **E** or **e** for exit

## Differences from Classic 2048

- **Merging**: Only one merge per line (or column) per move. You can easily adapt the code if you want the standard multi-merge behavior.
- **Score**: This version’s scoring might differ slightly from official 2048 (some merges and new tile additions shift the “score” logic).

## Possible Enhancements

- **Multi-Merge Behavior**: Adapt the code so multiple merges can happen per move (like standard 2048).
- **Persistent Score**: Save/load the highest score to a file.
- **Bigger Grids**: Easily extend the board to 6×6, 8×8, or beyond.

## License
Distributed under the [MIT License](https://opensource.org/licenses/MIT). See the `LICENSE` file for details.

---

Enjoy this console-based 2048 variant in C!
