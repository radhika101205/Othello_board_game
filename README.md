# Console-Based Othello Game in C

**File:** `othello_game.c`

## Overview

This is a fully functional console-based implementation of the classic board game **Othello (Reversi)** written in **C**. It allows **two players** to play alternately, flipping opponent pieces using the standard Othello rules. The game uses terminal colors and formatted outputs to enhance user experience.

---

## Game Rules

- The game is played on an **8x8 board**.
- **Player 1** uses the symbol `'X'`, and **Player 2** uses `'O'`.
- The game starts with four pieces in the center (two `X`s and two `O`s in diagonal).
- A move is valid only if it sandwiches at least one opponent's piece in any of the 8 directions.
- If a player has **no valid move**, they must **pass**.
- The game ends when:
  - The board is full (`64 pieces`), or
  - Neither player has a valid move, or
  - One player's pieces are entirely removed.

---

## Features

- ✅ Full Othello flipping logic (supports all 8 directions)
- ✅ Input validation and player prompts
- ✅ Turn-based system with auto-passing
- ✅ Colored terminal output using ANSI escape sequences
- ✅ Final board display and winner declaration
- ✅ Option to **restart** or **exit** after a game ends

---

## Compilation Instructions

To compile and run the program, use a terminal with a C compiler such as `gcc`:

```bash
gcc othello_game.c -o othello_game
./othello_game
```
---

## Controls

- Players enter moves as **row** and **column** numbers (from 1 to 8).
  - Example: `4 5` places a piece in row 4, column 5.
- At the end of the game:
  - Press `1` to **restart**
  - Press `0` to **exit**
- If a player has no valid moves:
  - Press `1` to **pass the turn**

---

## Sample Output

```text
welcome to this othello adventure:
Please enter player-1: Alice
Please enter player-2: Bob

Alice's Turn (X)
     1    2    3    4    5    6    7    8   
   ---- ---- ---- ---- ---- ---- ---- ----  
1 |    |    |    |    |    |    |    |    |
   ---- ---- ---- ---- ---- ---- ---- ----  
...
WINNER IS X
Would you like to end the game or restart?
To RESTART press '1' to exit press '0':
```
---

## Code Structure

| Function           | Description                                                  |
|--------------------|--------------------------------------------------------------|
| `main()`           | Runs the game loop, handles turns, input, and display.       |
| `declare_result()` | Counts scores and checks for endgame on full board.          |
| `endgame()`        | Ends game early if all pieces belong to one player.          |
| `flip()`           | Flips a board cell from `X` to `O` or vice versa.            |
| `check_valid()`    | Checks if a position is a valid candidate for flipping.      |
| `func()`           | Recursively checks sandwich condition and flips accordingly. |

---

## File Info

- **File:** `othello_game.c`
- **Language:** C
- **Type:** Console Game
- **Dependencies:** Standard C libraries (`<stdio.h>`, `<stdlib.h>`, `<string.h>`)

---

## Author

This project was developed as a hands-on implementation of:
- Game logic in C
- Recursive algorithms
- 2D array manipulation
- Terminal UI formatting with ANSI escape codes

---


Enjoy the game! 


