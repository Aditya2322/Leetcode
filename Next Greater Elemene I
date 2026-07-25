# ⏭️ Next Greater Element I | LeetCode 496

## Approach

I solved this problem using a **Monotonic Decreasing Stack** along with a **Hash Map**.

The idea is to preprocess the `nums2` array to determine the next greater element for every number. I maintain a stack in decreasing order of elements. While traversing `nums2`, whenever I encounter a number greater than the element at the top of the stack, it means I have found the next greater element for the stack's top element.

I store this mapping in a hash map and remove the element from the stack. After processing the entire array, any elements still remaining in the stack do not have a next greater element, so I map them to `-1`.

Finally, I traverse `nums1` and retrieve the corresponding next greater element directly from the hash map.

---

## My Thought Process

- Traverse `nums2` from left to right.
- Maintain a decreasing stack.
- Whenever the current element is greater than the stack's top element:
  - The current element becomes the next greater element.
  - Store the mapping in a hash map.
- Push the current element onto the stack.
- Assign `-1` to all remaining elements in the stack.
- Build the answer for `nums1` using the precomputed mappings.

---

## Concepts Used

- Monotonic Stack
- Stack
- Hash Map
- Arrays

---

## Time Complexity

- **Time:** O(n + m)
  - `n` = size of `nums2`
  - `m` = size of `nums1`

## Space Complexity

- **Space:** O(n)

---

## What I Learned

This problem strengthened my understanding of the **Monotonic Stack** pattern. Instead of searching for the next greater element for every number individually, preprocessing the larger array once allows constant-time lookups later. Combining a monotonic stack with a hash map results in an efficient linear-time solution.

---

## Key Takeaway

Whenever a problem asks for the **next greater** or **next smaller** element, think about using a **Monotonic Stack**. It helps process each element only once, making the solution optimal.

---

## Related Problems

- Next Greater Element II (LeetCode 503)
- Daily Temperatures (LeetCode 739)
- Final Prices With a Special Discount (LeetCode 1475)
- Sum of Subarray Minimums (LeetCode 907)
- Online Stock Span (LeetCode 901)
```
