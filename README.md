Console-Based Othello Game in C
Overview
This project is a console-based implementation of the classic board game Othello (Reversi), written from scratch in the C programming language. It allows two players to play alternately, flipping opponent pieces according to the game rules. The game features a full terminal-based UI with colored outputs and player prompts, providing a visually clear and interactive experience.

Game Rules
The game is played on an 8x8 board.

Players:

Player 1 uses symbol 'X'

Player 2 uses symbol 'O'

The game begins with four discs placed in the center of the board: two 'X' and two 'O', in a diagonal pattern.

Players alternate turns and can only place a piece if it sandwiches at least one opponent piece between their new piece and another of their own (in any direction).

If a player has no valid moves, they must pass.

The game ends when:

The board is full, or

Neither player has any valid moves left, or

All of one type of piece has been eliminated.

Features
✅ Full support for Othello flipping logic (8 directions)

✅ Input validation for moves and positions

✅ Player turn handling and auto-passing if no valid moves

✅ Colored and formatted output using ANSI escape sequences

✅ Option to restart or exit the game after completion

✅ Final board display and winner announcement

Compilation Instructions
To compile the game, use a C compiler such as gcc:

bash
gcc othello_game.c -o othello_game
To run the compiled program:

bash
./othello_game
Controls
Players enter their moves using row and column numbers (1 to 8).

Example input: 4 5 (places your piece in 4th row and 5th column)

When prompted at the end:

Enter 1 to restart the game

Enter 0 to exit the game

If you have no valid moves, enter 1 to pass your turn

Example Output
text
welcome to this othello adventure:
Please enter player-1: Alice
Please enter player-2: Bob

Alice's Turn (X)
     1    2    3    4    5    6    7    8   
   ---- ---- ---- ---- ---- ---- ---- ----  
1 |    |    |    |    |    |    |    |    |
   ---- ---- ---- ---- ---- ---- ---- ----  
...
Enter your input (row col): 5 4
...
WINNER IS X
Would you like to end the game or restart?
To RESTART press '1' to exit press '0':
Code Structure Summary
Function	Purpose
main()	Runs the game loop and manages turns, board state, and UI
declare_result()	Declares the result if the board is full and shows scores
endgame()	Checks for early termination conditions
flip()	Flips a disc to the opposite symbol
check_valid()	Validates a potential sandwich move
func()	Recursive logic to flip discs in valid directions
Dependencies
Standard C libraries:

stdio.h

stdlib.h

string.h

Acknowledgment
Course Instructor: Dr. Richa Singh

Team Members:

Nishu Verma

Sarah Fatima

Reshma Maurya

