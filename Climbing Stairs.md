# 🪜 Climbing Stairs | LeetCode 70

## Approach

I solved this problem using **Dynamic Programming** with **Space Optimization**.

The key observation is that to reach the `i-th` stair, there are only two possible ways:
- Take **1 step** from the `(i-1)th` stair.
- Take **2 steps** from the `(i-2)th` stair.

Therefore, the number of ways to reach the current stair is the sum of the ways to reach the previous two stairs.

Instead of storing all previous results in a DP array, I only kept track of the last two values since only those are needed to compute the current answer. This reduces the space complexity from **O(n)** to **O(1)**.

---

## My Thought Process

- Identify the base cases:
  - `n = 1` → 1 way
  - `n = 2` → 2 ways
- Observe that each stair depends only on the previous two stairs.
- Store the number of ways for the last two stairs.
- Compute the current value and update the previous values.
- Continue until reaching the `n-th` stair.

---

## Concepts Used

- Dynamic Programming
- Fibonacci Pattern
- Space Optimization

---

## Time Complexity

- **Time:** O(n)

## Space Complexity

- **Space:** O(1)

---

## What I Learned

This problem helped me understand how many Dynamic Programming problems can be optimized by recognizing that only a few previous states are required. It also reinforced the relationship between DP and the Fibonacci sequence, where each state depends on the previous two states.

---

## Key Takeaway

Whenever a DP recurrence depends only on the last few states, consider replacing the DP array with variables to reduce the space complexity while maintaining the same time complexity.
```
