# Web Sudoku Solver Visualizer

An interactive web-based Sudoku solver and visualizer that demonstrates different solving algorithms in real-time. Watch as the solver works through puzzles step-by-step with visual feedback.

## Features

### Solving Algorithms

- **Backtracking Algorithm**: A brute-force depth-first search (DFS) with backtracking that systematically explores all possible solutions
- **Logical Algorithm**: Uses human Sudoku solving techniques before falling back to backtracking:
  - Naked singles
  - Hidden singles
  - Candidate elimination
  - Falls back to backtracking for remaining squares

### Interactive Features

- **Board Editing**: Click on any cell and type a number (1-9) to edit the puzzle
- **Conflict Detection**: Automatically highlights conflicting cells in red
- **Visual Feedback**: 
  - Green highlights for solved squares
  - Yellow highlights for squares being explored during backtracking
  - Blue highlights for selected cells and related rows/columns/boxes
- **Real-time Statistics**: Track the number of squares checked during solving

### Controls

- **Difficulty Selection**: Choose from Easy, Medium, or Hard puzzles
- **Speed Control**: Adjust visualization speed (Slow, Medium, Fast, Instant)
- **Random Puzzles**: Generate random puzzles at your selected difficulty level
- **Reset**: Reset the board to its initial state or clear it completely

### Keyboard Shortcuts

- `1-9`: Enter a number in the selected cell
- `Backspace`: Remove a number from the selected cell
- `s`: Solve the puzzle (when no conflicts exist)
- `Escape`: Deselect the current cell

## Getting Started

1. Open `webSudoku/index.html` in a modern web browser
2. Select your preferred solving algorithm (Backtracking or Logical)
3. Choose a difficulty level and click "Random" to load a puzzle, or manually edit the board
4. Click "Solve" to watch the algorithm work through the puzzle

## Technical Details

### Algorithm Complexity

- **Backtracking**: Time complexity grows exponentially with the number of empty squares. Efficient for easy puzzles but can be slow for hard ones.
- **Logical**: Uses constraint propagation and human techniques to eliminate candidates before backtracking, significantly reducing the search space for hard puzzles.

### Technologies

- **JavaScript**: Core solving logic and canvas rendering
- **HTML5 Canvas**: Real-time visualization
- **CSS**: Modern, responsive styling

## Project Structure

```
webSudokuSolver/
├── README.md
└── webSudoku/
    ├── index.html      # Main HTML file
    ├── canvas.js       # Solving algorithms and canvas rendering
    └── style.css       # Styling and layout
```

## How It Works

1. **Board Representation**: The Sudoku board is represented as a 9x9 2D array
2. **Validation**: Each move is validated against Sudoku rules (row, column, and 3x3 box constraints)
3. **Visualization**: The canvas is redrawn after each step with appropriate color coding
4. **Solving**: Algorithms use async/await with sleep delays to create the visualization effect

Enjoy solving Sudoku puzzles and learning how different algorithms approach the problem!
