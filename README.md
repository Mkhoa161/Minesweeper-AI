# Minesweeper AI

This project implements a **Minesweeper game** along with an **AI player** capable of solving the game using logic and reasoning. The game board is generated with a random distribution of mines, and the AI uses knowledge-based reasoning to progressively deduce safe cells and mines. The AI is built using a set of logical statements (sentences) that help it make decisions based on the game state.

The game supports:
- An interactive Minesweeper game board.
- An AI that can automatically solve the game by marking safe cells and mines.

## Key Features
- **Minesweeper Game**: The game logic for generating the board, detecting mines, and counting neighboring mines.
- **AI Player**: The AI player uses a knowledge base to reason about the game and solve it by marking safe cells and mines.
- **Knowledge Representation**: The AI uses logical sentences to represent information about cells, mines, and safe areas.
- **Interactive Play**: The game provides an interactive representation of the board and allows for custom board sizes and mine counts.

## How It Works

### Minesweeper Game

- The game board is represented as a grid, with mines randomly placed on the board.
- Each cell in the grid can either be a mine or a safe space, and the player must flag mines while avoiding them.
- The game ends when all mines are flagged or the player clicks on a mine.

### AI Player

The AI player uses a **knowledge base** of logical sentences to keep track of the game state. The AI makes safe moves based on:
- **Known Safe Cells**: Cells that are marked as safe based on the AI's knowledge.
- **Known Mines**: Cells that are flagged as mines based on the AI's reasoning.
- **Inference**: The AI uses logical reasoning to infer new information from existing knowledge, adding new sentences to its knowledge base.

The AI can make moves automatically using the `make_safe_move()` and `make_random_move()` methods:
- **Safe Move**: The AI first tries to make a safe move based on its knowledge of the board.
- **Random Move**: If no safe move is available, the AI chooses a random move that hasn't been clicked yet.

### Game Logic

- **Board Initialization**: The board is created with specified height, width, and the number of mines. Mines are randomly placed on the board.
- **Mines and Safe Cells**: The number of mines surrounding each cell is calculated, and the AI tracks which cells are safe and which are likely to contain mines.

## Requirements

To run this project, you'll need Python 3.x installed. The project requires the following Python libraries:

- `random`
- `itertools`

These libraries are part of the standard Python library, so you don't need to install anything extra.

### Game Setup

To set up the game, you can initialize a **Minesweeper** object with the desired height, width, and number of mines:

```python
game = Minesweeper(height=8, width=8, mines=10)
