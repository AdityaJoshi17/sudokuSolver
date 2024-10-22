# sudokuSolver

# Sudoku Solver

This project is a **Sudoku Solver** built using HTML, CSS, and JavaScript. It provides an interactive web-based interface where users can input a Sudoku puzzle, and the solver applies a recursive backtracking algorithm to find the solution.

## Project Overview

The Sudoku Solver takes input in the form of a string or grid format representing the Sudoku puzzle. It uses a recursive function to solve the puzzle, ensuring that each number placed is valid according to Sudoku rules. The interface allows users to input puzzles of varying difficulty, including easy, medium, and hard puzzles.

### Features
- **Input Validation**: Ensures the puzzle is in the correct format before solving.
- **Backtracking Algorithm**: Efficiently solves puzzles using recursion and backtracking.
- **Puzzle Difficulty**: Comes pre-loaded with three difficulty levels: Easy, Medium, and Hard.
- **Step-by-step Solution**: Displays the solved Sudoku puzzle on the interface.

## How It Works
The solver uses a **recursive backtracking algorithm**:
1. It starts by finding an empty cell.
2. It checks for all possible numbers that can fit in that cell without violating Sudoku rules (i.e., no duplicates in the same row, column, or 3x3 box).
3. The algorithm recursively fills in the next empty cell until the puzzle is solved or returns false if no solution is found.

### Core Logic
- **Recursive Solve**: The main solving logic is in the `recursiveSolve` function, which tries possible values for empty cells and backtracks when no valid solution is found.
- **Validation**: The solver validates each row, column, and 3x3 box to ensure the solution is correct.
- **Intersections**: To determine possible numbers for a cell, it checks intersections across rows, columns, and boxes using `getAllIntersections`.

## Example Usage

```javascript
var EASY_PUZZLE = "1-58-2----9--764-52--4--819-19--73-6762-83-9-----61-5---76---3-43--2-5-16--3-89--";
var solver = SudokuSolver(true);
solver.solveAndPrint(EASY_PUZZLE);
