# Battleship Game

This project is a command-line implementation of the popular game “Battleship.” The game allows a user to play against an AI opponent. Players take turns firing at the opponent’s ships on a 6x6 grid. The first player to sink all of the opponent’s ships wins.

## Features
- **2D Grid**: The game is played on a 6x6 grid where ships are placed and shots are fired.
- **Ship Placement**: Players place ships of various sizes, including a 3-deck ship, two 2-deck ships, and four 1-deck ships.
- **AI Opponent**: The player faces off against an AI opponent that randomly places its ships and shoots at the player’s grid.
- **Game Mechanics**: Players take turns shooting at their opponent’s ships, with feedback displayed on the grid for successful or missed shots.
- **Ship Sinking**: When all the cells of a ship are hit, the ship is considered destroyed.

## Technologies Used
- **Python**: The core programming language for implementing the game logic.
- **Random**: Used to generate random ship placements and AI moves.

## How to Play

### 1. Game Setup

The game starts by greeting the user and providing instructions. Afterward, both the user and the AI will place their ships on their respective grids.

### 2. Player’s Turn

The player enters the coordinates (x, y) to shoot at the opponent’s grid. The player can see the grid with their ships and the shots they’ve fired, represented by ‘T’ for misses and ‘X’ for hits.

### 3. AI’s Turn

The AI randomly selects coordinates and fires on the player’s grid. The game will display the updated board with the AI’s shot results.

### 4. Winning the Game

The game continues until one player sinks all of the opponent’s ships. The player who sinks all the ships first wins the game.

## How to Run the Game

1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/yourusername/battleshipgame.git
    cd battleshipgame
    ```

2. Run the game:
    ```bash
    python battleship.py
    ```

## Controls
- **User Input**: The user is prompted to enter coordinates (x, y) for shooting. The coordinates must be separated by a space (e.g., 3 4).
- **AI Movement**: The AI automatically selects random coordinates to shoot at.

## Code Explanation

### Key Classes
- **Dot**: Represents a coordinate (x, y) on the grid.
- **Ship**: Represents a ship with a specific length, direction (horizontal/vertical), and location (bow coordinates). Ships consist of multiple Dot objects.
- **Board**: Manages the 6x6 grid, handles ship placement, shot registration, and checking for out-of-bounds or overlapping ships.
- **Player**: Abstract class for both the user and the AI, managing interactions with the board and handling shots.
- **User**: Inherits from Player. Prompts the user for coordinates to fire at.
- **AI**: Inherits from Player. Randomly selects coordinates for the AI’s turn.
- **Game**: Orchestrates the entire game loop, including ship placement, player turns, and determining the winner.

### Exception Handling
- **BoardOutException**: Raised when a ship or shot is out of bounds.
- **BoardCrossException**: Raised when two ships overlap or when a player shoots at the same coordinate twice.

## How to Play
1. **Place Ships**: The user places ships on their grid. The AI automatically places its ships.
2. **Start Playing**: Players take turns shooting at each other’s grids. The game will display the current state of both boards after every shot.
3. **Game End**: The game ends when one player sinks all of the opponent’s ships.

## Example

Here’s an example of what the game might look like during play:
```
Hello!
This is the game “Battleship!” and your opponent is the AI.
Before starting the game, familiarize yourself with the rules:
1. Battleship is played on a square grid with coordinates of 6x6.
2. Each player starts with several ships of different sizes: one three-deck ship, two two-deck ships, and four single-deck ships.
3. Ships are placed on the grid horizontally or vertically. They cannot touch each other or adjacent cells, nor can they go beyond the grid’s boundaries.
4. Players take turns firing at the opponent by announcing the coordinates of their target on the grid.
    - If the shot hits an empty cell, the mark changes to “T”.
    - If the shot hits a cell with a ship, the mark changes to “X”.
    - When all decks of a ship are hit, a message will appear in the console: “Ship destroyed!”
5. The goal of the game is to sink all of the opponent’s ships before they sink yours.
    - The first player whose entire fleet is sunk loses.

Your turn!

Enter coordinates for the shot x and y separated by a space: 3 4
```

## Troubleshooting
- Ensure that the input is in the correct format: x y (without commas).
- If the ship placement or shot results in an error, make sure the coordinates are within bounds (1 to 6 for both x and y).

## Game Flow
1. **Game Setup**: Both the user and the AI place their ships.
2. **Turns**: Players take turns firing shots.
3. **Win Condition**: The game ends when all of the opponent’s ships are destroyed.
