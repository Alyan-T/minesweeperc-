# Console Minesweeper (C++)

A fully functional, terminal-based implementation of the classic Minesweeper game written in C++. 

This project was originally built during my first semester of Computer Science. I recently revisited and refactored the code to improve input validation, fix hidden bugs (like Out-of-Bounds memory access), and polish the user interface. 

## Features
* **Classic Gameplay:** Standard Minesweeper mechanics including revealing cells, placing flags, and unflagging.
* **Flood-Fill Algorithm:** Automatically reveals adjacent empty cells when a '0' mine-count cell is opened using recursion.
* **Persistent Leaderboard:** Saves player names and high scores (fastest times) locally using C++ File I/O (`leaderboard.txt`).
* **Multiple Difficulties:** Play on Easy, Medium, Hard, or specify a Custom grid size and mine count.
* **Input Validation:** Built-in safeguards to clear the input buffer and prevent infinite loops if the user accidentally types letters instead of numbers.

## How to Play

When the game starts, you will be prompted to enter your Roll Number (username) and select a difficulty. 

During the game, input commands using the following format: `[Action] [Row] [Column]`

### Controls:
Reveal a cell: r <row> <col> (e.g., 'r 0 5')
Place a flag: f <row> <col> (e.g., 'f 2 3')
Remove a flag: u <row> <col> (e.g., 'u 2 3')

*Note: The game accepts both lowercase and uppercase action letters (e.g., 'r' or 'R').*

### Winning & Losing
Win: Correctly place flags on *all* the hidden mines without opening any of them.
Lose: You reveal a cell containing a mine ('X'), or the 60-second timer runs out.

## How to Run

To run this game locally, you need a C++ compiler (like 'g++') installed on your system.
