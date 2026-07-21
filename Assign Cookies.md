# 🍪 Assign Cookies | LeetCode 455

## Approach

I solved this problem using the **Greedy** algorithm.

The main idea is to satisfy as many children as possible by assigning the smallest available cookie that can satisfy each child. To achieve this, I first sorted both the children's greed factors and the cookie sizes.

Using two pointers, I compared the current smallest greedy child with the current smallest available cookie:

- If the cookie was large enough to satisfy the child, I assigned it and moved both pointers.
- Otherwise, I skipped the cookie and tried the next larger one.

This greedy strategy ensures that larger cookies are preserved for children with higher greed factors, maximizing the total number of satisfied children.

---

## My Thought Process

- Sort the greed factors.
- Sort the cookie sizes.
- Start with the least greedy child and the smallest cookie.
- If the cookie satisfies the child, assign it.
- Otherwise, try a larger cookie.
- Count the number of satisfied children.

---

## Concepts Used

- Greedy Algorithm
- Sorting
- Two Pointers
- Arrays

---

## Time Complexity

- **Time:** O(n log n + m log m)
  - Sorting the greed array: `O(n log n)`
  - Sorting the cookie array: `O(m log m)`
  - Two-pointer traversal: `O(n + m)`

## Space Complexity

- **Space:** O(1)
  - (Ignoring the space used by the sorting algorithm.)

---

## What I Learned

This problem reinforced the idea that making the **locally optimal choice** can lead to a globally optimal solution. By always assigning the smallest possible cookie that satisfies a child, unnecessary larger cookies are saved for children with greater greed, making the greedy approach both simple and efficient.

---

## Key Takeaway

When the objective is to maximize the number of successful assignments, consider:
- Sorting the inputs.
- Using two pointers.
- Making the smallest valid assignment first.

This greedy pattern is commonly used in scheduling, interval, and matching problems.
```
