# Sudoku Solver | LeetCode 37

## Problem Statement

Write a program to solve a Sudoku puzzle by filling the empty cells.

Rules:

- Each row must contain digits 1–9 exactly once.
- Each column must contain digits 1–9 exactly once.
- Each 3×3 subgrid must contain digits 1–9 exactly once.

The input board always has a unique solution.

---

## Approach

The Sudoku Solver is solved using **Backtracking**.

The algorithm scans the board until it finds an empty cell (`.`).

For that cell:

1. Try placing digits from `1` to `9`.
2. Check if the digit is valid.
3. If valid:
   - Place the digit.
   - Solve the remaining board recursively.
4. If no digit works, remove the digit and backtrack.

The recursion ends when every cell is filled.

---

## Algorithm

1. Traverse the board.
2. Find the first empty cell.
3. Try digits 1–9.
4. Validate the placement.
5. Place the digit.
6. Recur for the remaining board.
7. If recursion fails:
   - Remove the digit.
   - Try the next number.
8. Return true once the board is completely solved.

---

## Validity Check

A number can be placed only if:

- It is not present in the same row.
- It is not present in the same column.
- It is not present in the corresponding 3×3 subgrid.

---

## Optimized Approach

Instead of scanning rows, columns, and boxes every time, maintain three lookup tables:

- `row[9][10]`
- `col[9][10]`
- `box[9][10]`

This allows checking whether a number can be placed in **O(1)** time.

Box index is calculated as:

```
box = (row / 3) * 3 + (col / 3)
```

---

## Complexity

### Standard Backtracking

- Time: Exponential (worst case)
- Space: O(81) recursion stack

### Optimized Backtracking

- Validity check becomes O(1)
- Overall performance improves significantly.

---

## Concepts Used

- Backtracking
- Recursion
- Matrix Traversal
- Hashing
- Constraint Checking

---

## Key Learning

Sudoku Solver follows the standard backtracking workflow:

```
Find an empty cell
↓

Try every possible value
↓

Validate
↓

Recurse
↓

Backtrack if necessary
```

This recursive strategy is widely used in problems involving constraints and exhaustive search.

Examples include:

- N-Queens
- Rat in a Maze
- Crossword Puzzle
- Word Search
- Graph Coloring
