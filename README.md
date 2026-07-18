# 🔙 Backtracking Problems

This repository contains my solutions to various **Backtracking** problems from LeetCode. The goal of this repository is to improve my understanding of recursion, constraint satisfaction, and systematic problem-solving through backtracking.

## What is Backtracking?

Backtracking is a recursive algorithmic technique used to solve problems by exploring all possible choices. At each step, a decision is made, and if that decision eventually leads to an invalid solution, it is undone (backtracked) so that another choice can be explored.

The general workflow is:

```
Choose
   ↓
Check if the choice is valid
   ↓
Explore recursively
   ↓
If it doesn't work, Undo the choice (Backtrack)
```

## My Approach

For every backtracking problem, I follow a common strategy:

1. Understand the constraints of the problem.
2. Identify the recursive state (what changes in each recursive call).
3. Try every possible choice at the current state.
4. Check whether the choice is valid.
5. If valid, make the choice and recursively solve the remaining problem.
6. If the choice does not lead to a solution, undo it and try the next possibility.
7. Continue until all valid solutions are found or the required solution is obtained.

Whenever possible, I also optimize the solution by using auxiliary data structures such as hash arrays, lookup tables, or bitmasks to reduce unnecessary computations.

## Problems Covered

- N-Queens
- Sudoku Solver


## Concepts Practiced

- Backtracking
- Recursion
- Depth First Search (DFS)
- Constraint Satisfaction
- Pruning
- Matrix Traversal
- Hashing for Optimization

## What I Learned

Working on these problems has helped me:

- Build a strong understanding of recursion.
- Learn how to systematically explore all possible solutions.
- Recognize when to backtrack and undo previous decisions.
- Improve optimization techniques using auxiliary data structures.
- Develop a reusable problem-solving template for many recursive problems.

## General Backtracking Template

```cpp
void solve(...) {

    if(baseCase){
        // store or return answer
        return;
    }

    for(each possible choice){

        if(choice is valid){

            // Make the choice

            solve(...);

            // Undo the choice (Backtrack)
        }
    }
}
```

## Repository Goal

This repository serves as my personal collection of backtracking solutions and documents my learning journey while preparing for coding interviews and strengthening my Data Structures & Algorithms skills.
