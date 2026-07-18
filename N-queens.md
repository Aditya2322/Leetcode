# N-Queens | LeetCode 51

## Problem Statement

Given an integer `n`, return all distinct solutions to the `n-queens` puzzle.

Each solution contains a distinct board configuration where:
- Exactly one queen is placed in each row.
- No two queens attack each other.

---

## Approach

The problem is solved using **Backtracking**.

Since every row must contain exactly one queen, we place queens **row by row**.

For each row:
1. Try placing a queen in every column.
2. Check whether placing the queen is safe.
3. If safe:
   - Place the queen.
   - Move to the next row.
4. If no valid position exists, backtrack by removing the previously placed queen.

When all rows are filled, one valid configuration is obtained.

---

## How to Approach Any N-Queens Problem

### Step 1: Understand the Constraints

A queen can attack in:
- Same column
- Left diagonal
- Right diagonal

Since we place only one queen per row, checking the current row is unnecessary.

---

### Step 2: Decide the Recursion

Each recursive call represents one row.

```
solve(row)
```

If `row == n`, all queens are placed successfully.

---

### Step 3: Try Every Column

For every column in the current row:

- Check if the position is safe.
- Place the queen.
- Recur for the next row.
- Remove the queen (Backtrack).

---

### Step 4: Safety Check

Before placing a queen, verify:

- Column is empty
- Upper-left diagonal is empty
- Upper-right diagonal is empty

These checks ensure no queen attacks another.

---

## Optimized Approach

Instead of checking the board every time, maintain three arrays:

- `leftRow`
- `lowerDiagonal`
- `upperDiagonal`

These allow checking whether a position is safe in **O(1)** time.

```
Column -> leftRow[col]

Lower Diagonal -> row + col

Upper Diagonal -> (n - 1) + col - row
```

This significantly improves performance.

---

## Algorithm

1. Start from row 0.
2. Iterate through every column.
3. If safe:
   - Place queen.
   - Mark column and diagonals.
   - Recur for next row.
4. Backtrack after returning.
5. Store board when all rows are processed.

---

## Complexity

### Brute Force

- Time: Exponential

### Optimized Backtracking

- Time: O(N!)
- Space: O(N)

---

## Concepts Used

- Backtracking
- Recursion
- Matrix Traversal
- Hashing
- Diagonal Mapping

---

## Key Learning

N-Queens is a classic backtracking problem.

The general pattern is:

```
Choose
Explore
Backtrack
```

This pattern is applicable to many problems such as:
- Sudoku Solver
- Rat in a Maze
- Word Search
- Permutations
- Combination Sum
