Battleship Game

This is a console-based implementation of the classic Battleship game, where a player competes against an AI opponent.

How to Play

The game is played on a 6x6 grid.

Each player has a fleet of ships:

1 three-cell ship

2 two-cell ships

4 one-cell ships

Ships are placed either horizontally or vertically without touching each other.

Players take turns firing at enemy coordinates (x, y).

The game continues until one player sinks all enemy ships.

Gameplay Mechanics

○ represents an empty space.

■ represents a ship (hidden for AI).

X represents a hit.

T represents a miss.

Players take turns firing at enemy positions.

When a ship is completely destroyed, the game announces: "Ship sunk!".

Code Structure

Main Classes

Dot: Represents a coordinate on the board.

Ship: Stores ship attributes and its occupied coordinates.

Board: Manages the game grid, ship placement, and attacks.

Player: Base class for both AI and User.

User: Handles user input.

AI: Generates random moves for the AI opponent.

Game: Manages the game flow.

Exceptions

BoardOutException: Raised if a ship or shot is out of bounds.

BoardCrossException: Raised if ships overlap or a shot is repeated.

Running the Game

Ensure you have Python installed, then run:

python battleship.py



