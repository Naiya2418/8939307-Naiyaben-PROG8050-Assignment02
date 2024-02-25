# Gem Hunters Game

## Overview

This console-based 2D game, "Gem Hunters," is designed for two players who compete to collect the most gems within a set number of turns. The game is played on a 6x6 square board, where players move around to collect gems while avoiding obstacles.

## Game Elements

- **Players**: Player 1 starts in the top-left corner, and Player 2 starts in the bottom-right corner.
- **Gems**: Randomly placed on the board at the start of the game. Players collect gems by moving onto the corresponding squares.
- **Obstacles**: Random positions on the board represented by "O"; players cannot move through obstacles.

## How to Play

1. Players take turns to move on the board.
2. Input your movement through the console:
   - `U` for up
   - `D` for down
   - `L` for left
   - `R` for right
3. Players can move one square in any direction but cannot move diagonally or through obstacles.
4. If a player moves onto a square containing a gem, they collect the gem, and it's removed from the board.
5. The game ends after 30 moves (15 turns for each player).

## Code Structure

### Position Class

- `X`: int
- `Y`: int
- `Constructor`: `Position(int x, int y)`

### Player Class

- `Name`: string
- `Position`: Position
- `GemCount`: int
- `Methods`: 
  - `Move(char direction)`: Updates the player's position based on the input direction (U, D, L, R).

### Cell Class

- `Occupant`: string
- `Constructor`: `Cell(string occupant)`

### Board Class

- `Grid`: 2D array of type Cell
- `Constructor`: `Board()`
- `Methods`:
  - `Display()`: Prints the current state of the board to the console.
  - `IsValidMove(Player player, char direction)`: Checks if the move is valid.
  - `CollectGem(Player player)`: Checks if the player's new position contains a gem and updates the player's GemCount.

### Game Class

- `Board`: Board
- `Player1`: Player
- `Player2`: Player
- `CurrentTurn`: Player
- `TotalTurns`: int
- `Constructor`: `Game()`
- `Methods`:
  - `Start()`: Begins the game, displays the board, and alternates player turns.
  - `SwitchTurn()`: Switches between Player1 and Player2.
  - `IsGameOver()`: Checks if the game has reached its end condition.
  - `AnnounceWinner()`: Determines and announces the winner based on GemCount of both players.

### Program Class

- `Main()`: Entry point of the program; creates a Game instance and starts the game.

## How to Run

1. Clone the repository.
2. Open the solution in a C# development environment.
3. Run the program.

Have fun playing "Gem Hunters"!
