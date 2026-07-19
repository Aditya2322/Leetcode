# 🌀 Spiral Matrix | LeetCode 54

## Approach

I solved this problem by **simulating the spiral traversal** of the matrix using four boundary pointers.

Instead of marking visited cells, I maintained four boundaries that represent the current unvisited portion of the matrix:

- `top` – First unvisited row
- `bottom` – Last unvisited row
- `left` – First unvisited column
- `right` – Last unvisited column

At each step, I traversed the matrix in four directions:

1. **Left → Right** across the top row.
2. **Top → Bottom** along the right column.
3. **Right → Left** across the bottom row (if rows remain).
4. **Bottom → Top** along the left column (if columns remain).

After completing each traversal, I updated the corresponding boundary to shrink the remaining matrix. This process continued until all elements were visited.

## My Thought Process

- Maintain four boundaries representing the current layer.
- Traverse the top row.
- Traverse the right column.
- If valid, traverse the bottom row.
- If valid, traverse the left column.
- Shrink the boundaries after every traversal.
- Repeat until every element is added to the answer.

## Concepts Used

- Matrix Traversal
- Simulation
- Boundary Pointers
- Arrays

## Time Complexity

- **Time:** O(m × n)
- **Space:** O(1) (excluding the output array)

## What I Learned

This problem taught me how to efficiently traverse a matrix without using extra space for visited cells. Using boundary pointers makes the implementation clean, avoids revisiting elements, and is a common technique for many matrix traversal problems.

This pattern is also useful in problems involving:
- Spiral Matrix II
- Rotate Image
- Set Matrix Zeroes
- Matrix Boundary Traversal
- Zigzag Matrix Traversal
```
