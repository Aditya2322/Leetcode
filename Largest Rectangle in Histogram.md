# 📊 Largest Rectangle in Histogram | LeetCode 84

## Approach

I solved this problem using a **Monotonic Stack**.

The key idea is that for every bar in the histogram, I determine the maximum width over which that bar can act as the **smallest height**. To achieve this efficiently, I use a stack that stores indices of bars in **increasing order of heights**.

While traversing the histogram:

- If the current bar is taller than or equal to the bar at the top of the stack, I push its index onto the stack.
- If the current bar is shorter, I repeatedly pop bars from the stack because they can no longer extend beyond the current position.
- For every popped bar, I calculate:
  - **Height** = Height of the popped bar.
  - **Width** = Distance between the current index and the previous smaller element.
  - **Area** = Height × Width.
- I update the maximum rectangle area after every calculation.

After processing all bars, I continue popping any remaining bars from the stack and calculate their possible rectangle areas.

This ensures that every bar is processed only once, resulting in an efficient linear-time solution.

---

## My Thought Process

- Traverse the histogram from left to right.
- Maintain a stack of increasing bar heights.
- Whenever a smaller bar is encountered, compute the maximum rectangle for taller bars.
- Calculate the width using the previous smaller and next smaller elements.
- Update the maximum area.
- Process the remaining bars after the traversal is complete.

---

## Concepts Used

- Monotonic Stack
- Stack
- Arrays
- Greedy Observation

---

## Time Complexity

- **Time:** O(n)

## Space Complexity

- **Space:** O(n)

---

## What I Learned

This problem helped me understand how a **Monotonic Stack** can efficiently determine the previous and next smaller elements in a single traversal. Instead of checking every possible rectangle, maintaining an increasing stack allows each bar to be pushed and popped only once, leading to an optimal O(n) solution.

---

## Key Takeaway

Whenever a problem requires finding the **nearest greater/smaller element** or computing the contribution of each element over a range, consider using a **Monotonic Stack**. This pattern is widely used in histogram, stock span, trapping rainwater, and subarray-related problems.

---

## Related Problems

- Maximal Rectangle (LeetCode 85)
- Trapping Rain Water (LeetCode 42)
- Daily Temperatures (LeetCode 739)
- Next Greater Element (LeetCode 496)
- Sum of Subarray Minimums (LeetCode 907)
```
